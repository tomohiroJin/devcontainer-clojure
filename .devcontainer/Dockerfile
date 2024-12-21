# ベースイメージとしてClojure公式イメージを使用
FROM clojure

# 必要なパッケージのインストール
RUN apt-get update && apt-get install -y --no-install-recommends \
  curl \
  zip \
  unzip \
  rlwrap \
  && apt-get clean && rm -rf /var/lib/apt/lists/*

# Leiningenのインストール
RUN curl -O https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein && \
  mv lein /usr/local/bin/lein && \
  chmod +x /usr/local/bin/lein && \
  lein self-install

# ワークスペースディレクトリの作成
WORKDIR /workspace

# デフォルトコマンド
CMD ["lein", "repl"]
