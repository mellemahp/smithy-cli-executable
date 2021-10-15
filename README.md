# smithy-cli-executable
Simple repo to generate releases of a smithy-cli executable for use in bazel build rules in other projects. It basically just uses github actions and bazel to generate a convient zip file with all the jars inside. 

For more info about the open-source smithy project go check out the main AWS Labs repo [here](https://github.com/awslabs/smithy) or [the docs](https://awslabs.github.io/smithy/). 

This smithy executable also includes the following as runtime dependencies for convenience: 
- smithy-openapi
- smithy-aws-apigateway-openapi
- smithy-aws-traits


### Using in bazel build rules
