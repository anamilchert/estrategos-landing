# SDD – Spec-Driven Development
## Landing Page: eStrategoS B2B Sales Consulting

> Aplicado com Google Antigravity + AI for Code  
> Metodologia: Spec-Driven Development (SDD) via spec-kit  
> Ferramenta de prototipagem: Google Stitch (stitch.withgoogle.com)

---

## FASE 1 — CONSTITUTION (`/01-speckit.constitution`)

Princípios não-negociáveis do projeto, que o agente Antigravity valida em cada fase:

```
TECH STACK:
- HTML5 semântico + CSS3 (sem frameworks externos)
- JavaScript vanilla apenas para interações essenciais
- Sem jQuery, sem Bootstrap
- Responsivo: mobile-first, breakpoint principal em 768px

IDENTIDADE VISUAL:
- Cor primária: #F97316 (laranja eStrategoS)
- Background principal: #0A0A0A (quase preto)
- Tipografia display: Inter Bold / 700
- Tipografia corpo: Inter Regular / 400
- Border-radius padrão: 8px

CONTEÚDO:
- Idioma: Português brasileiro
- Tom: direto, orientado a resultado, sem jargão genérico
- Foco da página: conversão — levar o visitante ao CTA

PROIBIÇÕES:
- Não usar stock photos genéricas
- Não usar gradientes de múltiplas cores (apenas orange→transparent)
- Não usar animações que não sirvam à conversão
```

---

## FASE 2 — SPECIFICATION (`/02-speckit.specify`)

### Contexto do Produto
**Nome:** eStrategoS  
**Segmento:** Consultoria B2B em estruturação comercial  
**Proposta de valor central:** Escalar receita sem escalar headcount  
**Público-alvo (ICP):** Diretores e CEOs de empresas B2B com time comercial de 2–10 pessoas, faturamento entre R$1M–R$30M/ano, em busca de previsibilidade de pipeline

### Objetivo da Landing Page
Página única de conversão com objetivo de capturar leads qualificados via formulário de diagnóstico gratuito.

### Seções Obrigatórias

| # | Seção | Objetivo |
|---|-------|----------|
| 1 | Hero | Comunicar proposta de valor + CTA principal |
| 2 | Problema | Validar a dor do ICP |
| 3 | Solução (3 pilares) | Mostrar diferencial metodológico |
| 4 | Prova social | Credibilidade via depoimentos |
| 5 | Serviços | Clareza sobre o que é entregue |
| 6 | CTA final | Segunda chance de conversão |
| 7 | Footer | Dados de contato e navegação |

### Critérios de Aceite
- [ ] CTA principal visível sem scroll no desktop (above the fold)
- [ ] Carrega em menos de 2s (sem dependências externas)
- [ ] Legível em mobile (320px mínimo)
- [ ] Contraste AA para todos os textos
- [ ] Formulário com validação de campos obrigatórios

---

## FASE 3 — CLARIFY (`/03-speckit.clarify`)

Ambiguidades identificadas e resolvidas antes de gerar o plano:

**Q: O formulário deve integrar com algum CRM?**  
A: Não nesta versão (MVP). Formulário estático com `mailto:` ou placeholder de integração.

**Q: Quantos depoimentos na seção de prova social?**  
A: 3 depoimentos, com nome, cargo e empresa fictícios para o protótipo.

**Q: Existe logo da marca?**  
A: Usar logotipo tipográfico: "e**S**" em laranja + "strategoS" em branco.

**Q: Menu de navegação com quantos itens?**  
A: 4 itens: Início, Metodologia, Depoimentos, Contato. Sem página extra (scroll interno).

---

## FASE 4 — IMPLEMENTATION PLAN (`/04-speckit.plan`)

```
ESTRUTURA DE ARQUIVOS:
├── index.html        ← página principal
├── SDD.md            ← este documento
└── (assets embutidos em CSS inline ou via CDN Google Fonts)

ORDEM DE IMPLEMENTAÇÃO:
1. Reset CSS + tokens de design (variáveis CSS)
2. Header + nav fixa com scroll behavior
3. Seção Hero (headline, subtítulo, CTA)
4. Seção Problema (3 pain points em cards)
5. Seção Solução (3 pilares metodológicos)
6. Seção Depoimentos (3 cards com avatar placeholder)
7. Seção Serviços (2 tiers de serviço)
8. CTA Final + formulário
9. Footer
10. Media queries mobile
11. Micro-interações (hover nos botões, smooth scroll)
```

---

## FASE 5 — PROTÓTIPO (Google Stitch)

**Prompt utilizado no Google Stitch (Experimental Mode / Gemini 2.5 Pro):**

> "Create a high-fidelity landing page for a B2B sales consulting company called eStrategoS. Use a dark background (#0A0A0A) with bold orange (#F97316) as the primary accent color. Include: a hero section with headline 'Scale Your Revenue Without Scaling Your Team', a subtitle, and a CTA button 'Book a Free Diagnosis'; a section with 3 value proposition cards (Pipeline Structuring, ICP Definition, Sales Cadence); a social proof section with 3 client testimonials; a pricing section with 2 service tiers; and a footer. Typography: Inter Bold for headings. Style: clean, corporate, conversion-focused."

**Telas geradas no Stitch:**
- Screen 1: Hero + Nav
- Screen 2: Problema + Solução
- Screen 3: Depoimentos
- Screen 4: Serviços + CTA Final
- Screen 5: Footer

**Exportação:** HTML/CSS → implementado em `index.html`

---

## RASTREABILIDADE SDD

| Artifact | Status |
|----------|--------|
| Constitution | ✅ Definida |
| Specification | ✅ Documentada |
| Clarify | ✅ Ambiguidades resolvidas |
| Plan | ✅ Aprovado antes do código |
| Prototype (Stitch) | ✅ Alta fidelidade gerado |
| Implementation | ✅ `index.html` entregue |
| Validation | ✅ Critérios de aceite verificados |

---

*Gerado com método SDD aplicado via Google Antigravity + Google Stitch*
