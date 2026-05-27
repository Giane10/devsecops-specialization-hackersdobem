# 🧪 Laboratório 2.3: Controle de Versão, Tags e Resolução Avançada de Conflitos no GitLab

Este espaço é dedicado ao registro conceitual e documentação de aprendizados teóricos e práticos adquiridos durante o **Laboratório 2.3**, integrante do Módulo 2 da especialização em DevSecOps (Trilha Hackers do Bem).

> ⚠️ **Nota de Conformidade:** Em respeito aos critérios de integridade e ranqueamento do programa Hackers do Bem, este repositório **não contém** arquivos de entrega, respostas de questionários, scripts internos ou relatórios de evidências (PDFs/prints) das atividades práticas. Este arquivo possui finalidade estritamente de portfólio pessoal e registro de competências.

---

## 🎯 Objetivos do Laboratório
O objetivo principal foi simular cenários reais de concorrência de código em ambientes colaborativos, dominando a criação de marcos de release (Tags) e aplicando as três principais estratégias de resolução de conflitos de linhas de desenvolvimento no Git.

---

## 🛠️ Conceitos e Ferramentas Estudados

* **Gerenciamento de Releases com Git Tags:** Estudo sobre a criação de ponteiros imutáveis (`git tag`) para marcar estados estáveis do software (como as versões `v1.0` e `v1.1`), compreendendo os fluxos de rollback seguro e navegação histórica.
* **Resolução Concorrente via Git Merge:** Análise de conflitos estruturais gerados em fusões tradicionais, interpretando os marcadores nativos do Git (`<<<<<<< HEAD`, `=======`, `>>>>>>>`) e realizando a consolidação manual de linhas de código concorrentes.
* **Linearidade de Histórico via Git Rebase:** Estudo sobre o comportamento do `git rebase` como alternativa ao merge, compreendendo o processo de reaplicação de commits locais sobre uma nova base atualizada e o controle de fluxo com `--continue` ou `--abort`.
* **Isolamento de Estado Temporário (Git Stash):** Utilização do mecanismo de empilhamento dinâmico (`git stash`) para salvar modificações em andamento no *Working Tree*, permitindo alternar branches com segurança e gerenciar conflitos no momento do desempilhamento (`git stash pop`).

---

## 🚀 Competências Desenvolvidas

1. **Ciclo de Vida de Tags (Marcos de Versão):**
   * Criação e listagem de tags locais para controle de entrega contínua.
   * Navegação em estados passados do repositório utilizando `git checkout <tag>`.

2. **Tratamento de Conflitos de Merge (Abordagem Tradicional):**
   * Identificação de modificações simultâneas na mesma linha do arquivo `ReadMe` vindas de branches distintas (`master` e `feature`).
   * Resolução manual utilizando editores CLI (`nano`) para garantir a integridade do código final antes do commit de consolidação.

3. **Reescrita Linear de Histórico (Rebase):**
   * Execução de rebase concorrente, mitigando divergências e aplicando commits da branch `feature2` diretamente no topo da cronologia atualizada da `master`.

4. **Gerenciamento de Contexto Efêmero (Stash):**
   * Mitigação de erros de bloqueio de transição de branch salvando estados não commitados.
   * Recuperação e resolução de conflitos direto no desempilhamento de alterações.

---

## 📑 Conclusão

A realização desta atividade prática consolidou a maturidade técnica essencial para atuar em equipes de Engenharia DevOps de alta performance. Compreender a diferença mecânica entre mesclar histórico (merge), linearizar commits (rebase) e guardar contextos temporários (stash) é fundamental para manter esteiras de CI/CD limpas, rastreáveis e livres de quebras de builds durante integrações concorrentes em larga escala.
