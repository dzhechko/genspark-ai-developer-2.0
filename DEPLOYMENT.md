# Инструкция по развертыванию на GitHub Pages

## Вариант 1: Развертывание через интерфейс GitHub

### Шаг 1: Создайте репозиторий на GitHub

1. Войдите на [GitHub.com](https://github.com)
2. Нажмите "New repository"
3. Введите имя репозитория (например, `genspark-ai-guide`)
4. Выберите "Public"
5. **НЕ** добавляйте README, .gitignore или license (они уже есть в проекте)
6. Нажмите "Create repository"

### Шаг 2: Загрузите файлы

#### Вариант 2.1: Через командную строку (если настроен setup_github_environment)

```bash
cd /home/user/webapp
git remote add origin https://github.com/ВАШ_USERNAME/genspark-ai-guide.git
git branch -M main
git push -u origin main
```

#### Вариант 2.2: Через веб-интерфейс GitHub

1. Скачайте все файлы из проекта (используйте вкладку Scripts → Backup)
2. Распакуйте архив на вашем компьютере
3. На странице репозитория нажмите "uploading an existing file"
4. Перетащите все файлы из папки webapp
5. Нажмите "Commit changes"

### Шаг 3: Настройте GitHub Pages

1. Перейдите в Settings репозитория
2. Выберите раздел "Pages" в левом меню
3. В разделе "Build and deployment":
   - Source: выберите "Deploy from a branch"
   - Branch: выберите `main` и папку `/ (root)`
   - Нажмите "Save"

4. Подождите 1-2 минуты
5. Обновите страницу - появится ссылка на ваш сайт
6. Ваш сайт будет доступен по адресу: `https://ВАШ_USERNAME.github.io/genspark-ai-guide/`

## Вариант 2: Статический HTML для GitHub Pages

Если первый вариант не работает, можно использовать чистый HTML без Hono:

### Шаг 1: Создайте index.html

Вместо использования Hono, создайте один HTML файл с встроенным содержимым.

### Шаг 2: Загрузите на GitHub

1. Создайте новый репозиторий
2. Загрузите только файл `index.html`
3. Настройте GitHub Pages как в Варианте 1

## Вариант 3: Использование Cloudflare Pages (рекомендуется)

Если вы предпочитаете Cloudflare Pages:

```bash
# 1. Настройте Cloudflare API ключ
# Вызовите setup_cloudflare_api_key в интерфейсе

# 2. Соберите проект
npm run build

# 3. Разверните на Cloudflare
npm run deploy:cloudflare
```

Ваш сайт будет доступен по адресу: `https://genspark-ai-guide.pages.dev`

## Текущий статус

✅ **Локальная версия работает**: https://3000-ikqvxi55q9mxr8kfnjgux-2e1b9533.sandbox.novita.ai

📦 **Проект готов к развертыванию**

Выберите один из вариантов выше для публикации вашего сайта!

## Решение проблем

### GitHub Pages не работает

- Убедитесь, что репозиторий Public
- Проверьте, что выбрана правильная ветка (main)
- Подождите несколько минут после настройки
- Проверьте вкладку Actions - там не должно быть ошибок

### Cloudflare Pages не работает

- Убедитесь, что настроен API ключ через setup_cloudflare_api_key
- Проверьте, что проект собран: `npm run build`
- Посмотрите логи развертывания

## Автор

**Дмитрий Жечков** - [@llm_notes](https://t.me/llm_notes)
