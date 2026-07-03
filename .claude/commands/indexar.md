---
description: Regenera o INDEX.md varrendo todos os arquivos e extraindo uma linha de cada.
---

Regenere o `INDEX.md` do zero.

Passos:

1. Varra todos os arquivos `.md` do repositório, **exceto** `INDEX.md`,
   `README.md`, `CLAUDE.md`, o próprio `diario/` e a pasta `.claude/`.
   (Use `glob`/`grep` no frontmatter.)
2. Para cada arquivo, extraia: caminho relativo, `tipo` (do frontmatter) e uma
   descrição de uma linha (do título `#` ou do frontmatter).
3. Escreva o `INDEX.md` com o cabeçalho e uma tabela `arquivo | tipo | descrição`,
   uma linha por arquivo, ordenada por caminho. Mantenha a nota de que é
   regenerável via `/indexar`.
4. Reporte quantos arquivos foram catalogados.
