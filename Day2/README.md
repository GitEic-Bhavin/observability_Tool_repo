##### Install helm chart in local
[setup helm chart local](https://helm.sh/docs/intro/install/)

##### Set up heml prometheus, alertmanager, grafana
[setup prometheus by helm](https://github.com/GitEic-Bhavin/35D-Training-repo/tree/training/Project/Day35)

##### Setup eksctl.
```
ARCH=amd64
PLATFORM=$(uname -s)_$ARCH

curl -sLO "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"

# (Optional) Verify checksum
curl -sL "https://github.com/eksctl-io/eksctl/releases/latest/download/eksctl_checksums.txt" | grep $PLATFORM | sha256sum --check

tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz

sudo mv /tmp/eksctl /usr/local/bin
```

- You can follow official instructions for other plateform
[eks installations](https://eksctl.io/installation/)


