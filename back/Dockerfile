# ベースとなるDokcerイメージを指定する
FROM python:3

# コンソールのstdout（標準出力）と
# stderr（標準エラー出力）のバッファーを無効にする
ENV PYTHONUNBUFFERED 1

# ワークディレクトリを指定する。
WORKDIR /code

# ホストマシンにあるrequirements.txtをImage側のマシンへコピーする
COPY ./requirements.txt .

# pipコマンドを最新にし、
# requirements.txtファイル内のパッケージをインストールする
RUN pip install --upgrade pip && pip install -r ./requirements.txt