# RHEL 7 Kubernetes Pods

# Intro

- For more information on running Kubernetes on RHEL 7, see the [RHEL Container Docs](https://access.redhat.com/documentation/en/red-hat-enterprise-linux-atomic-host/version-7/getting-started-with-containers/#get_started_orchestrating_containers_with_kubernetes)

# Usage

- Once you have installed the necessary packages as described in the docs above, copy the pod files into the /etc/kubernetes/manifests directory.
```bash
$ mkdir -p /etc/kubernetes/manifests/ && cd /etc/kubernetes/manifests/
$ curl -s -L -O https://raw.githubusercontent.com/danielwhatmuff/rhel7-kubernetes-pods/master/apiserver.pod.json
$ curl -s -L -O https://raw.githubusercontent.com/danielwhatmuff/rhel7-kubernetes-pods/master/scheduler.pod.json
$ curl -s -L -O https://raw.githubusercontent.com/danielwhatmuff/rhel7-kubernetes-pods/master/controller-mgr.pod.json
```
- Ensure the kubelet service is started and and run the following to track progress...
```bash
$ kubectl get po
```

### Contributing
File issues in GitHub to report bugs or issue a pull request to contribute.
