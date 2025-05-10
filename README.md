# 📝 API REST de Contatos em Go

Este projeto é uma API REST desenvolvida em Go (Golang) para gerenciamento de contatos. Utilizando apenas a biblioteca padrão do Go, a aplicação permite operações de criação, leitura, atualização e exclusão (CRUD) de contatos, armazenados em memória.

## 🚀 Funcionalidades

- API REST para criação, edição, exclusão e listagem de contatos.
- Armazenamento em memória utilizando mapas (`map[int]Contact`).
- Estrutura modular com separação de responsabilidades.
- Manipulação de dados no formato JSON.

## 🛠️ Tecnologias Utilizadas

- **Go (Golang)**: Linguagem de programação utilizada.
- **net/http**: Pacote padrão para criação de servidores HTTP.
- **encoding/json**: Pacote padrão para manipulação de dados JSON.

## 🔧 Como o Sistema Funciona

- **Endpoints REST**: A API disponibiliza endpoints para operações CRUD sobre contatos.
- **Armazenamento em Memória**: Os contatos são armazenados em um mapa, simulando um banco de dados.
- **Manipulação de JSON**: As requisições e respostas são tratadas no formato JSON.
- **Roteamento**: Utilização do `http.ServeMux` para gerenciamento de rotas.

## 📋 Requisitos

- Go 1.20 ou superior.
- VSCode ou outro editor de texto de sua preferência.

## ⚙️ Como Configurar o Projeto

1. Clone este repositório:  
   https://github.com/Vinicius-Rodriguess/go-contacts-api.git  
   `cd go-contacts-api`

2. Compile e execute o projeto:  
   `go run main.go`

3. Acesse a API via navegador ou ferramentas como Postman:  
   `http://localhost:8080/contacts`

## 💾 Exemplo de Uso

### Listar Contatos

- **Método**: GET  
- **Endpoint**: `/contacts`  
- **Descrição**: Retorna a lista de todos os contatos.

### Criar Contato

- **Método**: POST  
- **Endpoint**: `/contacts`  
- **Corpo da Requisição**:

```json
{
  "name": "João Silva",
  "email": "joao.silva@example.com",
  "phone": "123456789"
}
```

- **Descrição**: Cria um novo contato.

### Atualizar Contato

- **Método**: PUT  
- **Endpoint**: `/contacts?id=1`  
- **Corpo da Requisição**:

```json
{
  "name": "João Silva",
  "email": "joao.silva@exemplo.com",
  "phone": "987654321"
}
```

- **Descrição**: Atualiza os dados do contato com ID 1.

### Excluir Contato

- **Método**: DELETE  
- **Endpoint**: `/contacts?id=1`  
- **Descrição**: Remove o contato com ID 1.

## 📌 Limitações Atuais

- Armazenamento em memória: os dados são perdidos ao reiniciar a aplicação.
- Ausência de autenticação e autorização.
- Falta de persistência em banco de dados.

## 📈 Melhorias Futuras

- Integração com banco de dados relacional utilizando GORM.
- Implementação de autenticação JWT.
- Documentação da API com Swagger.
- Testes automatizados com o pacote de testes do Go.
- Paginação e ordenação nos endpoints de listagem.

## 👨‍💻 Autor

**Vinicius Rodrigues**  
GitHub: [Vinicius-Rodriguess](https://github.com/Vinicius-Rodriguess)  
Email: rodrigues.vini.2004@gmail.com
