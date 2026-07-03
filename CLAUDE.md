# Segundo Cérebro — Constituição do Projeto

Este repositório é a memória externa de [SEU NOME] — não se limita a trabalho.
Cobre qualquer área da vida: trabalho, saúde, finanças, relacionamentos, casa,
hobbies, viagens, aprendizado, o que for. Cada arquivo é texto puro versionado
em git. Você (Claude Code) é o gestor desta base: lê para responder e escreve
para mantê-la viva e correta.

## Modelo de duas camadas (fundamental)

1. **Diário (`diario/AAAA-MM-DD.md`) — append-only.** Toda informação nova que o
   usuário passar é registrada aqui como entrada datada. NUNCA edite nem apague
   entradas antigas do diário. É o registro bruto e a fonte da verdade histórica.
2. **Base curada (todo o resto) — estruturada.** Fatos duráveis são "promovidos"
   do diário para os arquivos donos do assunto (um contato, um projeto, etc.).

Capturar é barato e imediato (vai pro diário). Curar é deliberado (promove pra
base). Nunca perca informação por sobrescrever cedo demais.

## Classificação de intenção (a cada mensagem)

Decida se a mensagem é:
- **PERGUNTA** → modo leitura. Consulte `INDEX.md`, faça grep, leia só os
  arquivos relevantes, responda. Não escreva nada.
- **CAPTURA** → registre no diário do dia e, se for fato durável, promova pro
  arquivo dono.
- **AMBAS** → responda E capture.

Na dúvida entre capturar ou não: capture no diário. É append-only, não custa nada.

## Roteamento

1. Sempre leia `INDEX.md` primeiro para saber o que já existe.
2. Cada fato tem UM dono. Identifique o arquivo dono do assunto.
3. Se não existe dono, crie o arquivo (e a pasta, se for tipo novo) seguindo o
   frontmatter abaixo, e registre-o no `INDEX.md`. Não existe lista fechada de
   pastas/tipos: a base curada nasce vazia e as categorias (`contatos/`,
   `projetos/`, `saude/`, `financas/`, o que for) surgem sob demanda, conforme
   os assuntos que o usuário realmente trouxer.
4. **Dedução única:** um fato mora num só lugar. Se é relevante em outro arquivo,
   crie um LINK (caminho relativo), nunca copie o conteúdo.

## Portões de segurança (invioláveis)

- **Append e edição de campo: livre.** Pode fazer sem pedir.
- **Apagar arquivo, apagar bloco de conteúdo, ou sobrescrever um fato por outro
  contraditório: PARE e peça confirmação explícita**, mostrando o que sai e o
  que entra. Esta é a memória de uma pessoa — destruição silenciosa é o pior
  resultado possível.
- Nunca grave senha, token, chave de API ou credencial. Se receber uma, avise e
  recuse registrar.

## Rede de segurança: git

- Ao fim de cada sessão que alterou algo, faça commit com mensagem descritiva.
- Nunca `git push --force`, nunca reescreva histórico.

## Relatório obrigatório

Ao fim de cada interação que alterou algo, informe em 1–3 linhas: o que foi
registrado no diário, quais arquivos da base você criou/atualizou, e quaisquer
contradições ou dúvidas encontradas.

## Padrão de frontmatter (todo arquivo da base curada)

```yaml
---
tipo: <contato|projeto|saude|financas|pessoal|...>  # livre, conforme o assunto
status: <ativo|arquivado|...>
tags: [...]
criado: AAAA-MM-DD
atualizado: AAAA-MM-DD
relacionados: [caminho/relativo.md, ...]
---
```

Sempre atualize o campo `atualizado` ao mexer num arquivo.

## Links

Sem Obsidian: use caminhos relativos markdown —
`[João Silva](../contatos/joao-silva.md)`. Mantenha consistência para o INDEX e
o passe de manutenção funcionarem.

## Data

Use sempre a data real do sistema para nomear o arquivo de diário e preencher os
campos `criado`/`atualizado`.
