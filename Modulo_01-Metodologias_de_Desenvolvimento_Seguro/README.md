
# 🛡️ SalaSegura: Engenharia de Software End-to-End com DevSecOps
### 🚀 Projeto Prático — Curso de Especialização do Hackers do Bem

Bem-vindo ao repositório do **SalaSegura**! Este projeto prático foi desenvolvido como parte do **Curso de Especialização em DevSecOps** do programa **Hackers do Bem**. Aqui, documento o ciclo de vida completo de desenvolvimento, segurança e operações de um sistema web de reserva de salas, integrando os conceitos avançados absorvidos na formação desde a concepção ágil até a conteinerização.

 > ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade e ranqueamento do programa Hackers do Bem, este repositório possui finalidade estritamente de portfólio pessoal e registro de conceitos arquiteturais e metodológicos, não contendo gabaritos ou arquivos confidenciais de entrega.

---

## 🗂️ Navegação do Projeto

Clique em qualquer uma das etapas abaixo para acessar a documentação técnica detalhada e os artefatar de cada entrega:

1. [📋 Etapa 1: Design, Contextualização e Requisitos](./01-design-e-requisitos/)
2. [🏃‍♂️ Etapa 2: Planejamento Ágil e Gerenciamento de Sprints](./02-planejamento-agil/)
3. [🏗️ Etapa 3: Arquitetura de Infraestrutura & DevOps](./03-arquitetura-devops/)
4. [🔐 Etapa 4: Segurança desde o Design (Shift-Left)](./04-shift-left-e-seguranca/)
5. [🐳 Etapa 5: Implementação Prática e Conteinerização](./05-ambientes-docker/)

---

## 🚀 Linha do Tempo do Projeto (Ciclo de Vida)

### [📋 1. Design, Contextualização e Requisitos](./01-design-e-requisitos/)
* **Concepção do SDLC:** Estruturação do ciclo de vida clássico do software, dividindo as fases entre Planejamento, Análise, Design, Desenvolvimento, Testes, Implantação e Manutenção.
* **Mapeamento de Papéis:** Definição clara das responsabilidades entre Analista de Negócios (requisitos), Desenvolvedor (código) e Especialista em Segurança (políticas de acesso).
* **Regras de Negócio:** Modelagem de acessos distintos para Usuários Comuns e Administradores, controle de reservas por horário e restrição de cancelamentos.

### [🏃‍♂️ 2. Planejamento Ágil e Gerenciamento de Sprints](./02-planejamento-agil/)
* **Metodologia Ágil:** Divisão do Product Backlog em Sprints semanais para focar no núcleo de valor do sistema.
* **Sprint Backlog:** Decomposição das funcionalidades em tarefas técnicas menores, estimando um esforço total de 32 horas de desenvolvimento multifuncional para as histórias de Autenticação (US01), Reserva de Sala (US02) e Prevenção de Conflitos (US03).

### [🏗️ 3. Arquitetura de Infraestrutura & DevOps](./03-arquitetura-devops/)
* **Stack DevOps Open Source:** Planejamento de uma infraestrutura escalável baseada em Git/GitLab para controle de versão, Jenkins para automação de Pipelines (CI/CD), Ansible e Terraform para Infraestrutura como Código (IaC).
* **Orquestração e Monitoramento:** Previsão de clusters Kubernetes rodando em nós Linux com escalabilidade automática (HPA), monitorados continuamente por Prometheus e Grafana.

### [🔐 4. Segurança desde o Design - Shift-Left](./04-shift-left-e-seguranca/)
* **Modelagem de Ameaças:** Proteção proativa mapeando riscos do OWASP Top 10, como Injeção de SQL (Risco Crítico), Quebra de Autenticação (Risco Alto) e Cross-Site Scripting - XSS (Risco Médio).
* **Controles e Testes:** Implementação de consultas parametrizadas (*Prepared Statements*), hashing seguro de senhas (BCrypt/Argon2), controle de acesso baseado em funções (RBAC) e planejamento de testes automatizados via SAST e DAST.

### [🐳 5. Implementação Prática e Conteinerização](./05-ambientes-docker/)
* **Ambiente Isolado:** Migração da aplicação desenvolvida em Golang para containers Docker individuais, garantindo a padronização do deploy.
* **Orquestração local:** Utilização do Docker-Compose para gerenciar o mapeamento de portas (8080:8080) e redes internas.
* **Persistência de Dados:** Resolução do desafio da volatilidade dos containers (natureza efêmera) através da configuração de **Docker Volumes**, mapeando o diretório da VM para o container e garantindo a retenção permanente dos dados.

---

## 🛠️ Tecnologias e Ferramentas Dominadas

<p id="tecnologias">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/GitLab-181717?style=for-the-badge&logo=gitlab&logoColor=orange" alt="GitLab" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux CLI" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/Scrum-004088?style=for-the-badge&logo=scrum&logoColor=white" alt="Scrum" />
</p>

* **Segurança Aplicada:** Modelagem de Ameaças (OWASP Top 10), Controle de Acesso Baseado em Funções (RBAC), Hashing de Senhas (BCrypt) e Estratégia Shift-Left.

---

---

## 📊 Resultados e Aprendizados
O projeto consolidou de forma prática os ensinamentos adquiridos no nível de especialização do Hackers do Bem. Integrar a segurança desde o início do planejamento (Shift-Left) e dominar a persistência em ambientes de containers isolados provou ser o caminho ideal para estruturar aplicações resilientes e alinhadas com as demandas reais de mercado.
