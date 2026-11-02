# Polygraph Intake — intake.plgrph.com

Передтестове анкетування (PWA). Один самодостатній `index.html` (CSS/JS інлайн) + `sw.js` + `manifest.json`. Хостинг: GitHub Pages (Deploy from a branch → `main` / root), DNS: Cloudflare (`intake` → CNAME на `hypnoser.github.io`).

## Структура
- `index.html`, `sw.js`, `manifest.json`, `icons/` — застосунок
- `pr/` — презентація (https://intake.plgrph.com/pr/)
- `assets/fonts/` — self-hosted Manrope для презентації

## Правила
- Дані сесій лежать у вибраній користувачем теці (File System Access API); у браузері — лише handle теки (IndexedDB `intake_fs`), PIN і чернетка згоди (localStorage).
- Зміна origin скидає ці налаштування: теку обирають знову.
- Архіви старих версій (`backup/`) і джерела збірки (`js/`, `body.html`, `styles.css`) навмисно не публікуються; вони є в історії `hypnoser/plgrph`.
