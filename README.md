# Балуюсь с Ansible

## Полезные команды

1. Получаем публичный ключ подключения по ssh

```text
ssh-keygen -t rsa
```

2. Устанавливаем ключ для подлючения без пароля

```text
ssh-copy-id {{user}}@{{host}}
```

3. Получить Факты

```text
ansible all -m setup -i inventory.ini 
```

4. Запуск плейбука

```text
ansible-playbook playbook.yaml -i inventory.ini
```

5. Проверка плейбука на правильность

```text
ansible-lint playbook.yaml
```


6. Создание роли для ansible

```text
ansible-galaxy init play_with_docker
```

7. dns 
```
#где искать куда обращаться 
/etc/resolv.conf

#формат конфигурации
/etc/netplan/50-cloud-init.yaml

#что бы применить изменения
sudo netplan try
```
 
8. network
```
# разрешить вход под root
# PermitRootLogin yes
sudo vi /etc/ssh/sshd_config 
service ssh restart

# Удалить ключ 2.
vim ~/.ssh/authorized_keys
```