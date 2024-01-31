# Attestation
# GitHub API Testing with Postman

## Описание проекта

Проект для тестирования GitHub API с использованием Postman. Включает коллекцию запросов для создания, изменения и удаления задач (issues) в репозитории.

## Инструкции по установке

1. Создайте аккаунт на GitHub, если его у вас еще нет.
2. Создайте репозиторий с произвольным содержимым.
3. Получите API-ключ на GitHub для использования в Postman.

## Инструкции по использованию коллекции

1. Импортируйте коллекцию Postman из файла `Attestation.postman_collection.json`.
2. При необходимости настройте переменные окружения: `github_owner`, `github_repo`, и `github_api_key`.
3. Запустите запросы для создания, изменения и удаления задач.

## Примеры запросов

### Создание Issue

- **Метод:** POST
- **URL:** `https://api.github.com/repos/OWNER/REPO/issues`
- **Тело запроса:**
  ```json
  {
    "title": "Issue 1",
    "body": "Something went wrong.",
    "labels": ["bug"],
    "assignees": ["ваш_логин_на_GitHub"]
  }
### Получение списка Issue
- **Метод:** GET
- **URL:** `https://api.github.com/repos/OWNER/REPO/issues`

### Изменение Issue
- **Метод:** PATCH
- **URL:** `https://api.github.com/repos/OWNER/REPO/issues/ISSUE_NUMBER`
- **Тело запроса:**
  ```json
  {
    "title": "Issue 2"
  }
### Удаление Issue 2 (задача будет заблокирована) 
- **Метод:** PUT
- **URL:** ` https://api.github.com/repos/OWNER/REPO/issues/ISSUE_NUMBER/lock`
