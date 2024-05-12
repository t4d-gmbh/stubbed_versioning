
<a name="0.7.8"></a>
## [0.7.8](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.7...0.7.8)

> 2024-05-12

### Fix

* enforce release only with clean tag

### Pull Requests

* Merge pull request [#101](https://github.com/t4d-gmbh/stubbed_versioning/issues/101) from t4d-gmbh/release-0.7.7


<a name="0.7.7"></a>
## [0.7.7](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.6...0.7.7)

> 2024-05-12

### Fix

* permissions for pr edits

### Pull Requests

* Merge pull request [#100](https://github.com/t4d-gmbh/stubbed_versioning/issues/100) from t4d-gmbh/release-0.7.6


<a name="0.7.6"></a>
## [0.7.6](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.5...0.7.6)

> 2024-05-12

With this version it is possible to publish a version before the associated Pull request is merged.
This is to avoid having to resolve merge conflicts before publishing and should be avoided whenever possible.

To release a version pre-merge of the corresponding `release-x.x.x` branch simply tag the commit you want to
relese with the clean targe version.


<a name="0.7.5"></a>
## [0.7.5](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.4...0.7.5)

> 2024-05-12

### Fix

* specify repo and pr

### Pull Requests

* Merge pull request [#97](https://github.com/t4d-gmbh/stubbed_versioning/issues/97) from t4d-gmbh/release-0.7.4


<a name="0.7.4"></a>
## [0.7.4](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.3...0.7.4)

> 2024-05-12

### Fix

* correctly request event

### Pull Requests

* Merge pull request [#96](https://github.com/t4d-gmbh/stubbed_versioning/issues/96) from t4d-gmbh/release-0.7.3


<a name="0.7.3"></a>
## [0.7.3](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.2...0.7.3)

> 2024-05-12

### Fix

* event is not picked up

### Pull Requests

* Merge pull request [#95](https://github.com/t4d-gmbh/stubbed_versioning/issues/95) from t4d-gmbh/release-0.7.2


<a name="0.7.2"></a>
## [0.7.2](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.7.1...0.7.2)

> 2024-05-12

### Fix

* release command was split


<a name="0.7.1"></a>
## [0.7.1](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.6.4...0.7.1)

> 2024-05-12

### Fix

* syntax error in condition

<a name="0.7.0"></a>
## [0.7.0](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.6.4...0.7.0)

> 2024-05-12

### Feature

* allow to trigger release before merging pr ([#89](https://github.com/t4d-gmbh/stubbed_versioning/issues/89))

### Fix

* Check label of pull request ([#91](https://github.com/t4d-gmbh/stubbed_versioning/issues/91)) ([#92](https://github.com/t4d-gmbh/stubbed_versioning/issues/92))


<a name="0.6.4"></a>
## [0.6.4](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.6.3...0.6.4)

> 2024-05-09

### Feature

* switching to usage of gh cli for releaseing ([#83](https://github.com/t4d-gmbh/stubbed_versioning/issues/83) + [#85](https://github.com/t4d-gmbh/stubbed_versioning/issues/85))

### Fix

* using wrong version for push action
* we need to actually set the option
* allow to push tags without branch
* overwrite existing tags on runner (closes [#71](https://github.com/t4d-gmbh/stubbed_versioning/issues/71))
* notice about branch protection ([#69](https://github.com/t4d-gmbh/stubbed_versioning/issues/69))
* create release notice from changelog ([#66](https://github.com/t4d-gmbh/stubbed_versioning/issues/66))
* target diff to previous version

### Pull Requests

* Merge pull request [#82](https://github.com/t4d-gmbh/stubbed_versioning/issues/82) from t4d-gmbh/release-0.6.4
* ..._many trial pull requests_
* Merge pull request [#61](https://github.com/t4d-gmbh/stubbed_versioning/issues/61) from t4d-gmbh/60-cleaning-up-release-workflow


<a name="0.6.3"></a>
## [0.6.3](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.6.2...0.6.3)

> 2024-05-07

### Fix

* target pr head commit

### Pull Requests

* Merge pull request [#58](https://github.com/t4d-gmbh/stubbed_versioning/issues/58) from t4d-gmbh/57-clean-tag-is-created-on-the-merge-commit-not-the-previous-one


<a name="0.6.2"></a>
## [0.6.2](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.6.1...0.6.2)

> 2024-05-07

### Fix

* typeo in release task


<a name="0.6.1"></a>
## [0.6.1](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.5.0...0.6.1)

> 2024-05-07

### Feature

* adding changes to release note

### Fix

* actually passing the body file to release
* better commit message for version pr ([#44](https://github.com/t4d-gmbh/stubbed_versioning/issues/44))

### Pull Requests

* Merge pull request [#53](https://github.com/t4d-gmbh/stubbed_versioning/issues/53) from t4d-gmbh/47-deleting-the-release-branch-on-merge-crashes-the-publish_version-action
* ... _irrelevant PR's for debugging_
* Merge pull request [#46](https://github.com/t4d-gmbh/stubbed_versioning/issues/46) from t4d-gmbh/release-0.6.0
* Merge pull request [#45](https://github.com/t4d-gmbh/stubbed_versioning/issues/45) from t4d-gmbh/40-better-infor-for-the-release


<a name="0.6.0"></a>
## [0.6.0](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.5.0...0.6.0)

> 2024-05-07

### Feature

* adding changes to release note

### Fix

* better commit message for version pr ([#44](https://github.com/t4d-gmbh/stubbed_versioning/issues/44))

### Pull Requests

* Merge pull request [#45](https://github.com/t4d-gmbh/stubbed_versioning/issues/45) from t4d-gmbh/40-better-infor-for-the-release


<a name="0.5.0"></a>
## [0.5.0](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.4.0...0.5.0)

> 2024-05-07

### Feature

* on-demand checks via label ([#41](https://github.com/t4d-gmbh/stubbed_versioning/issues/41))

### Fix

* only run publish action on pr for release- branches ([#42](https://github.com/t4d-gmbh/stubbed_versioning/issues/42))


<a name="0.4.0"></a>
## [0.4.0](https://github.com/t4d-gmbh/stubbed_versioning/compare/0.3.3...0.4.0)

> 2024-05-07

### Feature

* deleting branches with 0 diff and no PR ([#23](https://github.com/t4d-gmbh/stubbed_versioning/issues/23))

### Fix

* only diff to last clean tag ([#37](https://github.com/t4d-gmbh/stubbed_versioning/issues/37))
* make sure git-chglog reports all changes
* remove duplicated opiton

### Pull Requests

* Merge pull request [#27](https://github.com/t4d-gmbh/stubbed_versioning/issues/27) from t4d-gmbh/25-git-chglog-does-not-pick-up-all-changes-when-clone-with-depth-1
* Merge pull request [#19](https://github.com/t4d-gmbh/stubbed_versioning/issues/19) from t4d-gmbh/release-0.3.3


<a name="0.3.3"></a>
## 0.3.3

> 2024-04-26

### Fix

* typeo in workflow


<a name="0.3.2"></a>
## 0.3.2

> 2024-04-26

### Fix

* again minor typeos in README


<a name="0.3.1"></a>
## 0.3.1

> 2024-04-26

### Fix

* minor edits in documentation


<a name="0.3.0"></a>
## 0.3.0

> 2024-04-26

### Feature

* explaining why and how

