package(default_visibility = ["//visibility:public"])

filegroup(name = "empty")

load(":u22_x86_64_clang.bzl", "x86_64_toolchain_config")
load(":u22_aarch64_clang.bzl", "aarch64_toolchain_config")
# load(":u22_aarch64_gcc.bzl", "aarch64_toolchain_config")

x86_64_toolchain_config(name = "linux_x86_64_toolchain_config")
aarch64_toolchain_config(name = "u22_aarch64_toolchain_config")

cc_toolchain(
    name = "linux_x86_64_toolchain",
    toolchain_identifier = "linux_x86_64-toolchain",
    toolchain_config = ":linux_x86_64_toolchain_config",
    all_files = ":empty",
    compiler_files = ":empty",
    dwp_files = ":empty",
    linker_files = ":empty",
    objcopy_files = ":empty",
    strip_files = ":empty",
    supports_param_files = 0,
)

toolchain(
    name = "cc_toolchain_for_linux_x86_64",
    toolchain = ":linux_x86_64_toolchain",
    toolchain_type = "@bazel_tools//tools/cpp:toolchain_type",
    exec_compatible_with = [
        "@platforms//cpu:x86_64",
        "@platforms//os:linux",
    ],
    target_compatible_with = [
        "@platforms//cpu:x86_64",
        "@platforms//os:linux",
    ],
)

cc_toolchain(
    name = "u22_aarch64_toolchain",
    toolchain_identifier = "linux_aarch64-toolchain",
    toolchain_config = ":u22_aarch64_toolchain_config",
    all_files = ":empty",
    compiler_files = ":empty",
    dwp_files = ":empty",
    linker_files = ":empty",
    objcopy_files = ":empty",
    strip_files = ":empty",
    supports_param_files = 0,
)

toolchain(
    name = "cc_toolchain_for_u22_aarch64",
    toolchain = ":u22_aarch64_toolchain",
    toolchain_type = "@bazel_tools//tools/cpp:toolchain_type",
    exec_compatible_with = [
        "@platforms//cpu:x86_64",
        "@platforms//os:linux",
    ],
    target_compatible_with = [
        "@platforms//cpu:aarch64",
        "@platforms//os:linux",
    ],
)

platform(
    name = "aarch64",
    constraint_values = [
       "@platforms//cpu:arm64",
       "@platforms//os:linux",
    ],
)
