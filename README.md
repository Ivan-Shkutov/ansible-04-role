## Домашнее задание к занятию 4 «Работа с roles»

### Подготовка к выполнению

1. Необязательно. Познакомьтесь с LightHouse.

2. Создайте два пустых публичных репозитория в любом своём проекте: vector-role и lighthouse-role.

![1](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/1.png)

![2](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/2.png)

5. Добавьте публичную часть своего ключа к своему профилю на GitHub.

### Основная часть

Ваша цель — разбить ваш playbook на отдельные roles.

Задача — сделать roles для ClickHouse, Vector и LightHouse и написать playbook для использования этих ролей.

Ожидаемый результат — существуют три ваших репозитория: два с roles и один с playbook.

Что нужно сделать

1. Создайте в старой версии playbook файл requirements.yml и заполните его содержимым:

```
---
  - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
    scm: git
    version: "1.13"
    name: clickhouse 
```

![3](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/5.png)

2. При помощи ansible-galaxy скачайте себе эту роль.

![4](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/02.png)

4. Создайте новый каталог с ролью при помощи ansible-galaxy role init vector-role.

![5](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/04.png)

6. На основе tasks из старого playbook заполните новую role. Разнесите переменные между vars и default.

7. Перенести нужные шаблоны конфигов в templates.

8. Опишите в README.md обе роли и их параметры. Пример качественной документации ansible role по ссылке.

9. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.

10. Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в requirements.yml в playbook.

11. Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения roles с tasks.

12. Выложите playbook в репозиторий.

![6](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/06.png)

![7](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/07.png)

![8](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/05.png)

![9](https://github.com/Ivan-Shkutov/ansible-04-role/blob/main/08.png)

13. В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.

---

### Решение:

[playbook](https://github.com/Ivan-Shkutov/ansible-04-role/tree/main/playbook)




---
