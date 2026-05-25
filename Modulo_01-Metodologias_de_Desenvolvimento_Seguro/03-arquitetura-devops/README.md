# 🏗️ Planejamento de Infraestrutura e Pipeline DevOps

Nesta fase, desenhei a arquitetura de infraestrutura e o fluxo de trabalho automatizado para sustentar o sistema SalaSegura de forma escalável, resiliente e totalmente integrada.

### 🔹 Stack Tecnológica Open Source Selecionada
* **Controle de Versão:** Git (local) e GitLab (servidor).
* **CI/CD:** Jenkins para automação de esteiras de integração e entrega contínua.
* **Infraestrutura como Código (IaC):** Terraform para provisionamento de recursos e Ansible para gerenciamento de configuração.
* **Orquestração e Containers:** Docker para isolamento e Kubernetes para gerenciamento de clusters em nós Linux.
* **Monitoramento e Observabilidade:** Prometheus para coleta de métricas e Grafana para dashboards e alertas.

---

### 🔄 Conexão entre as Ferramentas & Feedback Contínuo (Melhoria DevOps)

Atendendo aos critérios de maturidade DevOps, as ferramentas foram integradas em um circuito fechado de automação e feedback:

#### 1. Do Código à Infraestrutura (IaC + CI/CD)
O pipeline inicia com o provisionamento automatizado via **Terraform** e configuração com **Ansible**. Quando um desenvolvedor realiza o check-in de código no **GitLab**, um webhook aciona o **Jenkins** instantaneamente. O Jenkins executa os testes unitários, compila a imagem **Docker** e realiza o deploy automatizado no cluster **Kubernetes**.

#### 2. Da Operação ao Monitoramento Ativo
Assim que o container do sistema de reservas entra em produção no Kubernetes, o **Prometheus** inicia a coleta contínua de métricas de saúde da aplicação (tempo de resposta e uso de CPU). 

#### 3. Fechamento do Circuito (Feedback Contínuo)
Se o volume de acessos ao sistema de reservas de salas disparar, o **Kubernetes** executa a escalabilidade horizontal (HPA). Se ocorrer uma falha crítica na API, o **Prometheus** detecta o comportamento anômalo e aciona os alertas do **Grafana**. O Grafana envia notificações imediatas com logs detalhados para o time de engenharia, que atua na correção do problema através do GitLab, reiniciando o ciclo de CI/CD com total segurança.