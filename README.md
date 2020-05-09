# Kustomization for Deploying Jenkins to OpenShift

This kustomization utilizes the [openshift-jenkins-operator](https://github.com/redhat-developer/openshift-jenkins-operator).

## Deploying Jenkins

Install openshift-jenkins-operator using:

```
$ oc apply --kustomize openshift-jenkins-operator/base
```

Verify that the operator installed successfully:

```
$ oc get csv --namespace jenkins
NAME                                 DISPLAY              VERSION   REPLACES   PHASE
jenkins-operator.v0.4.0              Jenkins Operator     0.4.0                Succeeded
```

Deploy Jenkins server:

```
$ oc apply --kustomize openshift-jenkins-instance/base
```
