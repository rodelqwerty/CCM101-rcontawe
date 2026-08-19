
# Checkpoint 4 – Research the Major Cloud Providers

## Cloud Provider Comparison

AWS, Microsoft Azure, and Google Cloud Platform (GCP) provide similar basic cloud services. However, each provider uses different names and features for these services. The table below compares their main services for compute, storage, networking, and identity and access management.

| **Infrastructure Component**             | **AWS**                                                                           | **Microsoft Azure**                                                                              | **Google Cloud Platform (GCP)**                                                               |
| ---------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| **Compute**                              | **Amazon EC2** – Provides virtual servers for running applications and workloads. | **Azure Virtual Machines** – Provides virtual machines for running applications and services.    | **Google Compute Engine** – Provides virtual machines for running applications and workloads. |
| **Storage**                              | **Amazon S3** – Stores and retrieves files and other types of data.               | **Azure Blob Storage** – Stores files and other unstructured data.                               | **Google Cloud Storage** – Stores and accesses data in the cloud.                             |
| **Networking**                           | **Amazon VPC** – Creates an isolated virtual network for AWS resources.           | **Azure Virtual Network (VNet)** – Provides a private network for Azure resources.               | **Google Cloud VPC** – Provides networking for Google Cloud resources.                        |
| **Identity and Access Management (IAM)** | **AWS IAM** – Controls who can access AWS resources and what they can do.         | **Microsoft Entra ID + Azure RBAC** – Manages identities and controls access to Azure resources. | **Google Cloud IAM** – Controls access to Google Cloud resources using roles and permissions. |

## Guide Questions

### 1. Which cloud provider offers the broadest range of services? Explain your answer.

**AWS** is generally considered to have one of the broadest selections of cloud services. It provides many services for computing, storage, networking, databases, security, analytics, and AI/ML.

### 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?

I would recommend **Microsoft Azure** because it works well with Microsoft products and technologies. Organizations using Windows Server, Microsoft 365, and Microsoft Entra ID can easily connect these services with Azure.

### 3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?

**Google Cloud Platform (GCP)** is widely known for its AI, ML, and Kubernetes services. Google created Kubernetes and provides **Google Kubernetes Engine (GKE)** and **Vertex AI** for containerized applications and AI/ML workloads.

### 4. What similarities did you observe among the three cloud providers?

All three providers offer similar basic infrastructure services, including computing, storage, networking, and identity management. The main difference is that they use different service names and may provide different features, but the basic purpose of the services is similar.

## Official Documentation Sources

### 🟠 Amazon Web Services (AWS)

| **Service**    | **Official Documentation**                                |
| -------------- | --------------------------------------------------------- |
| 🖥️ Amazon EC2 | [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/) |
| 💾 Amazon S3   | [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)   |
| 🌐 Amazon VPC  | [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/) |
| 🔐 AWS IAM     | [AWS IAM Documentation](https://docs.aws.amazon.com/iam/) |

### 🔵 Microsoft Azure

| **Service**                        | **Official Documentation**                                                                     |
| ---------------------------------- | ---------------------------------------------------------------------------------------------- |
| 🖥️ Azure Virtual Machines         | [Azure VM Documentation](https://learn.microsoft.com/en-us/azure/virtual-machines/)            |
| 💾 Azure Blob Storage              | [Azure Blob Storage Documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/)     |
| 🌐 Azure Virtual Network           | [Azure VNet Documentation](https://learn.microsoft.com/en-us/azure/virtual-network/)           |
| 🔐 Microsoft Entra ID / Azure RBAC | [Azure RBAC Documentation](https://learn.microsoft.com/en-us/azure/role-based-access-control/) |

### 🔴 Google Cloud Platform (GCP)

| **Service**         | **Official Documentation**                                                 |
| ------------------- | -------------------------------------------------------------------------- |
| 🖥️ Compute Engine  | [Compute Engine Documentation](https://docs.cloud.google.com/compute/docs) |
| 💾 Cloud Storage    | [Cloud Storage Documentation](https://docs.cloud.google.com/storage/docs)  |
| 🌐 Google Cloud VPC | [Google Cloud VPC Documentation](https://docs.cloud.google.com/vpc/docs)   |
| 🔐 Google Cloud IAM | [Google Cloud IAM Documentation](https://docs.cloud.google.com/iam/docs)   |

## Conclusion

AWS, Azure, and Google Cloud all provide the basic services needed to build and run cloud applications. Their service names are different, but the main ideas are similar: **compute runs applications, storage saves data, networking connects resources, and IAM controls access**.
