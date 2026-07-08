# Obsidian Codex Vault System

Sistema-base para usar o Codex como agente operacional dentro de um vault
Obsidian.

O repositorio combina regras duraveis, skills locais e um vault de exemplo para
ajudar o Codex a navegar, organizar, conectar e registrar conhecimento sem
baguncar notas pessoais.

## Para que serve

Use este projeto quando voce quiser que o Codex trabalhe em um vault Obsidian
com contexto persistente e regras claras.

Ele foi pensado para fluxos como:

- transformar fontes brutas em notas processadas;
- criar notas conceituais permanentes;
- sugerir conexoes entre notas usando `[[wikilinks]]`;
- registrar decisoes importantes;
- registrar logs de sessoes de trabalho;
- preservar a estrutura do vault e evitar alteracoes destrutivas.

## O que vem no repositorio

```text
.
|-- AGENTS.md
|-- LICENSE
|-- README.md
|-- .agents/
|   `-- skills/
|       |-- conectar-notas/
|       |-- criar-conceito/
|       |-- processar-fonte/
|       |-- registrar-decisao/
|       `-- registrar-log/
`-- example-vault/
    |-- 00 - Inbox/
    |-- 01 - Source Materials/
    |-- 02 - Knowledge/
    `-- 06 - Operations/
```

### `AGENTS.md`

Arquivo de instrucoes duraveis para o Codex. Ele define como o agente deve
buscar contexto, quais pastas deve ignorar, como tratar notas existentes e quais
cuidados tomar com privacidade.

### `.agents/skills/`

Biblioteca de workflows locais para tarefas recorrentes dentro do vault:

- `processar-fonte`: transforma fontes, transcricoes, PDFs, prints, artigos,
  aulas ou notas brutas em Markdown processado.
- `criar-conceito`: cria ou melhora notas permanentes em `02 - Knowledge/`.
- `conectar-notas`: sugere ou aplica conexoes coerentes entre notas com
  `[[wikilinks]]`.
- `registrar-decisao`: registra escolhas importantes em
  `06 - Operations/Decisoes.md`.
- `registrar-log`: registra sessoes de trabalho em
  `06 - Operations/Logs.md`.

### `example-vault/`

Vault ficticio e seguro para demonstrar a estrutura recomendada. Ele mostra
capturas, fontes processadas, conceitos, logs, decisoes e um mapa operacional.

## Estrutura recomendada do vault

O sistema assume uma organizacao simples:

```text
00 - Inbox/             capturas rapidas e entradas nao processadas
01 - Source Materials/  fontes brutas ou processadas
02 - Knowledge/         notas conceituais permanentes
03 - To Do/             tarefas e listas
04 - Projects/          projetos ativos e documentacao
05 - Daily Notes/       notas diarias, pensamentos e rascunhos
06 - Operations/        logs, decisoes, mapas e registros operacionais
_templates/             templates do Obsidian
.agents/skills/         workflows locais para Codex
```

A estrutura pode ser adaptada, mas manter estes nomes reduz ambiguidade para o
Codex e facilita buscas futuras.

## Como usar em um vault Obsidian

1. Clone este repositorio.

   ```bash
   git clone https://github.com/V-Medeiros/obsidian-codex-vault-system.git
   ```

2. Copie `AGENTS.md` para a raiz do seu vault Obsidian.

3. Copie a pasta `.agents/skills/` para a raiz do seu vault.

4. Crie ou adapte as pastas principais do vault:

   ```text
   00 - Inbox/
   01 - Source Materials/
   02 - Knowledge/
   03 - To Do/
   04 - Projects/
   05 - Daily Notes/
   06 - Operations/
   ```

5. Crie um mapa operacional em:

   ```text
   06 - Operations/Mapa do Vault.md
   ```

   Use `example-vault/06 - Operations/Mapa do Vault.md` como referencia.

6. Abra o vault pelo Codex e peca tarefas usando o nome das skills quando fizer
   sentido.

   Exemplos:

   ```text
   Use processar-fonte para transformar esta transcricao em uma nota.
   Use criar-conceito para criar uma nota permanente sobre esta ideia.
   Use conectar-notas para sugerir conexoes para esta nota.
   Registre esta decisao no vault.
   Registre um log desta sessao.
   ```

## Fluxo sugerido

1. Capture ideias soltas em `00 - Inbox/`.
2. Processe fontes em `01 - Source Materials/`.
3. Extraia conceitos duraveis para `02 - Knowledge/`.
4. Conecte conceitos, fontes e projetos com `[[wikilinks]]`.
5. Registre decisoes e logs em `06 - Operations/`.
6. Atualize `06 - Operations/Mapa do Vault.md` quando a estrutura mudar.

## Regras de seguranca

O projeto foi desenhado para proteger conteudo pessoal do vault:

- `.gitignore` evita versionar conteudo privado das pastas reais do vault.
- Arquivos internos de plugins como `.obsidian/`, `.smart-env/`, `.makemd/`,
  `.space/` e `.trash/` devem ser ignorados em buscas recursivas.
- Arquivos `.mdenc` nao devem ser alterados sem pedido explicito.
- Conflitos `sync-conflict` devem ser reportados antes de qualquer resolucao.
- Notas existentes nao devem ser apagadas, movidas, renomeadas ou reorganizadas
  sem confirmacao explicita.

## Como personalizar

- Edite `AGENTS.md` para refletir as regras reais do seu vault.
- Ajuste os templates em `.agents/skills/*/references/`.
- Adicione novas skills em `.agents/skills/` para workflows recorrentes.
- Atualize o mapa do vault sempre que novas areas importantes surgirem.

Ao personalizar, prefira regras especificas, caminhos reais e exemplos curtos.
Isso ajuda o Codex a tomar decisoes melhores sem depender de memoria implicita.

<img width="540" height="530" alt="image" src="https://github.com/user-attachments/assets/798c51f5-2a49-4347-bc01-eadbf7be65f9" />



## Licenca

Este projeto esta licenciado sob a licenca MIT. Veja `LICENSE` para detalhes.
