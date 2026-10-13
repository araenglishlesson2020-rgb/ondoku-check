# 音読チェック（単語クエスト用・マイク判定ページ）

単語クエスト（Google Apps Script）の「🎤 音読チェック」から開かれる判定ページ。
GASの画面内ではマイクが使えないため、このページ（GitHub Pages）で音声認識を行い、
語単位の判定結果を postMessage とスプレッドシートPOSTで返す。

- 本文・生徒名・送信先URLは、URLハッシュ（base64url JSON）で受け取る（サーバーには何も保存しない）
- 元ファイルの管理場所：`単語クエスト_サーバー版(AppsScript)/音読チェック_判定ページ(GitHubPages)/index.html`

## harapeko/（はらぺこ英語クエストの「新しい入口」・2026-10-13）

- `harapeko/index.html` ＝ アプリ本体の画面（Apps Script版 `Index.html` から生成）。URL: https://araenglishlesson2020-rgb.github.io/ondoku-check/harapeko/
- 目的：Apps Script 版で毎回出る「Google Apps Script のユーザーによって作成…」表示をなくす。データ（ログイン・記録・録音）は従来どおり Apps Script（doPost の `action:'rpc'`）→ スプレッドシート。
- **手で編集しない。** 画面を直す時は `単語クエスト_サーバー版(AppsScript)/Index.html` を直して
  `python3 _tools/新しい入口_GitHubPages版を生成.py` で作り直し → commit → push。
- ホーム画面追加用の自動ログインURLも同じ形：`…/harapeko/?k=合言葉`（または `?u=名前&k=合言葉`）
