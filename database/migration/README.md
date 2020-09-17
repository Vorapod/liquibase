# Vipera Database Migration README

## Run Migration Script on Local

```shell
docker run --rm -v $(pwd)/:/liquibase/ -e "LIQUIBASE_URL=jdbc:mysql://${DB-SERVER}:3306/vipera" -e "LIQUIBASE_USERNAME=vipera" -e "LIQUIBASE_PASSWORD=password" -e "LIQUIBASE_CHANGELOG=changelog.yaml" webdevops/liquibase:mysql update
```
