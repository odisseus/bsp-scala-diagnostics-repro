load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

skylib_version = "1.0.3"
http_archive(
    name = "bazel_skylib",
    sha256 = "1c531376ac7e5a180e0237938a2536de0c54d93f5c278634818e0efc952dd56c",
    type = "tar.gz",
    url = "https://mirror.bazel.build/github.com/bazelbuild/bazel-skylib/releases/download/{}/bazel-skylib-{}.tar.gz".format(skylib_version, skylib_version),
)


http_archive(
    name = "io_bazel_rules_scala",
    url = "https://github.com/andrefmrocha/rules_scala/archive/d6186617cfe64cef2074b23ca58daac75fe40d42.tar.gz",
    strip_prefix = "rules_scala-d6186617cfe64cef2074b23ca58daac75fe40d42",
)

load("@io_bazel_rules_scala//:version.bzl", "bazel_version")
bazel_version(name = "bazel_version")

register_toolchains(
    "//:diagnostics_reporter_toolchain"
)
