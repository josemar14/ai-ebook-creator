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
A IA (quando configurada) estrutura, melhora o texto e gera sinopse.  
Gera PDF completo com capas, capítulos, imagens e sugestões de publicação.

**O que o usuário consegue fazer hoje:**
- Enviar texto, áudio (upload ou gravação) e imagens
- Configurar API Key (OpenAI / Grok / custom) — salva só no navegador
- Gerar e-book com IA real (estrutura + sinopse) ou modo local
- Baixar PDF com imagens e página de “onde vender”

---

## 2. Stack e arquitetura

| Camada | Tecnologia |
|--------|------------|
| Frontend | HTML + CSS + JavaScript (vanilla) |
| PDF | jsPDF (CDN) |
| Áudio | Upload + MediaRecorder |
| IA | OpenAI / xAI Grok / qualquer OpenAI-compatible (via fetch) |

**Entrypoint:** `index.html`  
**Persistência local:** `localStorage` (config de IA)  

---

## 3. Regras que a IA não pode esquecer

### 3.1 Fluxo do usuário

- Aceitar texto e/ou áudio (gravação ou arquivo)
- Aceitar múltiplas imagens
- Se tiver API Key → chamar IA para estruturar + gerar sinopse
- Sem chave ou erro → fallback para detecção local de capítulos
- Sempre gerar PDF baixável com imagens e plataformas de venda
- Nunca gravar API Key no repositório (só localStorage do usuário)

### 3.2 Idioma e experiência

- Interface em **português (Brasil)**
- Manter app simples (HTML primeiro)

---

## 4. Secrets / env (somente nomes)

`OPENAI_API_KEY` · `GROK_API_KEY` / `XAI_API_KEY`  
(As chaves ficam apenas no navegador do usuário via localStorage)

---

## 5. Fluxo operacional do usuário

1. (Opcional) Cola API Key e escolhe provedor/modelo → Salvar
2. Define título + cola roteiro / grava áudio + adiciona imagens
3. Clica em “Gerar E-book com IA”
4. Vê estrutura + sinopse (se IA) + stats
5. Baixa o PDF
6. Vê sugestões de onde publicar

---

## 6. Decisões e bugs recentes

| Tema | Decisão / fix |
|------|----------------|
| Stack | HTML vanilla + jsPDF + MediaRecorder + fetch IA |
| IA | Suporte OpenAI, Grok (xAI) e custom OpenAI-compatible |
| Chave | Só no localStorage do usuário — nunca no repo |
| Fallback | Modo local se não houver chave ou a API falhar |
| CORS | Documentado: chamadas diretas do browser podem ser bloqueadas; backend proxy recomendado depois |
| Fase atual | Fase 2 em andamento (IA real básica pronta) |

---

## 7. Arquivos-chave

| Arquivo | Função |
|---------|--------|
| `Celebro.md` | Memória operacional |
| `ROADMAP.md` | Fases e prioridades |
| `index.html` | App completo |
| `README.md` | Documentação |
| `AGENTS.md` | Multi-agente |

---

## 8. Ainda opcional / próximo

- Transcrição de áudio (Whisper)
- Backend proxy (CORS + segurança da key)
- EPUB
- Deploy

---

## 9. Como a IA deve trabalhar neste repo

1. Preferir editar arquivos existentes  
2. Após mudanças de fluxo, atualizar este `Celebro.md`  
3. Não gravar segredos neste arquivo  
4. Responder no idioma do usuário (português)  
5. Consultar `ROADMAP.md` para priorizar  

---

*Memória operacional do projeto. Mantenha curto, factual e atualizado.*
