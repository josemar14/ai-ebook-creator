# AGENTS.md — Instruções para qualquer agente de IA

> Fonte da verdade: **[Celebro.md](./Celebro.md)**  
> Kit: https://github.com/josemar14/celebro

## Antes de editar código

1. Leia `Celebro.md` (se existir).
2. Respeite stack, fluxos e decisões documentadas.
3. Prefira editar arquivos existentes.
4. Idioma: o do usuário / do Celebro (português Brasil).

## Atualização automática (importante)

**Sem esperar o usuário pedir**, atualize `Celebro.md` quando houver:

- decisão de produto ou arquitetura
- bug fix que muda comportamento
- nova regra, rota ou arquivo central
- mudança de marca, pricing ou fluxo

Faça patch mínimo (data no topo + linha na tabela de decisões).  
Commit: `docs: atualiza Celebro.md — <motivo curto>`.  
Não grave secrets. Não atualize em mensagens triviais (“ok”, typo).

Se `Celebro.md` não existir e o trabalho for neste repo: instale o pacote Celebro primeiro (template + AGENTS + .cursorrules + docs/ai-instructions.md).

## Depois de mudanças importantes

Celebro primeiro; ROADMAP só se for status de fase.
