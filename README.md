# Groover Mod Hub Catalog

Este repositório funciona como o catálogo online do **Groover Mod Hub**.

Ele guarda:

- `mods.json`: lista principal de mods disponíveis;
- `app_update.json`: controle futuro de atualizações do Hub;
- `images/`: capas e galerias dos mods;
- `changelogs/`: changelogs em Markdown;
- `schemas/`: modelos de validação JSON;
- `templates/`: exemplos para cadastrar mods manualmente durante os testes.

## Estrutura

```txt
groover-modhub-catalog/
├── mods.json
├── app_update.json
├── README.md
├── images/
├── changelogs/
├── schemas/
├── templates/
└── docs/
```

## Como usar nos testes iniciais

1. Crie uma Release no GitHub para o arquivo `.scs` ou `.zip` do mod.
2. Copie o link de download do asset da Release.
3. Edite o `mods.json` e adicione o mod usando o modelo de `templates/mod.example.json`.
4. O Hub deve ler o `mods.json` pela URL raw do GitHub.

Exemplo de URL raw:

```txt
https://raw.githubusercontent.com/SEU_USUARIO/groover-modhub-catalog/main/mods.json
```

## Observações importantes

- Releases não são pastas dentro do repositório. Elas ficam na área **Releases** do GitHub.
- O Hub dos usuários deve apenas ler este repositório.
- O Publisher, futuramente, será responsável por criar releases, enviar arquivos, imagens, changelogs e atualizar `mods.json` automaticamente.
- Não coloque token do GitHub neste repositório.
