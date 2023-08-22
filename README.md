# EKS Cluster Configuration

This repository provides an example `eks-cluster-config.yaml` file that defines a basic Amazon EKS cluster configuration. The configuration includes details for the cluster's metadata, availability zones, managed node groups, IAM settings, and addons.

## Prerequisites

- Log in with your AWS credentials using `aws configure`.
- Install `eksctl` by following the installation guide [here](https://eksctl.io/introduction/#installation).
- Have an existing Amazon EC2 Key Pair. If you don't have one, create a new key pair.

## Usage

1. Clone this repository to your local machine:
   
   ```bash
   git clone https://github.com/your-username/eks-cluster-config.git
   cd eks-cluster-config
   ```
   
3. Open the eks-cluster-config.yaml file and modify the placeholders between < > with your actual values.
   
4. To create the EKS cluster, use the following command:
   
   ```bash
   eksctl create cluster -f eks-cluster-config.yaml
   ```
   
6. To delete the EKS cluster, use the following command:
   
   ```bash
   eksctl delete cluster --name=<CLUSTER NAME> --region=<REGION>
   ```

## Configuration Details

The `eks-cluster-config.yaml` file includes various configuration settings:

- **Cluster Metadata:** Defines the name and region for the cluster.
- **Availability Zones:** Specifies the availability zones to be used.
- **Managed Node Group:** Describes the node group settings, including instance type, scaling, volumes, SSH access, IAM policies, and more.
- **IAM Configuration:** Sets up IAM roles and policies associated with the cluster.
- **Addons Configuration:** Specifies any addons you want to enable for the cluster.

Make sure to modify the values in the configuration file to match your requirements.
