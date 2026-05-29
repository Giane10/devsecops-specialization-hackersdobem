# DevSecOps - Aula 2.4: Pipelines e Integração Contínua com GitLab

## 🎯 Objetivo da Atividade
Configuração e execução prática de uma esteira automatizada de CI/CD (Integração Contínua e Entrega Contínua) utilizando o GitLab. O pipeline foi estruturado para realizar o build, os testes unitários com cobertura de código e o deploy final automatizado de uma aplicação em Go (Golang) utilizando contêineres Docker.

## 🛠️ Tecnologias e Conceitos Utilizados
* **GitLab CI/CD:** Automação e orquestração de esteiras de desenvolvimento (Pipeline as Code).
* **GitLab Runner:** Instalação e registro do agente local responsável pela execução dos estágios do pipeline.
* **Docker & Docker Compose:** Provisionamento do Runner em ambiente isolado e empacotamento da aplicação.
* **Go (Golang):** Execução de testes de unidade e compilação do binário da aplicação de exemplo.
* **Segurança e Autenticação:** Implementação de *Personal Access Tokens* (`glpat-`) para tráfego seguro via Git/Terminal.

## 📋 Etapas do Laboratório
- [x] Passo 1: Preparação do Ambiente e Registro do GitLab Runner via Docker Compose
- [x] Passo 2: Preparação do Build (Dockerfile e código Go)
- [x] Passo 3: Configuração do Pipeline Básico e Testes de Cobertura (`.gitlab-ci.yml`)
- [x] Passo 4: Configuração do Deploy Automatizado (Entrega Contínua)
- [x] Passo 5: Validação da Aplicação no Navegador (Acesso via porta adaptada `8081`)

## 🚀 Desafios Superados e Aprendizados Práticos
* **Gerenciamento de Infraestrutura e Conflitos:** Durante a fase de deploy, identificou-se que a porta padrão `8080` da máquina virtual já estava em uso pelos serviços nativos do GitLab. O problema foi mitigado alterando estrategicamente o mapeamento de portas do contêiner no pipeline para a porta `8081` (`-p 8081:8080`), garantindo o isolamento e o sucesso da entrega sem impactar o servidor de código.
* **Controle de Fluxo e Autenticação:** Resolução de problemas de conexão e sincronização de *branches* no terminal Linux, utilizando chaves de acesso seguro no lugar de senhas convencionais para garantir a integridade do `git push`.

---
*Status: 🚀 Laboratório 100% Concluído, validado com sucesso e documentado.*