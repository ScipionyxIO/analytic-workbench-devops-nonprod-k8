# Analytic Workbench DevOps - Kubernetes

# Install Kubectl
In order to install kubeclient follow the instructions from https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-with-homebrew-on-macos.

For the inpatient:

	curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/darwin/amd64/kubectl
	chmod +x ./kubectl
	sudo mv ./kubectl /usr/local/bin/kubectl

# Set the Kubectl Environment variables
Copy the proper config/config-<environment> to ~/.kube/config:

	cp config/config-<environment> ~/.kube/config


