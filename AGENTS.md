# AGENTS.md

Instrucoes duraveis para Codex trabalhar em um vault Obsidian.

## Regras Criticas

- Antes de qualquer busca recursiva, ignore `.obsidian/`, `.smart-env/`, `.makemd/`, `.space/`, `.trash/` e `.obsidian/themes/`.
- Use `06 - Operations/Mapa do Vault.md` como ponto de entrada quando ele existir.
- Nao trate arquivos internos de plugins, caches, logs ou estado de interface como notas do vault.
- Para buscar notas, limite a exploracao inicial a `00 - Inbox/`, `01 - Source Materials/`, `02 - Knowledge/`, `03 - To Do/`, `04 - Projects/`, `05 - Daily Notes/`, `06 - Operations/`, `_templates/`, `copilot/` e `.agents/`.
- Nao apague, mova, renomeie ou reorganize notas existentes sem confirmacao explicita.
- Nao altere arquivos `.mdenc` sem pedido explicito.
- Se encontrar conflitos `sync-conflict`, reporte antes de resolver.

## Papel do Vault

Este vault e uma segunda mente operacional: Obsidian guarda memoria, contexto, fontes, projetos e decisoes; Codex ajuda a ler, sintetizar, conectar, editar e executar workflows repetiveis.

Priorize:

- preservar a estrutura existente;
- criar notas Markdown uteis e conectadas;
- manter links no estilo Obsidian `[[Nome da nota]]`;
- registrar decisoes, tarefas, logs e aprendizados quando isso ajudar continuidade;
- proteger privacidade e evitar expor conteudo sensivel sem necessidade.

## Estrutura Recomendada

- `00 - Inbox/`: capturas rapidas e entradas ainda nao processadas.
- `01 - Source Materials/`: fontes brutas ou processadas.
- `02 - Knowledge/`: notas conceituais permanentes.
- `03 - To Do/`: tarefas e listas.
- `04 - Projects/`: projetos ativos e documentacao.
- `05 - Daily Notes/`: notas diarias, pensamentos e rascunhos.
- `06 - Operations/`: logs, decisoes, tarefas operacionais e mapas.
- `_templates/`: templates do Obsidian.
- `.agents/skills/`: workflows locais para Codex.

## Como Buscar Contexto

1. Verifique a pasta relacionada ao pedido do usuario.
2. Procure notas existentes antes de criar uma nova nota.
3. Use `rg` para buscar nomes, tags e wikilinks.
4. Se o pedido envolver projeto, leia primeiro `04 - Projects/<Projeto>/`.
5. Se envolver conceito, leia primeiro `02 - Knowledge/`.
6. Se envolver fonte, leia primeiro `01 - Source Materials/`.

## Skills Locais

Use `.agents/skills/` como biblioteca de workflows.

- `processar-fonte`: transformar fontes brutas em notas uteis.
- `criar-conceito`: criar ou aprimorar notas conceituais.
- `conectar-notas`: sugerir ou criar conexoes coerentes.
- `registrar-decisao`: registrar decisoes importantes.
- `registrar-log`: registrar sessoes de trabalho e pendencias.

## Regras de Escrita

- Use `[[wikilinks]]` para conexoes internas relevantes.
- Escolha poucos links bons em vez de muitos links decorativos.
- Prefira linguagem clara, natural e consultavel.
- Evite a formula "X nao e apenas/nao e simplesmente/nao e..., e Y".
- Ao criar nota nova, use titulo claro, frontmatter simples e secoes consistentes.
- Ao final de trabalhos relevantes, ofereca registrar log, decisao ou aprendizado em `06 - Operations/`.

## Privacidade

Trate o vault como privado. Nao publique notas pessoais, fontes privadas, diarios, logs reais, decisoes reais, arquivos cifrados ou estados de plugins.
