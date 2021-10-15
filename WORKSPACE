load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# import libraries from maven
RULES_JVM_EXTERNAL_TAG = "2.8"

RULES_JVM_EXTERNAL_SHA = "79c9850690d7614ecdb72d68394f994fef7534b292c4867ce5e7dec0aa7bdfad"

http_archive(
    name = "rules_jvm_external",
    sha256 = RULES_JVM_EXTERNAL_SHA,
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "software.amazon.smithy:smithy-model:1.12.0",
        "software.amazon.smithy:smithy-cli:1.12.0",
        "software.amazon.smithy:smithy-openapi:1.12.0",
        "software.amazon.smithy:smithy-aws-traits:1.12.0",
        "software.amazon.smithy:smithy-aws-apigateway-openapi:1.12.0",
        "software.amazon.smithy:smithy-linters:1.12.0",
        "software.amazon.smithy:smithy-aws-apigateway-traits:1.12.0",
    ],
    excluded_artifacts = [],
    repositories = [
        "https://repo1.maven.org/maven2",
    ],
)
