# ESA RIO Construtora — Landing Page Premium

Landing page de altíssimo padrão para a **ESA RIO Construtora**, construtora premium do Rio de Janeiro fundada em 2009 pelos diretores **Evandro Amorim** e **André Souza**.

> "Arquitetura que pertence ao Rio." — pedra, céu, mar, luz natural, premium com alma carioca.

---

## 🆕 Atualizações desta versão

### ✅ Correções aplicadas (problemas reportados)
1. **Headline "Construindo o Rio do Futuro."** — não é mais cortada ao carregar.
   - SplitText agora anima por **palavras inteiras** (não por caracteres), preservando quebras naturais.
   - `word-break:keep-all` + `.word{white-space:nowrap}` impedem o corte vertical.
   - `overflow-wrap:break-word` + `padding:0 12px` garantem respiro lateral.
2. **Bolinhas/partículas atrás da logo no hero — REMOVIDAS.**
   - O `<canvas id="hero-canvas">` foi removido do hero.
   - Three.js agora renderiza apenas o **produto 3D estilo Nike** na seção "Por que a ESA RIO?".
3. **Seção CTA "Pronto para encontrar seu próximo lar?" — refeita do zero.**
   - **Removidos:** grid quadriculado animado, dots flutuantes (`cta-dots`), glow pulsante, animações em loop infinito que causavam lag.
   - **Substituído por:** gradient azul profissional + skyline SVG estática + linha de luz horizontal sutil + parallax leve no scroll.
   - Resultado: **performance ~60fps**, visual limpo e profissional.
4. **Marquee de parceiros — não pausa mais no hover.** Animação contínua sem interrupção.
5. **Logos pequenas (FURBAN, SEEDUC, Volta Redonda) — aumentadas.**
   - Cards `.cliente-card` aumentados (`min-height:180px`, `padding:24px 18px`).
   - `max-height` das imagens elevado para `130px` (e `140px` em `.logo-large`).
   - FURBAN, SEEDUC e Volta Redonda receberam classe `.logo-large` para ocupar mais espaço.
6. **Logo NAGA — agora versão fundo branco** (substituiu a versão escura).
7. **Logo Pobre Juan — agora fundo branco com elementos pretos** (gerada via IA).
8. **Badge do hero alterado:** "Construtora Premium · Rio de Janeiro" → **"Construtora · Rio de Janeiro"**.
9. **FLB-AP + PDT adicionadas** ao marquee em **célula dupla** (`.partner-card.partner-double`):
   - FLB-AP à esquerda + PDT à direita, dentro da mesma célula.

### ✨ Novos recursos (avançados)
1. **Lenis Smooth Scroll Engine** — scroll suave nativo (já estava ativo, mantido).
2. **Parallax no background** — hero, about-image, emp-card-img e portfolio-card com parallax via GSAP ScrollTrigger.
3. **WebGL / Three.js — Produto 3D interativo** (estilo Nike):
   - Torre/edifício 3D representando obras ESA RIO (cubo azul + topo branco metálico + base preta + anel de luz cyan).
   - Posicionado no canto superior direito da seção "Por que a ESA RIO?".
   - Renderização **sob demanda** (apenas quando visível) via `IntersectionObserver`.
   - Escondido em mobile/tablet (`<1024px`) para preservar performance.
4. **Reveal de produto 3D ao scroll (estilo Nike)** — `ScrollTrigger.onUpdate` controla escala, rotação X/Y e opacidade conforme o usuário rola pela seção de diferenciais.
5. **Split-text em headlines animadas** — todos os `<h2>` (exceto hero) animam palavra a palavra com stagger.
6. **Seções com scroll horizontal** — `.portfolio-scroll` mantém scroll horizontal nativo com snap.
7. **Meta Pixel + Google Ads** — tags configuradas no `<head>` (substituir `fb-pixel-id` e `AW-XXXXXX` pelos IDs reais).
8. **Botões com setas animadas** — `.about-link`, `.conhecer`, `Ver Todos os Empreendimentos`, `Ver Portfólio Completo` ganharam transição de `gap` e mudança de cor no hover.

