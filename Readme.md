

```
sudo usermod -a -G microk8s ${USER}
# open a new shell for the user, with updated group membership 
su - ${USER}
```


```
(base) ajinkya@ajinkya-AB350-Gaming-3:~$ microk8s.enable kubeflow
```
error:
```
Enabling dns...
Enabling storage...
Enabling ingress...
Enabling metallb:10.64.140.43-10.64.140.49...
Waiting for other addons to finish initializing...
Addon setup complete. Checking connectivity...

Couldn't contact api.jujucharms.com from within the Kubernetes cluster
Please check your network connectivity before enabling Kubeflow.

See here for troubleshooting help:

    https://microk8s.io/docs/troubleshooting#heading--common-issues

```

Solution
```
sudo snap switch microk8s --channel=latest/candidate
sudo snap refresh
```
