# 🔐 Plano de Ação para Desenvolvimento Seguro (Secure SDLC)

Nesta etapa, estruturei a integração de práticas de segurança em todas as fases do ciclo de desenvolvimento do sistema SalaSegura, aplicando o conceito de Shift-Left (Segurança desde a Concepção).

---

### 🔄 Ciclo de Vida Seguro Integrado (DevSecOps)

#### 📋 1. Planejamento & Requisitos (Modelagem de Ameaças)
Identificação proativa de riscos baseada no OWASP Top 10 aplicados ao contexto de reservas:
* **SQL Injection (Crítico):** Risco de extração de dados sensíveis dos usuários.
* **Quebra de Autenticação (Alto):** Risco de acessos indevidos a funções administrativas.
* **XSS (Médio):** Injeção de scripts em campos textuais de agendamento.

#### 🏗️ 2. Design & Arquitetura (Proteção por Design)
Mecanismos estruturais adotados na fundação do software:
* **RBAC (Role-Based Access Control):** Controle de acesso baseado em perfis (Admin vs. Comum).
* **Menor Privilégio:** Bloqueio nativo de funções de cancelamento para usuários comuns.
* **Defesa em Profundidade:** Camadas sobrepostas envolvendo WAF, autenticação JWT e validação no backend.

#### 💻 3. Desenvolvimento & Codificação (Controles no Código)
Padrões de desenvolvimento seguro exigidos na implementação da API:
* **Prepared Statements:** Parametrização de queries para anular ataques SQLi.
* **Sanitização:** Limpeza e filtragem de inputs nos formulários web.
* **Hashing Avançado:** Criptografia de senhas utilizando Argon2 ou BCrypt.

#### 🧪 4. Testes & Validação (Garantia de Qualidade de Segurança)
Estratégia de testes automatizados e manuais integrada à esteira:
* **SAST:** Análise estática do código-fonte durante a fase de build.
* **DAST:** Testes dinâmicos aplicados contra a aplicação simulando ataques em execução.
* **Pentest:** Teste de penetração simulando cenários reais de invasão.

---

### 📊 Governança e Melhoria Contínua
A segurança é gerenciada através de métricas de vulnerabilidades mapeadas por sprint, garantindo que o feedback dos testes retroalimente a fase de requisitos do próximo ciclo de desenvolvimento.