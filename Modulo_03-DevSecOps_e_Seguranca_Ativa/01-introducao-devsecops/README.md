

## 🚀 Atividade Prática 01: Migrando de DevOps para DevSecOps

Este repositório documenta a execução da primeira atividade prática do Módulo 3, cujo tema central foi a transição prática da cultura DevOps para o ecossistema de **DevSecOps**. O objetivo foi integrar conceitos de segurança cibernética diretamente em um fluxo de desenvolvimento ágil (*Shift-Left*). 

A prática envolveu a análise manual e automatizada de vulnerabilidades em contêineres, otimização de infraestrutura e a criação de políticas estritas de bloqueio em uma esteira de Integração Contínua (CI/CD).

---

## 🛠️ Tecnologias e Ferramentas Utilizadas
* **Trivy:** Scanner de vulnerabilidades focado em alvos como imagens de contêineres, pacotes e licenças.
* **Docker Slim:** Ferramenta de engenharia reversa para otimização e redução drástica da superfície de ataque de imagens Docker.
* **GitLab CI/CD:** Plataforma utilizada para a automação e orquestração do pipeline de DevSecOps.
* **Golang:** Linguagem da aplicação base utilizada no laboratório.

---

## 📦 Etapas Executadas no Laboratório

### 1. Análise Manual de Segurança e Geração de Relatórios (Trivy)
Após sanar as limitações de espaço em disco no ambiente da máquina virtual, foi realizada uma varredura manual com o Trivy na imagem original da aplicação (`reserva-salas`). Foram gerados quatro relatórios específicos para documentação:
* `trivy_report.txt` (Visão geral)
* `trivy_severity_report.txt` (Foco em severidades HIGH e CRITICAL)
* `trivy_package_report.txt` (Auditoria de pacotes)
* `trivy_license_report.txt` (Auditoria de licenças)

Durante a auditoria, foi analisada detalhadamente a falha **CVE-2026-39820** no painel do NVD (National Vulnerability Database). Esta vulnerabilidade afeta funções nativas do Go (`ParseAddress`, `ParseAddressList` e `ParseDate`), permitindo ataques de Negação de Serviço (DoS) por esgotamento de CPU e alocação excessiva de memória através de entradas maliciosas.

### 2. Redução de Footprint com Docker Slim
Para mitigar a superfície de ataque e otimizar o consumo de infraestrutura, a imagem foi reconstruída utilizando o Docker Slim.
* **Resultado prático:** A imagem original foi compactada de **896MB** para apenas **9.74MB** na versão `reserva-salas.slim`. Essa redução eliminou binários e pacotes desnecessários, removendo grande parte das vulnerabilidades sem afetar o funcionamento do sistema.

### 3. Automação da Esteira DevSecOps (GitLab CI/CD)
A segurança foi integrada diretamente no ciclo de vida da aplicação através da edição do arquivo `.gitlab-ci.yml`, onde foi adicionado o estágio de teste `test3` com o job `security_scan`.

Foram realizados dois testes principais na esteira:
* **Fase de Monitoramento Passivo:** O pipeline executou a varredura na imagem `.slim` e concluiu com sucesso (**Passed**), demonstrando a conformidade inicial do ambiente.
* **Fase de Bloqueio Estrito (Security Gate):** Foi adicionado o parâmetro `--exit-code 1` no script do Trivy. Como esperado, o pipeline falhou deliberadamente (**Failed**), provando que o mecanismo é capaz de travar o deploy e impedir que um código vulnerável chegue ao ambiente de produção.

---

## 🎯 Conclusão e Aprendizados
Esses relatórios gerados funcionam como uma verdadeira fotografia da segurança do projeto em tempo real, servindo de guia para o time de desenvolvimento corrigir falhas e para auditorias futuras comprovarem a conformidade do software. 

A prática comprovou como a automação reduz erros humanos e traz agilidade, enquanto o método manual nos dá a base crítica necessária para entender o contexto e o impacto real de cada vulnerabilidade no ecossistema de nuvem.