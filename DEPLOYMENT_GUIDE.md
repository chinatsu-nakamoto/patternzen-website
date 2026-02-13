# PatternZen Website デプロイガイド
## GitHub Pages へのデプロイ手順

**作成日**: 2026年2月13日
**ステータス**: ✅ ローカルGit準備完了

---

## 📋 現在の状態

✅ **完了した作業**:
- Gitリポジトリの初期化
- 全ファイルのコミット完了（10ファイル、2291行）
- コミットID: `f1bb68c`

⏳ **次のステップ**:
- GitHubリポジトリの作成
- リモートリポジトリへのプッシュ
- GitHub Pagesの有効化

---

## 🚀 デプロイ手順（全5ステップ）

### ステップ1: GitHubリポジトリを作成

#### 方法A: GitHub Web UIで作成（推奨）

1. **GitHubにログイン**
   - https://github.com にアクセス
   - ログインしていない場合はログイン

2. **新しいリポジトリを作成**
   - 右上の「+」アイコン → 「New repository」をクリック

3. **リポジトリ設定**
   ```
   Repository name: patternzen-website
   Description: PatternZen Legal Documents Website (Privacy Policy & Terms of Service)
   Visibility: Public ✅ (GitHub Pagesに必要)

   ⚠️ 以下はチェックを入れない:
   [ ] Add a README file
   [ ] Add .gitignore
   [ ] Choose a license
   ```

4. **「Create repository」をクリック**

---

### ステップ2: リモートリポジトリに接続

GitHubリポジトリ作成後、表示される画面に従ってコマンドを実行します：

```bash
cd C:\projects\japanesepatterns\website

# リモートリポジトリを追加（GitHubのユーザー名を置き換えてください）
git remote add origin https://github.com/YOUR_USERNAME/patternzen-website.git

# ブランチ名をmainに変更
git branch -M main

# GitHubにプッシュ
git push -u origin main
```

**注意**: `YOUR_USERNAME` を実際のGitHubユーザー名に置き換えてください。

#### 認証について

初回プッシュ時、GitHubの認証が求められます：

**方法1: Personal Access Token（推奨）**
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. 「Generate new token (classic)」をクリック
3. Note: `PatternZen Website`
4. Expiration: 90 days（または任意）
5. Scopes: `repo` にチェック
6. 「Generate token」をクリック
7. トークンをコピー（二度と表示されません）
8. プッシュ時のパスワード欄にトークンを貼り付け

**方法2: GitHub CLI**
```bash
# GitHub CLIをインストール済みの場合
gh auth login
```

---

### ステップ3: GitHub Pagesを有効化

1. **GitHubリポジトリページを開く**
   - https://github.com/YOUR_USERNAME/patternzen-website

2. **Settingsタブをクリック**

3. **左サイドバーの「Pages」をクリック**

4. **Source設定**
   - Branch: `main` を選択
   - Folder: `/ (root)` を選択
   - 「Save」をクリック

5. **デプロイ待機**
   - 通常1-5分で完了
   - ページ上部に緑色のチェックマークが表示されます

6. **公開URLを確認**
   - 表示される URL:
   ```
   https://YOUR_USERNAME.github.io/patternzen-website/
   ```

---

### ステップ4: デプロイ確認

#### 4.1 アクセステスト

以下のURLにアクセスして、すべてのページが正しく表示されることを確認：

```
✅ トップページ（英語）
https://YOUR_USERNAME.github.io/patternzen-website/

✅ トップページ（日本語）
https://YOUR_USERNAME.github.io/patternzen-website/index-ja.html

✅ プライバシーポリシー（英語）
https://YOUR_USERNAME.github.io/patternzen-website/privacy-policy.html

✅ プライバシーポリシー（日本語）
https://YOUR_USERNAME.github.io/patternzen-website/privacy-policy-ja.html

✅ 利用規約（英語）
https://YOUR_USERNAME.github.io/patternzen-website/terms-of-service.html

✅ 利用規約（日本語）
https://YOUR_USERNAME.github.io/patternzen-website/terms-of-service-ja.html
```

#### 4.2 機能テスト

- [ ] ヘッダーのナビゲーションリンクが動作する
- [ ] フッターのリンクが動作する
- [ ] 言語切り替え（EN ↔ 日本語）が動作する
- [ ] Back to Topボタンが動作する
- [ ] 外部リンク（NDL等）が新しいタブで開く
- [ ] CSSスタイルが正しく適用されている

#### 4.3 レスポンシブテスト

ブラウザの開発者ツール（F12）でデバイスモードを開き、以下を確認：

- [ ] デスクトップ（1920x1080）
- [ ] タブレット（768x1024）
- [ ] スマートフォン（375x667）

#### 4.4 HTTPS確認

- [ ] URLが `https://` で始まっている
- [ ] ブラウザのアドレスバーに鍵アイコンが表示されている

---

### ステップ5: Google Play / App Store に記入

デプロイ確認が完了したら、以下のURLをストア申請フォームに記入します：

#### Google Play Console

