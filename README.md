
# Library System

O **Library System** é um projeto em Java desenvolvido para gerenciar bibliotecas de forma eficiente. Ele permite o cadastro de livros, usuários, empréstimos, devoluções e outras funcionalidades essenciais para a gestão de uma biblioteca.

## Funcionalidades

- **Cadastro de Livros**: Adicionar, editar, remover e consultar livros.
- **Cadastro de Usuários**: Registrar novos usuários e gerenciar seus dados.
- **Empréstimos**: Realizar empréstimos de livros para usuários cadastrados.
- **Devoluções**: Registrar a devolução de livros emprestados.
- **Relatórios**: Gerar relatórios de livros disponíveis, emprestados e usuários com pendências.
- **Busca Avançada**: Pesquisar livros por título, autor, gênero, etc.

## Tecnologias Utilizadas

- **Java**: Linguagem de programação principal.
- **SpringBoot**: Biblioteca de organização do Projeto.
- **PostgreSQL**: Banco de dados para armazenamento de informações.
- **JDBC**: Conexão com o banco de dados.
- **Maven**: Gerenciamento de dependências e build do projeto.
- **Git**: Controle de versão.

## Diagrama UML

Abaixo está o diagrama UML que representa a estrutura do sistema:

![Diagrama UML](uml-diagram.png)

### Descrição do Diagrama UML

- **Classes Principais**:
  - `Livro`: Representa um livro com atributos como título, autor, ISBN, etc.
  - `Usuario`: Representa um usuário da biblioteca com nome, CPF, endereço, etc.
  - `Emprestimo`: Gerencia os empréstimos de livros, relacionando `Livro` e `Usuario`.
  - `Biblioteca`: Classe principal que gerencia as operações do sistema.

- **Relacionamentos**:
  - Um `Usuario` pode realizar múltiplos `Emprestimos`.
  - Um `Livro` pode estar associado a vários `Emprestimos`.
  - A classe `Biblioteca` coordena todas as operações.

## Como Executar o Projeto

1. **Pré-requisitos**:
   - Java JDK 11 ou superior.
   - MySQL instalado e configurado.
   - Maven instalado.

2. **Clone o Repositório**:
   ```bash
   git clone https://github.com/GuilhermexL/library-system.git
   ```

3. **Configuração do Banco de Dados**:
   - Crie um banco de dados no MySQL chamado `library_system`.
   - Configure as credenciais de acesso no arquivo `src/main/resources/config.properties`.

4. **Compilar e Executar**:
   ```bash
   mvn clean install
   mvn exec:java -Dexec.mainClass="com.librarysystem.Main"
   ``` 
## **Metas do Projeto**  

**Fase 1 - Configuração Inicial**  
- [x] Criar o projeto no **Spring Initializr**  
- [x] Configurar o **PostgreSQL** como banco de dados  
- [x] Definir a estrutura do projeto (MVC)  

**Fase 2 - Implementação das Funcionalidades**  
- [x] Criar a entidade **Livro**  
- [x] Implementar repositório JPA para persistência dos dados  
- [x] Criar serviço para regras de negócio  
- [x] Criar controlador REST para gerenciar livros  

**Fase 3 - Melhorias e Validações**  
- [ ] Adicionar validações nos dados (ex: título obrigatório)  
- [ ] Implementar logs para monitoramento da aplicação  
- [ ] Criar testes unitários para os serviços  

**Fase 4 - Integrações e Deploy**  
- [ ] Criar documentação da API com **Swagger**  
- [ ] Criar interface web para interação com os dados 

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Desenvolvido por Guilherme Santos - [2025]