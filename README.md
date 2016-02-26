# Amazon API Gateway Swagger Exporter

The **Amazon API Gateway Swagger Exporter** lets you export API specification from existing [Amazon API Gateway][service-page] APIs in a Swagger API representation.

This tool was inspired by [Amazon API Gateway Importer][aws-apigateway-importer]

[service-page]: http://aws.amazon.com/api-gateway/
[aws-apigateway-importer]: https://github.com/awslabs/aws-apigateway-importer

## Usage

### Prerequisites

This tool requires the [AWS CLI](http://aws.amazon.com/cli).
Download and configure following [instructions](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html) to set up your system for accessing your AWS account.

Alternatevly, you can use environment variables to provide AWS access credentials and AWS region.
Environment variables override AWS CLI configuration and can be useful for scripting.
The following variables are supported: AWS\_ACCESS\_KEY\_ID, AWS\_SECRET\_ACCESS\_KEY and AWS\_DEFAULT\_REGION.

Build with `mvn assembly:assembly`

### Export an existing API in Swagger YAML format, output to console

```sh
./aws-api-export.sh --api API_ID
```

### Export an existing API in Swagger JSON format, save to a file

```sh
./aws-api-export.sh --api API_ID --format json --output FILENAME.json
```

### Describe all CLI parameters
```sh
./aws-api-exporter.sh
```

For Windows environments replace `./aws-api-export.sh` with `./aws-api-export.cmd` in the examples.

