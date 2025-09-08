## Patch Notes
There are 3 commons-lang flavor libraries built by the Apache community:
- `commons-lang3`: The latest version of the library, which includes new features and improvements over previous versions. It is recommended for new projects.
- `commons-lang`: The predecessor of `commons-lang3`, which is no longer actively maintained. It is not recommended for new projects, but may still be used in legacy systems.
- `common-lang`: The oldest version of the library, which is also no longer actively maintained. It is not recommended for new projects and should be avoided if possible.

`commons-lang` had been declared dead by Apache but is still widely used even in most recent libraries such as biojava-structure due to transitive dependencies.
As such, it is still important to keep it secure and up-to-date.

This project is a fork of `commons-lang` and is maintained by [Sapio Sciences LLC](https://www.sapiosciences.com/) to respond to latest CVE patches.
Sapio publishes the library under its own artifactory repository under the same group ID and artifact ID, appended with an additional patch number.
For example: `org.apache.commons:commons-lang:2.6-SapioCVE202548924` will patch CVE-2025-48924 and all earlier dated CVEs.

After publication, the artifact is considered locked down and will not be allowed to be overwritten in the repository server. New patches will use a new version number.
If a republication is required, then the version number will be appended with an additional "bx" where x is an incrementing number starting at 2 for the first patch.

## Supported Java Versions
The original commons-lang 2.6 was built for language version 1.3.
Due to the need for ease of patching, the language version has been updated to 1.8.