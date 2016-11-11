### Flume Elasticsearch Slink

#### Desc

Support Elasticsearch 2.3.3 API

#### Why

As you know the latest flume still uses elasticsearch 0.90.1 jar which are very old. In my new porject, we are using ES 2.3.3. So I update the existing flume es sink source to support es 2.3.3 jar.

#### How to use

1. mvn clean install -Dmaven.test.skip=true

2. copy new built jar to flume lib folder and remove old one

3. add ext supported jars require by elasticsearch 2.3.3 api, and remove others not required or old.

   ```
   To add: 
   /opt/flume/lib/compress-lzf-1.0.2.jar
   /opt/flume/lib/elasticsearch-2.3.3.jar
   /opt/flume/lib/fastjson-1.2.3.jar
   /opt/flume/lib/flume-ng-elasticsearch-sink-1.7.1.jar
   /opt/flume/lib/guava-18.0.jar
   /opt/flume/lib/hppc-0.7.1.jar
   /opt/flume/lib/jackson-core-2.6.6.jar
   /opt/flume/lib/jackson-dataformat-cbor-2.6.6.jar
   /opt/flume/lib/jackson-dataformat-smile-2.6.6.jar
   /opt/flume/lib/jackson-dataformat-yaml-2.6.6.jar
   /opt/flume/lib/jsr166e-1.1.0.jar
   /opt/flume/lib/libra-flume-ext-0.0.1-SNAPSHOT.jar
   /opt/flume/lib/lucene-core-5.5.0.jar
   /opt/flume/lib/t-digest-3.0.jar

   To delete:
   /opt/flume/lib/flume-ng-elasticsearch-sink-1.7.0.jar
   /opt/flume/lib/guava-11.0.2.jar
   /opt/flume/lib/jackson-core-2.3.1.jar
   ```

#### FAQ

1. Q: Why skip maven test during building?

   A:  I just run it in my project instead of updating existing test case.
