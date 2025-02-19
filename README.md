
This project is a modification of 
# Azure Hipster Shop: AKS Microservices Demo
to be deployed onto digital ocean.
Disclaimer: No affiliation with DO other than being a customer.

This project is an extension of the project "Hipster Shop: Cloud-Native Microservices Demo Application" from Google, available here: https://github.com/GoogleCloudPlatform/microservices-demo

The main focus here is to be able to deploy that demo project to Azure Kubernetes Service using best practices.

## 0. Getting started

### Introduction

Hipster Shop is a demo project to test a microservices architecture on Kubernetes. It comprises an online shop powered by 10 different microservices, written in different programming languages (Java, Go, C#, Python, JavaScript/NodeJS). It is not a functional service or optimized, and its purpose is only for learning and testing. It comes with Locust preconfigured, a load generator that will start to run simulated traffic on the shop as soon as it boots up. 

The original Hipster Shop demo is intended for use in a local Kubernetes cluster or deployed to Google Kubernetes Engine. As Kubernetes is a standard, to add value to this demo we will explain how to deploy it on Azure Kubernetes Services (AKS) using Terraform, with a special focus on specific requirements for this cloud provider.

We will also deploy Prometheus as a metric extractor and Grafana as a visualization tool for those metrics into the Kubernetes cluster using Helm.

![general_diagram](./docs/img/general_diagram.png)

### How to use

This instructions comes with some __optional__, __alternative__ and __improvement__ parts. You can skip them if you like for a straight forward procedure. The improvements will suggest additional task that you could investigate on your own to improve this exercise.

We will assume we use a __bash__ shell environment. Whenever an example script starts with $, it means you should type what is beyond the symbol in your terminal. Sometimes the expected output of a command is shown, to make it easier to identify output information.

If you are using Windows, most of the explanations here could be used in cmd.exe, but you can achieve full compatibility by using [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

*Improvement:* Adapt the explanations and scripts to be able to use them from Windows's cmd.exe or Powershell.

### Contents

* [0. Getting started](./README.md)
* [1. Prerequisites](./docs/01_prerequisites.md)
* [2. Initial Azure resources setup](./docs/02_setup_az_sp.md)
* [3. Provision infrastructure with Terraform](./docs/03_infra_terraform.md)
* [4. Get credentials](./docs/04_get_credentials.md)
* [5. Installing Prometheus and Grafana using Helm](./docs/05_helm.md)
* [6. Deploy microservices with Skaffold](./docs/06_cluster_skaffold.md)
* [7. Terminate and free resources](./docs/98_free_resources.md)
* [Appendix: Troubleshooting](./docs/99_troubleshooting.md)

---
[Next step: 1. Prerequisites](./docs/01_prerequisites.md)  
