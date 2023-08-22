# Statflo Reusable GitHub Actions Workflows

## Inputs

### Java - PR

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| service_path | string | . | Path of the service being deployed AND artifactId in pom.xml (must match) | True |
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

### JavaScript - PR

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| working_directory | string | . | Sets a working directory if a monorepo is being used | False |

### JavaScript - Deploy

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| working_directory | string | . | Sets a working directory if a monorepo is being used | False |
| s3_bucket | string |  | Address of the s3 bucket (`s3://` is not required) | True |
| s3_bucket_region | string | ca-central-1 | Region where the s3 bucket is located | False |
| cf_dist_id | string |  | Cloudfront Distribution ID where s3 website is hosted | True |
| build_env | string |  | Sets a app specific environment variable as needed | False |
| AWS_ACCESS_KEY | string |  | SECRET: AWS access key to deploy to environment | True |
| AWS_SECRET_ACCESS_KEY | string |  | SECRET: AWS secret access key to deploy to environment | True |

### JavaScript - Deploy

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| working_directory | string | . | Sets a working directory if a monorepo is being used | False |
| s3_bucket | string |  | Address of the s3 bucket (`s3://` is not required) | True |
| s3_bucket_region | string | ca-central-1 | Region where the s3 bucket is located | False |
| cf_dist_id | string |  | Cloudfront Distribution ID where s3 website is hosted | True |
| build_env | string |  | Sets a app specific environment variable as needed | False |
| versioning | boolean | False | Set to true if want to use versioning feature | False | 
| AWS_ACCESS_KEY | string |  | SECRET: AWS access key to deploy to environment | True |
| AWS_SECRET_ACCESS_KEY | string |  | SECRET: AWS secret access key to deploy to environment | True |

### Revision Update

| Name | Value | Default | Description | Required |
|---|---|---|---|---|
| service_path | string | . | Path of the service | False |
| commit_id | string |  | Commit hash that needs to be added to revision file | True |
| revision_file | string |  |Name of revision file that needs to be updated | True |

