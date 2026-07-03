# Segundo Cérebro

Memória externa pessoal — cobre qualquer área da vida (trabalho, saúde, finanças,
relacionamentos, hobbies, o que surgir), não só trabalho. 100% arquivos markdown
versionados em git.
Sem banco de dados, sem embeddings, sem RAG. A base é lida sob demanda com
`grep`/`glob`/`read`.

## Como usar

Abra esta pasta no Claude Code e **converse em linguagem natural**. Cada mensagem
pode ser uma pergunta (o Claude lê a base e responde), uma captura (registra a
informação) ou ambas. O Claude é o gestor: decide qual arquivo é dono de cada
fato, o que atualizar e quando criar arquivo/pasta nova. O protocolo completo
está em [CLAUDE.md](CLAUDE.md).

Ou use os slash commands:

- `/anotar <texto>` — força captura: registra no diário e promove fatos duráveis.
- `/perguntar <dúvida>` — força leitura: responde sem escrever na base.
- `/diario` — fecha o dia: promove para a base tudo que for durável.
- `/revisar` — dispara o subagente curador para auditar a base.
- `/indexar` — regenera o `INDEX.md`.

## Estrutura

- `diario/` — registro bruto, append-only (1 arquivo por dia).
- `contatos/`, `projetos/`, `stack/`, `protocolos/`, `tarefas/`, `kpis/` — base
  curada (1 arquivo por coisa com ciclo de vida próprio).
- `glossario.md` — siglas e termos (arquivo único de consulta).
- `INDEX.md` — catálogo de todos os arquivos (regenerável via `/indexar`).

Git é a rede de segurança: cada sessão que altera algo termina em commit.
