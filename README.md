# Serverless-vs-Terraform

Make a comparison between Serverless Framework and Terraform as tools for IaC. answer the following:

1.  What type of infrastructure and application deployments are each tool best suited for?

- Serverless Framework is best suited for workloads that leverage serverless compute resources such as AWS Lambda. It is best suited for deployments that rely heavily on managed cloud services like databases (eg. AWS DynamoDB, RDS).

- Terraform is best suited for managing a combination of cloud services and traditional infrastructure (eg. VMs, Databases). It is best suited for multi-cloud deployments where resources are spread across multiple providers.
  
2. How do their primary objectives differ?

- Serverless Framework's primary objective is to simplify the deployment of serverless applications with minimal configuration and management overhead.

- Terraform’s primary objective is to provision infrastructure and manage them across various providers and on-premise environments.
  
3. How do they differ in terms of learning curve and ease of use for developers or DevOps teams?

- Serverless Framework is generally more accessible compared to Terraform in terms of learning curve and ease of use because it uses a YAML configuration file to define the functions, events and resources required. Terraform uses the Hashicorp Configuration Language (HCL) and requires understanding of the resources, relationships and dependencies of the managed infrastructure, its complexity increases significantly as we venture beyond basic setups.

4. What are the differences in how each tool handles state tracking and deployment changes?

- Terraform handles state tracking by using a local or remote state file to track the current state of infrastructure and compares the execution plan by comparing the configuration with the existing state, applying only the necessary changes

- Serverless Framework tracks state by using AWS CloudFormation under the hood and compares the configuration (serverless.yaml) to the current state in the cloud and updates the resources accordingly using CLoudFormation

5. In what scenarios would you recommend using Serverless Framework over Terraform, and vice versa?

- I would recommend using Serverless Framework for building, deploying and managing event-driven serverless applications. On the other hand, I would recommend using Terraform to manage complex, multi-cloud infrastructure set-ups.

6. Are there scenarios where using both together might be beneficial?

- An example of a scenario that we can use both is to use Terraform to manage global infrastructure (eg. VPCs, load balancers, databases) and use the Serverless Framework to deploy and manage the application components (eg. Lambda, API gateway).
