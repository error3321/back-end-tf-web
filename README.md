# back-end-tf-web
Back-End do trabalho final da disciplina de WEB

Integrantes:

Ana Luysa
Cristal Dáfinny
Cristhian Fernandes
Ellen Alves
Henry Guilherme

URL API:https://back-end-tf-web-one.vercel.app/

GET/usuarios
Descrição: Retorna todos os usuários
[
  {
    "id_usuario": 1,
    "nome": "João Silva",
    "email": "joao@example.com",
    "criado_em": "2025-11-10T14:20:00Z"
  }
]

GET/usuario/:id
Descrição: Retorna um único usuário
{
  "id_usuario": 1,
  "nome": "João Silva",
  "email": "joao@example.com",
  "criado_em": "2025-11-10T14:20:00Z"
}

POST/usuario
Descrição: Cadastra um usuário
{
  "nome": "Nome do usuário",
  "senha": "senha123",
  "email": "email@exemplo.com"
}
Resposta 201 Created
{
  "id_usuario": 10,
  "nome": "Nome do usuário",
  "email": "email@exemplo.com",
  "criado_em": "2025-11-23T12:00:00Z"
}

PUT/usuario/:id
Descrição: Atualiza os dados de um usuário
{
  "nome": "Nome atualizado",
  "senha": "novaSenha123",
  "email": "novo-email@email.com"
}

DELETE/usuario/:id
Descrição: Exclui um usuário


GET/produto
Descrição: Retorna todos os produtos.
[
  {
    "id_produto": 1,
    "nome": "Super Retro",
    "descricao": "Jogo clássico",
    "preco": 59.90,
    "estoque": 5,
    "destaque": true,
    "data_cadastro": "2025-06-10",
    "imagem": "prod1.jpg",
    "ativo": true
  }
]

GET/produto/:id
Descrição: Retorna um único produto pelo ID.

POST/produto
Descrição: Cadastra um produto.
{
  "nome": "Nome do produto",
  "descricao": "Descrição",
  "preco": 120.50,
  "estoque": 10,
  "destaque": false,
  "data_cadastro": "2025-11-23",
  "imagem": "imagem.jpg",
  "ativo": true
}

PUT/produto/:id
Descrição: Atualiza um produto.

DELETE/produto/:id
Descrição: Desativa ou remove um produto.


GET/compra
Descrição: Retorna todas as compras.
[
  {
    "id_compra": 1,
    "id_usuario": 1,
    "usuario_nome": "João Silva",
    "id_produto": 2,
    "produto_nome": "Mega Retro",
    "quantidade": 2,
    "data_compra": "2025-11-10T14:20:00Z"
  }
]

GET/compra/:id
Descrição: Retorna uma compra específica.

POST/compra
Descrição: Registra uma nova compra.
{
  "id_usuario": 1,
  "id_produto": 2,
  "quantidade": 1
}
Resposta: 201 Created
{
  "id_compra": 42,
  "id_usuario": 1,
  "id_produto": 2,
  "quantidade": 1,
  "data_compra": "2025-11-23T12:28:00Z"
}

PUT/compra/:id
Descrição: Atualiza a quantidade da compra.

DELETE/compra/:id
Descrição: Cancela uma compra.