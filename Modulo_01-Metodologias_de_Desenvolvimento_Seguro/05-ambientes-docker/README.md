# 🐳 Implantação Prática e Conteinerização com Docker

Nesta fase do projeto, o sistema web desenvolvido em Golang foi isolado em um ambiente de microsserviços utilizando Docker, com foco primordial na arquitetura de persistência de dados.

### 🔹 Tecnologias e Comandos Utilizados
* **Dockerfile:** Criação da imagem personalizada, compilando o binário em Go e estruturando os templates HTML.
* **Docker-Compose:** Orquestração do serviço, automatizando o mapeamento da porta local `8080` para a porta `8080` do container.
* **Diagnóstico:** Uso do comando `docker ps` para validar a integridade e o status operacional do container.

### 🧠 O Desafio da Persistência e a Efemeridade (Docker Volumes)
Por padrão, os containers Docker operam de forma **efêmera** (volátil). Isso significa que todo dado gerado ou modificado dentro do container existe apenas na sua camada de escrita temporária. No cenário simulado, ao rodar um `docker-compose down`, todos os dados de agendamentos eram destruídos com o container.

Para resolver isso e transformar o ambiente em uma solução resiliente de nível de produção, configurei a diretiva `volumes` no arquivo de orquestração:

* **Mapeamento:** `/home/aluno/reserva-salas/dados` (VM Host) -> `/app/dados` (Container)

Isso garantiu que os arquivos JSON de reservas persistissem de forma permanente no disco da máquina anfitriã (host), tornando a aplicação totalmente estável e segura contra reinicializações.

### 🧪 Verificação e Validação Prática do Ambiente
A homologação do sucesso da arquitetura de volumes seguiu os seguintes passos técnicos no terminal:

1. **Inicialização:** Subida do ambiente em segundo plano via `docker-compose up -d`.
2. **Inspeção de Saúde:** Uso do comando `docker ps` para garantir que o container do sistema de reservas permanecia ativo e saudável na porta correspondente.
3. **Teste de Resiliência:** Cadastrei novos agendamentos de salas na interface, forcei a destruição completa do container com `docker-compose down` e verifiquei o diretório local da VM, comprovando que os arquivos JSON permaneciam intactos no host. Ao subir o container novamente, a aplicação carregou o estado anterior instantaneamente.