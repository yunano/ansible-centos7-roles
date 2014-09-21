ansible-centos7-roles
=====================

CentOS 7用のAnsible role集。
今のところssh-key, ssh-copy-id, chrony, cobblerを収録している。

## 使い方

```
# yum install epel-release
# yum install ansible
# git clone https://github.com/yunano/ansible-centos7-roles/
# cd ansible-centos7-roles/
# mv example ../<適当な名前>
# cd ../<さっきの適当な名前>
# (環境に合わせて適当にファイルをいじる)
# vi /etc/hosts # インベントリファイルに載せるホスト名を解決できるように
# ansible-vault encrypt vars/credentials.yml # 望むなら
# ansible-playbook -i hosts-env1 site.yml # ansible-vaultを使っているなら--ask-vault-passも付ける
```

インベントリファイル名をhosts-{何とか}にしておくとgroup_varsの{何とか}.ymlを読むようにしている。
exampleだとインベントリファイル名がhosts-env1、group_varsにはenv1.yml。

## Licensing

MIT
