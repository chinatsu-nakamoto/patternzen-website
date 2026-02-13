# PatternZen Website
## 法的文書公開用静的Webサイト

**作成日**: 2026年2月13日
**バージョン**: 1.0

---

## 📄 概要

このWebサイトは、PatternZenアプリのプライバシーポリシーと利用規約を公開するための静的サイトです。
Google Play / App Storeの申請時に必要な法的文書のURLを提供します。

---

## 🗂️ ファイル構成

```
website/
├── index.html                    # トップページ（英語）
├── index-ja.html                 # トップページ（日本語）
├── privacy-policy.html           # プライバシーポリシー（英語）
├── privacy-policy-ja.html        # プライバシーポリシー（日本語）
├── terms-of-service.html         # 利用規約（英語）
├── terms-of-service-ja.html      # 利用規約（日本語）
├── styles.css                    # 共通スタイルシート
└── README.md                     # このファイル
```

---

## 🌐 公開URL（予定）

### オプション1: GitHub Pages（推奨）
- **URL**: https://username.github.io/patternzen-website/
- **メリット**: 無料、簡単、SSL対応、自動デプロイ
- **デメリット**: カスタムドメインが必要な場合は設定が必要

### オプション2: Vercel
- **URL**: https://patternzen.vercel.app/
- **メリット**: 無料、高速、自動デプロイ、カスタムドメイン簡単
- **デメリット**: アカウント作成が必要

### オプション3: Netlify
- **URL**: https://patternzen.netlify.app/
- **メリット**: 無料、簡単、自動デプロイ
- **デメリット**: アカウント作成が必要

### オプション4: カスタムドメイン
- **URL**: https://www.patternzen.com/
- **メリット**: ブランド統一、プロフェッショナル
- **デメリット**: ドメイン購入・更新費用、設定が必要

---

## 🚀 デプロイ方法

### 方法1: GitHub Pages（推奨）

#### ステップ1: GitHubリポジトリ作成
```bash
# 新しいリポジトリを作成
git init
git add .
git commit -m "Initial commit: PatternZen website"

# GitHubリポジトリに接続（リポジトリ作成後）
git remote add origin https://github.com/username/patternzen-website.git
git branch -M main
git push -u origin main
```

#### ステップ2: GitHub Pages設定
1. GitHubリポジトリページを開く
2. **Settings** → **Pages** に移動
3. **Source** で `main` ブランチを選択
4. ルートディレクトリ `/` を選択
5. **Save** をクリック

#### ステップ3: 公開URL確認
- 5分程度で公開されます
- URL: `https://username.github.io/patternzen-website/`

#### ステップ4: カスタムドメイン設定（オプション）
1. ドメインのDNS設定で CNAMEレコードを追加
   ```
   www.patternzen.com → username.github.io
   ```
2. GitHub Pages設定で **Custom domain** に `www.patternzen.com` を入力
3. **Enforce HTTPS** を有効化

---

### 方法2: Vercel

#### ステップ1: Vercelアカウント作成
- https://vercel.com/ でアカウント作成（GitHubでサインイン推奨）

#### ステップ2: プロジェクトインポート
```bash
# Vercel CLIインストール（オプション）
npm install -g vercel

# デプロイ
vercel
```

または、Vercel Web UIから：
1. **New Project** をクリック
2. GitHubリポジトリを接続
3. プロジェクト設定確認
4. **Deploy** をクリック

#### ステップ3: カスタムドメイン設定
1. Vercel Project設定 → **Domains**
2. カスタムドメインを追加
3. DNS設定の指示に従う

---

### 方法3: Netlify

#### ステップ1: Netlifyアカウント作成
- https://www.netlify.com/ でアカウント作成

#### ステップ2: サイトデプロイ
**方法A: ドラッグ＆ドロップ**
1. Netlify ダッシュボードを開く
2. `website` フォルダをドラッグ＆ドロップ
3. 自動的にデプロイされます

**方法B: Git連携**
1. **New site from Git** をクリック
2. GitHubリポジトリを接続
3. ビルド設定（不要）
4. **Deploy site** をクリック

#### ステップ3: カスタムドメイン設定
1. Site settings → **Domain management**
2. **Add custom domain** をクリック
3. DNS設定の指示に従う

---

### 方法4: Firebase Hosting

#### ステップ1: Firebase CLI インストール
```bash
npm install -g firebase-tools
```

#### ステップ2: Firebase初期化
```bash
# ログイン
firebase login

# プロジェクトディレクトリで初期化
firebase init hosting

# 設定:
# - Public directory: . (カレントディレクトリ)
# - Single-page app: No
# - GitHub Actions: No
```

