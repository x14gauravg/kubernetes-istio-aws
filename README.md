# Instructions to install Kubernetes on AWS
aws-k8-install-instructions.txt

# install Istio on AWS

Just apply file istio_default_k8_native.yaml on the cluster. When you applky the file, you will get some errors such as objects not created, apply the file again.  This is because certain yaml objects are created at last of the file, which some of the previous objects require first

kubectl apply -f istio_default_k8_native.yaml


# Install Istio on Minikube
Just apply file istio_demo_k8_native.yaml on the cluster. When you applky the file, you will get some errors such as objects not created, apply the file again.  This is because certain yaml objects are created at last of the file, which some of the previous objects require first

kubectl apply -f istio_default_k8_native.yaml

# Start minikube with 4096 memory. 
-p flag allows to give a cluster name

minikube -p gg --memory 4096

# Run demo of canary release
kubectl apply -f demo-canaryrelease.yaml

# Run demo of dark release
kubectl apply -f demo-darkrelease.yaml



