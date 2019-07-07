load("@build_stack_rules_proto//github.com/grpc/grpc-web:closure_grpc_library.bzl", "closure_grpc_library")

package(
    default_visibility = ["//:__subpackages__"],
)

proto_library(
    name = "a_proto",
    srcs = ["a.proto"],
)

proto_library(
    name = "say_hello_service_proto",
    srcs = ["say_hello_service.proto"],
    deps = [":a_proto"],
)

proto_library(
    name = "say_goodbye_service_proto",
    srcs = ["say_goodbye_service.proto"],
)

closure_grpc_library(
    name = "say_goodbye_service_closure",
    deps = [":say_goodbye_service_proto"],
)

closure_grpc_library(
    name = "say_hello_service_closure",
    transitive = True,
    deps = [":say_hello_service_proto"],
)
