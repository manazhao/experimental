load(
    "@io_bazel_rules_closure//closure:defs.bzl",
    "closure_js_binary",
    "closure_js_library",
)
load("@build_stack_rules_proto//github.com/grpc/grpc-web:closure_grpc_library.bzl", "closure_grpc_library")

package(
    default_visibility = ["//:__subpackages__"],
)

proto_library(
    name = "a_proto",
    srcs = ["a.proto"],
)

proto_library(
    name = "b_proto",
    srcs = ["b.proto"],
    deps = [":a_proto"],
)

closure_grpc_library(
    name = "a_closure",
    deps = [":a_proto"],
)

closure_grpc_library(
    name = "b_closure",
    deps = [":b_proto"],
)
