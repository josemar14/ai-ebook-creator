# Celebro.md — Cérebro do projeto AI Ebook Creator

> Para a IA / dev: leia no início de cada sessão longa.  
> Atualize quando houver decisão de produto, bug fix importante ou mudança de fluxo.  
> Detalhe de fases → `ROADMAP.md`.  
> Kit: https://github.com/josemar14/celebro

**Última atualização:** 2026-08-27  
**Dono:** josemar14  
**Repo:** https://github.com/josemar14/ai-ebook-creator  
**Produção / URL principal:** (ainda não publicado)  

---

## 1. O que é o produto

App web (HTML) de **criação de e-book com IA**.  
O usuário envia roteiro/história (texto ou áudio), imagens e outros arquivos.  
Um agente de IA lê tudo, organiza a história, integra áudio/imagem/texto e gera o e-book completo.  
No final, a IA sugere plataformas para publicar e vender o e-book.

**O que o usuário consegue fazer hoje:**
- Enviar texto, áudio e imagens
- Detectar capítulos automaticamente
- Gerar e baixar PDF real
- Receber sugestões de canais de venda (Amazon KDP, Hotmart, Gumroad etc.)

---

## 2. Stack e arquitetura

| Camada | Tecnologia |
|--------|------------|
| Frontend | HTML + CSS + JavaScript (vanilla) |
| PDF | jsPDF (CDN) |
| IA | Agente de IA (Grok / OpenAI / Claude — a definir) |
| Áudio | Upload + (futuro) MediaRecorder + transcrição via IA |

**Entrypoint:** `index.html`  
**Rotas / módulos principais:** Single Page App (tudo em index.html por enquanto)  

---

## 3. Regras que a IA não pode esquecer

### 3.1 Fluxo do usuário

- Aceitar input em texto **ou** áudio
- Aceitar múltiplas imagens e arquivos
- Organizar história de forma coerente (capítulos, sequência lógica)
- Integrar imagens no lugar certo da narrativa (futuro)
- No final sempre sugerir plataformas de venda
- Gerar PDF baixável

### 3.2 Idioma e experiência

- Interface e respostas em **português (Brasil)** por padrão
- Manter o app simples e focado (HTML primeiro)

---

## 4. Secrets / env (somente nomes)

`OPENAI_API_KEY` · `GROK_API_KEY` · (outros a definir)

---

## 5. Fluxo operacional do usuário

1. Usuário abre o app, define título e envia roteiro (texto ou áudio) + imagens
2. Sistema detecta capítulos e estrutura o conteúdo
3. Usuário revisa a estrutura
4. Baixa o PDF
5. Recebe sugestões de onde publicar e vender

---

## 6. Decisões e bugs recentes

| Tema | Decisão / fix |
|------|----------------|
| Criação do repo | Repo criado em 2026-08-24 com Celebro instalado |
| Nome do projeto | ai-ebook-creator |
| Stack inicial | HTML + vanilla JS + jsPDF |
| Protótipo | index.html com upload + mock de IA |
| PDF real | Geração de PDF funcional no navegador (2026-08-27) |
| Capítulos | Detecção melhorada (regex de capítulo + divisão por tamanho) |
| Organização | ROADMAP.md criado |
| Prioridade atual | Fase 1 — Core útil (gravação de áudio, imagens no PDF) |

---

## 7. Arquivos-chave

| Arquivo | Função |
|---------|--------|
| `Celebro.md` | Memória operacional do projeto |
| `ROADMAP.md` | Fases e prioridades |
| `AGENTS.md` | Instruções multi-agente |
| `.cursorrules` | Regras para Cursor |
| `docs/ai-instructions.md` | Instruções para outros chats |
| `index.html` | Entrypoint do app (protótipo funcional + PDF) |
| `README.md` | Documentação principal |

---

## 8. Ainda opcional / próximo

- Gravação de áudio direto no navegador
- Incluir imagens no PDF
- Integração real com API de IA
- Exportação EPUB
- Definir modelo de IA preferido
- Deploy

---

## 9. Como a IA deve trabalhar neste repo

1. Preferir editar arquivos existentes  
2. Após mudanças de fluxo, atualizar este `Celebro.md`  
3. Não gravar segredos neste arquivo  
4. Responder no idioma do usuário (português)  
5. Consultar `ROADMAP.md` para priorizar tarefas  

---

*Memória operacional do projeto. Mantenha curto, factual e atualizado.*
