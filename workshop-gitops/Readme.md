```m
OpenShift Console Access
Your OpenShift cluster console is available at:
https://console-openshift-console.apps.cluster-q6vfx.q6vfx.sandbox230.opentlc.com

User login is available with:

Username: user1
Password: openshift

Administrator login is available with:

Admin Username: opentlc-mgr
Admin Password: r3dh4t1!

The OpenShift API is available at:
https://api.cluster-q6vfx.q6vfx.sandbox230.opentlc.com:6443

The oc command line utility is available for download at:
http://mirror.openshift.com/pub/openshift-v4/clients/ocp/4.12.12/openshift-client-linux-4.12.12.tar.gz
```


```bash
kubectl get secret openshift-gitops-cluster \
-o json \
-n openshift-gitops |\
jq '.data["admin.password"]' -r |\
base64 --decode | xargs echo
# JuTg5ynGPEFiwH7L0sRKatzMe9xZd3Op
```