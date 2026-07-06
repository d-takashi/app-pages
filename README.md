# app-pages

複数のiOSアプリについて、App Store Connectに設定する公開ページを1つのリポジトリで管理するための静的サイトです。

主な対象URLは以下です。

- Support URL
- Privacy Policy URL
- 必要に応じた Marketing URL
- 必要に応じた Terms URL

## Hosting

This site is published with GitHub Pages.

Public URLs:

- Site root: `https://d-takashi.github.io/app-pages/`
- Apps: `https://d-takashi.github.io/app-pages/apps/`
- 就活ES通過くん: `https://d-takashi.github.io/app-pages/apps/es-tsuka-kun/`
- 就活ES通過くん 利用規約: `https://d-takashi.github.io/app-pages/apps/es-tsuka-kun/terms/`
- 就活ES通過くん プライバシーポリシー: `https://d-takashi.github.io/app-pages/apps/es-tsuka-kun/privacy/`
- 就活ES通過くん 特定商取引法に基づく表記: `https://d-takashi.github.io/app-pages/apps/es-tsuka-kun/commercial-transaction/`

## Structure

```text
docs/
  index.html
  styles.css
  apps/
    index.html
    log/
      index.html
      support/
        index.html
      privacy/
        index.html
        legal.css
      terms/
        index.html
        legal.css
```

## Adding An App

1. Create `docs/apps/<app-slug>/`.
2. Add `index.html` for the app overview or Marketing URL.
3. Add `support/index.html` or use a direct support/contact URL in App Store Connect.
4. Add `privacy/index.html` with the app's Privacy Policy.
5. Add `terms/index.html` when Terms of Use are needed.
6. Link the app from `docs/apps/index.html`.
7. Update the relevant URLs in App Store Connect.

## App Store Connect URL Examples

Log:

- Marketing URL: `https://d-takashi.github.io/app-pages/apps/log/`
- Privacy Policy URL: `https://d-takashi.github.io/app-pages/apps/log/privacy/`
- Terms URL: `https://d-takashi.github.io/app-pages/apps/log/terms/`
- Support URL: Logの問い合わせフォームURLを直接設定する想定
