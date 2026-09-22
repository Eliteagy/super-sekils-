# 04 - Infrastructure as Code and AMI Provisioning

**Tags:** #aws #cloudformation #packer #saltstack #infrastructure

## Infrastructure at Scale
Managing centralized load balancing meant deploying thousands of Envoy proxies across ~13 AWS regions.

## CloudFormation for Provisioning
The proxy infrastructure was defined using AWS CloudFormation, which orchestrated:
- VPCs, Subnets, and Internet Gateways (IGWs).
- Security Groups and IAM Roles.
- Auto Scaling Groups (ASGs) and Network Load Balancers (NLBs, Layer 4).
- AWS Certificate Manager (ACM) and Route 53 records.
- Parameters injected at runtime (secrets, keys, etc.).

## Creating the Standard Image (AMI)
To ensure the proxies booted with the correct baseline, a custom Amazon Machine Image (AMI) pipeline was established.
- **Tools Used:** HashiCorp Packer and SaltStack (configuration management similar to Ansible/Puppet).
- **Pipeline Flow:**
  1. Packer spins up an EC2 instance in a dev account.
  2. SaltStack uploads configuration and executes the provisioning step.
  3. The instance is snapshot and converted into an AMI.
- **AMI Contents:** Included Envoy installation, logging agents, security hardening, network tuning, and observability agents (for logs, tracing, and metrics).
