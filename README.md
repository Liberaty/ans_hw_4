# Домашнее задание к занятию 4 «Работа с roles»

## Подготовка к выполнению

1. * Необязательно. Познакомьтесь с [LightHouse](https://youtu.be/ymlrNlaHzIY?t=929).
2. Создайте два пустых публичных репозитория в любом своём проекте: vector-role и lighthouse-role.
3. Добавьте публичную часть своего ключа к своему профилю на GitHub.

## Основная часть

Ваша цель — разбить ваш playbook на отдельные roles. 

Задача — сделать roles для ClickHouse, Vector и LightHouse и написать playbook для использования этих ролей. 

Ожидаемый результат — существуют три ваших репозитория: два с roles и один с playbook.

**Что нужно сделать**

1. Создайте в старой версии playbook файл `requirements.yml` и заполните его содержимым:

   ```yaml
   ---
     - src: git@github.com:AlexeySetevoi/ansible-clickhouse.git
       scm: git
       version: "1.13"
       name: clickhouse 
   ```

***Ответ:***

![4.1.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.1.png?raw=true)

2. При помощи `ansible-galaxy` скачайте себе эту роль.

***Ответ:***

![4.2.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.2.png?raw=true)

3. Создайте новый каталог с ролью при помощи `ansible-galaxy role init vector-role`.

***Ответ:***

![4.3.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.3.png?raw=true)

4. На основе tasks из старого playbook заполните новую role. Разнесите переменные между `vars` и `default`. 
5. Перенести нужные шаблоны конфигов в `templates`.
6. Опишите в `README.md` обе роли и их параметры. Пример качественной документации ansible role [по ссылке](https://github.com/cloudalchemy/ansible-prometheus).
7. Повторите шаги 3–6 для LightHouse. Помните, что одна роль должна настраивать один продукт.
8. Выложите все roles в репозитории. Проставьте теги, используя семантическую нумерацию. Добавьте roles в `requirements.yml` в playbook.

***Ответ:***

![4.8.1.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.8.1.png?raw=true)

![4.8.2.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.8.2.png?raw=true)

![4.8.3.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.8.3.png?raw=true)

9. Переработайте playbook на использование roles. Не забудьте про зависимости LightHouse и возможности совмещения `roles` с `tasks`.

***Ответ:***

![4.9.png](https://github.com/Liberaty/ans_hw_4/blob/main/img/4.9.png?raw=true)

10. Выложите playbook в репозиторий.
11. В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.

***Ответ:***

[Ссылка](https://github.com/Liberaty/lighthouse-role) на lighthouse

[Ссылка](https://github.com/Liberaty/vector-role) на vector

[Ссылка](https://github.com/Liberaty/ans_hw_4) на playbook

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.