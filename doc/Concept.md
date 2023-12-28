# Kubernetes DevOps tools for AsciiArtify 
## Intro
Review of three container orchestration system for automating software deployment: **minikube**, **kind** and **k3d**.<br/>
**minikube** is a tool that runs a single-node Kubernetes cluster in a virtual machine on your laptop.<br/>
**kind** is a tool for running local Kubernetes clusters using Docker container “nodes”.<br/>
**k3d** is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker. k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes.<br/>

| **Tool** | **minikube** | **kind** | **k3d** |
|---|---|---|---|
| **OS** | Windows, MacOs, Linux | Windows, MacOs, Linux | Windows, MacOs, Linux |
| **Architecture** | arm, arm64, x86, x64 | x64, arm64 | arm, arm64, x86, x64 |
| **Automation capabilities** | Has integration with various CI platforms | May be used for CI, good for automation tests | Good for automation, has quick deployments and fast startup |
| **Easy of use** | Good for beginners, focusing on making it easy to learn and develop | Pretty complex | Easy to use, need basic understanding |
| **Pros** | Good for beginners; Easy to use; Built-in dashboard | Flexibility on cluster configuration; Less resource consumptions | Good documentatation and community support; Lightweight; Fast cluster deployment; Good for teams (possibility to share cluster configuration file) |
| **Cons** | Can be slow to start up | Limited community documentation | No copying of locally-built images into cluster |

## Conclusion
After tools exploration I think that k3d fits. k3d is a powerful tool that simplifies Kubernetes setups for local development. It offers a lightweight, flexible, and cost-effective way to test and develop applications in a Kubernetes environment. With k3d, developers can quickly iterate over their Kubernetes configurations, test their applications in a realistic environment, and seamlessly integrate Kubernetes into their existing workflows.

## Demo
![Demo](/demo.gif)