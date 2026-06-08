# 🛠️ Lab 3.5: Práticas em DevSecOps - Infraestrutura como Código (IaC)

Este repositório armazena o registo concetual e o mapeamento de competências desenvolvidas durante o **Lab 3.5** do Módulo 3 (Trilha Hackers do Bem). O foco central desta atividade prática foi a introdução e implementação de **Infraestrutura como Código (IaC)** utilizando Terraform. O objetivo foi automatizar integralmente o aprovisionamento do ecossistema de observabilidade (Aplicação Web, Prometheus e Grafana) estabelecido nos laboratórios anteriores, substituindo a intervenção manual por definições declarativas.

> ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade do programa Hackers do Bem, este documento contém exclusivamente registos concetuais, arquiteturas e lições aprendidas. Não são expostos relatórios oficiais de entrega, respostas de questionários ou artefactos protegidos da plataforma de ensino.

---

## 🎯 Objetivos do Laboratório
* **Aprovisionamento Declarativo:** Substituir a execução imperativa de comandos Docker pela elaboração de um ficheiro de configuração unificado (`main.tf`) utilizando a linguagem HCL (HashiCorp Configuration Language).
* **Automação de Observabilidade:** Orquestrar o download de imagens e a criação simultânea dos contentores da aplicação, do coletor de métricas e do dashboard visual de forma automatizada e previsível.
* **Gestão de Ciclo de Vida:** Dominar os fluxos essenciais de operação de IaC, desde a inicialização de provedores até à destruição limpa e controlada dos recursos instanciados.

---

## 🔬 Competências e Aprendizados Desenvolvidos

### 1. Definição de Infraestrutura (Linguagem HCL)
* **Mapeamento de Provedores:** Configuração do bloco `terraform { required_providers }` para integração com o provider oficial do Docker (`kreuzwerker/docker`), habilitando a comunicação da ferramenta de IaC com o daemon do Docker.
* **Declaração de Recursos:** Estruturação dos blocos `resource "docker_image"` e `resource "docker_container"`, definindo com precisão o mapeamento de portas externas/internas, volumes de configuração e variáveis de ambiente (como credenciais do Grafana).
* **Orquestração de Dependências:** Utilização do argumento `depends_on` para garantir a ordem correta de inicialização da topologia (ex: assegurar que o Grafana só seja aprovisionado após o Prometheus estar ativo).

### 2. Operacionalização do Fluxo Terraform
* **Inicialização e Validação:** Uso do `terraform init` para descarregar plugins de provedores necessários e preparar o diretório de trabalho.
* **Previsibilidade e Planeamento:** Execução do `terraform plan` para gerar e analisar o plano de execução, garantindo que as mudanças propostas na infraestrutura correspondam exatamente ao estado desejado antes da aplicação real.
* **Execução Automatizada:** Aplicação do plano através do `terraform apply`, testemunhando a subida de múltiplos serviços complexos com um único comando, consolidando a agilidade do modelo DevSecOps.

### 3. Governança e Limpeza de Ambiente
* **Validação de Estado:** Verificação do aprovisionamento em tempo real através do CLI (`docker ps`) e acesso aos endpoints web (Grafana na porta 3000), comprovando que o código gerou uma infraestrutura funcional.
* **Descarte Controlado:** Execução do `terraform destroy` para desprovisionar e limpar todos os recursos criados de forma segura, garantindo que não haja custos ocultos, consumo de disco residual ou falhas de segurança por ambientes esquecidos ligados.

---

## 🧠 Desafios de Infraestrutura e Troubleshooting
A transição de um modelo de "cliques e comandos manuais" para "infraestrutura como código" exige uma mudança fundamental de raciocínio. O desafio deste laboratório esteve focado na abstração do ambiente.

**Lições aprendidas na Automação:**
* **Mudança de Paradigma (Imperativo vs. Declarativo):** Compreender que no Terraform não dizemos *como* fazer (ex: `docker run -p 3000:3000`), mas sim *o que* queremos que exista (o estado final do contentor).
* **Sintaxe e Tipagem Rigorosa:** A linguagem HCL exige precisão. O mapeamento correto de arrays para portas (`ports { internal = ..., external = ... }`) e configurações de ambiente provou que um simples erro de formatação barra o planeamento da infraestrutura.
* **Idempotência na Prática:** O laboratório evidenciou que rodar o Terraform múltiplas vezes não cria infraestruturas duplicadas, mas apenas ajusta o ambiente para bater com o código fonte, um pilar essencial para a estabilidade e automação de deploys na nuvem.

Este exercício consolidou a visão de que, em ambientes Cloud e DevOps modernos, servidores não são "animais de estimação" configurados à mão, mas sim "recursos de rebanho" aprovisionados, escalados e destruídos via código.

---

## 🛠️ Tecnologias e Conceitos Praticados
<p>
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white" alt="Terraform" />
  <img src="https://img.shields.io/badge/HashiCorp_HCL-000000?style=flat-square&logo=hashicorp&logoColor=white" alt="HCL" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Infrastructure_as_Code-00ADD8?style=flat-square&logo=git&logoColor=white" alt="IaC" />
  <img src="https://img.shields.io/badge/DevSecOps-4CAF50?style=flat-square&logo=linux&logoColor=white" alt="DevSecOps" />
</p>

---
> 🖥️ *Ambiente de infraestrutura automatizada homologado com sucesso via Terraform CLI.*