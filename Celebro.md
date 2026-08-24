# Celebro.md — Cérebro do projeto AI Ebook Creator

> Para a IA / dev: leia no início de cada sessão longa.  
> Atualize quando houver decisão de produto, bug fix importante ou mudança de fluxo.  
> Detalhe de fases → `ROADMAP.md` (se existir).  
> Kit: https://github.com/josemar14/celebro

**Última atualização:** 2026-08-24  
**Dono:** josemar14  
**Repo:** https://github.com/josemar14/ai-ebook-creator  
**Produção / URL principal:** (ainda não publicado)  

---

## 1. O que é o produto

App web (HTML) de **criação de e-book com IA**.  
O usuário envia roteiro/história (texto ou áudio), imagens e outros arquivos.  
Um agente de IA lê tudo, organiza a história, integra áudio/imagem/texto e gera o e-book completo.  
No final, a IA sugere plataformas para publicar e vender o e-book.

**O que o usuário consegue fazer:**
- Enviar texto, áudio e imagens
- Deixar a IA estruturar capítulos e gerar o conteúdo
- Baixar o e-book (PDF/EPUB)
- Receber sugestões de canais de venda (Amazon KDP, Hotmart, Gumroad etc.)

---

## 2. Stack e arquitetura

| Camada | Tecnologia |
|--------|------------|
| Frontend | HTML + CSS + JavaScript (vanilla ou leve framework) |
| IA | Agente de IA (Grok / OpenAI / Claude — a definir) |
| Geração de e-book | PDF / EPUB (bibliotecas JS ou backend) |
| Áudio | Transcrição via IA |

**Entrypoint:** `index.html` (planejado)  
**Rotas / módulos principais:** (ainda em definição)  

---

## 3. Regras que a IA não pode esquecer

### 3.1 Fluxo do usuário

- Aceitar input em texto **ou** áudio
- Aceitar múltiplas imagens e arquivos
- Organizar história de forma coerente (capítulos, sequência lógica)
- Integrar imagens no lugar certo da narrativa
- No final sempre sugerir plataformas de venda

### 3.2 Idioma e experiência

- Interface e respostas em **português (Brasil)** por padrão
- Manter o app simples e focado (HTML primeiro)

---

## 4. Secrets / env (somente nomes)

`OPENAI_API_KEY` · `GROK_API_KEY` · (outros a definir)

---

## 5. Fluxo operacional do usuário

1. Usuário abre o app e envia roteiro (texto ou áudio) + imagens + arquivos
2. Agente IA processa, transcreve áudio se necessário, organiza a história
3. IA gera o e-book estruturado (capítulos + imagens)
4. Usuário revisa / baixa o e-book
5. IA sugere onde publicar e vender

---

## 6. Decisões e bugs recentes

| Tema | Decisão / fix |
|------|----------------|
| Criação do repo | Repo criado em 2026-08-24 com Celebro instalado |
| Nome do projeto | ai-ebook-creator |
| Stack inicial | HTML + IA (detalhes a definir) |

---

## 7. Arquivos-chave

| Arquivo | Função |
|---------|--------|
| `Celebro.md` | Memória operacional do projeto |
| `AGENTS.md` | Instruções multi-agente |
| `.cursorrules` | Regras para Cursor |
| `docs/ai-instructions.md` | Instruções para outros chats |
| `index.html` | (planejado) Entrypoint do app |

---

## 8. Ainda opcional

- Definir modelo de IA preferido
- Escolher formato final prioritário (PDF, EPUB ou ambos)
- Decidir se terá backend ou só front-end + APIs
- Login de usuários / histórico de e-books

---

## 9. Como a IA deve trabalhar neste repo

1. Preferir editar arquivos existentes  
2. Após mudanças de fluxo, atualizar este `Celebro.md`  
3. Não gravar segredos neste arquivo  
4. Responder no idioma do usuário (português)  

---

*Memória operacional do projeto. Mantenha curto, factual e atualizado.*
