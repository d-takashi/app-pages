# app-pages

複数のiOSアプリについて、App Store Connectに設定する公開ページを1つのリポジトリで管理するための静的サイトです。

主な対象URLは以下です。

- Support URL
- Privacy Policy URL
- 必要に応じた Marketing URL
- 必要に応じた Terms URL

## 公開方針

GitHub Pagesで `docs/` を公開ディレクトリとして使う想定です。

想定URL:

- Site root: `https://d-takashi.github.io/app-pages/`
- Apps: `https://d-takashi.github.io/app-pages/apps/`

## ディレクトリ構成

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
    perfect-pomodoro/
      index.html
      support/
        index.html
      privacy/
        index.html
```

## 新しいアプリを追加するとき

1. `docs/apps/<app-slug>/` を作成する。
2. `index.html` を作成し、アプリ紹介またはMarketing URL用ページにする。
3. `support/index.html` を作成するか、App Store Connectに直接設定する問い合わせフォームURLを決める。
4. `privacy/index.html` を作成し、アプリの実装実態に合うPrivacy Policyを置く。
5. 必要なら `terms/index.html` を作成する。
6. `docs/apps/index.html` と `docs/index.html` から辿れるようにリンクを追加する。
7. App Store ConnectのURL欄を更新する。

## App Store Connect URL例

Log:

- Marketing URL: `https://d-takashi.github.io/app-pages/apps/log/`
- Privacy Policy URL: `https://d-takashi.github.io/app-pages/apps/log/privacy/`
- Terms URL: `https://d-takashi.github.io/app-pages/apps/log/terms/`
- Support URL: Logの問い合わせフォームURLを直接設定する想定

Perfect Pomodoro:

- Marketing URL: `https://d-takashi.github.io/app-pages/apps/perfect-pomodoro/`
- Privacy Policy URL: `https://d-takashi.github.io/app-pages/apps/perfect-pomodoro/privacy/`
- Support URL: `https://d-takashi.github.io/app-pages/apps/perfect-pomodoro/support/`

## 移植元

Logのlegalページは `rec-life` リポジトリの以下から移植しています。

- `/Users/takashi/Documents/all-i-need/10_repos/rec-life/docs/legal/privacy-policy.html`
- `/Users/takashi/Documents/all-i-need/10_repos/rec-life/docs/legal/terms.html`
- `/Users/takashi/Documents/all-i-need/10_repos/rec-life/docs/legal/legal.css`

移植時点では、元の `rec-life` 側のファイルは変更していません。

## TODO

- Logアプリ本体やfastlane metadata内に残っている旧URL `https://d-takashi.github.io/log-privacy-policy/` を、新URLへ切り替えるか判断する。
- 既存の `d-takashi/log-privacy-policy` リポジトリを残すか、リダイレクト・アーカイブするか判断する。
- Perfect Pomodoroの各ページ本文は、アプリ実装とApp Store申請内容に合わせて作成する。
- Perfect PomodoroのPrivacy Policyは、データ収集、端末内保存、カメラ・写真・通知などの利用実態を確認してから最終化する。
