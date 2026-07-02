# Obsidian Codex Vault System

Sistema leve para usar Codex com um vault Obsidian por meio de instrucoes locais e Agent Skills.

Este repositorio e um template de sistema. Ele nao deve conter notas pessoais, fontes privadas, diario, logs reais, decisoes reais nem estado de plugins do Obsidian.

## O que inclui

- `AGENTS.md` enxuto para orientar Codex dentro do vault.
- Skills locais em `.agents/skills/` para:
  - processar fontes;
  - criar notas conceituais;
  - conectar notas com `[[wikilinks]]`;
  - registrar decisoes;
  - registrar logs de trabalho.
- Templates de referencia carregados sob demanda.
- `example-vault/` com notas ficticias para demonstracao.

## O que nao publicar

Nunca publique seu vault real sem revisao manual. Mantenha fora do repositorio:

- `00 - Inbox/` real;
- `01 - Source Materials/` real;
- `02 - Knowledge/` real;
- `03 - To Do/` real;
- `04 - Projects/` real;
- `05 - Daily Notes/` real;
- `06 - Operations/Logs.md` real;
- `06 - Operations/Decisoes.md` real;
- `.obsidian/`, `.smart-env/`, `.makemd/`, `.space/`, `.trash/`;
- arquivos `*.mdenc`;
- caches, estados de plugins e arquivos sensiveis.

## Instalacao

1. Copie `AGENTS.md` para a raiz do seu vault Obsidian.
2. Copie `.agents/skills/` para a raiz do seu vault.
3. Ajuste os nomes de pastas e regras no `AGENTS.md` conforme sua estrutura.
4. Reinicie ou reabra a sessao do Codex se necessario para detectar as skills.

## Estrutura recomendada do vault

```text
00 - Inbox/
01 - Source Materials/
02 - Knowledge/
03 - To Do/
04 - Projects/
05 - Daily Notes/
06 - Operations/
_templates/
.agents/
```

## Publicacao no GitHub

Crie um repositorio separado para este sistema. Nao inicialize Git diretamente no vault real se houver qualquer chance de publicar notas privadas.

```bash
git init
git add AGENTS.md .agents README.md LICENSE .gitignore example-vault
git commit -m "Initial Obsidian Codex vault system"
git branch -M main
git remote add origin git@github.com:USER/obsidian-codex-vault-system.git
git push -u origin main
```

Antes de publicar, rode uma revisao manual procurando nomes, caminhos locais, conteudo pessoal e arquivos inesperados.

## Licenca

MIT. Edite `LICENSE` para incluir o titular correto antes de publicar.
