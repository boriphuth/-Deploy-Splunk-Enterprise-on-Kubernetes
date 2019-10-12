# -Deploy-Splunk-Enterprise-on-Kubernetes
https://www.ibm.com/cloud/blog/solving-business-problems-with-splunk-on-ibm-cloud-kubernetes-service

```
$ kubectl create ns splunk
$ kubectl -n splunk apply -f tiller-rbac-config.yaml
$ helm init --service-account tiller --tiller-namespace splunk
$ helm update
$ helm install --name kubecon-demo-2018 --tiller-namespace splunk --namespace splunk -f values.yaml https://github.com/splunk/splunk-connect-for-kubernetes/releases/download/v1.0.1/splunk-connect-for-kubernetes-1.0.1.tgz

$ helm install --name splunk-connect-k8 \
--namespace splunk \
--tiller-namespace splunk \
-f values1.yaml \
https://github.com/splunk/splunk-connect-for-kubernetes/releases/download/v1.0.1/splunk-connect-for-kubernetes-1.0.1.tgz

$ helm install --name splunk-connect-k8 \
--namespace splunk \
--tiller-namespace splunk \
-f values.yaml \
https://github.com/splunk/splunk-connect-for-kubernetes/releases/download/v1.0.1/splunk-connect-for-kubernetes-1.0.1.tgz

```