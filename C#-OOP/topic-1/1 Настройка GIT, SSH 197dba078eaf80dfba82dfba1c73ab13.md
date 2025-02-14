# 1. Настройка GIT, SSH

Status: On Hold
Date: February 11, 2025

## `Pomodoro Timer`

---

[https://flocus.com/minimalist-pomodoro-timer/](https://flocus.com/minimalist-pomodoro-timer/)

## `Objectives`

---

<aside>
<img src="https://www.notion.so/icons/light-bulb_gray.svg" alt="https://www.notion.so/icons/light-bulb_gray.svg" width="40px" /> Обратить внимание!

</aside>

- [ ]  Установка GIT
    - [ ]  https://github.com/Hexlet/ru-instructions/blob/main/git.md
- [ ]  Установка SSH ключей
    - [ ]  https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
- [ ]  Интеграция SSH ключе в GitHub
    - [ ]  https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
- [ ]  Что такое протакол SSH
    - [ ]  https://ru.hexlet.io/blog/posts/ssh

---

## `Learning Materials`

---

**Первоначальная настройка GIT**

- Установка `name` и `email`, которе подставляются в итсорию изменений проекта
    
    ```bash
    # Выполняется из любой директории
    git config --global user.name "<имя фамилия>"
    git config --global user.email "<ваш емейл>"
    ```
    

**Защищённый протокол SSH для создания ключей**

После создания аккаунта нужно выполнить еще одну важную операцию — добавления [ssh-ключей](https://guides.hexlet.io/ru/ssh/) на github.com.

Ключи позволяют работать репозиториям с GitHub без необходимости постоянно вводить логин и пароль при синхронизации локального и удаленного репозитория (находящегося на GitHub).

- Создание SSH ключей
    
    ```bash
    # Создание ssh-ключей
    ssh-keygen -t ed25519  -C "your_email@example.com"
    # Дальше будет несколько вопросов. На все вопросы нужно нажимать Enter.
    
    # Запуск агента ssh, который следит за ключами
    eval "$(ssh-agent -s)"
    
    # Добавления нового ssh-ключа в агент
    ssh-add ~/.ssh/id_ed25519
    ```
    
    > **Your identification has been saved in** /Users/cancer/.ssh/id_ed25519
    **Your public key has been saved in** /Users/cancer/.ssh/id_ed25519.pub
    **The key fingerprint is:**
    SHA256:pPaa4y9zv6wc6+1SJ6HwYwyFpWhp2bD8gdhTeNsgd4o [throatcancer@yandex.ru](mailto:throatcancer@yandex.ru)
    > 
- Сам ключ
    
    AAAAC3NzaC1lZDI1NTE5AAAAIDr9SR0eYV6MOY3P0ywaixJRP35rTdzbKiU8BBpoU8nw
    
- Вывести содержимое ключа
    
    ```bash
    cat ~/.ssh/id_ed25519.pub
    ```
    
- Проверить подключение к GitHub
    
    ```bash
    ssh -T git@github.com
    "Hi tirion! You've successfully authenticated, but GitHub does not provide shell access."
    ```
    

## `Work Desk`

---

---

---

---