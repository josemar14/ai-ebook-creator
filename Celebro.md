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
- Enviar texto, áudio (upload ou gravação) e imagens
- Detectar capítulos automaticamente
- Ver preview rico (nº de capítulos, palavras, imagens)
- Gerar e baixar PDF real **com imagens incluídas**
- Receber sugestões de canais de venda

---

## 2. Stack e arquitetura

| Camada | Tecnologia |
|--------|------------|
| Frontend | HTML + CSS + JavaScript (vanilla) |
| PDF | jsPDF (CDN) |
| Áudio | Upload + MediaRecorder (gravação no navegador) |
| IA | Agente de IA (Grok / OpenAI / Claude — a definir) |

**Entrypoint:** `index.html`  
**Rotas / módulos principais:** Single Page App (tudo em index.html por enquanto)  

---

## 3. Regras que a IA não pode esquecer

### 3.1 Fluxo do usuário

- Aceitar input em texto **ou** áudio (upload ou gravação)
- Aceitar múltiplas imagens e arquivos
- Organizar história de forma coerente (capítulos)
- Incluir imagens no PDF
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

1. Usuário define título e envia roteiro (texto ou grava/áudio) + imagens
2. Sistema detecta capítulos e mostra preview com estatísticas
3. Usuário revisa a estrutura
4. Baixa o PDF (com imagens e página de publicação)
5. Recebe sugestões de onde publicar e vender

---

## 6. Decisões e bugs recentes

| Tema | Decisão / fix |
|------|----------------|
| Criação do repo | 2026-08-24 |
| Stack | HTML + vanilla JS + jsPDF + MediaRecorder |
| PDF real | Funcional com capa + capítulos + imagens + plataformas |
| Gravação de áudio | MediaRecorder implementado (2026-08-27) |
| Imagens no PDF | Incluídas em páginas dedicadas |
| Preview | Stats (capítulos, palavras, imagens) |
| Fase atual | Fase 1 quase completa → próxima = Fase 2 (IA real) |

---

## 7. Arquivos-chave

| Arquivo | Função |
|---------|--------|
| `Celebro.md` | Memória operacional |
| `ROADMAP.md` | Fases e prioridades |
| `AGENTS.md` | Instruções multi-agente |
| `.cursorrules` | Regras para Cursor |
| `docs/ai-instructions.md` | Instruções para outros chats |
| `index.html` | App completo (protótipo avançado) |
| `README.md` | Documentação principal |

---

## 8. Ainda opcional / próximo

- Melhorar estilos de capa do PDF (polish)
- **Fase 2:** Integração real com API de IA
- Transcrição de áudio
- Exportação EPUB
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
