# Task 3: Infrastructure as Code (IaC) with Terraform

Overview

This project demonstrates how to use terraform as Infrastructure as Code (IaC) to provision and manage a local Docker container.

The objective of this task is to define the Docker infrastructure using Terraform configuration instead of creating the container manually with Docker commands.

 Objective

Provision a local Docker container using Terraform and demonstrate the complete Terraform workflow:

- Initialize the Terraform project
- Create an execution plan
- Apply the configuration
- Verify the Docker container
- Check Terraform state
- Destroy the infrastructure

## Technologies Used

- Terraform
- Docker
- GitHub

## Project Structure

```text
Terraform-docker-task/
│
├── main.tf
├── README.md
└── Screenshots/
    ├── terraform-init.png
    ├── terraform-plan.png
    ├── terraform-apply.png
    ├── docker-ps.png
    ├── terraform-state.png
    └── terraform-destroy.png
```

## Terraform Configuration

The `main.tf` file contains the Terraform configuration required to communicate with Docker and provision the Docker container.

The Docker provider is used to allow Terraform to interact with the local Docker engine.

## Execution Steps

### 1. Initialize Terraform

```bash
terraform init
```

This initializes the Terraform working directory and downloads the required provider.

### 2. Create Terraform Plan

```bash
terraform plan
```

This previews the changes Terraform intends to make without actually creating the resources.

### 3. Apply the Configuration

```bash
terraform apply
```

Terraform creates the resources defined in `main.tf`.

When prompted, enter:

```text
yes
```

### 4. Verify the Docker Container

```bash
docker ps
```

This verifies that the Docker container created by Terraform is running.

### 5. Check Terraform State

```bash
terraform state list
```

This displays the resources currently managed by Terraform.

Terraform also maintains a state file to keep track of the infrastructure it manages.

### 6. Destroy the Infrastructure

```bash
terraform destroy
```

When prompted, enter:

```text
yes
```

This removes the infrastructure created by Terraform.

## Terraform Workflow

```text
main.tf
   ↓
terraform init
   ↓
terraform plan
   ↓
terraform apply
   ↓
Docker Container
   ↓
terraform state list
   ↓
terraform destroy
```

Screenshots

Execution screenshots are included in the `Screenshots` directory.

They demonstrate:

1. Terraform initialization
2. Terraform plan
3. Terraform apply
4. Docker container verification
5. Terraform state
6. Terraform destroy

## Outcome

This task demonstrates the basic principles of **Infrastructure as Code** using Terraform and Docker. It shows how infrastructure can be defined in code, planned, provisioned, inspected, and destroyed in a consistent and repeatable way.
