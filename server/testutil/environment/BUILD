load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    testonly = 1,
    srcs = ["environment.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/testutil/environment",
    visibility = ["//visibility:public"],
    deps = [
        "//server/backends/blobstore:go_default_library",
        "//server/backends/invocationdb:go_default_library",
        "//server/backends/memory_cache:go_default_library",
        "//server/config:go_default_library",
        "//server/real_environment:go_default_library",
        "//server/rpc/filters:go_default_library",
        "//server/testutil/healthcheck:go_default_library",
        "//server/util/db:go_default_library",
        "@org_golang_google_grpc//:go_default_library",
        "@org_golang_google_grpc//test/bufconn:go_default_library",
    ],
)
