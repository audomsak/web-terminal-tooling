# Web Terminal Tooling

Default OpenShift Console Web Terminal tooling container.

Includes tools that a Kubernetes and OpenShift developer would like find in their terminal:
- [jq](https://github.com/stedolan/jq)
- [oc](https://github.com/openshift/origin) [4.9.0](https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/ocp/4.9.0)
- [kubectl](https://github.com/kubernetes/kubectl) [v0.21.0-beta.1](https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/ocp/4.8.3)
- [odo](https://github.com/openshift/odo) [v2.3.1](https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/odo/v2.3.1)
- [helm](https://helm.sh/) [3.6.2](https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/helm/3.6.2)
- [KNative](https://github.com/knative/client) [v0.23.0](https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/serverless/0.23.0)
- [Tekton CLI](https://github.com/tektoncd/cli) [0.19.1](https://mirror.openshift.com/pub/openshift-v4/x86_64/clients/pipeline/0.17.2)
- [rhoas](https://github.com/redhat-developer/app-services-cli) [0.34.2](https://github.com/redhat-developer/app-services-cli/releases/tag/0.34.2)
- [submariner](https://github.com/submariner-io/submariner) [v0.12.1](https://github.com/submariner-io/submariner/releases/tag/v0.12.1)
- [Maven](https://maven.apache.org/) [3.5.4](https://archive.apache.org/dist/maven/maven-3/3.5.4/binaries/)
- [Java](https://openjdk.org/projects/jdk/17/) [17.0.5](https://rockylinux.pkgs.org/8/rockylinux-appstream-aarch64/java-17-openjdk-devel-17.0.5.0.8-2.el8_6.aarch64.rpm.html)
- [PostgreSQL client](https://www.postgresql.org/download/linux/redhat/) [10](https://download.postgresql.org/pub/repos/yum/10/redhat/rhel-8-x86_64/)

## Contributing

### How to build

There is [template.Dockerfile](https://github.com/redhat-developer/web-terminal-tooling/blob/master/build/template.Dockerfile) that is processed by build.sh script to apply needed changes before build. So, execute the following but before uncomment configuration params if needed.

```bash
TOOL=podman # can be docker
MODE=local # can be brew
WEB_TERMINAL_TOOLING_IMG=web-terminal-tooling:local
./build.sh
```

### How to run

```bash
podman run -ti --rm web-terminal-tooling:local bash
```
## Container Registry

Avaliable at [Red Hat Quay](https://quay.io/repository/asuksunt/web-terminal-tooling?tab=tags)

Upstream and downstream are synced via this [job](https://codeready-workspaces-jenkins.rhev-ci-vms.eng.rdu2.redhat.com/job/web-terminal-sync-web-terminal-tooling/)
