package(default_visibility = ["//visibility:public"])

licenses(["notice"])

cc_library(
    name = "pytorch",
    hdrs = glob(["*"]),
    srcs = ["lib/libtorch.so"],
    includes = [
        "include",
        "include/torch/csrc/api/include",
        "include/torch/csrc/api/include/torch"
    ],
    copts = [
        "-Iinclude",
        "-Iinclude/torch",
        "-Iinclude/torch/csrc/api/include/torch",
    ],
    linkopts = [
        "-L/usr/local/apollo/libtorch/lib",
        "-lc10",
        "-lc10_cuda",
        "-lcaffe2",
        "-lcaffe2_detectron_ops_gpu",
        "-lcaffe2_gpu",
        "-lcaffe2_module_test_dynamic",
        "-lcaffe2_observers",
        "-lfoxi",
        "-liomp5",
        "-lmklml_intel",
        "-lonnxifi",
        "-lshm",
        "-lthnvrtc",
        "-ltorch_python",
    ],
    deps = [
        "@python27",
    ]
)
