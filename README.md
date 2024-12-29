# talos-k8s-iac

## TODO

- [ ] Set up OIDC Provider
- [ ] Secure Grafana Login
- [ ] Secure telegram token
- [ ] Make all services highly available (If possible)
- [ ] Move manifests next to the charts they belong to?
- [ ] Deploy default alerts for all charts (If possible)

## Machines and IPs

- `192.168.178.95`
- `192.168.178.90`
- `192.168.178.105`

## Talos Commands

```shell
talosctl gen config nailab https://192.168.178.105:6443
```

```shell
talosctl get disks --insecure --nodes <IP>
```

```shell
talosctl apply-config --insecure --nodes <IP> --file controlplane.yaml
```

```shell
talosctl apply-config --insecure --nodes <IP> --file worker.yaml
```

```shell
talosctl bootstrap --nodes <IP> --endpoints <IP> --talosconfig=./talosconfig
```

```shell
talosctl kubeconfig --nodes <IP> --endpoints <IP> --talosconfig=./talosconfig
```

```shell
talosctl dashboard --nodes 192.168.178.95 --endpoints 192.168.178.95 --talosconfig=./talosconfig
```

```shell
talosctl dashboard --nodes 192.168.178.95 --endpoints 192.168.178.95 --talosconfig=./talosconfig
```

```shell
talosctl services --nodes 192.168.178.95 --endpoints 192.168.178.95 --talosconfig=./talosconfig
```

```shell
talosctl apply-config --nodes 192.168.178.105 --endpoints 192.168.178.105 --file controlplane.yaml --talosconfig=./talosconfig
```

```shell
talosctl reboot --nodes 192.168.178.95 --endpoints 192.168.178.95 --talosconfig=./talosconfig
```

```shell
talosctl reset --nodes 192.168.178.95 --endpoints 192.168.178.95 --talosconfig=./talosconfig
```

```shell
talosctl -e 192.168.178.95 -n 192.168.178.95 patch mc -p @patch.yaml --talosconfig=./talosconfig
```

```shell
talosctl upgrade-k8s --nodes 192.168.178.105 --endpoints 192.168.178.105 --talosconfig=./talosconfig
```
