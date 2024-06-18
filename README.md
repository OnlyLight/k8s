# K8S crawler
## 1. Run application
- Run progres -> redis -> kafka, kafka-connect -> es -> migrate -> crawler, comsumer, api, website
```
cd config/ && \
  kubectl apply -f pospostgres-config.yaml,postgres.yaml && \
  kubectl apply -f redis.yaml && \
  kubectl apply -f kafka-config.yaml,kafka.yaml,kafka-connect-config.yaml,kafka-connect.yaml && \
  kubectl apply -f es-config.yaml,es.yaml && \
  kubectl apply -f migrate-init.yaml,migrate.yaml && \
  kubectl apply -f crawler.yaml,consumer.yaml,api.yaml,website.yaml && \
```

NOTE: restart config ```kubectl rollout restart```