1. **Play Console** → **アプリ** → **PatternZen** → **ストアの設定**
2. **プライバシーポリシー** セクション:
   ```
   https://YOUR_USERNAME.github.io/patternzen-website/privacy-policy.html
   ```

#### App Store Connect（iOS版リリース時）

1. **App Store Connect** → **マイApp** → **PatternZen** → **App情報**
2. **プライバシーポリシーURL**:
   ```
   https://YOUR_USERNAME.github.io/patternzen-website/privacy-policy.html
   ```
3. **利用規約URL**（オプション）:
   ```
   https://YOUR_USERNAME.github.io/patternzen-website/terms-of-service.html
   ```

---

## 🔄 更新手順（将来の変更時）

### プライバシーポリシーまたは利用規約を更新する場合

1. **ファイルを編集**
   ```bash
   cd C:\projects\japanesepatterns\website
   # エディタでファイルを編集
   ```

2. **変更をコミット**
   ```bash
   git add .
   git commit -m "Update privacy policy - [変更内容]"
   ```

3. **GitHubにプッシュ**
   ```bash
   git push origin main
   ```

4. **自動デプロイ**
   - GitHub Actionsが自動的にデプロイします
   - 1-3分で反映されます

5. **確認**
   - 公開URLで変更が反映されていることを確認

---

## 🎨 カスタムドメイン設定（オプション）

独自ドメイン（例: www.patternzen.com）を使用する場合：

### ステップ1: ドメインのDNS設定

ドメインレジストラ（お名前.com、Cloudflare等）で以下を設定：

**Aレコード**:
```
Type: A
Name: @
Value: 185.199.108.153
       185.199.109.153
       185.199.110.153
       185.199.111.153
TTL: 3600
```

**CNAMEレコード**:
```
Type: CNAME
Name: www
Value: YOUR_USERNAME.github.io
TTL: 3600
```

### ステップ2: GitHub Pages設定

1. GitHub リポジトリ → Settings → Pages
2. **Custom domain** に `www.patternzen.com` を入力
3. 「Save」をクリック
4. **Enforce HTTPS** にチェック（DNS設定後24時間以内に有効化）

### ステップ3: 確認

```bash
# DNS設定の伝播を確認（10分-24時間かかる場合があります）
nslookup www.patternzen.com
```

---

## 🐛 トラブルシューティング

### 問題1: ページが404エラー

**原因**: デプロイがまだ完了していない
**解決**:
- 5-10分待ってから再度アクセス
- GitHub リポジトリ → Actions タブでデプロイ状況を確認

### 問題2: CSSが適用されていない

**原因**: ファイルパスが間違っている
**解決**:
- HTMLファイルで `styles.css` が正しくリンクされているか確認
- ブラウザの開発者ツール（F12）→ Network タブで404エラーを確認

### 問題3: リンクが404エラー

**原因**: ファイル名の大文字・小文字が間違っている
**解決**:
- GitHubは大文字・小文字を区別します
- リンクとファイル名が完全に一致しているか確認

### 問題4: git pushで認証エラー

**原因**: Personal Access Tokenが無効または期限切れ
**解決**:
- 新しいTokenを生成（上記「ステップ2」参照）
- または GitHub CLI を使用

### 問題5: カスタムドメインが反映されない

**原因**: DNS設定の伝播に時間がかかっている
**解決**:
- 最大24-48時間待つ
- `nslookup` コマンドで確認
- DNS設定が正しいか再確認

---

## 📊 デプロイ状況の確認

### GitHub Actions

1. GitHubリポジトリ → **Actions** タブ
2. 最新のワークフロー実行を確認
3. 緑色のチェックマーク = 成功
4. 赤色のバツマーク = 失敗（ログを確認）

### ビルドログ確認

1. Actions → 失敗したワークフローをクリック
2. エラーメッセージを確認
3. 該当箇所を修正してプッシュ

---

## ✅ デプロイ完了チェックリスト

### 初回デプロイ
- [ ] GitHubリポジトリ作成完了
- [ ] ローカルからプッシュ完了
- [ ] GitHub Pages有効化完了
- [ ] 公開URL確認完了
- [ ] 全ページアクセス確認
- [ ] 全リンク動作確認
- [ ] レスポンシブデザイン確認
- [ ] HTTPS接続確認

### ストア申請準備
- [ ] プライバシーポリシーURL記録
- [ ] 利用規約URL記録
- [ ] Google Play Consoleに入力済み
- [ ] App Store Connectに入力済み（iOS版時）

---

## 📞 サポート

デプロイに関する質問や問題がある場合:
- **Email**: chayk0vsk11@gmail.com
- **GitHub Issues**: リポジトリのIssuesタブ

---

## 🔗 関連リンク

- [GitHub Pages ドキュメント](https://docs.github.com/pages)
- [カスタムドメイン設定](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site)
- [GitHub Actions](https://docs.github.com/actions)

---

**作成日**: 2026年2月13日
**バージョン**: 1.0
**ステータス**: ✅ ローカルGit準備完了 → ⏳ GitHub作成待ち

---

© 2026 PatternZen. All rights reserved.
