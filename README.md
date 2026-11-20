# PROJETO-ALMOXERIFADO
# Controle de Almoxarifado

Sistema web de controle de almoxarifado para organizar as prateleiras
de **Fundos de Formas** e **Fundos de Blocos** por cliente (SGQ • Qualidade).

## Sobre o projeto

O almoxarifado guarda peças de moldes de vários clientes. Cada cliente tem
sua própria prateleira, dividida em duas listas:
- **Fundos de Formas**
- **Fundos de Blocos**

As posições são numeradas (1, 2, 3...). Quando uma posição fica vazia,
ela aparece como **vaga** e o sistema indica a **próxima posição livre**.
O objetivo é saber rapidamente onde cada peça está e onde há espaço para guardar.

## Funcionalidades

- Abas por cliente com contador de peças
- Cadastro, edição e exclusão de peças
- Posições vagas visíveis, com opção de preencher
- Cálculo automático da próxima posição livre
- Busca por ART, número, modelo (TG/DG) e revisão
- Filtro: Cliente Atual / Todos os Clientes
- Exportar CSV
- Restaurar dados de exemplo
- Dados salvos no navegador (localStorage)

## Dicionário de dados

| Campo | Significado |
|---|---|
| Nº | Posição na prateleira |
| ART | Artigo (produto que o molde fabrica) |
| Modelo | TG, DG ou vazio |
| Cav | Rev. Cavidade (revisão da cavidade) |
| Cli | Rev. Cliente (revisão do cliente) |
| Categoria | Fundo de Forma ou Fundo de Bloco |

Legenda: **1º R = Revisão Cavidade | 2º R = Revisão Cliente**
Exemplo: `5 - 1514 TG R0 R0` = posição 5, artigo 1514, modelo TG,
rev. cavidade R0, rev. cliente R0.

Estrutura da peça no código:
{ pos, art, modelo, cav, cli }

## Tecnologias

- HTML
- CSS
- JavaScript (sem frameworks)

## Como rodar

1. Clonar o repositório:
   git clone https://github.com/USUARIO/controle-almoxarifado.git
2. Abrir a pasta no VS Code
3. Abrir o `index.html` no navegador
   (ou usar a extensão Live Server do VS Code)

## Estrutura de arquivos

controle-almoxarifado/
├── index.html
├── style.css
├── script.js
└── README.md

## Como contribuir (regras do grupo)

- Nunca trabalhar direto na `main`
- Uma branch por cartão do Trello (nome igual ao do cartão, ex.: `html-header`)
- Rodar `git pull` antes de começar qualquer tarefa
- Commits pequenos e com mensagem clara
- Abrir Pull Request ao terminar; outra pessoa revisa e faz o merge
- Quadro de tarefas: [link do Trello]

## Padrão de nomes

- CSS: minúsculo com hífen (`.item-peca`, `.btn-primario`)
- JS: camelCase (`renderListas`, `proximaPosicaoLivre`)
- IDs principais: `#abas`, `#busca`, `#lista-formas`, `#lista-blocos`,
  `#modal-peca`, `#modal-cliente`

## Equipe

- [Nome 1]
- [Nome 2]
- [Nome 3]
- [Nome 4]

## Site publicado

[link do GitHub Pages, quando existir]
