---
description: Fecha o dia — promove para a base curada tudo que for durável no diário de hoje.
---

Fechamento do dia (siga o protocolo em `CLAUDE.md`).

Passos:

1. Descubra a data real do sistema (`date +%Y-%m-%d`) e leia
   `diario/AAAA-MM-DD.md` inteiro.
2. Leia `INDEX.md` para saber quais arquivos donos já existem.
3. Para cada fato durável ainda **não promovido**, leve-o ao arquivo dono
   (contato, projeto, stack, etc.), criando o arquivo + registro no `INDEX.md`
   quando faltar dono. Atualize o campo `atualizado`.
4. **Dedução única:** não copie entre arquivos — use links relativos. O diário
   permanece intacto (append-only); promover não apaga nada dele.
5. **Portões de segurança:** sobrescrever fato contraditório ou apagar → PARE e
   confirme com o usuário, mostrando o que sai e o que entra.
6. Liste o que foi promovido (fato → arquivo dono) e o que ficou de fora e por
   quê.
