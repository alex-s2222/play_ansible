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
