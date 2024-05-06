package(default_visibility = ["//visibility:public"])

constraint_setting(name = "clang_version")

constraint_value(
    name = "clang_14",
    constraint_setting = ":clang_version",
)

constraint_value(
    name = "clang_17",
    constraint_setting = ":clang_version",
)

platform(
    name = "aarch64",
    constraint_values = [
       "@platforms//cpu:arm64",
       "@platforms//os:linux",
    ],
)
