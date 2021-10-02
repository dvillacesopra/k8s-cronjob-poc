# README

## REQUIREMENTS

- A Kubernetes cluster
- `kubectl` command line tool installed
- Helm installed

## PROCESSES

Inside of the directory with all the content of this project:

### INSTALL

```shell
> helm install --debug cronjobpoc .
```

Before continue, wait one minute (or one and a half) until the installation process finish the internal initialization task, so you can execute following command on a new shell process:

```shell
> kubectl port-forward -n cronjobpoc service/hazelcast-mng 8081:8080
```

If no error is printed, you can visit the Hazelcast Management Center by opening the browser and visit the link <http://localhost:8081>

Specifically, you can visit the SQL Browser feature (<http://localhost:8081/clusters/dev/sql-browser>) to query for the entries each time a job finish successfully.

### UNINSTALL

```shell
> helm uninstall --debug cronjobpoc
```

## DEPLOY ON OKTETO

[![Develop on Okteto](https://okteto.com/develop-okteto.svg)](https://cloud.okteto.com/#/deploy?repository=https://github.com/dvillacesopra/k8s-cronjob-poc&branch=master)

## Reference links

- <https://kubernetes.io/docs/tasks/tools/>
- <https://kubernetes.io/docs/reference/kubectl/overview/>
- <https://kubernetes.io/docs/concepts/configuration/configmap/>
- <https://kubernetes.io/docs/concepts/workloads/controllers/deployment/>
- <https://kubernetes.io/docs/concepts/services-networking/service/>
- <https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/>
- <https://github.com/hazelcast/management-center-docker>
- <https://github.com/hazelcast/management-center-docker#start-with-a-preconfigured-cluster>
- <https://helm.sh/>
