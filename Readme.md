# Projeto de Estudos com Grafana, Prometheus e PostgreSQL

Este projeto tem como objetivo a criação de um ambiente de monitoramento e análise de dados utilizando Grafana, Prometheus e PostgreSQL, todos containerizados com Docker.

## Visão Geral

A ideia é utilizar esta stack como base para estudos e futuros projetos, incluindo a integração com outras tecnologias para análise e visualização de dados, com foco na preparação para o bootcamp de Engenharia de Dados.

## Tecnologias

- **Grafana:** Para visualização e dashboards.
- **Prometheus:** Para coleta de métricas.
- **PostgreSQL:** Como banco de dados relacional.
- **Docker:** Para orquestração dos containers.

## Como Executar

A stack é executada utilizando Docker. Cada serviço pode ser iniciado individualmente através dos scripts fornecidos.

**Observação:** Se você estiver em um ambiente Linux ou macOS, pode ser necessário dar permissão de execução aos scripts com o comando `chmod +x <nome_do_script>`.

### 1. PostgreSQL (`postegres-local`)

Para iniciar o container do PostgreSQL, execute o script:

```bash
./postegres-local
```
- **Imagem:** `postgres:alpine`
- **Porta:** `5432`
- **Volume:** `pgdata` para persistência dos dados.

### 2. Prometheus (`prometheus`)

Para iniciar o container do Prometheus, execute o script:

```bash
./prometheus
```
- **Imagem:** `prom/prometheus`
- **Porta:** `9090`

### 3. Grafana (`criando_grafana_docker`)

Para iniciar o container do Grafana, execute o script:

```bash
./criando_grafana_docker
```
- **Imagem:** `grafana/grafana-enterprise`
- **Porta:** `3000`
- **Volume:** `grafana-storage` para persistência de dashboards e configurações.

---

### Acessando os Serviços

Após a execução dos scripts, os serviços estarão disponíveis nos seguintes endereços:

- **Grafana:** `http://localhost:3000`
- **Prometheus:** `http://localhost:9090`
- **PostgreSQL:** `localhost:5432`

## Planos Futuros

Este projeto será expandido durante o bootcamp de Engenharia de Dados, com a inclusão de:

- **Python:** Para scripts de coleta e processamento de dados.
- **AWS:** Para deploy e utilização de serviços de nuvem.