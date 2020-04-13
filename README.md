# Ansible k3s install

Ansibleを使ってk3sをシングルノードセットアップするためのスクリプトです。
シングルノードであり、かつハンズオントレーニング用のものです。
特にセキュリティについては意図的に緩めているのでプロダクション運用は禁止です。


## 設定方法

### セットアップ対象ホストの指定

複数台セットアップする場合、セットアップ対象ホストのFQDN、またはIPアドレスが異なる場合は、
`inventory/inventory.ini`を修正してください。

```ini
[k3s]
192.168.56.101
```

### 実行方法

```console
$ ansible-playbook -i inventory/inventory.ini playbook/main.yml
```

## 注意点

amd64のみの対応であり、armなどには対応していないので注意してください。