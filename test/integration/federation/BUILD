package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "api_test.go",
        "crud_test.go",
    ],
    tags = [
        "automanaged",
        "integration",
    ],
    deps = [
        "//federation/apis/federation/v1beta1:go_default_library",
        "//federation/pkg/federatedtypes:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/apis/autoscaling/v1:go_default_library",
        "//pkg/apis/batch/v1:go_default_library",
        "//pkg/apis/extensions/v1beta1:go_default_library",
        "//test/integration/federation/framework:go_default_library",
        "//vendor/github.com/pborman/uuid:go_default_library",
        "//vendor/github.com/stretchr/testify/assert:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
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
    srcs = [
        ":package-srcs",
        "//test/integration/federation/framework:all-srcs",
    ],
    tags = ["automanaged"],
)
