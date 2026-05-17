# 📋 Design, Contextualização e Requisitos do Software

Nesta etapa inicial, estabeleci as fundações do sistema "SalaSegura", utilizando o modelo clássico de SDLC (Planejamento, Análise, Design, Desenvolvimento, Testes, Implantação e Manutenção).

### 🔹 Definição de Papéis e Responsabilidades
* **Analista de Negócios:** Levantamento e mapeamento dos requisitos funcionais do sistema.
* **Desenvolvedor:** Responsável pela codificação das regras de negócio e interface.
* **Especialista em Segurança:** Definição das políticas de acesso e proteção de dados.

### 🔹 Requisitos do Sistema & Validação
* **Regras de Negócio:** O sistema gerencia logins de usuários comuns e administradores, listagem de salas disponíveis, agendamentos por horário e concede permissão exclusiva de cancelamento para administradores.
* **Estratégia de Validação:** O software foi desenhado para ser validado por testes de funcionalidade (fluxo de reserva), testes de conflito (bloqueio de horários duplicados) e testes de segurança (privilégios de acesso).

### 🔄 Mapeamento do Ciclo Seguro (Rastreabilidade Técnica)
Atendendo às boas práticas de arquitetura de software, o ciclo de vida deste projeto conecta diretamente os requisitos de negócio à sua validação em ambiente produtivo:

1. **O Requisito (Análise):** O sistema deve mitigar agendamentos duplicados para a mesma sala e horário.
2. **O Design (Arquitetura):** Desenho de uma lógica de backend que realiza uma checagem síncrona no banco de dados antes de persistir a reserva.
3. **A Implementação (Código):** Escrita da regra de negócio de gestão de conflitos em tempo real na API desenvolvida em Go.
4. **O Teste (Validação):** Execução de testes de conflito automatizados simulando tentativas de reservas concorrentes no mesmo período.