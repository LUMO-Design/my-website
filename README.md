# LUMO Design & Systems — Corporate Website

京都発 Web開発 & システムインテグレーション会社のコーポレートサイト。

## 公開URL

https://lumodesign.jp

## GitHub Pages デプロイ手順

### 1. リポジトリ作成 & push

```bash
cd my-website
git init
git add .
git commit -m "Initial commit: LUMO corporate site"
git branch -M main
git remote add origin git@github.com:<YOUR_USERNAME>/my-website.git
git push -u origin main
```

### 2. GitHub Pages を有効化

1. GitHubでリポジトリページを開く
2. **Settings** → **Pages**
3. Source: **Deploy from a branch**
4. Branch: **main** / **/ (root)** を選択
5. **Save**

数分で `https://<username>.github.io/my-website/` に公開されます。

### 3. カスタムドメイン設定（lumodesign.jp）

#### GitHub側
- Settings → Pages → **Custom domain** に `lumodesign.jp` を入力 → Save
- **Enforce HTTPS** にチェック

#### DNS側（lumodesign.jp のDNS管理画面）

**Aレコード（Apex ドメイン）:**

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**または CNAME（www サブドメイン経由の場合）:**

```
www  CNAME  <username>.github.io.
```

> ※ Apexドメイン（lumodesign.jp）を直接使う場合はAレコード、
> www.lumodesign.jp を使う場合はCNAMEレコードを設定。

### 4. 確認

- DNS反映後（最大24〜48時間、通常は数分〜数時間）
- `https://lumodesign.jp` でアクセス確認
- HTTPS証明書はGitHubが自動発行（Let's Encrypt）

## ファイル構成

```
my-website/
├── index.html   ← メインページ（CSS/JS含む単一ファイル）
├── CNAME        ← カスタムドメイン指定
├── .nojekyll    ← Jekyll処理スキップ
└── README.md    ← このファイル
```

## 技術スタック

- HTML5 / CSS3 / Vanilla JavaScript
- Google Fonts（Cormorant Garamond, Noto Sans JP, Noto Serif JP）
- 外部依存なし、単一HTMLファイルで完結

---

© 2005-2026 LUMO Design & Systems
