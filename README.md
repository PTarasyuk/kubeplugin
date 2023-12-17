# kubeplugin

`kubeplugin` is a kubectl plugin displays CPU/Memory usage for a resource type (Pod/Node) in a namespace.

## Installation

Ensure you have [krew](https://krew.sigs.k8s.io/docs/user-guide/setup/install/) installed.

```bash
kubectl krew install --manifest=https://raw.githubusercontent.com/PTarasyuk/kubeplugin/v0.0.1/kubeplugin.yaml
```

## Usage

```bash
kubectl kubeplugin [resource_type] [namespace]
```

Options:

- `-h`, `--help` -  Display help message
- `-v`, `--version` - Display version
- `[resource_type]` - Specify one of the following resource types:

  - `pods` - display CPU/memory usage of pods. Aliases: `pod`, `po`
  - `nodes` - display CPU/memory usage of nodes. Aliases: `node`, `no`

- `[namespace]` - Specify the namespace; optional parameter, by default `kube-system`

## Examples

```bash
# Display help
kubectl kubeplugin -h

# Get top output for pods in the default namespace `kube-system`
kubectl kubeplugin pod

# Get top output for nodes in a specific namespace
kubectl kubeplugin node mynamespace
```

## Uninstall

```bash
kubectl krew uninstall kubeplugin
```
