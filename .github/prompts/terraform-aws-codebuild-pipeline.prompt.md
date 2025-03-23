# Terraform AWS CodeBuild Pipeline Module

Create a Terraform module for setting up AWS CodeBuild projects to execute Terraform operations.

## Requirements

1. Create a Terraform module that provisions two separate AWS CodeBuild projects:
   - One for running `terraform plan` operations
   - One for running `terraform apply` operations
2. Configure the CodeBuild projects to:
   - Pull and execute Terraform code from specified repositories
   - Handle Terraform state management (remote state)
   - Report build status and logs back to the Django UI
   - Support various Terraform versions
   - Support arbitrary Terraform modules
3. Implement integration points for the Django UI:
   - Webhook endpoints for triggering builds
   - Status notification via SNS or EventBridge
   - Log streaming for real-time updates

## Module Structure

1. Follow Terraform module best practices for structure and organization.
2. Create separate resource files for logical groupings.
3. Provide comprehensive variable definitions with proper descriptions and defaults.
4. Include useful outputs for integration with other components.
5. Create examples directory with common usage patterns.

## Features

1. Support for custom Docker images with pre-installed Terraform versions.
2. Integration with AWS VCS providers for source code.
3. Secure handling of Terraform variables and secrets.
4. Source caching to speed up builds.
5. Configurable compute types and environments.
6. Support for VPC integration to access private resources.
7. Configurable timeouts and build queues.
8. Artifact handling for storing Terraform plans.

## Build Specifications

1. Create CodeBuild buildspec templates for plan and apply operations.
2. Implement proper error handling and exit code management.
3. Configure environment variables for Terraform operations.
4. Handle Terraform initialization with backends.
5. Set up proper logging for build output.

## Security Considerations

1. Implement security group best practices if using VPC.
2. Use principle of least privilege for CodeBuild service roles.
3. Secure handling of sensitive environment variables.
4. Implement proper logging and monitoring.
5. Support assumable roles for specific infrastructure deployments.

## Documentation

1. Create comprehensive README with usage examples.
2. Document all variables and outputs clearly.
3. Include architecture diagrams.
4. Provide guidance on security best practices.
