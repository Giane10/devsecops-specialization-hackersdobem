# 🛠️ Lab 3.4: Monitoramento Contínuo e Resposta a Incidentes

Este repositório armazena o registro conceitual e o mapeamento de competências desenvolvidas durante o **Lab 3.4** do Módulo 3 (Trilha Hackers do Bem). O foco central desta atividade prática foi a implementação de um ecossistema de observabilidade, integrando monitoramento contínuo (Prometheus) e visualização de dados (Grafana) para garantir a saúde, segurança e disponibilidade de uma aplicação web em um ambiente DevSecOps.

> ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade do programa Hackers do Bem, este documento contém exclusivamente registros conceituais, arquiteturas e lições aprendidas. Não são expostos relatórios oficiais de entrega, respostas de questionários ou artefatos protegidos da plataforma de ensino.

---

## 🎯 Objetivos do Laboratório
* **Instrumentação de Aplicação:** Modificação do código-fonte (Go) para exposição de métricas customizadas através de bibliotecas de exportação do Prometheus.
* **Orquestração de Observabilidade:** Implantação de um *stack* de monitoramento contínuo via Docker Compose, unificando a aplicação web, o servidor de coleta (Prometheus) e a plataforma de visualização (Grafana).
* **Configuração de Dashboards:** Mapeamento de fontes de dados e criação de painéis visuais para o monitoramento de eventos, métricas de negócio e status de disponibilidade em tempo real.

---

## 🔬 Competências e Aprendizados Desenvolvidos

### 1. Instrumentação de Código (Exposição de Métricas)
* **Adaptação de Backend:** Alteração da lógica da aplicação `reservas.go` para importar bibliotecas `github.com/prometheus/client_golang`.
* **Exposição de Dados:** Registro de métricas customizadas (`reservationsCounter`) e habilitação do endpoint `/metrics`, permitindo que o servidor de monitoramento realize o *scrape* das informações de negócio da aplicação.
* **Gerenciamento de Dependências:** Atualização dos arquivos `go.mod` e `Dockerfile` para integrar as dependências necessárias de monitoramento no build da imagem.

### 2. Orquestração e Observabilidade (Stack Docker)
* **Configuração de Infraestrutura:** Estruturação de volumes persistentes para persistência de dados do Prometheus e Grafana, garantindo a integridade do histórico de métricas.
* **Service Discovery:** Configuração do `docker-compose.yml` definindo os serviços web, prometheus e grafana, estabelecendo dependências de inicialização (`depends_on`) e exposição de portas para integração entre componentes.
* **Configuração de Data Source:** Vinculação do Grafana ao Prometheus como *Data Source*, parametrizando a URL interna do servidor para centralização da visualização de dados.

### 3. Visualização e Análise de Incidentes
* **Dashboard Design:** Criação de painéis visuais no Grafana, parametrizando queries de métricas para monitorar o status (`up/down`) e o fluxo de reservas da aplicação.
* **Simulação de Resposta:** Testes de resiliência através de interrupção forçada (`docker stop`) e retomada (`docker start`) do container da aplicação, observando a variação em tempo real das métricas no dashboard.
* **Troubleshooting Operacional:** Validação da eficácia do monitoramento como ferramenta de resposta rápida a incidentes, identificando lapsos de disponibilidade através da telemetria visual.

---

## 🧠 Desafios de Infraestrutura e Troubleshooting
O desafio deste laboratório residiu na orquestração de um ambiente *multi-container* com recursos limitados. A carga de execução do stack Prometheus+Grafana, somada à aplicação em Go, exigiu atenção redobrada à integridade dos volumes de dados e à conectividade entre os containers.

**Lições aprendidas no Troubleshooting:**
* **Conectividade de Redes Docker:** Garantir que o Prometheus conseguisse alcançar o endpoint `/metrics` da aplicação, respeitando as definições de rede do `docker-compose`.
* **Gerenciamento de Espaço:** Monitoramento constante de recursos (`df -h`, `docker system df`) para evitar erros de escrita em disco durante a persistência de logs e métricas.
* **Consistência de Dashboard:** O ajuste fino nas queries do Grafana demonstrou que um monitoramento efetivo depende tanto da coleta correta dos dados (instrumentação) quanto da precisão na visualização.

Este laboratório reforçou que, em um ambiente DevSecOps, o monitoramento não é apenas "olhar gráficos", mas sim instrumentar o sistema de forma que ele comunique seu estado de saúde proativamente.

---

## 🛠️ Tecnologias e Conceitos Praticados
<p>
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Observability-000000?style=flat-square&logo=observability&logoColor=white" alt="Observability" />
</p>

---
> 🖥️ *Ambiente de observabilidade homologado com sucesso em sistema Linux via Docker CLI.*