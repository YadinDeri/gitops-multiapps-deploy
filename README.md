# GitOps Project

This repository is structured to facilitate GitOps practices for deploying applications across multiple environments including development, testing, pre-production, and production.

## Project Structure

- **apps/**: Contains environment-specific configurations for applications.
  - **dev/**: Configuration values for deploying applications in the development environment.
    - `nginx-values.yaml`: Configuration values for the Nginx application.
    - `app1-values.yaml`: Configuration values for App1.
    - `app2-values.yaml`: Configuration values for App2.
  - **test/**: Intended for test environment configurations.
  - **preprod/**: Intended for pre-production environment configurations.
  - **prod/**: Intended for production environment configurations.

- **base/**: Contains base configurations and Helm charts for applications.
  - **nginx/**: Contains deployment and service configurations for the Nginx application.
    - `deployment.yaml`: Deployment configuration for Nginx.
    - `service.yaml`: Service configuration for Nginx.
  - **app1/**: Helm chart for App1.
    - `Chart.yaml`: Metadata for the Helm chart.
    - **templates/**: Contains templates for deployment and service.
      - `deployment.yaml`: Deployment template for App1.
      - `service.yaml`: Service template for App1.
    - `values.yaml`: Default configuration values for App1.
  - **app2/**: Contains deployment and service configurations for App2.
    - `deployment.yaml`: Deployment configuration for App2.
    - `service.yaml`: Service configuration for App2.

- **applicationset.yaml**: Defines the ApplicationSet resource for managing multiple applications in a GitOps workflow.

## Getting Started

1. Clone the repository:
   ```
   git clone <repository-url>
   cd gitops
   ```

2. Configure your Kubernetes cluster and ensure you have the necessary permissions.

3. Deploy applications using the provided Helm charts and values files for each environment.

## Usage

- Modify the values files in the `apps/<environment>/` directory to customize the deployment configurations for each application in the respective environment.
- Use Helm to deploy the applications defined in the `base/` directory.

## Contributing

Contributions are welcome! Please submit a pull request or open an issue for any enhancements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.