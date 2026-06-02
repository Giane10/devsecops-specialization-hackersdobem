# 🏗️ Especialização em DevOps & DevSecOps — Trilha Hackers do Bem

Bem-vindo(a) ao meu repositório de especialização técnica! Este espaço foi projetado para consolidar toda a minha jornada de aprendizado na trilha de **DevOps e DevSecOps**, conectando os fundamentos de segurança cibernética a práticas modernas de engenharia e automação de software.

O objetivo deste portfólio é demonstrar, de forma prática e evolutiva, como construir, monitorar e proteger o ciclo de vida completo de uma aplicação (End-to-End).

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

### 📁 [Módulo 03: DevSecOps e Segurança Ativa](./Modulo_03-DevSecOps_e_Seguranca_Ativa) *(Em andamento)*
* **O que foi feito até o momento:** O fechamento do ciclo onde o ecossistema se torna verdadeiramente blindado. No primeiro laboratório prático, implementei uma esteira completa de segurança em uma aplicação Go. Realizei a análise manual e documental de vulnerabilidades (como a CVE-2026-39820) utilizando o **Trivy**. Além disso, apliquei engenharia reversa com o **Docker Slim** para reduzir o footprint da aplicação de 896MB para 9.74MB, diminuindo a superfície de ataque. Por fim, integrei tudo no **GitLab CI/CD**, criando políticas rigorosas de bloqueio de deploy automatizado via código de saída (*exit-code*).
* **Próximos passos:** Monitoramento contínuo do ambiente em tempo real e estratégias eficientes de resposta a incidentes.

### 📁 [Estudo de Caso](./Estudo_de_Caso) *(Brevemente)*
* **O que será feito:** Um espaço exclusivo dedicado à análise aprofundada de um cenário real de mercado, aplicando de forma prática e integrada todas as competências de engenharia e segurança adquiridas ao longo da especialização.

---

## 🛠️ Tecnologias e Ferramentas Exploradas
* **Cultura & Processos:** DevOps, DevSecOps, Secure SDLC, Planejamento Ágil (Scrum/Kanban), Gestão de Vulnerabilidades.
* **Segurança & Auditoria:** Trivy (Análise de CVEs, Pacotes e Licenças).
* **Contêineres & Infraestrutura:** Docker, Docker Slim (Otimização de Footprint).
* **Controle de Versão & Plataforma:** Git, GitLab CI/CD.
* **Linguagens & Tecnologias:** Golang (construção e testes da API do laboratório).

---
✨ *Portfólio mantido com orgulho e dedicação por Giane do Nascimento Costa durante a trilha Hackers do Bem.*