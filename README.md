# kubectl-plugins

![plugin count](https://aegisbadges.appspot.com/static?subject=plugin%20count&status=0&color=318FE0)
[![license](https://aegisbadges.appspot.com/static?subject=license&status=Apache-2.0&color=318FE0)](./LICENSE.md)

This repository is a custom plugin index for [Krew (kubectl plugin manager)](https://krew.sigs.k8s.io/), which contains all the kubectl plugins that I've developed.

## Usage

Configure this custom plugin index on your Krew plugin manager

```shell
$ kubectl krew index add tohjustin https://github.com/tohjustin/kubectl-plugins.git
$ kubectl krew index list
INDEX      URL
default    https://github.com/kubernetes-sigs/krew-index.git
tohjustin  https://github.com/tohjustin/kubectl-plugins.git
```

To install plugins from this index

```shell
$ kubectl krew install tohjustin/$PLUGIN_NAME
```

To remove plugins installed from this index, you don't need to specify its index

```shell
$ kubectl krew uninstall $PLUGIN_NAME
```

To remove custom plugin index

```shell
$ kubectl krew index remove tohjustin
```
