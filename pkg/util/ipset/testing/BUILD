load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["fake.go"],
    importpath = "k8s.io/kubernetes/pkg/util/ipset/testing",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/util/ipset:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
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

go_test(
    name = "go_default_test",
    srcs = ["fake_test.go"],
    importpath = "k8s.io/kubernetes/pkg/util/ipset/testing",
    library = ":go_default_library",
    deps = [
        "//pkg/util/ipset:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
    ],
)
