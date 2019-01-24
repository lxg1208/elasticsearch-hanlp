FROM elasticsearch:5.4.3-alpine
MAINTAINER lxg1208 (xuegang_1208@163.com)

COPY plugins/elasticsearch-hanlp ./plugins/elasticsearch-hanlp
COPY config/jvm.options ./config/jvm.options

RUN grep 'ES_CLASSPATH=' ./bin/elasticsearch.in.sh | sed 's/"\$ES_HOME\/lib\/\*"/"\$ES_HOME\/lib\/\*\:\$ES_HOME\/plugins\/elasticsearch-hanlp\/"/g' -i ./bin/elasticsearch.in.sh

VOLUME /usr/share/elasticsearch/dictionary
