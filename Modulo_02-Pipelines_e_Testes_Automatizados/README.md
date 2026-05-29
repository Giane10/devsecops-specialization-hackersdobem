
# 🛡️ Módulo 2: Infraestrutura Ágil e Pipeline Lifecycle

Este repositório centraliza o registro conceitual, arquiteturas de infraestrutura e competências desenvolvidas ao longo do **Módulo 2** da especialização em DevOps e DevSecOps (Trilha Hackers do Bem).

> ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade e ranqueamento do programa Hackers do Bem, este repositório **não contém** artefatos de entrega, relatórios de evidências, respostas de questionários ou scripts internos das atividades práticas. O conteúdo possui finalidade estritamente de portfólio pessoal e registro de jornada acadêmica.

---

## 🗺️ Mapa do Módulo e Status de Execução

Abaixo estão listados os laboratórios práticos deste módulo, acompanhados de seus respectivos status de conclusão e links para os registros conceituais detalhados:

| Laboratório | Descrição Técnica | Status | Registro |
| :--- | :--- | :---: | :---: |
| **Lab 2.1** | Configuração do Ambiente de Trabalho com o GitLab (Docker Server) | 🟢 Concluído | [Visualizar](./01-Introdução_Git_GitLab/) |
| **Lab 2.2** | Operação do Ambiente de Trabalho e Governança via API REST | 🟢 Concluído | [Visualizar](./02-Infraestrutura_Agil_GitLab/) |
| Lab 2.3 | Controle de Versão, Tags e Resolução de Conflitos no GitLab | 🟢 Concluído | [Visualizar](./03-Controle_de_Versao_e_Conflitos/) |
| **Lab 2.4** | Criação e Configuração de Pipelines de CI/CD no GitLab | 🟢 Concluído | [Visualizar](./04-Pipelines_e_Integracao_Continua/) |
| **Lab 2.5** | *A definir de acordo com o cronograma do curso* | ⚪ Planejado | *Aguardando* |

---

## 🚀 Resumo das Competências Consolidadas

### 🐳 [Lab 2.1] Configuração de Infraestrutura e Gerenciamento Base
* **Provisionamento Isolado:** Estudo da arquitetura e inicialização de um servidor completo do GitLab Server utilizando contêineres Docker para isolamento de ambiente.
* **Governança Inicial e RBAC:** Administração via interface gráfica (GUI) e linha de comando (CLI) para criação de grupos, provisionamento de usuários de teste e estabelecimento de papéis hierárquicos (*Maintainer*).

### 🧪 [Lab 2.2] Operação Avançada e Automação de Governança
* **Administração via API REST:** Utilização do utilitário `curl` para consultas e alterações de permissões de acesso diretamente pela CLI através de requisições `GET` e `PUT`.
* **Maturidade de Desenvolvimento (Git Flow):** Implementação prática de estratégias de ramificação estáveis, utilizando *feature branches* (`feature01`) para isolamento de escopo técnico e execução de fusões (*merge*) seguras na branch principal.
* **Cultura Ágil:** Rastreabilidade de demandas e gerenciamento visual de tarefas integrado através de ecossistemas de *Issues*.

### 🔀 [Lab 2.3] Controle de Versão Avançado e Resolução de Conflitos
* **Ciclo de Vida de Releases (Tags):** Estudo e criação de ponteiros imutáveis (`git tag`) para congelar e documentar versões estáveis de software, garantindo a rastreabilidade e rollback seguro de builds.
* **Resolução Estrutural Concorrente (Merge & Rebase):** Análise e tratamento manual de divergências e conflitos de código na mesma linha de arquivos concorrentes, compreendendo o impacto do `git merge` na preservação do histórico e do `git rebase` na linearização de commits.
* **Gerenciamento de Contexto Efêmero (Stash):** Aplicação prática do mecanismo de empilhamento (`git stash`) para isolamento temporário de modificações em andamento, mitigando bloqueios de transição de branches no terminal.

### 🚀 [Lab 2.4] Pipelines e Integração Contínua (CI/CD)
* **Provisionamento de Runners:** Implantação e gerenciamento de um agente isolado de execução (`gitlab-runner`) integrado via contêiner Docker (`docker-compose`).
* **Automação de Pipelines (`.gitlab-ci.yml`):** Estruturação de esteiras automatizadas divididas em estágios críticos de ciclo de vida (`build`, `test`, `deploy`), garantindo a compilação isolada de artefatos (Pipeline as Code).
* **Garantia de Qualidade (QA):** Implementação de jobs de testes automatizados com relatórios de cobertura de código (*coverage*) nativos na esteira para validação da aplicação em Go.
* **Ciclo de Deploy e Gerenciamento de Infraestrutura:** Configuração de entrega contínua com substituição automatizada de instâncias e mitigação proativa de conflitos de rede, adaptando o mapeamento de portas do contêiner para `8081` de forma a isolar o tráfego dos serviços nativos do GitLab.
* **Segurança na Autenticação:** Uso prático de *Personal Access Tokens* (`glpat-`) como boas práticas de DevSecOps para tráfego e push seguro de código via CLI.

---

## 🛠️ Tecnologias Dominadas neste Módulo
<p id="tecnologias">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/GitLab-181717?style=for-the-badge&logo=gitlab&logoColor=orange" alt="GitLab" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux CLI" />
</p>

---
*Este repositório é um portfólio dinâmico e está em constante construção de acordo com o avanço cronológico das aulas e liberação dos módulos.*


