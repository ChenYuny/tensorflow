licenses(["notice"])  # Apache 2.0

package(default_visibility = ["//tensorflow:internal"])

load("//tensorflow:tensorflow.bzl", "py_test")

py_library(
    name = "tflite_lstm",
    srcs = ["tflite_lstm.py"],
    srcs_version = "PY2AND3",
    visibility = ["//visibility:public"],
    deps = [
        "//tensorflow:tensorflow_py",
        "//tensorflow/contrib/lite/python:lite",
        "//tensorflow/python:framework",
        "@six_archive//:six",
    ],
)

py_test(
    name = "unidirectional_sequence_lstm_test",
    size = "large",
    srcs = ["unidirectional_sequence_lstm_test.py"],
    srcs_version = "PY2AND3",
    tags = [
        "manual",
        "no_oss",
        "no_pip",
        "notap",
    ],
    deps = [
        ":tflite_lstm",
        "//tensorflow:tensorflow_py",
        "//tensorflow/contrib/lite/python:lite",
        "//tensorflow/examples/tutorials/mnist:input_data",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform",
        "//tensorflow/python/tools:optimize_for_inference",
        "//third_party/py/numpy",
        "@six_archive//:six",
    ],
)
