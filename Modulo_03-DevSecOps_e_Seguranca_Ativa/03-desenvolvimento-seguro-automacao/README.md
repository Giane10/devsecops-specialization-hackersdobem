
# 🛠️ Lab 3.3: Desenvolvimento Seguro e Automação de Tarefas de Segurança

Este repositório armazena o registro conceitual e o mapeamento de competências desenvolvidas durante o **Lab 3.3** do Módulo 3 (Trilha Hackers do Bem). O foco central desta atividade prática foi a automação de políticas de segurança (Shift-Left) através da integração nativa de ferramentas de análise estática (SAST) e análise de composição de software (SCA) no pipeline de CI/CD.

> ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade do programa Hackers do Bem, este documento contém exclusivamente registros conceituais, arquiteturas e lições aprendidas. Não são expostos relatórios oficiais de entrega, respostas de questionários ou artefatos protegidos da plataforma de ensino.

---

## 🎯 Objetivos do Laboratório
* **Aprofundamento em SAST (Análise Estática de Segurança):** Explorar a triagem fina e a governança de vulnerabilidades de código-fonte diretamente nos painéis de monitoramento.
* **Instalação e Configuração de Plugins SCA:** Homologar a extensão do ecossistema SonarQube com o plugin OWASP Dependency-Check para rastreio de componentes de terceiros.
* **Automação de Esteira (Pipeline Security):** Configurar o pipeline do GitLab CI/CD para executar varreduras automatizadas a cada build e centralizar os dados coletados.

---

## 🔬 Competências e Aprendizados Desenvolvidos

### 1. Auditoria Fina e Triagem de Security Hotspots
* **Mapeamento Conceitual:** Análise avançada sobre o perfil de qualidade customizado (**Perfil HDB**), com foco na exploração de regras para a linguagem Go.
* **Revisão Manual Prática:** Triagem manual focada em identificar e mitigar riscos críticos de brechas arquiteturais através do filtro `Security Hotspot` no SonarQube, inspecionando falhas como *Hard-coded credentials* (credenciais fixas no código) e *Using hardcoded IP addresses* (endereços de IP fixos no código).
* **Hardening Estrutural:** Estudo e aplicação de defesas ativas e preventivas na lógica de software, definindo a obrigatoriedade da cláusula estrita `else` terminando cadeias de `if/else if` (evitando estados indefinidos) e a inserção mandatória do bloco `default` em instruções `switch` (captura obrigatória de exceções e dados inesperados).

### 2. Extensão de Recursos e Configuração SCA (SonarQube)
* **Gerenciamento do Marketplace:** Execução prática de instalação e deploy interno do plugin **OWASP Dependency-Check** através da aba de administração do servidor SonarQube, seguida pelo ciclo completo de reinicialização segura do serviço.
* **Governança do Plugin:** Configuração detalhada de parâmetros avançados do mecanismo de scanner, habilitando nativamente as diretrizes para catalogar achados como `Security-Hotspot`, ativar o sumarizador (`Summarize`) e padronizar o mapeamento de caminhos através da flag `Use Filepath`.

### 3. Orquestração e Integração no GitLab CI/CD
* **Arquitetura da Esteira (`.gitlab-ci.yml`):** Expansão do pipeline multi-estágio através da criação e acoplamento de uma nova fase de testes chamada `test4`, posicionada de forma sequencial logo após as etapas primárias de análise.
* **Automação do Script de Varredura:** Construção e parametrização do job automatizado `dependency_check`, utilizando a imagem oficial dockerized `owasp/dependency-check`. O script executa:
  * Isolamento de escopo e mapeamento de diretórios locais via shell CLI.
  * Chamada do binário principal mapeando o projeto alvo (`--project "my-golang-app"`), injetando a flag de scanner (`--scan`) e especificando a saída nativa em formato estruturado (`--format "HTML" --out dependency-check-report.html`).
  * Acoplamento automático do relatório gerado ao motor de upload do `sonar-scanner` por meio da propriedade específica `-Dsonar.dependencyCheck.htmlReportPath`.

### 4. Parametrização Imutável do Projeto (`sonar-project.properties`)
* **Mapeamento de Artefatos:** Edição estrita das propriedades de compilação e qualidade para instruir o analisador a anexar múltiplos formatos de relatórios de vulnerabilidade de dependências.
* **Centralização de Logs:** Adição e acoplamento das diretivas de relatórios nos formatos `html`, `xml` e `json` (`sonar.dependencyCheck.htmlReportPath`, `xmlReportPath` e `jsonReportPath`), garantindo a rastreabilidade cross-platform dos pacotes externos utilizados na aplicação Go.

---

## 🧠 Nota de Resiliência e Infraestrutura (Bastidores do Lab)
Trabalhar com infraestrutura ágil em ambientes locais demonstra que o desafio vai muito além do código de segurança. Durante a execução deste laboratório, a orquestração simultânea de múltiplos contêineres pesados em execução em segundo plano no Docker (como o motor do SonarQube, o banco PostgreSQL e a instância local do GitLab) provocou gargalos físicos e o travamento temporário da Máquina Virtual (VM).

A resolução não exigiu apenas o conhecimento dos comandos técnicos, mas paciência e troubleshooting consultivo: o controle manual de janelas ativas, o encerramento planejado de abas redundantes do navegador web e a administração cadenciada dos tempos de resposta do sistema garantiram que todo o ambiente se estabilizasse, permitindo coletar com sucesso todas as evidências visuais necessárias e consolidar o aprendizado prático em sua totalidade. No fim, o valor real está no conhecimento assimilado para proteger sistemas no mundo real.

---

## 🛠️ Tecnologias e Conceitos Praticados
<p>
  <img src="https://img.shields.io/badge/GitLab_CI/CD-181717?style=flat-square&logo=gitlab&logoColor=orange" alt="GitLab CI" />
  <img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=flat-square&logo=sonarqube&logoColor=white" alt="SonarQube" />
  <img src="https://img.shields.io/badge/OWASP_Dependency--Check-000000?style=flat-square&logo=owasp&logoColor=white" alt="OWASP" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go Language" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker Engine" />
  <img src="https://img.shields.io/badge/Linux_CLI-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux Shell" />
</p>

---
> 🖥️ *Ambiente simulado e homologado com sucesso em sistema Linux via linha de comando (Docker CLI).*