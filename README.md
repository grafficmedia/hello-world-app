Hello! For this exercise, you'll be adding some build-and-release specific
functionality to an example React Native app.

There are two tasks listed under each of the two headings below.

## Environment Variable-Driven App Versioning

For the first task in this exercise, we'd like for you to use environment
variables to change the version number and build number of this example
application, via the shell script at [`scripts/build.sh`](./scripts/build.sh).

The script must utilize environment variables called `BUILD_NUMBER` and
`VERSION_NUMBER` to inject these values into:

1. The existing iOS configuration ([`Info.plist`](./ios/HelloWorld/Info.plist), where the build number is represented as `CFBundleVersion` and the version number is `CFBundleShortVersionString`).
2. The existing Android configuration ([`android/app/build.gradle`](./android/app/build.gradle)) where the build number is `versionCode` and the version number is `versionName`).

Feel free to use any tools you'd like (e.g. `plutil`).


## GitHub Action to tag builds

[GitHub Actions](https://docs.github.com/en/actions) are one convenient way to
perform arbitrary actions when e.g. pull requests are opened or when code is
merged into the main branch of a repository.


We'd like for you to create a GitHub Action that creates a git tag when a branch
is merged into main. Any arbitrary tag you'd like to use is fine, so long as
there's a GitHub action that creates a tag.
