# AI Ebook Creator

Criador de e-book inteligente com IA.

O usuário envia roteiro/história (texto ou áudio), imagens e outros arquivos.  
A IA organiza a história, estrutura capítulos e gera o e-book.  
No final, sugere plataformas para publicar e vender.

**Repo:** https://github.com/josemar14/ai-ebook-creator

---

## Status atual

✅ Protótipo funcional em HTML  
✅ Upload de texto, áudio, imagens e arquivos  
✅ Detecção automática de capítulos  
✅ Geração e download de **PDF real**  
✅ Sugestões de plataformas de venda  
🚧 Integração com IA real (próxima fase)

---

## Como usar agora

1. Clone o repositório:
   ```bash
   git clone https://github.com/josemar14/ai-ebook-creator.git
   cd ai-ebook-creator
   ```
2. Abra o arquivo `index.html` no navegador (duplo clique ou Live Server).
3. Preencha o título e o roteiro.
4. (Opcional) Adicione áudio e imagens.
5. Clique em **Gerar E-book com IA**.
6. Baixe o PDF.

> Não precisa de servidor nem instalação. Funciona 100% no navegador.

---

## Estrutura do projeto

```
ai-ebook-creator/
├── index.html          ← App principal (protótipo)
├── Celebro.md          ← Memória operacional do projeto
├── AGENTS.md           ← Instruções para agentes de IA
├── ROADMAP.md          ← Fases e prioridades
├── .cursorrules        ← Regras para Cursor
├── docs/
│   └── ai-instructions.md
└── README.md
```

---

## Memória operacional (Celebro)

Este projeto usa o método [Celebro](https://github.com/josemar14/celebro):

- **Celebro.md** → cérebro do projeto (leia sempre no início de sessões longas)
- **ROADMAP.md** → fases e status
- **AGENTS.md** → ponteiro multi-agente

A IA atualiza o Celebro automaticamente quando há decisões de produto.

---

## Roadmap resumido

| Fase | Foco | Status |
|------|------|--------|
| 0 | Fundação | ✅ |
| 1 | Core útil (PDF, detecção, gravação) | 🚧 |
| 2 | Inteligência real (API de IA) | ⏳ |
| 3 | EPUB + publicação | ⏳ |
| 4 | Produto (deploy, login…) | ⏳ |
| 5 | Polimento e escala | ⏳ |

Veja o detalhe em [ROADMAP.md](./ROADMAP.md).

---

## Próximos passos prioritários

1. Gravação de áudio direto no navegador
2. Incluir imagens no PDF
3. Integração com API de IA (Grok / OpenAI / Claude)
4. Exportação EPUB

---

## Licença

A definir.
