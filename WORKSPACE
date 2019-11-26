load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

##############  begin llvm toolchain definition ##############
http_archive(
    name = "com_grail_bazel_toolchain",
    strip_prefix = "bazel-toolchain-master",
    urls = ["https://github.com/grailbio/bazel-toolchain/archive/master.tar.gz"],
)

load("@com_grail_bazel_toolchain//toolchain:rules.bzl", "llvm_toolchain")

llvm_toolchain(
    name = "llvm_toolchain",
    llvm_version = "8.0.0",
)

load("@llvm_toolchain//:toolchains.bzl", "llvm_register_toolchains")

llvm_register_toolchains()
############### end LLVM toolchain ###################
