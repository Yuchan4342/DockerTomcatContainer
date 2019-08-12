# Docker tomcat container
Refered https://knowledge.sakura.ad.jp/15253/

## 実行の仕方
### Dockerfile を使って Docker イメージを作成する
Dockerfile のあるディレクトリに移動して以下を実行する.  
```docker build -t tomcat:1 .```

### 作成した Docker イメージからコンテナを起動する
ホストのポート番号(8081)は適宜変更できる.  
```docker run -it -d --name tomcat-1 -p 8081:8080 tomcat:1```

### Dockerfile_2 を使って Docker イメージを作成する
Java のインストール動作において Dockerfile のときのキャッシュを使うことを確認できる.  
```docker build -t tomcat:2 -f Dockerfile_2 .```
