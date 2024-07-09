# Statflo Reusable GitHub Actions Workflows Documentation

This documentation outlines the inputs required for various GitHub Actions workflows within the Statflo repository. These workflows facilitate automated processes for different programming languages and deployment scenarios, including Java, Docker, JavaScript, and more.

## Workflow Inputs Overview

### Common Inputs Across Workflows

- `service_path`: Specifies the path of the service being deployed. It is also used to match the `artifactId` in `pom.xml` for Java workflows and to track infrastructure folders for Docker deployments.
- `AWS_ACCESS_KEY_DEVELOPMENT`: A secret key for AWS access, required for workflows interacting with AWS services like ECR.
- `AWS_SECRET_ACCESS_KEY_DEVELOPMENT`: A secret key for AWS secret access, necessary for authentication with AWS services.

### Java Workflows

- `java_distribution`: The distribution of JDK being used. Supported distributions can be found in the [setup-java GitHub Action documentation](https://github.com/actions/setup-java).
- `java_version`: Specifies the version of JDK to be used.

### Docker Workflows

- `environment`: Defines the deployment environment (e.g., development, production).
- `namespace`: Specifies the namespace of the service, used for ECR and Kubernetes configurations.
- `shared_context`: Indicates whether the Dockerfile needs context from the entire repository.

### JavaScript Workflows

- `working_directory`: Sets a working directory, useful in monorepo setups.
- `s3_bucket`: The address of the S3 bucket for deployments, without the `s3://` prefix.
- `s3_bucket_region`: The AWS region where the S3 bucket is located.
- `cf_dist_id`: The CloudFront Distribution ID for the deployed website.
- `build_env`: An application-specific environment variable.

### JavaScript NX Workflows

- `versioning`: Enables versioning for deployments, allowing for rollback and history tracking.

### Revision Update Workflow

- `commit_id`: The commit hash that needs to be added to the revision file.
- `revision_file`: The name of the revision file to be updated.

## Usage

To use these workflows, configure the required inputs in your `.github/workflows/` YAML files. Ensure that secrets like `AWS_ACCESS_KEY_DEVELOPMENT` and `AWS_SECRET_ACCESS_KEY_DEVELOPMENT` are set in your repository's secrets settings.

For more detailed instructions on setting up and using these workflows, refer to the specific documentation sections for each programming language and deployment scenario.