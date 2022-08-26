# Statflo Reusable GitHub Actions Workflows

## Inputs

### Java - PR

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| service | string | . | Path of the service being deployed | True |
| java_distribution | string | temurin | Distribution of JDK being used, refer to [this](https://github.com/actions/setup-java) for a list of distributions available | True |
| java_version | string |  | Version of JDK being used, refer to link above for references of available versions | True |

### Java - Deploy

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| environment | string | development | Environment being deployed to | True |
| service_path | string | . | Path of service being deployed, used for tracking infrastructure folders | False |
| service | string | . | Name of the service in Kubernetes (i.e sso) | True |
| namespace | string |  | Namespace (if applicable) of the service (used for ECR) | True |
| java_distribution | string | temurin | Distribution of JDK being used, refer to [this](https://github.com/actions/setup-java) for a list of distributions available | True |
| java_version | string |  | Version of JDK being used, refer to link above for references of available versions | True |
| AWS_ACCESS_KEY_DEVELOPMENT | string |  | SECRET: AWS access key to access a specific ECR | True |
| AWS_SECRET_ACCESS_KEY_DEVELOPMENT | string |  | SECRET: AWS secret access key to access a specific ECR | True |

### Docker - PR

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| service_path | string | . | Path of service being deployed, used for tracking infrastructure folders | False |
| service | string |  | Name of the service in Kubernetes (i.e sso) | False |

### Docker - Deploy

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| environment | string | development | Environment being deployed to | True |
| service_path | string | . | Path of service being deployed, used for tracking infrastructure folders | False |
| service | string | . | Name of the service in Kubernetes (i.e sso) | False |
| namespace | string |  | Namespace (if applicable) of the service (used for ECR) | True |
| AWS_ACCESS_KEY_DEVELOPMENT | string |  | SECRET: AWS access key to access a specific ECR | True |
| AWS_SECRET_ACCESS_KEY_DEVELOPMENT | string |  | SECRET: AWS secret access key to access a specific ECR | True |
