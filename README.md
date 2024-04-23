# Online Shop Microservices Deployment with Kubernetes and Helm

This repository contains the configuration files and Helm charts for deploying an online shop microservices architecture using Kubernetes and Helm. The project employs containerization for scalability and Kubernetes for orchestration, enabling efficient management of the microservices ecosystem.

## Prerequisites

- Kubernetes cluster (e.g., AWS EKS, Google Kubernetes Engine, Minikube)
- Helm installed on the local machine
- Basic knowledge of Kubernetes and Helm

## Components

### Microservices

- **Email Service:** Sends email notifications to users.
- **Recommendation Service:** Provides product recommendations based on user preferences.
- **Product Catalog Service:** Manages product information and inventory.
- **Payment Service:** Handles payment processing securely.
- **Shipping Service:** Manages shipping logistics for orders.
- **Ad Service:** Displays targeted advertisements to users.
- **Cart Service:** Manages user shopping carts and checkout processes.
- **Currency Service:** Converts prices between different currencies for international users.
- **Checkout Service:** Orchestrates the checkout process, integrating payment, shipping, and order confirmation.
- **Frontend:** Provides the user interface for browsing and purchasing products.

### Helm Charts

Each microservice is packaged as a Helm chart for easy deployment and management. Values in the `values.yaml` files can be customized to configure each microservice's deployment settings.

## Deployment Steps

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Modify the Helm charts in the `k8s_config/charts` directory as needed.
4. Deploy the microservices using Helm:
   ```bash
   helm install my-online-shop k8s_config/charts/microservices

## Usage

1. **Wait for Deployment:** Allow some time for the deployment process to complete. Once finished, verify the resources created in your Kubernetes cluster.

2. **Access the Online Shop Frontend:** After deployment is complete, access the online shop frontend using the provided URL.

3. **Explore Features:**
    - Browse Products: Explore the catalog of products available in the online shop.
    - Add Items to Cart: Select products and add them to your shopping cart.
    - Complete Checkout Process: Proceed to checkout, enter payment and shipping details, and complete the purchase.

4. **Monitor Kubernetes Cluster:**
    - Resource Utilization: Keep an eye on resource utilization to ensure optimal performance and avoid resource exhaustion.
    - Pod Health: Monitor the health of individual pods to identify any issues or failures.
    - System Performance: Observe the overall system performance to detect any bottlenecks or areas for improvement.

5. **Scale Microservices:**
    - Based on Traffic Load: Scale individual microservices as needed to handle fluctuations in traffic load and ensure responsiveness.
    - Resource Requirements: Adjust the resources allocated to microservices based on their requirements and performance metrics.

6. **Troubleshoot Issues:**
    - Kubernetes Logs: Check the logs of pods to identify any errors or issues.
    - Kubernetes Events: Monitor Kubernetes events for changes and potential problems in the cluster.
    - Kubernetes Metrics: Utilize Kubernetes metrics to analyze resource usage, pod health, and cluster performance.