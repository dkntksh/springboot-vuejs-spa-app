FROM node:lts-alpine
# 静的コンテンツを配信するシンプルな http サーバをインストールする
RUN npm install -g http-server
# カレントワーキングディレクトリとして '/app/frontend' フォルダを指定する
WORKDIR /app/frontend
# `package.json` と `package-lock.json` （あれば）を両方コピーする
COPY package*.json ./
# プロジェクトの依存ライブラリをインストールする
RUN npm install

# カレントワーキングディレクトリ(つまり 'app' フォルダ)にプロジェクトのファイルやフォルダをコピーする
COPY . .
# 本番向けに圧縮しながらアプリケーションをビルドする
RUN npm run build
CMD ["http-server", "dist", "-p", "3000"]