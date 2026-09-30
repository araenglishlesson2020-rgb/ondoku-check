# 音読チェック（単語クエスト用・マイク判定ページ）

単語クエスト（Google Apps Script）の「🎤 音読チェック」から開かれる判定ページ。
GASの画面内ではマイクが使えないため、このページ（GitHub Pages）で音声認識を行い、
語単位の判定結果を postMessage とスプレッドシートPOSTで返す。

- 本文・生徒名・送信先URLは、URLハッシュ（base64url JSON）で受け取る（サーバーには何も保存しない）
- 元ファイルの管理場所：`単語クエスト_サーバー版(AppsScript)/音読チェック_判定ページ(GitHubPages)/index.html`
