# 🔺 Jekyll ポートフォリオサイト

Windows で **Jekyll + GitHub Pages** による IT エンジニアポートフォリオサイトです。  
Three.js 作品「四面体 PCHF の体積 3D 解説」を組み込んだ構成になっています。

## ✨ 主な特徴

- ✅ **完全無料** - GitHub Pages でホスティング
- ✅ **レスポンシブデザイン** - PC・スマホ対応  
- ✅ **Three.js 対応** - 3D 作品の埋め込み可能
- ✅ **Windows 最適化** - RubyInstaller での動作確認済み
- ✅ **SEO 対応** - 検索エンジン最適化済み

## 🚀 Windows セットアップ手順

### 1. Ruby のインストール

```powershell
# RubyInstaller for Windows をダウンロード
# https://rubyinstaller.org/ から最新版をインストール

# インストール後、MSYS2 development toolchain をインストール
ridk install

# バージョン確認
ruby -v
gem -v
```

### 2. Jekyll のインストール

```powershell
# Jekyll と Bundler をインストール
gem install jekyll bundler

# インストール確認
jekyll -v
```

### 3. プロジェクトのセットアップ

```powershell
# このリポジトリをクローン
git clone https://github.com/soramoyou04/pages.git
cd pages

# 依存関係をインストール
bundle install

# ローカルサーバーを起動
bundle exec jekyll serve
```

### 4. ブラウザで確認

```
http://127.0.0.1:4000
```

## 📁 プロジェクト構造

```
.
├── _config.yml              # Jekyll 設定
├── _layouts/
│   └── default.html         # 共通レイアウト
├── assets/
│   └── css/
│       └── style.css        # メインスタイル
├── projects/
│   ├── tetrahedron-volume.html      # 作品紹介ページ
│   └── tetrahedron-viewer/
│       └── index.html       # Three.js ビューア
├── index.md                 # トップページ
├── Gemfile                  # Ruby 依存関係
└── README.md               # このファイル
```

## 🎯 カスタマイズ方法

### あなたの情報に更新

1. **_config.yml** - サイト基本情報を更新
2. **index.md** - 自己紹介とスキルを修正
3. **_layouts/default.html** - GitHub リンクを更新

### Three.js 作品の組み込み

現在の `projects/tetrahedron-viewer/index.html` はプレースホルダーです。  
あなたの既存の Four tetrahedron 作品に置き換えてください：

```powershell
# 既存の Three.js ファイルを配置
cp path/to/your/threejs-app/* projects/tetrahedron-viewer/
```

## 🌍 GitHub Pages での公開

### 1. GitHub リポジトリの作成

個人サイトの場合：
```
リポジトリ名: soramoyou04.github.io
```

プロジェクト用の場合：  
```
リポジトリ名: portfolio (任意の名前)
```

### 2. ファイルをプッシュ

```powershell
git init
git add .
git commit -m "Initial Jekyll portfolio site"
git branch -M main
git remote add origin https://github.com/soramoyou04/pages.git
git push -u origin main
```

### 3. GitHub Pages を有効化

1. GitHub リポジトリページの **Settings** へ
2. **Pages** セクション
3. **Source** を `Deploy from a branch` に設定
4. **Branch** を `main` / `(root)` に設定
5. **Save** をクリック

約 1-2 分で以下の URL で公開されます：
```
https://soramoyou04.github.io/pages/
```

## 🛠️ 開発コマンド

```powershell
# ローカル開発サーバー開始
bundle exec jekyll serve

# 下書きモードで開始 
bundle exec jekyll serve --drafts

# ライブリロード有効
bundle exec jekyll serve --livereload

# 本番環境ビルド
bundle exec jekyll build
```

## 📝 よくあるトラブルシューティング

### Windows で bundle install が失敗する

```powershell
# Windows 用の gem を明示的にインストール
gem install tzinfo-data
gem install wdm
bundle install
```

### ポートが使用中のエラー

```powershell
# 別のポートで開始
bundle exec jekyll serve --port 4001
```

### 文字化けする場合

```powershell
# コードページを UTF-8 に設定
chcp 65001
bundle exec jekyll serve
```

## 🔄 更新と保守

### Jekyll アップデート

```powershell
bundle update jekyll
bundle install
```

### GitHub Pages gem 更新

```powershell
bundle update github-pages
```

## 📚 参考リンク

- [Jekyll 公式ドキュメント](https://jekyllrb.com/)
- [GitHub Pages と Jekyll](https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll)
- [RubyInstaller for Windows](https://rubyinstaller.org/)
- [Three.js 公式サイト](https://threejs.org/)

## 📄 ライセンス

MIT License - 自由にカスタマイズしてお使いください。

---

**🎉 セットアップ完了です！質問があれば GitHub Issues でお気軽にどうぞ。**