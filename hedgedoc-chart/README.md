# hedgedoc-chart

A lightweight yet comprehensive helm chart for [HedgeDoc](https://hedgedoc.org/),

Linted with [`kube-score`](https://github.com/zegl/kube-score),
[`kube-linter`](https://github.com/stackrox/kube-linter)
and [`yamllint`](https://github.com/stackrox/kube-linter).

Tested with [`helm-unittest`](https://github.com/helm-unittest/helm-unittest).

## Getting Started

Please read the charts [`README.md`](./charts/hedgedoc/README.md) to get started.

## Contributing

Please check the [`CONTRIBUTING.md`](./CONTRIBUTING.md) to learn how to contribute to `hedgedoc`

## Development

### Installing dependencies

You can install all required dependencies via `Task` and `Homebrew`

```shell
brew install go-task
task install
```

If you'd like to use other tools,
you can find all dependencies and relevant commands in the [`taskfile.yaml`](./taskfile.yaml)

### Rendering the Helm Chart

```shell
task render
```

### Running linters

```shell
task lint
```

### Generate documentation

```shell
task docs
```
