# 図形模写マスター - Vercel デプロイ手順

## ファイル構成

```
shape-master-vercel/
├── index.html     # ゲーム本体（自己完結型）
├── vercel.json    # Vercel 設定ファイル
└── README.md      # この手順書
```

## デプロイ方法

### 方法1: Vercel ダッシュボード（最も簡単）

1. [vercel.com](https://vercel.com) にアクセスしてログイン（またはサインアップ）
2. ダッシュボードで **「Add New → Project」** をクリック
3. **「Import Git Repository」** ではなく **「Deploy」** ボタン下の  
   **「Or drag & drop your project folder」** へこのフォルダをドラッグ＆ドロップ
4. そのまま **「Deploy」** をクリック
5. 数秒でデプロイ完了 → 発行されたURLでゲームが公開される 🎉

### 方法2: Vercel CLI（コマンドライン）

```bash
# Vercel CLIをインストール（未インストールの場合）
npm install -g vercel

# このフォルダに移動してデプロイ
cd shape-master-vercel
vercel

# 本番デプロイ（カスタムドメイン等）
vercel --prod
```

### 方法3: GitHub経由（継続的デプロイ）

1. このフォルダをGitHubリポジトリにpush
2. Vercelダッシュボードでそのリポジトリをインポート
3. 以降はGitにpushするたびに自動デプロイ

## 注意事項

- 外部ライブラリへの依存なし（完全オフライン動作）
- BGMはBase64エンコード済みで内蔵されています
- スマートフォン・タブレットでのタッチ操作にも対応しています
