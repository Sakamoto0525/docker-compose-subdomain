# ベースイメージとして Node.js の公式イメージを使用
FROM node:21

# 作業ディレクトリを設定
WORKDIR /app/application1

# package.json と package-lock.json をコピー
COPY package*.json ./

# 依存関係をインストール
RUN npm install

# Next.js アプリケーションのソースコードをコピー
COPY . .

# 環境変数の設定（必要に応じて変更してください）
ENV PORT=15000

# Next.js のビルドを実行
RUN npm run build

# コンテナがリッスンするポートを指定
EXPOSE 15000

# アプリケーションを起動
CMD ["npm", "run", "start"]
