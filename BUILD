genrule(
    name = "release",
    srcs = ["smithy_cli_executable_deploy.jar"],
    outs = ["smithy_cli.jar"],
    cmd = "cp $(location smithy_cli_executable_deploy.jar) $@",
    visibility = ["//visibility:public"],
)

java_binary(
    name = "smithy_cli_executable",
    main_class = "software.amazon.smithy.cli.SmithyCli",
    resources = [
        ":smithy_resources",
    ],
    runtime_deps = [
        ":smithy_deps",
    ],
)

java_library(
    name = "smithy_deps",
    exports = [
        "@maven//:software_amazon_smithy_smithy_cli",
        "@maven//:software_amazon_smithy_smithy_openapi",
    ],
)

java_library(
    name = "smithy_resources",
    exports = [
        "@maven//:software_amazon_smithy_smithy_aws_apigateway_openapi",
        "@maven//:software_amazon_smithy_smithy_aws_traits",
    ],
)
