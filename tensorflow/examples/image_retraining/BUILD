# Description:
# Transfer learning example for TensorFlow.

licenses(["notice"])  # Apache 2.0

exports_files(["LICENSE"])

py_binary(
    name = "retrain",
    srcs = [
        "retrain.py",
    ],
    srcs_version = "PY2AND3",
    visibility = ["//tensorflow:__subpackages__"],
    deps = [
        "//tensorflow:tensorflow_py",
    ],
)

py_test(
    name = "retrain_test",
    size = "small",
    srcs = [
        "label_image.py",
        "retrain.py",
        "retrain_test.py",
    ],
    data = [
        ":data/labels.txt",
        "//tensorflow/examples/label_image:data/grace_hopper.jpg",
    ],
    srcs_version = "PY2AND3",
    deps = [
        "//tensorflow:tensorflow_py",
        "//tensorflow/python:framework_test_lib",
        "//tensorflow/python:platform_test",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(
        [
            "**/*",
        ],
        exclude = [
            "**/METADATA",
            "**/OWNERS",
        ],
    ),
    visibility = ["//tensorflow:__subpackages__"],
)
