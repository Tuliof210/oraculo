---
description: Força modo captura — registra no diário de hoje e promove fatos duráveis.
argument-hint: <texto a registrar>
---

Modo **CAPTURA** (siga o protocolo em `CLAUDE.md`).

Texto a registrar:

$ARGUMENTS

Passos:

1. Descubra a data real do sistema (`date +%Y-%m-%d`) e abra/crie
   `diario/AAAA-MM-DD.md`. **Append-only:** adicione uma entrada datada com
   este texto. Nunca edite entradas anteriores.
2. Leia `INDEX.md` para saber o que já existe.
3. Para cada fato durável no texto, identifique o arquivo dono (contato,
   projeto, stack, etc.). Se não existe dono, crie o arquivo com o frontmatter
   padrão e registre-o no `INDEX.md`. Atualize o campo `atualizado`.
4. **Dedução única:** um fato mora num só arquivo; em outros, use link relativo.
5. **Portões de segurança:** append e edição de campo são livres. Apagar ou
   sobrescrever um fato por outro contraditório → PARE e peça confirmação,
   mostrando o que sai e o que entra. Nunca grave senhas/tokens/credenciais.
6. Reporte em 1–3 linhas: o que foi pro diário, quais arquivos da base mudaram,
   e contradições/dúvidas.
