# Infrastructure Deployment

## Preparation
Move config to ~/.kube/config

cp config ~/.kube/config

Download kubectl from https://kubernetes.io/docs/tasks/tools/install-kubectl/

### Mac
1 - Manual
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/darwin/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
2 - Brew 
brew install kubectl


## Creating

kubectl create -f namespace.yaml

kubectl config set-context dev 	--namespace=development 	--cluster='Infrastructure' --user='Infrastructure'
kubectl config set-context prod 	--namespace=production 	--cluster='Infrastructure' --user='Infrastructure'
kubectl config set-context uat 	--namespace=uat 			--cluster='Infrastructure' --user='Infrastructure'

kubectl config use-context dev|prod|uat

kubectl create -f infrastructure.yaml