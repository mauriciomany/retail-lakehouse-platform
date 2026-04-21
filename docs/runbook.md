# Runbook Operacional

## 1. Objetivo

Documentar procedimentos operacionais básicos da plataforma.

## 2. Subir ambiente

```bash
docker compose up -d
```

## 3. Parar ambiente

```bash
docker compose down
```

## 4. Verificar status dos serviços

```bash
docker compose ps
```

## 5. Ver logs

```bash
docker compose logs -f
```

Ou por serviço:

```bash
docker compose logs -f minio
docker compose logs -f spark
docker compose logs -f trino
docker compose logs -f superset
docker compose logs -f nessie
```

## 6. Serviços esperados

- MinIO
- Nessie
- Spark
- Trino
- Superset

## 7. Portas utilizadas

- MinIO API: 19000
- MinIO Console: 19001
- Nessie: 19120
- Trino: 18080
- Superset: 18088
- Spark UI: 18081

## 8. Procedimento de validação inicial

- verificar containers em execução
- acessar MinIO Console
- acessar Trino
- acessar Superset
- verificar catálogo e buckets

## 9. Boas práticas

- não versionar dados runtime
- não versionar segredos
- manter documentação atualizada ao mudar a arquitetura
- validar ambiente antes de iniciar novas etapas
