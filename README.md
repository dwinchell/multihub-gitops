# multihub-gitops
An example of centralized GitOps with multiple hubs

# Getting Started

**IMPORTANT: When you clone this, use the --recurse-submodules option**

This repository uses a submodule. In order for git to correctly pull the code, specify the --recurse-submodules option as part of the clone command:

```
git clone --recurse-submodules https://github.com/dwinchell/multihub-gitops.git
```
2. Install the Pattern.
```
./pattern.sh make install
```

3. Populate the secret data that the example application displays.
```
oc new-project validated-patterns-secrets
oc create secret generic --from-literal="secret=Secret Data" config-demo -n validated-patterns-secrets
```

4. View the example application at http://config-demo-config-demo.your.cluster/
