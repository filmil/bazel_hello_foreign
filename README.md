[![Test](https://github.com/filmil/bazel_hello_foreign/actions/workflows/test.yml/badge.svg)](https://github.com/filmil/bazel_hello_foreign/actions/workflows/test.yml)
[![Tag and Release](https://github.com/filmil/bazel_hello_foreign/actions/workflows/tag-and-release.yml/badge.svg)](https://github.com/filmil/bazel_hello_foreign/actions/workflows/tag-and-release.yml)
[![Publish to my Bazel registry](https://github.com/filmil/bazel_hello_foreign/actions/workflows/publish.yml/badge.svg)](https://github.com/filmil/bazel_hello_foreign/actions/workflows/publish.yml)
[![Publish on Bazel Central Registry](https://github.com/filmil/bazel_hello_foreign/actions/workflows/publish-bcr.yml/badge.svg)](https://github.com/filmil/bazel_hello_foreign/actions/workflows/publish-bcr.yml)

# `bazel`-compiled library

This project builds the `elfutils` library and its associated binaries (like `eu-addr2line`, `eu-readelf`, etc.) in a hermetic way using Bazel. It fetches the `elfutils` source code from `sourceware.org`, and uses `rules_foreign_cc` to configure and build it. The project includes a simple test to ensure the library builds correctly, and an integration test to verify that the built artifacts can be used by another Bazel project. The CI/CD pipelines are set up with GitHub Actions to test the build, tag releases, and publish to a Bazel registry.

```
bazel test //...
```
