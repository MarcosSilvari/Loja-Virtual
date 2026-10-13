# 🛒 Mini E-commerce

Loja virtual feita só com **HTML, CSS e JavaScript puro**. Os produtos vêm de uma API pública, e dá para buscar por nome, filtrar por categoria e montar um carrinho de compras com quantidade e total.

O visual segue um tema escuro com tons neon roxo/magenta e efeitos de brilho.

<!-- Adicione aqui um print do projeto: ![Print do Mini E-commerce](print.png) -->

## ✨ Funcionalidades

- Lista de produtos carregada da API **DummyJSON**, com imagem, título, descrição e preço
- **Busca por nome**, atualizada a cada letra digitada
- **Filtro por categoria**, com as categorias criadas automaticamente a partir dos produtos
- Busca e categoria funcionam **juntas** (por exemplo, categoria "beauty" e o texto "lip")
- Mensagem quando nenhum produto é encontrado
- **Carrinho de compras** na lateral:
  - adicionar produtos
  - quantidade por produto (clicar de novo no mesmo produto aumenta a quantidade)
  - remover (diminui a quantidade ou tira o item do carrinho)
  - total calculado automaticamente (preço × quantidade)
- Layout responsivo: em telas pequenas, o carrinho passa para baixo dos produtos

## 🛠️ Tecnologias

- **HTML5**: estrutura da página
- **CSS3**: Grid, Flexbox, `position: sticky`, tema escuro com efeitos de brilho e media queries
- **JavaScript (ES6)**: `fetch` com `async/await`, manipulação do DOM, `filter`, `find`, `forEach`, `Set` e o operador spread
- **[DummyJSON](https://dummyjson.com/)**: API de produtos de teste
- **[Font Awesome](https://fontawesome.com/)**: ícones

## ⚙️ Como funciona

1. Ao abrir a página, o JavaScript busca os produtos em `https://dummyjson.com/products`.
2. Os produtos são guardados em uma lista e desenhados na tela como cards.
3. As categorias (sem repetir) preenchem o campo de seleção.
4. A função `aplicarFiltros` lê o texto da busca e a categoria escolhida **ao mesmo tempo** e mostra só os produtos que combinam com os dois.
5. Ao clicar em **Adicionar ao Carrinho**:
   - se o produto já está no carrinho, a quantidade aumenta
   - se não está, ele entra com quantidade 1
6. O carrinho é redesenhado e o total é recalculado.

## 📁 Estrutura do projeto

```
mini-ecommerce/
├── index.html
├── style.css
├── script.js
└── README.md
```

## 🚀 Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/MarcosSilvari/mini-ecommerce.git
   ```
2. Entre na pasta do projeto:
   ```bash
   cd mini-ecommerce
   ```
3. Abra o `index.html` no navegador (dois cliques ou extensão *Live Server* do VS Code).

Não precisa instalar nada, mas é preciso ter **conexão com a internet** para carregar os produtos.

## 🧠 O que eu aprendi

- Consumir uma API com `fetch` e `async/await`
- Gerar vários elementos na tela a partir de uma lista de dados
- Filtrar listas com `.filter()` e achar itens com `.find()`
- Combinar duas condições de filtro (busca e categoria) em uma única função
- Remover valores repetidos com `Set`
- Copiar objetos acrescentando campos com o operador spread
- Controlar quantidade e total de um carrinho
- Deixar a página responsiva com CSS Grid e media queries

## 🔮 Melhorias futuras

- [ ] Carregar o carrinho salvo ao abrir a página (`localStorage`)
- [ ] Mostrar o subtotal de cada item no carrinho
- [ ] Mostrar um aviso de "Carregando..." enquanto os produtos chegam
- [ ] Tratar falha de conexão com uma mensagem na tela
- [ ] Ordenar os produtos por preço
- [ ] Finalizar a compra (página de resumo)
- [ ] Publicar com GitHub Pages

## 👨‍💻 Autor

**Marcos Silari**
Estudante de Análise e Desenvolvimento de Sistemas (ADS) na Cruzeiro do Sul.

- GitHub: [@MarcosSilvari](https://github.com/MarcosSilvari)

## 🖼️ Créditos

- Dados e imagens dos produtos: [DummyJSON](https://dummyjson.com/)
- Ícones: [Font Awesome](https://fontawesome.com/)
