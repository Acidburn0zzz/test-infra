load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["creator.go"],
    visibility = ["//visibility:public"],
    deps = [
        "//ghclient:go_default_library",
        "//robots/issue-creator/testowner:go_default_library",
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/github.com/google/go-github/github:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["creator_test.go"],
    library = ":go_default_library",
    deps = [
        "//robots/issue-creator/testowner:go_default_library",
        "//vendor/github.com/google/go-github/github:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
