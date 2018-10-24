
```shell
docker run -d --name es_test \
        -p 9200:9200 -p 9300:9300 \
        -v $PWD/esdata:/usr/share/elasticsearch/data \
        -v /etc/localtime:/etc/localtime \
        gswyhq/elasticsearch-ce-alpine:v5.6.10

```

elasticsearch的docker镜像，安装了ik、pinyin分词插件，注释掉了：VOLUME /usr/share/elasticsearch/data；

git clone https://github.com/docker-library/elasticsearch.git

cp -r elasticsearch/5/alpine elasticsearch-ce-alpine

wget -c -t 0 -O elasticsearch-analysis-ik-5.6.10.zip https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v5.6.10/elasticsearch-analysis-ik-5.6.10.zip

wget -c -t 0 -O elasticsearch-analysis-pinyin-5.6.10.zip https://github.com/medcl/elasticsearch-analysis-pinyin/releases/download/v5.6.10/elasticsearch-analysis-pinyin-5.6.10.zip


