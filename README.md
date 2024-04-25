# Stubbed Versioning

This project contains an exemplary setup for a version release pipeline that fulfills the following requirements:

1. Adheres to versioning standards - [semver](semver.org) in this case
1. Use [git tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging) as single source of
   truth for the versioning
1. Allow to include information about the version in the code-base itself
1. Allow to run and address resulting issues of designated pre-release tests (and pot. other worklfows)
1. Include the released state of the repository in the reference branch

The combination of these requirements leads to a non-trivial version release workflow described below in 
[#requirements-on-release-worklow](#requirements-on-release-worklow).

This repository defines various github actions that lead you through a release workflow which asserts that
the above defined requirements can be fulfilled.

## The version release pipeline

Assume you want to release a new version, say `1.2.0`, based on HEAD of `main`.
All you need to do it push the git tag `1.2.0-rc1` to github.

The [initiate_version_stub.yml](.github/workflows/initiate_stub.yml) action
will be triggered and create a new branch `release-1.2.0`, along with Pull Request to merge this
branch back to `main`.

Any push to the newly create branch `release-1.2.0` will trigger the pipeline defined in
[prepare_version_release.yml](.github/workflows/prepare_version_release.yml).
Further will the Pull Request allow you to nicely track
all the changes you made related to the points **3.** and **4.** from above.

Once you are satisfied with the state of the `release-1.2.0` branch, simply close the Pull Request
by merging it.

Upon merge the action [publish_version.yml](.github/workflows/publish_version.yml) will create the
git tag `1.2.0`, so a cleaned version of your initial `1.2.0-rc1` on HEAD of `release-1.2.0`
and publish a
[github release](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)
for this tag.
In doing so it asserts that changes made during the preparation of the release are ported back to
the reference branch (point **5.** from above).

## How to get you started

It is easiest to try it yourself.

To do so:

- [fork this repository](https://github.com/t4d-gmbh/stubbed_versioning/fork)
- add some change to `main` e.g. by editing the README.md
- create a new git tag with `-rcX` appended to the patch and push it:
      
      git tag -a 2.0.0-rc1 -m 'Trying new things'
      git push --tags

- now give github a minute and then head to the Rull requests of your newly forked repository 
- you might add some changes to the newly created branch (`release-2.0.0` if you follow this steps by the letter)
- merge the Pull request and give github a minute to run the actions
- you will find that the changes introduced in the `release-2.0.0` branch were merged to `main`
- when heading to the main URL of the repository you will see a new Release added


## Details

### Requirements on release workflow

With **2.** a version is tied to a specific commit.
However, with **3.**, **4.** or **5.** changes to the repository might need to be introduced, leading
to new commits and, as a consequence to a new version, if one wants to avoid deleting existing git tags.
_Which is what you should do!_

The general approach to address this deadlock is by introducing release candidates or pre-release versions.
Those are versions with an additional `-rcX` (or similar) string appended to the
[`patch` version number](https://semver.org/#spec-item-9)

Points **3.** and **4.** can be addressed by creating a new branch on which release-specific
workflows can be run the content of the repository prepared for the creation of a new git tag.

To make sure that the changes introduced in this release branch also make their way to the default
branch, the release branch should be merged into the default branch as soon as the version is
ready to be published.


