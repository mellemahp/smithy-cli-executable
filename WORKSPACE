load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# import libraries from maven
RULES_JVM_EXTERNAL_TAG = "4.2"
RULES_JVM_EXTERNAL_SHA = "cd1a77b7b02e8e008439ca76fd34f5b07aecb8c752961f9640dea15e9e5ba1ca"

http_archive(
    name = "rules_jvm_external",
    sha256 = RULES_JVM_EXTERNAL_SHA,
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

SMITHY_VERSION = "1.26.2"

maven_install(
    artifacts = [
        "software.amazon.smithy:smithy-model:%s" % SMITHY_VERSION,
        "software.amazon.smithy:smithy-cli:%s" % SMITHY_VERSION,
        "software.amazon.smithy:smithy-openapi:%s" % SMITHY_VERSION,
        "software.amazon.smithy:smithy-aws-traits:%s" % SMITHY_VERSION,
        "software.amazon.smithy:smithy-aws-apigateway-openapi:%s" % SMITHY_VERSION,
        "software.amazon.smithy:smithy-linters:%s" % SMITHY_VERSION,
        "software.amazon.smithy:smithy-aws-apigateway-traits:%s" % SMITHY_VERSION,
        "software.amazon.smithy.typescript:smithy-typescript-codegen:0.7.0",
    ],
    excluded_artifacts = [],
    repositories = [
        "https://repo1.maven.org/maven2",
    ],
)
