workspace(name = "example")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "com_grail_bazel_toolchain",
    sha256 = "54b54eedc71b93b278c44b6c056a737dc68545c6da75f63d0810676e1181f559",
    strip_prefix = "bazel-toolchain-76ce37e977a304acf8948eadabb82c516320e286",
    urls = ["https://github.com/djmarcin/bazel-toolchain/archive/76ce37e977a304acf8948eadabb82c516320e286.tar.gz"],
)

load("@com_grail_bazel_toolchain//toolchain:deps.bzl", "bazel_toolchain_dependencies")

bazel_toolchain_dependencies()

load("@com_grail_bazel_toolchain//toolchain:rules.bzl", "llvm_toolchain")

llvm_toolchain(
    name = "llvm_toolchain",
    llvm_version = "11.0.0",
)

load("@llvm_toolchain//:toolchains.bzl", "llvm_register_toolchains")

llvm_register_toolchains()
