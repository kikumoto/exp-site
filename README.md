# Static Site

Simple static website for deployment with Coolify using Nixpacks.

## Files

- `index.html` - Main page
- `404.html` - Custom 404 error page
- `package.json` - Node.js project configuration
- `nixpacks.toml` - Nixpacks configuration for static site

## Coolify Deployment (Nixpacks方式)

このプロジェクトはCoolifyのNixpacksを使用してデプロイするように設定されています：

### Coolifyでの設定手順：

1. **新しいアプリケーションを作成**
2. **Build Pack** を `Nixpacks` に設定
3. **Static Site** オプションを `true` に設定
4. **Public Directory** を `dist` に設定（重要！）
5. GitHubリポジトリのURLを指定
6. デプロイを実行

### 重要な設定項目：

- **Static Site**: `true` (これによりnginxで静的ファイルが配信されます)
- **Public Directory**: `dist` (ビルド後の静的ファイルが配置される場所)
- **Build Pack**: `Nixpacks`

### ビルド処理

- `npm run build` により、HTMLファイルが `dist/` ディレクトリにコピーされます
- Coolifyが `dist/` ディレクトリの内容を nginx で配信します

## Local Development

ローカルでの確認は `index.html` をブラウザで直接開いてください。
