# 🏗️ Especialização em DevOps & DevSecOps — Trilha Hackers do Bem

Bem-vindo(a) ao meu repositório de especialização técnica! Este espaço foi projetado para consolidar toda a minha jornada de aprendizado na trilha de **DevOps e DevSecOps**, conectando os fundamentos de segurança cibernética a práticas modernas de engenharia, automação de infraestrutura e observabilidade de software.

O objetivo deste portfólio é demonstrar, de forma prática e evolutiva, como construir, automatizar, monitorar e proteger o ciclo de vida completo de uma aplicação (End-to-End).

---

## 🧑‍🏫 Orientação e Coordenação

* **Professor/Instrutor:** Leandro Hilário Venâncio Volpato
* **Instituições:** RNP, SENAI, Ministério da Ciência, Tecnologia e Inovação e SOFTEX

---

## 📖 Estrutura do Portfólio (A Jornada por Capítulos)

O repositório está organizado de forma cronológica e modular, onde cada pasta conta uma parte da história do desenvolvimento seguro:

### 📁 [Módulo 01: Metodologias de Desenvolvimento Seguro](./Modulo_01-Metodologias_de_Desenvolvimento_Seguro) *(Concluído)*
* **O que foi feito:** O ponto de partida estratégico. Aqui, o foco foi entender o ciclo de vida do software (SDLC) sob a ótica da segurança (*Shift-Left*). O laboratório prático envolveu o planejamento ágil, arquitetura DevOps e o design de segurança física e lógica do projeto **SalaSegura**, finalizando com o isolamento do ambiente de trabalho usando **Docker e Contêineres**.

### 📁 [Módulo 02: Pipelines e Testes Automatizados](./Modulo_02-Pipelines_e_Testes_Automatizados) *(Concluído)*
* **O que foi feito:** A transição da estratégia para a automação prática. Neste capítulo, implementei uma infraestrutura ágil ao subir um servidor próprio do **GitLab via Docker**. Realizei o controle de versão de uma aplicação web em **Golang**, geri permissões e acessos granulares (RBAC) via interface gráfica e API (cURL).

### 📁 [Módulo 03: DevSecOps e Segurança Ativa](./Modulo_03-DevSecOps_e_Seguranca_Ativa) *(Concluído)*
* **O que foi feito:** O fechamento do ciclo onde o ecossistema se torna verdadeiramente blindado, automatizado e resiliente. Realizei a auditoria de segurança de imagens com **Trivy** e utilizei o **Docker Slim** para aplicar engenharia reversa, reduzindo o footprint de uma aplicação Go de 896MB para 9.74MB. Construí esteiras de CI/CD completas no **GitLab CI/CD**, integrando análise estática de código (SAST) via **SonarQube** e análise de dependências (SCA) com **OWASP Dependency-Check**. Por fim, implementei um ecossistema de observabilidade em tempo real com **Prometheus e Grafana** para resposta a incidentes e automatizei 100% do deploy desse ambiente utilizando **Terraform** como Infraestrutura como Código (IaC).

### 📁 [Estudo de Caso](./Estudo_de_Caso) *(Concluído)*
* **O que foi feito:** O ápice da especialização. Desenhei e implementei uma arquitetura de DevSecOps real com foco em Hardening e automação de alta performance. Construí uma esteira de CI/CD utilizando **GitHub Actions** para uma aplicação em **Python**. O pipeline aplica o conceito de *Shift-Left* integrando paralelismo inteligente com análise estática (SAST) via **Bandit**, análise de dependências (SCA) via **Pip-Audit**, e inspeção de qualidade com **SonarCloud**, garantindo o bloqueio de vulnerabilidades antes do empacotamento e publicação segura da imagem no Docker Hub.
---

## 🛠️ Tecnologias e Ferramentas Utilizadas

### Visão Categorizada
* **Cultura & Processos:** DevOps, DevSecOps, Secure SDLC, Planejamento Ágil (Scrum/Kanban), Gestão de Vulnerabilidades, Resposta a Incidentes, Engenharia de Confiabilidade (SRE).
* **Infraestrutura como Código (IaC):** Terraform, HashiCorp HCL.
* **Segurança, SAST & SCA:** SonarQube, SonarCloud, OWASP Dependency-Check, Trivy, Bandit, Pip-Audit.
* **Observabilidade & Telemetria:** Prometheus, Grafana.
* **Contêineres, Artefatos & Otimização:** Docker, Docker Compose, Docker Hub, Docker Slim.
* **Controle de Versão & CI/CD:** Git, GitLab CI/CD, GitHub Actions.
* **Linguagens, Ambientes & SO:** Python, Golang, Linux, Bash Shell Scripting, PowerShell, VS Code.

### Painel Visual de Tecnologias
<p align="left">
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" alt="Terraform" />
  <img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white" alt="SonarQube" />
  <img src="https://img.shields.io/badge/OWASP-000000?style=for-the-badge&logo=owasp&logoColor=white" alt="OWASP" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Docker_Hub-0db7ed?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Hub" />
  <img src="https://img.shields.io/badge/GitLab_CI/CD-181717?style=for-the-badge&logo=gitlab&logoColor=orange" alt="GitLab CI/CD" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" alt="PowerShell" />
  <img src="https://img.shields.io/badge/VS_Code-0078D4?style=for-the-badge&logo=visual%20studio%20code&logoColor=white" alt="VS Code" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

---
✨ *Portfólio mantido com orgulho e dedicação por Giane do Nascimento Costa durante a trilha Hackers do Bem.*