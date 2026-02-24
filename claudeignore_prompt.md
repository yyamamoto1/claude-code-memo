# ==========================================
#  .claudeignore
# エージェントのコンテキストと推論を保護する防壁
# ==========================================

# 1. 依存関係とパッケージ（絶対に読ませない）
node_modules/
vendor/
.venv/
env/
venv/

# 2. 巨大なロックファイル（トークン消費の最大の敵）
package-lock.json
yarn.lock
pnpm-lock.yaml
poetry.lock
Gemfile.lock
Cargo.lock

# 3. ビルド成果物とキャッシュ（ノイズ）
dist/
build/
out/
.next/
.nuxt/
.svelte-kit/
target/
.cache/
.turbo/

# 4. 機密情報（セキュリティの観点から物理的に遮断）
.env
.env.*
*.pem
*.key
*.cert
*.p12
credentials.json
id_rsa
*.sqlite3
*.db

# 5. ログとテストカバレッジ
*.log
coverage/
.nyc_output/

# 6. バイナリ・メディアファイル（テキストとして読み込ませない）
*.jpg
*.jpeg
*.png
*.gif
*.svg
*.ico
*.mp4
*.pdf
*.zip
*.tar.gz
*.wasm

# 7. IDEとOSのメタデータ
.vscode/
.idea/
.DS_Store
Thumbs.db

# 8. Git内部ファイル
.git/
