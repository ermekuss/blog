Toktarov Notes (Jekyll + GitHub Pages)

Публикация:
1) Загрузите содержимое папки в репозиторий:
   - Личный сайт: USERNAME.github.io
   - Проектный сайт: любой репозиторий (URL будет /REPO/)

2) GitHub Pages:
   Settings → Pages → Deploy from a branch → Branch: main → /(root)

Как пополнять контент:
- Посты добавляйте в папку _posts/ (формат: YYYY-MM-DD-title.md)
- Для разделов используйте categories: [pikir] / [monocast] / [maqala] / [kerek]
- Резюме редактируйте в cv.md
- Ссылки редактируйте в kerek.md
- Соцсети укажите в _config.yml (social.facebook / social.x / social.linkedin)

Локальный запуск (опционально):
bundle install
bundle exec jekyll serve
