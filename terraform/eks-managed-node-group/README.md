# EKS 클러스터 및 VPC 자동화

# Version

- **cli enviroment**: window
- **kubectl version**: v1.30.3-eks-2f46c53
- **aws version**: aws-cli/2.17.5 Python/3.11.8 Windows/10 exe/AMD64
- **terraform**: >= 1.3.2
- **required_providers version(hashicorp/aws)**: = >= 5.61
- **terraform-aws-modules/eks/aws version**: ~> 20.0
- **eks cluster_version**: 1.30

# EKS Managed Node Group Image

- `eks-al2.tf` demonstrates an EKS cluster using EKS managed node group that utilizes the EKS Amazon Linux 2 optimized AMI

See the [AWS documentation](https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html) for additional details on Amazon EKS managed node groups.

## Usage

To provision the provided configurations you need to execute:

```bash
$ terraform init
$ terraform plan
$ terraform apply --auto-approve
```

Note that this example may create resources which cost money. Run `terraform destroy` when you don't need these resources.

## EKS configmap update

```bash
$ aws eks update-kubeconfig --name bookstore-cluster
```

## shortcut key settings

```bash
$ doskey k=kubectl $*
```
