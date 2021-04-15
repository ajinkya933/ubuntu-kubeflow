

```
sudo usermod -a -G microk8s ${USER}
# open a new shell for the user, with updated group membership 
su - ${USER}
```

```
sudo snap switch microk8s --channel=latest/candidate
sudo snap refresh
```
