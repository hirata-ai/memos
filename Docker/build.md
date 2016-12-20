# Dockerfile からイメージをビルドする
* 今いるフォルダ内のDockerfile をビルドする
`docker build -t [image_name](:tag_name) .`

# ビルドしたイメージからコンテナを起動する
`docker run -dit --name [container_name] [image_name] /bin/bash`

# 起動中のコンテナでコマンドを実行する
`docker exec -ti [container_name] /bin/bash`