#### ステップ3: デプロイ
```bash
firebase deploy --only hosting
```

#### ステップ4: URL確認
- URL: `https://your-project-id.web.app/`

---

## ✅ デプロイ後の確認事項

### 1. URLアクセステスト
- [ ] トップページ（英語）が表示される
- [ ] トップページ（日本語）が表示される
- [ ] プライバシーポリシー（英語）が表示される
- [ ] プライバシーポリシー（日本語）が表示される
- [ ] 利用規約（英語）が表示される
- [ ] 利用規約（日本語）が表示される

### 2. ナビゲーションテスト
- [ ] ヘッダーリンクが正しく動作する
- [ ] フッターリンクが正しく動作する
- [ ] 言語切り替えが正しく動作する
- [ ] 「Back to top」ボタンが正しく動作する

### 3. レスポンシブテスト
- [ ] PC（1920x1080）で正しく表示される
- [ ] タブレット（768x1024）で正しく表示される
- [ ] スマートフォン（375x667）で正しく表示される

### 4. SSL/HTTPS確認
- [ ] HTTPSで接続できる
- [ ] SSL証明書が有効

---

## 📝 Google Play / App Store 申請時の記入URL

デプロイ完了後、以下のURLをアプリストアの申請フォームに記入してください：

### Google Play Console
- **プライバシーポリシーURL**: `https://your-domain.com/privacy-policy.html`
- **利用規約URL**: `https://your-domain.com/terms-of-service.html` （オプション）

### App Store Connect
- **Privacy Policy URL**: `https://your-domain.com/privacy-policy.html`
- **Terms of Use URL**: `https://your-domain.com/terms-of-service.html` （オプション）

---

## 🔧 カスタマイズ

### カラーパレット変更
`styles.css` の `:root` セクションを編集：

```css
:root {
  --primary-color: #2C3E50;      /* メインカラー */
  --secondary-color: #E8F0F2;    /* 背景カラー */
  --accent-color: #D4AF37;       /* アクセントカラー */
  --text-color: #1A1A1A;         /* テキストカラー */
  --background-color: #FFFFFF;   /* 背景カラー */
}
```

### メールアドレス変更
すべてのHTMLファイルで `chayk0vsk11@gmail.com` を検索して置換してください。

### ドメイン名変更
すべてのHTMLファイルでリンクを更新してください。

---

## 🛠️ 保守・更新

### プライバシーポリシー更新時
1. `privacy-policy.html` と `privacy-policy-ja.html` を編集
2. 「最終更新日」を更新
3. 変更内容をコミット＆プッシュ
4. 自動的にデプロイされます（GitHub Pages/Vercel/Netlify使用時）

### 利用規約更新時
1. `terms-of-service.html` と `terms-of-service-ja.html` を編集
2. 「最終更新日」を更新
3. 変更内容をコミット＆プッシュ
4. 自動的にデプロイされます

---

## 🐛 トラブルシューティング

### 問題: ページが表示されない
**原因**: デプロイが完了していない
**解決**: 5-10分待ってから再度アクセス

### 問題: CSSが適用されていない
**原因**: ファイルパスが間違っている
**解決**: `styles.css` のパスを確認（相対パス）

### 問題: リンクが404エラー
**原因**: ファイル名が間違っている
**解決**: ファイル名の大文字・小文字を確認

### 問題: HTTPSにならない
**原因**: SSL証明書が有効化されていない
**解決**: ホスティングサービスの設定で「Enforce HTTPS」を有効化

---

## 📞 サポート

質問や問題がある場合:
- **Email**: chayk0vsk11@gmail.com
- **対応時間**: 平日 10:00-18:00（日本時間）

---

## 📄 ライセンス

このWebサイトのコンテンツ（プライバシーポリシー、利用規約）は PatternZen に帰属します。

HTMLテンプレートとCSSは、自由に使用・改変できます。

---

## 🔗 関連リンク

- [Google Play Console](https://play.google.com/console/)
- [App Store Connect](https://appstoreconnect.apple.com/)
- [GitHub Pages ドキュメント](https://docs.github.com/pages)
- [Vercel ドキュメント](https://vercel.com/docs)
- [Netlify ドキュメント](https://docs.netlify.com/)

---

**作成日**: 2026年2月13日
**バージョン**: 1.0
**次回レビュー**: デプロイ後

---

© 2026 PatternZen. All rights reserved.
