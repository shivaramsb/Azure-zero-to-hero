### Project Overview
- **Application**: E-commerce app with 8 microservices
- **Databases**: MySQL and MongoDB
- **In-memory Data Store**: Redis
- **Components**: Deployments, StatefulSets, Persistent Volumes, Storage Classes, Ingress Configuration

### Architecture
- **Initial Setup**: Deployed locally on a laptop
- **Source Code**: Available on GitHub (Instana Robot Shop by IBM)
- **Microservices**: Each written in different programming languages (Node.js, Python, PHP, etc.)

### User Workflow
1. **Registration**: User registers an account.
2. **Login**: User logs in with credentials.
3. **Browsing**: Categories include Artificial Intelligence and Robots.
4. **Product Interaction**: Users can rate products and add them to the cart.
5. **Checkout**: Users can select quantity, add to cart, and proceed to checkout.
6. **Shipping Calculation**: Based on user location.
7. **Payment**: Integration with payment gateways like PayPal or Stripe (not implemented in demo).
8. **Order Confirmation**: Users receive a confirmation message.

### Microservices Breakdown
1. **User Service**: Handles user registration and login.
2. **Catalog Service**: Manages product categories and details.
3. **Cart Service**: Manages the shopping cart.
4. **Payment Service**: Handles payment processing.
5. **Shipping Service**: Calculates shipping costs based on location.
6. **Dispatch Service**: Manages order dispatch information.
7. **Web Service**: Hosts the user interface.
8. **Ratings Service**: Manages product ratings using Redis.

### Databases
- **MySQL**: Stores product images and related data.
- **MongoDB**: Stores user registration and secure information.

### Containerization
- **Docker Files**: Each microservice has a Dockerfile for containerization.
- **Examples**:
  - **Node.js**: Uses `node` base image, installs dependencies, and runs the server.
  - **Python**: Uses `python` base image, installs dependencies, and runs the application.
  - **Go**: Uses multi-stage builds to reduce image size.
  - **Java**: Uses multi-stage builds to create and run JAR files.

### Kubernetes Deployment
- **Helm Charts**: Used for deploying microservices on AKS.
- **Templates**: YAML files for deployments, services, and stateful sets.
- **Values.yaml**: Contains dynamic values for different environments (Dev, Staging, Prod).

### Persistent Storage
- **Redis**: Configured as a StatefulSet with a Persistent Volume Claim (PVC).
- **Storage Classes**: Default storage class in AKS is Azure Disk.

### Ingress Configuration
- **Ingress Controller**: Enabled in AKS for external access.
- **Ingress Resource**: Configured to route traffic to the web service.

### Deployment Steps
1. **Create AKS Cluster**: Using Azure portal.
2. **Containerize Microservices**: Using Dockerfiles.
3. **Deploy Using Helm**: Apply Helm charts to deploy microservices.
4. **Enable Ingress**: Configure Ingress controller for external access.

### Troubleshooting
- **Persistent Volume Claims**: Ensure correct storage class and access modes.
- **Ingress Issues**: Check logs and configurations for errors.

### Conclusion
- **Project Benefits**: Hands-on experience with microservices, containerization, and Kubernetes.
- **Learning Outcomes**: Understanding of deploying a complex application on AKS.
