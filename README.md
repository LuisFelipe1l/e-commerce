# e-commerce
Cliente {
  id: UUID,
  nome: String,
  email: String,
  senha: String (criptografada),
  endereco: {
    rua: String,
    cidade: String,
    estado: String,
    cep: String
  },
  dataCadastro: Date
}
Pedido {
  id: UUID,
  clienteId: UUID,
  itens: [
    {
      produtoId: UUID,
      quantidade: Number,
      precoUnitario: Number
    }
  ],
  total: Number,
  status: String,
  dataCriacao: Date
}
Produto {
  id: UUID,
  nome: String,
  descricao: String,
  preco: Number,
  estoque: Number,
  categoria: String,
  imagens: [String],
  dataCriacao: Date
}
