# Ansible k3s install

Ansibleを使ってk3sをシングルノードセットアップするためのスクリプトです。
シングルノードであり、かつハンズオントレーニング用のものです。
特にセキュリティについては意図的に緩めているのでプロダクション運用は禁止です。


## 設定方法

複数台セットアップする場合、セットアップ対象ホストのFQDN、またはIPアドレスが異なる場合は、
`inventory/inventory.ini`を修正してください。

```ini
[k3s]
192.168.56.101
```

```console
$ ansible-playbook -i inventory/inventory.ini playbook/main.yml
```