---

## 🎯 Funcionalidades atuais

### Páginas / Rotas
- `/` (`index.html`) — Landing page única com 12 seções.

### Seções implementadas
1. **Loader** — barra de progresso + logo ESA RIO em caixa branca com glow ciano sutil.
2. **Navbar** — fixed, transparente que escurece no scroll, logo em caixa branca compacta.
3. **Hero** — slideshow Ken Burns + headline com split-text por palavras + parallax suave.
4. **Credenciais** — 4 contadores animados (16+ anos, 80+ obras, 5000+ clientes, 100% prazo).
5. **Sobre** — grid 2 colunas com parallax no retrato dos diretores.
6. **Empreendimentos** — grid 3x2 com filtros (Todos / Lançamento / Em Obras / Entregues) + parallax nas imagens.
7. **Diferenciais** — grid 3x2 + **produto 3D Three.js** (Nike-style, scroll reveal).
8. **Portfólio** — scroll horizontal com snap (5 obras públicas).
9. **Parceiros** — marquee infinito (NAGA, Reserva, Selfit, Pobre Juan + célula dupla FLB-AP/PDT).
10. **Depoimentos** — carrossel com autoplay (3 slides).
11. **Clientes** — grid 4 colunas (FURBAN, SEEDUC, Paraíba do Sul, Volta Redonda).
12. **CTA Central** — gradiente azul + skyline SVG + parallax leve.
13. **Contato** — formulário (Mailchimp-ready) + cards de contato (WhatsApp, e-mail, telefone, endereço).
14. **Footer** — logo em caixa branca + 4 colunas + redes sociais + bottom legal.
15. **Cookie consent** (LGPD/GDPR).

---

## 🛣️ URIs funcionais

| Caminho/Hash | Destino |
|---|---|
| `index.html#hero` | Início |
| `index.html#sobre` | Seção Sobre |
| `index.html#empreendimentos` | Empreendimentos |
| `index.html#diferenciais` | Diferenciais (com 3D) |
| `index.html#portfolio` | Portfólio (scroll horizontal) |
| `index.html#parceiros` | Parceiros (marquee) |
| `index.html#depoimentos` | Depoimentos |
| `index.html#clientes` | Clientes |
| `index.html#cta` | CTA Central |
| `index.html#contato` | Formulário de contato |

### Filtros (parâmetros via JS, não querystring)
- Botões `.filter-tab` com `data-filter="all|lancamento|obras|entregue"` filtram cards `.emp-card[data-status]`.

### Eventos GTM/GA disparados (`dataLayer.push`)
- `page_view`, `hero_view`, `cta_click`, `whatsapp_click`, `form_submit`, `cookie_consent`.

---

## 🎨 Design System

| Token | Valor |
|---|---|
| `--color-black` | `#0D0D0D` |
| `--color-blue` | `#1B4FD8` |
| `--color-blue-dark` | `#1340B0` |
| `--color-blue-light` | `#E6EFFF` |
| `--color-gold` | `#F0B429` |
| `--font-serif` | Playfair Display |
| `--font-sans` | DM Sans |
| `--container` | `1280px` |
| `--pad-y` | `120px` (desktop) / `80px` (tablet) / `64px` (mobile) |

### Breakpoints
- **Mobile:** `< 640px` — coluna única, botões 100%, logos menores.
- **Tablet:** `640–1024px` — 2 colunas, padding reduzido.
- **Desktop:** `> 1024px` — layout completo + produto 3D visível.

---

## 📂 Estrutura de arquivos

