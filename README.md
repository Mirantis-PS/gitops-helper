# GitOps Helper

This tool automates the process of setting up and managing management cluster configurations, making it easier to maintain consistency and reproducibility.

## Features
- Automates configuration generation for GitOps-managed clusters.
- Simplifies the management of cluster state through Git.
- Provides a streamlined workflow for setting up managed clusters.

## Prerequisites
Before using GitOps Helper, ensure you have the following:
- Docker installed on your system.
- The templated repository of the [k0rdent-gitops](https://github.com/Mirantis-PS/k0rdent-fluxcd-template/) repository checked out locally

## Usage
To create a managed cluster configuration, you need to

1. Run the gitops-helper tool using Docker
    ```sh
    docker run -it -v $(pwd):/repo ghcr.io/mirantis-ps/gitops-helper:main create managed-cluster
    ```
1. Review and modify the generated configuration files as needed.
1. Commit and push the files to your Git repository.
1. Watch your GitOps-managed cluster to sync the state.

## License
This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for more details.

