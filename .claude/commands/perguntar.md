---
description: Força modo leitura — consulta a base e responde sem escrever nada.
argument-hint: <sua dúvida>
---

Modo **LEITURA** (siga o protocolo em `CLAUDE.md`). **Não escreva nada na base.**

Dúvida:

$ARGUMENTS

Passos:

1. Leia `INDEX.md` para localizar os arquivos relevantes.
2. Faça `grep`/`glob` pelos termos da dúvida e leia só os arquivos que importam.
3. Responda de forma direta, citando os arquivos-fonte (caminho relativo).
4. Se encontrar uma contradição ou lacuna na base, aponte na resposta — mas não
   corrija nem grave nada agora (isto é modo leitura). Se o usuário quiser
   registrar algo, ele usa `/anotar`.
