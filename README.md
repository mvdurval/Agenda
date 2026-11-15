# Agenda: Comunidade Católica em Québec

Agenda de eventos da Comunidade Católica em Québec. É um site estático, sem banco de dados e sem servidor, que pode ser instalado na tela inicial do celular como um aplicativo.

## Funcionalidades

- Lista de eventos com categoria, data, hora e endereço (link para o Google Maps)
- Filtros por categoria e mês, combináveis, com botão "Limpar"
- Download de cada evento como arquivo `.ics` (Apple Calendar, Google Agenda e Outlook)
- Funciona offline depois do primeiro acesso
- Versão protegida por pergunta e resposta, gerada pela ferramenta `proteger.html`

## Estrutura

| Arquivo | Função |
|---|---|
| `index.html` | Aplicação principal e arquivo oficial. Contém a lista `EVENTOS` e a constante `TEMA`. |
| `manifest.webmanifest` | Dados de instalação do app |
| `sw.js` | Cache para funcionamento offline |
| `icon.svg` | Ícone do app |
| `proteger.html` | Ferramenta local que gera `index-protegido.html` |

## Como usar

1. Baixe o repositório ou clone-o.
2. Abra `index.html` no navegador (Edge, Chrome ou Safari). Não é preciso instalar nada.

## Como atualizar os eventos

Edite a lista `EVENTOS` no `index.html`:

```js
{ id: 1, titulo: "Missa dominical", categoria: "Missa", data: "2026-11-22", hora: "10:00", endereco: "Endereço completo, Québec, QC", obs: "" }
