# Agenda — Comunidade Católica em Québec

Agenda de eventos da Comunidade Católica em Québec, em uma única página HTML estática. Funciona no celular (Android e iPhone) e no computador, sem banco de dados, cadastro, cookies ou rastreadores.

## Funcionalidades

- **Fichas de eventos**: cada ficha mostra o ícone do assunto, o título, o assunto, a data em três linhas (dia da semana, dia/mês, hora), o local com o endereço e uma observação opcional.
- **Endereço clicável**: abre o local no Google Maps.
- **Salvar na agenda**: tocar na data baixa um arquivo `.ics`, compatível com Apple Calendar, Google Agenda e Outlook (fuso America/Toronto).
- **Filtros combináveis** na barra fixa do topo: por mês e por assunto, com vários selecionados ao mesmo tempo. O botão **Limpar** volta a mostrar tudo.
- **Lista agrupada por mês**, com o contador de eventos.
- **Eventos passados somem sozinhos.**
- **Temas de cores** definidos no código: claro, escuro, pergaminho (o atual), oliveira e vitral.
- **Fontes embutidas** (Figtree e Young Serif), sem pedidos a servidores externos.
- **Aviso de privacidade e uso** no rodapé.

## Assuntos

| Assunto | Ícone |
|---|---|
| Santifica | santo |
| Missa | cálice |
| Café com Jesus | xícara |
| Catequese | livro |
| Perseverança | âncora |
| Comitê | pessoas |
| Oração | casa |

## Como usar

Abra o `index.html` no navegador. Não há instalação nem dependências. Por ser um arquivo único, ele pode ser hospedado em qualquer serviço de páginas estáticas.

## Como atualizar os eventos

Toda a configuração fica no bloco `CONTEÚDO: edite aqui`, no início do script do `index.html`.

Cada evento é uma linha da lista `EVENTOS`:

```js
{ titulo: 'Missa em Português', cat: 'missa', data: '2026-11-21', hora: '17:00', local: 'Église Sainte-Ursule', endereco: '3290 Rue Armand Hamelin, Québec, QC G1W 2W9' },
```

| Campo | Obrigatório | Formato |
|---|---|---|
| `titulo` | sim | texto |
| `cat` | sim | id do assunto: `santifica`, `missa`, `cafe`, `catequese`, `perseveranca`, `comite`, `oracao` |
| `data` | sim | `AAAA-MM-DD` |
| `hora` | sim | `HH:MM` |
| `local` | sim | nome do local |
| `endereco` | sim | endereço usado no link do Google Maps |
| `obs` | não | observação exibida no fim da ficha |
| `duracao` | não | duração em minutos, usada só no arquivo de calendário |

Outras opções do mesmo bloco:

| Constante | Função | Valor atual |
|---|---|---|
| `TEMA` | tema de cores | `'pergaminho'` |
| `MOSTRAR_PASSADOS` | `false` esconde os eventos que já passaram | `false` |
| `DURACAO_PADRAO_MIN` | duração do evento no `.ics` quando falta `duracao` | `60` |
| `FUSO` | fuso horário do `.ics` | `'America/Toronto'` |
| `CATEGORIAS` | assuntos, nomes e ícones | 7 assuntos |
| `ICONES` | desenhos disponíveis para os assuntos | — |

## Pedidos de inclusão, alteração ou exclusão

A comunidade envia os pedidos no WhatsApp da comunidade, e um membro do comitê organizador atualiza o arquivo.

## Privacidade

A página não coleta dados de quem a visita. Ela guarda no aparelho apenas preferências locais, e nada disso é enviado a ninguém. Os nomes e endereços das casas que recebem encontros aparecem com a autorização de cada anfitrião e servem só para chegar ao encontro.

> Se este repositório for público, não publique nele os endereços reais das casas. Use um repositório privado ou uma versão do `index.html` sem esses dados.

## Créditos

Iniciativa de membros voluntários da comunidade, sem vínculo oficial com a Igreja Católica ou com uma paróquia.

Fontes: Figtree (c) 2022 The Figtree Project Authors e Young Serif (c) The Young Serif Project Authors, ambas sob a SIL Open Font License 1.1.
