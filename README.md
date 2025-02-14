
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
- **MySQL**: Banco de dados para armazenamento de informações.
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
   cd library-system
   ```

3. **Configuração do Banco de Dados**:
   - Crie um banco de dados no MySQL chamado `library_system`.
   - Configure as credenciais de acesso no arquivo `src/main/resources/config.properties`.

4. **Compilar e Executar**:
   ```bash
   mvn clean install
   mvn exec:java -Dexec.mainClass="com.librarysystem.Main"
   ```

## Contribuição

Contribuições são bem-vindas! Siga os passos abaixo:

1. Faça um fork do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`).
3. Commit suas mudanças (`git commit -m 'Adicionando nova feature'`).
4. Push para a branch (`git push origin feature/nova-feature`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Desenvolvido por [Seu Nome] - [2025]