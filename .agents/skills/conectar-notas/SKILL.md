---
name: conectar-notas
description: Use quando Codex precisar sugerir ou criar conexoes coerentes entre notas Markdown no vault Obsidian usando [[wikilinks]], especialmente ao revisar notas, fontes, conceitos, projetos ou areas.
---

# Conectar Notas

## Objetivo

Melhorar a rede de conhecimento do vault com conexoes pequenas, relevantes e explicaveis.

## Workflow

1. Ler a nota ou conjunto de notas em foco.
2. Buscar notas existentes com nomes, tags ou temas relacionados.
3. Separar conexoes fortes, conexoes possiveis e notas ainda inexistentes.
4. Sugerir conexoes antes de editar quando a mudanca afetar notas existentes.
5. Ao editar, adicionar uma secao `## Conexoes` se ela nao existir.
6. Usar bullets curtos com `[[wikilinks]]` e motivo quando fizer sentido.

## Tipos de Conexao

- Fonte -> conceito: uma transcricao ou livro alimenta uma nota em `02 - Knowledge/`.
- Conceito -> conceito: ideias complementares, opostas ou dependentes.
- Conceito -> projeto: conhecimento aplicado em `04 - Projects/`.
- Projeto -> decisao: escolhas registradas em `06 - Operations/Decisoes.md`.
- Aprendizado -> conceito: experiencia pratica que melhora uma nota permanente.

## Formato Sugerido

```markdown
## Conexoes

- [[Nome da nota]] - motivo curto da conexao.
- [[Outro conceito]]
```

## Regras

- Nao criar links decorativos.
- Nao adicionar dezenas de conexoes de uma vez.
- Priorizar notas existentes, mas permitir wikilinks futuros quando o conceito for claramente util.
- Manter nomes de notas estaveis e naturais em portugues quando o vault ja usa portugues.
- Pedir confirmacao antes de alterar varias notas existentes em lote.
