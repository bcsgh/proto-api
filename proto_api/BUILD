exports_files(["proto_api.bzl"])

proto_library(
    name = "api_meta_proto",
    srcs = ["api_meta.proto"],
    deps = [
        "@protobuf//:descriptor_proto",
    ],
    visibility = ["//visibility:public"],
)

cc_proto_library(
    name = "api_meta_cc",
    deps = [":api_meta_proto"],
)

####################################
cc_proto_library(
    name = "descriptor_proto_cc",
    deps = ["@protobuf//:descriptor_proto"],
)

cc_binary(
    name = "gen_metadata_tool",
    srcs = ["gen_metadata_tool.cc"],
    deps = [
        "@abseil-cpp//absl/flags:flag",
        "@abseil-cpp//absl/flags:parse",
        ":api_meta_cc",
        ":descriptor_proto_cc",
    ],
    visibility = ["//visibility:public"],
)
