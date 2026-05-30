# My Golang App - Esteira de CI/CD com DevSecOps 🚀🛡️

Este repositório contém uma aplicação demonstrativa em Go (`main.go`) estruturada para validar a integração de uma esteira automatizada de Integração Contínua (CI/CD) utilizando **GitLab CI/CD** e análise estática de código e segurança com o **SonarQube**.

O projeto foi desenvolvido e validado integralmente dentro do ambiente de Máquina Virtual (VM) do laboratório prático do Módulo 2.

## 🛠️ Tecnologias e Ferramentas Utilizadas

- **Linguagem:** Go (Golang 1.22.1)
- **Containerização:** Docker & Docker Compose
- **Orquestração de CI/CD:** GitLab CI/CD (com GitLab Runner local)
- **Qualidade & Segurança (SAST):** SonarQube Community Build

## 🚀 Estrutura do Pipeline (.gitlab-ci.yml)

A esteira de automação foi configurada para executar de forma sequencial e fluida, garantindo a validação do código a cada `git push` na branch `master`. Os estágios configurados são:

1. **Build:** Compilação inicial da aplicação em Go para garantir que não há erros de sintaxe.
2. **Test:** Execução dos testes unitários automatizados.
3. **Test2 (Code Analysis):** Integração com o Sonar Scanner para submeter os relatórios de cobertura e qualidade para o servidor local do SonarQube.
4. **Deploy:** Simulação do deploy e empacotamento da aplicação.

## 📊 Resultados Obtidos no SonarQube

Após a execução bem-sucedida da esteira (Pipeline #6), o SonarQube gerou os seguintes indicadores de qualidade e segurança:

- **Status do Quality Gate:** `PASSED` (Aprovado com sucesso)
- **Cobertura de Código (Coverage):** **90.9%** (Métrica atingida através do arquivo de testes `main_test.go`)
- **Débito Técnico (Technical Debt):** Zerado (0h), comprovando a manutenibilidade do código.
- **Security Hotspots:** 1 ponto de atenção identificado no `Dockerfile` devido à boa prática de execução de privilégios de usuário (`root`).

## 📁 Arquivos Principais do Projeto

- `main.go`: Código-fonte principal da API/aplicação em Go.
- `main_test.go`: Arquivo contendo os testes unitários estruturados para validar as funções do código principal.
- `Dockerfile`: Arquivo de configuração para geração da imagem Docker isolada.
- `.gitlab-ci.yml`: Script de automação que define o comportamento de todos os estágios do pipeline.
- `sonar-project.properties`: Arquivo de propriedades responsável por mapear as chaves do projeto e tokens de autenticação com o servidor SonarQube.

---
*Projeto desenvolvido para fins acadêmicos como evidência prática do Módulo 2.*