# Statflo Reusable GitHub Actions Workflows

## Inputs

### Java - PR

| Name | Value | Default | Description |
|---|---|---|---|
| service | string | . | Path of the service being deployed |
| java_distribution | string | temurin | Distribution of JDK being used, refer to [this](https://github.com/actions/setup-java) for a list of distributions available |
| java_version | string |  | Version of JDK being used, refer to link above for references of available versions |

### Java - Deploy

| Name | Value | Default | Description |
|---|---|---|---|
| environment | string |  | Environment being deployed to |
| service_path | string | . | Path of service being deployed, used for tracking infrastructure folders |
| service | string | . | Name of the service in Kubernetes (i.e sso) |
| package_name | string |  | Full path used by ECR to maintain image (i.e common/sso) |
| java_distribution | string | temurin | Distribution of JDK being used, refer to [this](https://github.com/actions/setup-java) for a list of distributions available |
| java_version | string |  | Version of JDK being used, refer to link above for references of available versions |
| AWS_ACCESS_KEY_DEVELOPMENT | string |  | SECRET: AWS access key to access a specific ECR |
| AWS_SECRET_ACCESS_KEY_DEVELOPMENT | string |  | SECRET: AWS secret access key to access a specific ECR |
