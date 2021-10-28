# POAO baseimages

Base docker images for PO Arbeidsoppfølging (POAO).

Bygger videre på base images fra https://github.com/navikt/baseimages.

## Bygg lokalt
```shell script
docker build -t poao-baseimages-java-11 --build-arg java_version=11 ./java
```
