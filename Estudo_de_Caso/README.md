# 🛡️ Estudo de Caso: Pipeline DevSecOps - Hackers do Bem

## 📌 Sobre o Projeto
Este repositório contém a implementação de uma esteira de Integração Contínua e Entrega Contínua (CI/CD) focada em **Hardening e Governança de Código**. Desenvolvido como parte do estudo de caso do programa Hackers do Bem, o objetivo principal desta arquitetura é aplicar a cultura *Shift-Left*, garantindo que nenhuma vulnerabilidade chegue ao ambiente de produção.

Em vez de um fluxo tradicional de aprovação simples, o pipeline atua como um inspetor rigoroso de segurança e qualidade, bloqueando falhas antes da geração do artefato final.

## 🛠️ Tecnologias e Ferramentas Utilizadas
*   **Linguagem:** Python
*   **Containerização:** Docker
*   **Automação de CI/CD:** GitHub Actions
*   **SAST (Static Application Security Testing):** Bandit
*   **SCA (Software Composition Analysis):** Pip-Audit
*   **Inspeção de Qualidade:** SonarCloud

## ⚙️ Arqu Arquitetura do Pipeline

O fluxo foi desenhado com foco em **alta performance (Paralelismo Inteligente)** e feedback rápido (Fail-Fast). O tempo total de execução da esteira é de aproximadamente **2m 24s**.

A arquitetura é dividida nos seguintes estágios:

### 1. Testes Unitários com Hardening
O estágio inicial executa testes nativos da aplicação. Para mitigar ataques de cadeia de suprimentos (*Supply Chain Attacks*), as dependências são instaladas de forma estrita:
*   Uso de `unittest`.
*   Instalação trancada via `pip install --require-hashes` e `--only-binary :all:`.

### 2. Análise Simultânea de Segurança e Qualidade
Após a aprovação dos testes, o pipeline se divide em três frentes que rodam em paralelo para otimização de tempo:
*   **Análise SAST:** Varredura estática do código fonte com o `Bandit` em busca de falhas comuns de segurança em Python. O artefato gerado é salvo para auditoria.
*   **Análise de Dependências:** O `Pip-Audit` verifica o ambiente. O pipeline é configurado com tolerância zero para vulnerabilidades conhecidas nas bibliotecas de terceiros.
*   **Qualidade de Código:** Integração corporativa com o `SonarCloud` para análise profunda de *bugs*, *code smells* e *hotspots* de segurança.

### 3. Build e Entrega Garantida
A imagem da aplicação só é construída e enviada ao repositório se o código passou ileso por todas as barreiras anteriores.
*   Construção da imagem Docker.
*   Tagueamento dinâmico.
*   Publicação segura no **Docker Hub** utilizando *secrets* armazenadas no GitHub.

## 🚀 Próximos Passos (Roadmap)
*   [ ] Implementação de DAST (Dynamic Application Security Testing).
*   [ ] Configuração do Continuous Deployment (CD) para atualização automatizada do servidor de produção.

## 🤝 Agradecimentos
Um agradecimento especial ao professor Leandro Venâncio pelo direcionamento técnico cirúrgico, e aos times da RNP, SENAI e SOFTEX por viabilizarem o programa Hackers do Bem e fornecerem uma base sólida para o desenvolvimento seguro de software.