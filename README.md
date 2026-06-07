# Windows OS教養講座

業務システム開発・運用に関わるソフトウェアエンジニア向けの、Windows OS学習教材サイトです。

Windowsを一般ユーザー向けの操作対象としてではなく、企業システム、業務アプリ、認証、権限、ネットワーク、ログ、セキュリティ、更新管理、運用自動化を支える基盤として理解することを目的にしています。

## ファイル構成

```text
windows-os-literacy/
├─ index.html
├─ chapters/
│  ├─ chapter-01.html
│  ├─ chapter-02.html
│  ├─ chapter-03.html
│  ├─ chapter-04.html
│  ├─ chapter-05.html
│  ├─ chapter-06.html
│  ├─ chapter-07.html
│  ├─ chapter-08.html
│  ├─ chapter-09.html
│  ├─ chapter-10.html
│  ├─ chapter-11.html
│  ├─ chapter-12.html
│  ├─ chapter-13.html
│  ├─ chapter-14.html
│  ├─ chapter-15.html
│  ├─ chapter-16.html
│  ├─ chapter-17.html
│  ├─ chapter-18.html
│  ├─ chapter-19.html
│  └─ chapter-20.html
├─ assets/
│  └─ style.css
└─ README.md
```

## ローカルでの開き方

静的HTMLとして作成しているため、Webサーバーは不要です。

1. `index.html` をブラウザで開きます。
2. 目次から各章へ移動します。
3. 印刷する場合は、ブラウザの印刷機能を使います。

macOSやLinuxのターミナルから開く例です。

```bash
open index.html
```

Windowsのエクスプローラーでは、`index.html` をダブルクリックして開けます。

## GitHub Pagesで公開する方法

この教材は静的HTMLだけで構成しているため、GitHub Pagesでは `main` ブランチのルートを公開元にできます。

基本方針は次の通りです。

- リポジトリ名は `windows-os-literacy` を想定します。
- 公開元は `main` ブランチの `/` です。
- `index.html` がサイトの入口になります。
- 外部CDNやビルド処理は不要です。

GitHub側でPagesを有効化する場合は、リポジトリの `Settings` から `Pages` を開き、`Build and deployment` の公開元として `Deploy from a branch`、ブランチとして `main`、フォルダとして `/root` を選びます。

公開後のURLは、通常は次の形式になります。

```text
https://<GitHubユーザー名>.github.io/windows-os-literacy/
```

## iPhoneから内容を更新する運用

iPhoneのChatGPTアプリからこのプロジェクトの内容を更新したい場合は、次の流れを想定します。

1. ChatGPTに章の追加や修正を依頼します。
2. Codexがローカルファイルを編集します。
3. 変更内容を確認します。
4. CodexがGitにコミットします。
5. CodexがGitHubへpushします。
6. GitHub Pagesに反映されたURLをiPhoneのブラウザで開きます。

GitHub Pagesの反映には少し時間がかかる場合があります。
更新後すぐに古い内容が表示される場合は、ブラウザの再読み込みやキャッシュの影響も確認します。

## 章を追加・修正する方法

各章は `chapters/chapter-XX.html` の形式で管理します。

- 章番号は2桁に統一します。
- 共通CSSは `assets/style.css` に追加します。
- 各章固有のCSSは原則として追加しません。
- 章ページでは `../assets/style.css` を読み込みます。
- 目次ページでは `assets/style.css` を読み込みます。
- 章間リンクは、前章、目次、次章の3方向を確認します。

章本文を追加する場合は、次の構成を基本にします。

1. ヒーローセクション
2. この章の目的
3. 目次
4. 本文
5. 図解
6. 実務での観点
7. コマンド例
8. 章のまとめ
9. 理解度チェック
10. 次章への接続

## 注意事項

- 外部CDNや外部ライブラリは使っていません。
- 画像ファイルは使わず、HTML/CSSだけで図解しています。
- Windowsの機能や管理方法は、環境、エディション、バージョン、組織ポリシーにより異なる場合があります。
- セキュリティ、認証、証明書、更新管理に関する説明は、安全な企業運用を前提にしています。
- 第2章から第6章は本文を作成済みです。第7章から第20章は、章間リンクと目次確認用の準備ページとして配置しています。
