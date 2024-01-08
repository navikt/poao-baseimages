# POAO baseimages

Base docker images for PO Arbeidsoppfølging (POAO).

Bygger videre på base images fra https://github.com/navikt/baseimages.

## Bygg lokalt
```shell script
docker build -t poao-baseimages-java11 --build-arg java_version=11 ./java
```

## Hvordan ta i bruk base image

### Java
```dockerfile
FROM ghcr.io/navikt/poao-baseimages/java:<11|17|21>
COPY <path-to-jar> app.jar
```

## Remote debugging med Java base image

I Java base imagene så er remote debugging skrudd på for port 5005 i development clustrene "dev-fss" og "dev-gcp".
For å kunne remote debugge en kjørende applikasjon så må man først port-forwarde til podden hvor applikasjonen kjører.

```shell script
kubectl port-forward pod/<pod-name> 5005:5005
```

Hvis ikke allerede gjort, opprett en ny configuration i IntelliJ av type "Remote".
Start debuggingen slik som man vanligvis ville gjort lokalt.
