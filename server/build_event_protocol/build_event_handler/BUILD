load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = ["build_event_handler.go"],
    importpath = "github.com/buildbuddy-io/buildbuddy/server/build_event_protocol/build_event_handler",
    visibility = ["//visibility:public"],
    deps = [
        "//proto:build_event_stream_go_proto",
        "//proto:build_events_go_proto",
        "//proto:cache_go_proto",
        "//proto:invocation_go_proto",
        "//proto:publish_build_event_go_proto",
        "//proto:user_id_go_proto",
        "//server/build_event_protocol/accumulator:go_default_library",
        "//server/build_event_protocol/build_status_reporter:go_default_library",
        "//server/build_event_protocol/event_parser:go_default_library",
        "//server/build_event_protocol/target_tracker:go_default_library",
        "//server/environment:go_default_library",
        "//server/interfaces:go_default_library",
        "//server/metrics:go_default_library",
        "//server/remote_cache/hit_tracker:go_default_library",
        "//server/tables:go_default_library",
        "//server/util/perms:go_default_library",
        "//server/util/protofile:go_default_library",
        "//server/util/status:go_default_library",
        "@com_github_golang_protobuf//proto:go_default_library",
        "@com_github_golang_protobuf//ptypes:go_default_library_gen",
        "@com_github_prometheus_client_golang//prometheus:go_default_library",
        "@org_golang_google_grpc//status:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["build_event_handler_test.go"],
    embed = [":go_default_library"],
    deps = [
        "//proto:build_event_stream_go_proto",
        "//proto:build_events_go_proto",
        "//proto:invocation_go_proto",
        "//proto:publish_build_event_go_proto",
        "//server/testutil/auth:go_default_library",
        "//server/testutil/environment:go_default_library",
        "@com_github_stretchr_testify//assert:go_default_library",
        "@io_bazel_rules_go//proto/wkt:any_go_proto",
    ],
)
