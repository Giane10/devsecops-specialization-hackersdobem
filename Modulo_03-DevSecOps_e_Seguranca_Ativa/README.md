# 🛡️ Módulo 3: DevSecOps e Segurança Ativa

Este repositório centraliza o registro conceitual, arquiteturas de infraestrutura e competências desenvolvidas ao longo do **Módulo 3** da especialização em DevOps e DevSecOps (Trilha Hackers do Bem).

> ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade e ranqueamento do programa Hackers do Bem, este repositório **não contém** artefatos de entrega, relatórios de evidências, respostas de questionários ou scripts internos das atividades práticas. O conteúdo possui finalidade estritamente de portfólio pessoal e registro de jornada acadêmica.

---

## 🗺️ Mapa do Módulo e Status de Execução

Abaixo estão listados os laboratórios práticos deste módulo, acompanhados de seus respectivos status de conclusão e links para os registros conceituais detalhados:

| Laboratório | Descrição Técnica | Status | Registro |
| :--- | :--- | :---: | :---: |
| **Lab 3.1** | Introdução ao DevSecOps, Auditoria Trivy e Otimização de Imagens | 🟢 Concluído | [Visualizar](./01-introducao-devsecops/) |
| Lab 3.2 | Segurança de Software e Análise de Vulnerabilidade | 🟡 Em andamento | [Visualizar](./02-seguranca-software-vulnerabilidade/) |
| Lab 3.3 | Desenvolvimento Seguro e Automação de Tarefas de Segurança | ⚪ Brevemente | [Visualizar](./03-desenvolvimento-seguro-automacao/) |
| Lab 3.4 | Monitoramento Contínuo e Resposta a Incidentes em DevSecOps — Parte 1 | ⚪ Brevemente | [Visualizar](./04-monitoramento-continuo-incidentes-p1/) |
| Lab 3.5 | Monitoramento Contínuo e Resposta a Incidentes em DevSecOps — Parte 2 | ⚪ Brevemente | [Visualizar](./05-monitoramento-continuo-incidentes-p2/) |

---

## 🚀 Resumo das Competências Consolidadas

### 🛡️ [Lab 3.1] Introdução ao DevSecOps, Auditoria Trivy e Otimização de Imagens
* **Cultura Shift-Left e Auditoria Manual:** Implementação prática de verificação estática de segurança (SCA) na imagem base Go utilizando a ferramenta Trivy. Diagnóstico e resolução de contenção física de armazenamento em disco dentro do ambiente da VM para viabilizar as rotinas de scanner.
* **Documentação e Engenharia de Relatórios:** Geração estruturada de arquivos de histórico em tempo real (`trivy_report.txt`, `trivy_severity_report.txt`, `trivy_package_report.txt` e `trivy_license_report.txt`), funcionando como fotografias de segurança e artefatos de conformidade para desenvolvedores e auditorias futuras.
* **Análise Crítica de Ameaças (CVE):** Investigação e desmembramento técnico da falha de severidade ALTA **CVE-2026-39820** no painel do NVD (National Vulnerability Database), compreendendo o vetor de ataque de Negação de Serviço (DoS) por esgotamento de CPU e alocação de memória em funções de parsing de strings em Go.
* **Redução Drástica de Superfície de Ataque:** Aplicação de engenharia reversa via **Docker Slim** para otimização de infraestrutura imutável, alcançando a redução real e enxuta do footprint do contêiner de **896MB para 9.74MB**, eliminando dependências e binários supérfluos.
* **Orquestração e Security Gates em CI/CD:** Automação e integração de pipelines de segurança no GitLab CI/CD através do arquivo `.gitlab-ci.yml`. Implementação prática de políticas estritas de bloqueio (*exit-code* ativo) para barrar deploys de códigos vulneráveis em produção e posterior normalização do fluxo.

### 🔬 [Lab 3.2] Segurança de Software e Análise de Vulnerabilidade
* *Resumo técnico das competências em consolidação de acordo com o progresso das aulas práticas desta unidade.*

---

## 🛠️ Tecnologias Dominadas neste Módulo
<p id="tecnologias">
  <img src="https://img.shields.io/badge/Trivy-460BF2?style=for-the-badge&logo=trivy&logoColor=white" alt="Trivy" />
  <img src="https://img.shields.io/badge/Docker_Slim-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Slim" />
  <img src="https://img.shields.io/badge/GitLab_CI/CD-181717?style=for-the-badge&logo=gitlab&logoColor=orange" alt="GitLab CI/CD" />
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux CLI" />
</p>

---
*Este repositório é um portfólio dinâmico e está em constante construção de acordo com o avanço cronológico das aulas e liberação dos módulos.*