# 🏃‍♂️ Planejamento de Sprints e Gerenciamento Ágil

Nesta fase, documentei a primeira iteração do ciclo de desenvolvimento ágil (Scrum) focado no "núcleo de valor" do sistema de reservas SalaSegura.

### 🔹 Sprint Backlog (Sprint 1 - Duração: 1 semana)
Priorizei e selecionei as User Stories críticas para garantir um incremento de software funcional e seguro:
* **US01:** Autenticação de Perfil (Login para Comum e Admin) -> *Esforço Estimado: 10h (Interface + Lógica)*
* **US02:** Reserva de Sala (Formulário de agendamento e seleção de horários) -> *Esforço Estimado: 10h (Modelagem DB + Frontend)*
* **US03:** Prevenção de Conflitos (Regra de negócio para validação de disponibilidade em tempo real) -> *Esforço Estimado: 12h (Lógica Backend + Testes)*

**Esforço Total Estimado:** 32 horas de desenvolvimento multifuncional e colaborativo.

---

### 🔄 Rituais de Encerramento (Melhoria de Processo Ágil)

Para cobrir o ciclo de vida completo do Scrum e garantir a melhoria contínua da equipe, foram mapeados os seguintes rituais de fechamento:

#### 🔹 Sprint Review (Revisão e Feedback)
* **Status do Incremento:** O núcleo funcional (login, reservas e validação de disponibilidade) foi demonstrado e homologado como "Pronto" (Done).
* **Feedback:** Recebemos a recomendação de implementar alertas de log imediatos na tela para o usuário assim que a reserva for confirmada nas próximas iterações.

#### 🔹 Sprint Retrospective (Retrospectiva)
* **O que funcionou bem:** A divisão de tarefas técnicas menores permitiu uma estimativa precisa e realista das 32 horas de esforço.
* **O que pode ser aprofundado:** Houve um pequeno gargalo na integração do frontend com o backend em Go na metade da semana.
* **Ação Corretiva:** Estabelecer contratos de API rígidos antes de iniciar o desenho das interfaces nas próximas sprints.

#### 🎯 Próxima Iteração (Planejamento Contínuo)
Os próximos itens priorizados para evolução do produto serão:
1. Desenvolvimento do endpoint e botão de cancelamento exclusivo para o perfil Administrador (US04).
2. Criação de logs de auditoria para rastreamento de tentativas falhas de autenticação.