```
/
├── index.html                  Landing page única (HTML+CSS+JS inline)
├── README.md                   Este arquivo
└── images/
    ├── logo-esa-rio.png        Logo principal ESA RIO (com fundo branco)
    ├── logo-naga.png           NAGA — fundo branco
    ├── logo-reserva.png        Reserva
    ├── logo-selfit.png         Selfit Academia
    ├── logo-pobrejuan.png      Pobre Juan — fundo branco, logo preta
    ├── logo-flb-ap.png         FLB-AP (célula dupla)
    ├── logo-pdt.png            PDT (célula dupla)
    ├── logo-furban.png         FURBAN — Volta Redonda
    ├── logo-seeduc.png         SEEDUC RJ
    ├── logo-paraibadosul.png   Prefeitura Paraíba do Sul
    └── logo-voltaredonda.png   Prefeitura Volta Redonda
```

---

## 🛠️ Stack técnica

- **HTML5 semântico** — `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`.
- **CSS3** — variáveis, grid, flexbox, custom properties, `clamp()`, prefers-reduced-motion.
- **JavaScript ES6+** — vanilla, sem build step.
- **Bibliotecas (CDN jsDelivr):**
  - **GSAP 3.12.5** + ScrollTrigger — animações performáticas.
  - **Three.js r128** — produto 3D estilo Nike.
  - **Lenis 1.0.42** — smooth scroll engine.
- **Tracking:** Google Tag Manager + Meta Pixel + Google Ads gtag.

---

## ♿ Acessibilidade (WCAG AA)

- Skip-link "Pular para o conteúdo".
- HTML semântico (header/main/section/article/footer).
- `alt` em todas as imagens.
- `aria-label`, `aria-current`, `aria-expanded`, `aria-selected` em interativos.
- Foco visível, navegação por teclado funcional (Esc fecha menu mobile).
- `prefers-reduced-motion: reduce` desativa animações pesadas.
- Botões com área de toque ≥ 44px.
- Contraste mínimo WCAG AA respeitado.

---

## ⚡ Performance

- **Sem dependências externas** além de CDNs (jsDelivr).
- **CSS inline** em `<style>` (zero RTT extra).
- **Imagens com `loading="lazy"`** em todas as logos e cards.
- **Three.js renderiza sob demanda** (apenas quando produto 3D visível).
- **Removidas animações infinitas pesadas** (cta-grid, cta-dots, cta-glow).
- Marquee usa `transform:translateX` (GPU-accelerated).

---

## 🚧 Não implementado / próximos passos

1. **IDs reais de tracking** — substituir `GTM-XXXXXXX`, `fb-pixel-id`, `AW-XXXXXX` pelos IDs reais.
2. **Action Mailchimp** — substituir `#mailchimp-action-placeholder` pela URL real.
3. **Dados reais de empreendimentos** — substituir imagens stock do Pexels por fotos oficiais ESA RIO.
4. **Página interna por empreendimento** — atualmente todos os "Conhecer →" levam ao formulário de contato.
5. **Política de privacidade** — link `<a href="#">` no banner de cookies precisa apontar para página real.
6. **Integração WhatsApp Business** — número (21) 99351-1000 funcional, mas pode integrar com chat widget.
7. **CMS/Headless** — para a equipe ESA RIO publicar novos empreendimentos sem dev.
8. **Open Graph / Cover real** — substituir `og-cover.jpg` placeholder.

---

## 🚀 Deploy

Para publicar o site, vá até a aba **Publish** do projeto — o deploy é feito com um clique.

---

## 📞 Contatos ESA RIO Construtora

- **WhatsApp:** (21) 99351-1000
- **Evandro Amorim (Diretor):** (24) 98142-3825
- **André Souza (Diretor):** (21) 97693-7843
- **E-mail:** construtora.esario@gmail.com
- **Endereço:** Av. Dr. Randolfo Pena, 1118 — Jatobá — Paraíba do Sul/RJ — CEP 25850-000
- **Filial:** Nova Iguaçu/RJ
- **Instagram:** [@construtoraesa](https://instagram.com/construtoraesa)

---

© 2025 ESA RIO Construtora — Construído com ♥ no Rio de Janeiro.
