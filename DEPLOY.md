# Vercel + GitHub でデプロイする手順

## 1. GitHub にリポジトリを作る

1. [GitHub](https://github.com) にログインする。
2. **New repository** で新しいリポジトリを作成（例: `minicity-lab`）。
3. ローカルでこのフォルダを Git で管理し、GitHub にプッシュする。

```bash
# このプロジェクトのフォルダで
git init
git add minicity_lab.html assets/ vercel.json
git commit -m "Initial: 動くトミカの世界 LP"
git branch -M main
git remote add origin https://github.com/あなたのユーザー名/minicity-lab.git
git push -u origin main
```

※ 不要なファイル（`.md` や画像の分析用ファイルなど）をリポジトリに入れたくない場合は、先に `.gitignore` を作成してから `git add` してください。

---

## 2. Vercel で GitHub と連携する

1. [Vercel](https://vercel.com) にアクセスし、**Sign Up** または **Log In**。
2. **Add New…** → **Project** を選択。
3. **Import Git Repository** で **GitHub** を選び、**Continue** で GitHub 認証（必要なら許可）。
4. 一覧から **先ほど作ったリポジトリ**（例: `minicity-lab`）を選び、**Import**。
5. **Configure Project** ではそのまま **Deploy** で問題ありません。
   - **Root Directory**: 空のまま（リポジトリのルートがプロジェクトのルート）。
   - **Build Command**: 空のまま（静的サイトのため不要）。
   - **Output Directory**: 空のまま。

---

## 3. デプロイ後の確認

- デプロイが終わると、`https://〇〇〇.vercel.app` のような URL が表示されます。
- トップ（`/`）にアクセスすると、`vercel.json` の設定で **minicity_lab.html** の内容が表示されます。
- `assets/` 内の画像もそのまま配信されます。

---

## 4. 今後の更新の流れ

1. ローカルで `minicity_lab.html` や `assets/` を編集。
2. コミットして GitHub にプッシュ。

```bash
git add .
git commit -m "文言・デザインの更新"
git push origin main
```

3. Vercel が自動で再デプロイし、数分以内に本番サイトに反映されます。

---

## 補足

- **カスタムドメイン**: Vercel のプロジェクト設定 → **Domains** から独自ドメインを追加できます。
- **プレビュー**: プルリクエストごとにプレビュー用 URL が発行されます。
- **index.html にしたい場合**: `minicity_lab.html` を `index.html` にリネームしてプッシュすれば、`vercel.json` の rewrite は削除して構いません（ルートが自動で `index.html` になります）。
