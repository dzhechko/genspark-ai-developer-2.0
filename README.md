# Genspark AI Developer 2.0 - Руководство

## Описание проекта

Современный интерактивный веб-сайт с обучением по работе с Genspark AI Developer 2.0 для создания мобильных Android-приложений.

## Особенности

- 📱 **Mobile-friendly** - адаптивный дизайн для всех устройств
- 🎨 **Современный UI** - красивый интерфейс с Tailwind CSS
- 📊 **Отслеживание прогресса** - интерактивная система прогресса обучения
- 🔄 **Интерактивность** - раскрывающиеся секции с подробной информацией
- 💾 **Сохранение прогресса** - автоматическое сохранение в localStorage
- 🌐 **SEO-оптимизация** - мета-теги для поисковых систем

## Содержание

1. Настройка основ приложения
2. Настройка хранилища данных (Hive/Firebase)
3. Настройка Firebase (опционально)
4. Описание приложения через AI
5. Предварительный просмотр и улучшения
6. Сборка APK/AAB
7. Сохранение и публикация

## Технологический стек

- **Framework**: Hono (Cloudflare Workers)
- **Frontend**: HTML, Tailwind CSS, Vanilla JavaScript
- **Deployment**: Cloudflare Pages / GitHub Pages
- **Icons**: Font Awesome

## Установка и запуск

### Локальная разработка

\`\`\`bash
# Установка зависимостей
npm install

# Сборка проекта
npm run build

# Запуск в режиме разработки (sandbox)
pm2 start ecosystem.config.cjs

# Проверка
curl http://localhost:3000
\`\`\`

### Деплой на Cloudflare Pages

\`\`\`bash
# Сборка и деплой
npm run deploy:cloudflare
\`\`\`

### Деплой на GitHub Pages

#### Простой способ (рекомендуется)

Используйте готовый файл `index.html`:

1. Создайте репозиторий на GitHub
2. Загрузите файл `index.html` через веб-интерфейс
3. Settings → Pages → Source: main branch, / (root)
4. Ваш сайт: `https://username.github.io/repo-name/`

#### Полный деплой проекта

\`\`\`bash
# Если настроен setup_github_environment
git remote add origin https://github.com/username/repo.git
git branch -M main
git push -u origin main
\`\`\`

**📘 Подробные инструкции: [DEPLOYMENT.md](DEPLOYMENT.md)**

## Структура проекта

\`\`\`
webapp/
├── index.html             # 🌟 Готовый HTML для GitHub Pages
├── src/
│   ├── index.tsx          # Главный файл приложения Hono
│   └── renderer.tsx       # Renderer
├── dist/                  # Скомпилированные файлы (после build)
├── public/                # Статические файлы
├── ecosystem.config.cjs   # PM2 конфигурация
├── package.json           # Зависимости и скрипты
├── vite.config.ts         # Конфигурация Vite
├── wrangler.jsonc         # Конфигурация Cloudflare
├── README.md              # Это файл
└── DEPLOYMENT.md          # 📘 Подробная инструкция по деплою
\`\`\`

## Автор

**Дмитрий Жечков**
- Telegram: [@llm_notes](https://t.me/llm_notes)

## Лицензия

MIT License

## Дата создания

Декабрь 2024
