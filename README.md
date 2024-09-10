# Lab4-kubernetes first 10 quistions 

Here's a sample `README.md` file for the tasks related to Kubernetes namespaces:

```markdown
# Kubernetes Namespace Operations

This document provides a step-by-step guide on managing Kubernetes namespaces using `kubectl` commands.

## 1. Understanding Namespaces

A namespace in Kubernetes is a way to organize and manage resources within a cluster. It allows for resource isolation and management across different environments or projects.

## 2. Creating a New Namespace

To create a new namespace, use the following command:

```sh
kubectl create namespace <namespace-name>
```

Replace `<namespace-name>` with the name of your desired namespace.

## 3. Listing All Namespaces

To list all namespaces in the cluster, use:

```sh
kubectl get namespaces
```

## 4. Default Namespace

The default namespace in Kubernetes is named `default`. If you do not specify a namespace, resources will be created in this namespace.

## 5. Deleting a Namespace

To delete a namespace and all resources within it, use:

```sh
kubectl delete namespace <namespace-name>
```

## 6. Switching Between Namespaces

To switch between namespaces, you can use the `--namespace` flag in your commands or set the current context:

```sh
kubectl get pods --namespace=<namespace-name>
```


## 7. Creating a Deployment in a Specific Namespace

To create a deployment in a specific namespace:

```sh
kubectl create deployment <deployment-name> --image=<image-name> --namespace=<namespace-name>
```

## 8. Resource Name Collision

Namespaces allow for the same resource name to exist in different namespaces. This means two different namespaces can have resources with identical names without conflict.

## 9. Checking Resource Quotas and Limits

To check resource quotas and limits for a specific namespace:

```sh
kubectl get resourcequotas --namespace=<namespace-name>
```

## 10. Configuring Default Namespace in kubectl Context

To configure `kubectl` to always use a specific namespace by default:

```sh
kubectl config set-context --current --namespace=<namespace-name>
```

