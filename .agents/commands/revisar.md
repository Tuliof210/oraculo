---
description: Dispara o subagente curador para auditar a base (contradições, duplicatas, órfãos, obsoletos).
---

Acione o subagente **curador** (via Agent tool, `subagent_type: curador`) para um
passe de manutenção sobre toda a base curada.

O curador deve apenas **relatar e propor** — nunca apagar nem sobrescrever por
conta própria. Peça a ele um relatório com:

- Contradições (mesmo fato divergindo entre arquivos).
- Duplicatas (conteúdo copiado que deveria ser link — viola a dedução única).
- Arquivos órfãos (ninguém referencia) e links quebrados.
- Itens obsoletos (tarefas concluídas há muito, `status` velho, `atualizado` antigo).

Ao receber o relatório, apresente-o ao usuário. Qualquer ação destrutiva sugerida
passa pelos **portões de segurança**: só execute após confirmação explícita,
mostrando o que sai e o que entra.
