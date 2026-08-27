# ROADMAP — AI Ebook Creator

Última atualização: 2026-08-27

---

## Fase 0 — Fundação ✅

- [x] Repositório + Celebro + README
- [x] Protótipo HTML (upload texto/áudio/imagens)
- [x] Detecção de capítulos + PDF + plataformas

---

## Fase 1 — Core útil ✅

- [x] Título do e-book
- [x] Detecção inteligente de capítulos
- [x] PDF funcional
- [x] Gravação de áudio (MediaRecorder)
- [x] Imagens no PDF
- [x] Preview rico (stats)

---

## Fase 2 — Inteligência real ✅ (quase completa)

- [x] Integração OpenAI / Grok / custom
- [x] API Key no localStorage
- [x] Estruturação e melhoria de capítulos pela IA
- [x] Sinopse automática
- [x] Fallback modo local
- [x] Transcrição de áudio (Whisper) — botão + auto se só áudio
- [x] Texto de vendas / blurb
- [ ] Reescrita/expansão mais profunda por capítulo (polish)
- [ ] Posicionamento inteligente de imagens na narrativa

---

## Fase 3 — Formatos e publicação ⏳ (próxima)

- [ ] Exportar EPUB
- [ ] Template de capa editável
- [ ] Metadados (autor, etc.)
- [ ] Checklist de publicação por plataforma

---

## Fase 4 — Produto

- [ ] Backend proxy (CORS + segurança da key)
- [ ] Login / histórico
- [ ] Deploy

---

## Fase 5 — Polimento

- [ ] Temas, i18n, templates de gênero, monetização

---

## Notas técnicas

- Whisper exige provedor OpenAI (ou compatible com `/audio/transcriptions`)
- Chamadas do browser podem falhar por CORS → backend proxy recomendado na Fase 4

*Atualize sempre que houver avanço real.*
