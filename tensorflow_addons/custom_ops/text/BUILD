licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//visibility:public"])

load("//tensorflow_addons:addons_bazel_macros.bzl", "D_GLIBCXX_USE_CXX11_ABI")

cc_binary(
    name = "_skip_gram_ops.so",
    srcs = [
        "cc/kernels/skip_gram_kernels.cc",
        "cc/ops/skip_gram_ops.cc",
    ],
    copts = [
        "-pthread",
        "-std=c++11",
        D_GLIBCXX_USE_CXX11_ABI,
    ],
    linkshared = 1,
    deps = [
        "@local_config_tf//:libtensorflow_framework",
        "@local_config_tf//:tf_header_lib",
    ],
)
