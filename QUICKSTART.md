# 🚀 クイックスタート: 3ステップでデプロイ

**所要時間**: 約10分

---

## ✅ 事前準備完了

以下はすでに完了しています：
- ✅ Webサイトファイル作成（8ファイル）
- ✅ Gitリポジトリ初期化
- ✅ 初回コミット完了

---

## 📋 あなたがやること（3ステップのみ）

### ステップ1: GitHubリポジトリを作成（2分）

1. https://github.com/new にアクセス
2. 以下を入力：
   ```
   Repository name: patternzen-website
   Description: PatternZen Legal Documents
   Public: ✅ チェック

   ⚠️ 以下は空欄/チェックなし:
   [ ] Add a README
   [ ] Add .gitignore
   [ ] Add a license
   ```
3. 「Create repository」をクリック

---

### ステップ2: コマンドを3つ実行（3分）

GitHubリポジトリ作成後、以下のコマンドを実行：

**⚠️ 重要**: `YOUR_USERNAME` を実際のGitHubユーザー名に置き換えてください

```bash
# 1. リモートリポジトリを追加
git remote add origin https://github.com/YOUR_USERNAME/patternzen-website.git

# 2. ブランチ名を変更
git branch -M main

# 3. プッシュ
git push -u origin main
```

**認証が求められたら**:
- Username: GitHubユーザー名
- Password: Personal Access Token（下記参照）

**Personal Access Token の作成**:
1. https://github.com/settings/tokens
2. 「Generate new token (classic)」
3. Note: `PatternZen`
4. Scopes: `repo` にチェック
5. 「Generate token」
6. トークンをコピーしてパスワード欄に貼り付け

---

### ステップ3: GitHub Pages を有効化（2分）

1. GitHubリポジトリページを開く
2. **Settings** タブをクリック
3. 左サイドバーの **Pages** をクリック
4. Source:
   - Branch: `main` を選択
   - Folder: `/ (root)` を選択
5. **Save** をクリック

**3-5分待つ**と、このURLでアクセスできます：
```
https://YOUR_USERNAME.github.io/patternzen-website/
```

---

## ✅ 完了！

以下のURLをGoogle Play / App Storeの申請フォームに記入してください：

### プライバシーポリシー（必須）
```
https://YOUR_USERNAME.github.io/patternzen-website/privacy-policy.html
```

### 利用規約（推奨）
```
https://YOUR_USERNAME.github.io/patternzen-website/terms-of-service.html
```

---

## 🔍 確認

デプロイ完了後、以下をチェック：
- [ ] トップページが表示される
- [ ] プライバシーポリシーが表示される
- [ ] 利用規約が表示される
- [ ] 全リンクが動作する
- [ ] HTTPSで接続できる

---

## ❓ 問題が発生した場合

詳細な手順は `DEPLOYMENT_GUIDE.md` を参照してください。

---

**所要時間**: 合計約10分
**難易度**: ★☆☆☆☆（簡単）
