# Lúmina Habitat — Experiência Institucional Conceitual para Engenharia

Landing page institucional fictícia criada como estudo de **design, conteúdo e desenvolvimento front-end** para o setor de engenharia, arquitetura e construção.

> **Aviso:** Lúmina Habitat não é uma empresa real. Marca, projetos, métricas e mensagens foram criados exclusivamente para demonstração em portfólio. O formulário não transmite nem armazena dados.

## Visão do projeto

O projeto moderniza uma landing page legada sem abandonar sua estrutura original. A evolução concentrou-se em remover informações empresariais reais, organizar a narrativa, renovar a identidade visual, reduzir integrações desnecessárias e tornar a experiência mais consistente em desktop, tablet e mobile.

### Principais melhorias

- identidade fictícia original **Lúmina Habitat**;
- conteúdo inteiramente conceitual, sem nomes, contatos ou resultados empresariais reais;
- hierarquia visual e microcopy revisadas;
- imagens locais com licenças abertas, sem hotlink de bancos de imagem;
- formulário demonstrativo transparente, com validação no navegador e sem coleta de dados;
- remoção de pixels, tags de anúncios, mapa, mensageiro flutuante, links sociais vazios e placeholders de produção;
- navegação responsiva com menu mobile e estados de foco visíveis;
- suporte a `prefers-reduced-motion`;
- animações mais leves em dispositivos móveis;
- loader reduzido para não bloquear a experiência;
- favicon, metadados SEO e Open Graph atualizados.

## Seções

1. Hero com slideshow arquitetônico e chamadas principais
2. Indicadores do conceito
3. Apresentação da marca fictícia
4. Projetos conceituais com filtros
5. Princípios e diferenciais
6. Serviços
7. Estudos visuais em scroll horizontal
8. Ecossistema de disciplinas
9. Diretrizes de experiência em carrossel
10. Setores e escalas de atuação
11. CTA institucional
12. Formulário demonstrativo
13. Footer com aviso de projeto fictício

## Stack e tecnologias

| Tecnologia | Uso no projeto |
| --- | --- |
| **HTML5** | Estrutura semântica e conteúdo da página |
| **CSS3** | Design system, Grid, Flexbox, `clamp()`, media queries e estados responsivos |
| **JavaScript ES6+** | Navegação, filtros, carrossel, validação e interações |
| **GSAP 3 + ScrollTrigger** | Revelações, parallax e animações vinculadas ao scroll |
| **Three.js** | Objeto arquitetônico 3D na seção de diferenciais |
| **Lenis** | Rolagem suave apenas em desktop compatível |
| **Google Fonts** | Playfair Display e DM Sans |
| **SVG** | Identidade visual, favicon, ícones e skyline |

Não há framework, bundler ou etapa de build. A aplicação é estática e pode ser servida diretamente por qualquer servidor HTTP.

## Design system

- **Azul principal:** `#2864FF`
- **Azul profundo:** `#1646C8`
- **Navy:** `#07111E`
- **Menta de destaque:** `#90F3DF`
- **Fundo claro:** `#F6F7FA`
- **Tipografia de títulos:** Playfair Display
- **Tipografia de interface:** DM Sans
- **Container máximo:** `1280px`

### Breakpoints principais

- **Desktop:** acima de `1024px`
- **Tablet:** até `1024px`
- **Mobile:** até `640px`
- **Mobile compacto:** até `390px`

## Recursos de acessibilidade

- skip link para o conteúdo principal;
- landmarks semânticos (`header`, `main`, `section`, `article`, `aside`, `footer`);
- labels associados aos campos de formulário;
- feedback do formulário com `role="status"` e `aria-live`;
- menu mobile com `aria-expanded` e fechamento pela tecla `Esc`;
- estados de foco com alto contraste;
- áreas de toque mínimas em controles;
- suporte à preferência de movimento reduzido;
- contraste e hierarquia orientados às recomendações WCAG 2.2 AA.

## Como executar localmente

```bash
python3 -m http.server 4173
```

Acesse `http://localhost:4173`.

Também é possível usar a extensão Live Server ou qualquer servidor estático equivalente.

## Estrutura

```text
.
├── index.html
├── README.md
└── images/
    ├── architecture-01.webp ... architecture-06.webp
    ├── architecture-08.webp
    ├── favicon.svg
    └── logo-lumina-habitat.svg
```

## Comportamento do formulário

O formulário valida nome, telefone e e-mail apenas no cliente. O envio é interceptado por JavaScript e exibe uma confirmação demonstrativa. Nenhum endpoint externo é chamado e nenhum dado é persistido.

## Créditos das imagens

As fotografias arquitetônicas foram encontradas por pesquisa com filtro de licença Creative Commons/Public Domain e armazenadas localmente para evitar hotlink. Consulte as páginas de origem para autoria e termos completos:

- [Fundação Iberê Camargo — Gustavo.kunst, CC BY-SA 3.0 / GFDL](https://commons.wikimedia.org/wiki/File:Fundacao-Ibere-Camargo01.jpg)
- [CCBB Brasília](https://commons.wikimedia.org/wiki/File:CCBB_-_BSB_(8197422842).jpg)
- [Auditório Ibirapuera](https://commons.wikimedia.org/wiki/File:Audit%C3%B3rio_Ibirapuera_Parque_do_Ibirapuera_S%C3%A3o_Paulo_2019-6180.jpg)
- [FAU-USP — Fernando Stankuns](https://commons.wikimedia.org/wiki/File:Fau_usp.jpg)
- [FAU-USP, imagem 04 — Mike Peel](https://commons.wikimedia.org/wiki/File:Architecture_and_Urbanism_College_of_University_of_S%C3%A3o_Paulo_2016_04.jpg)
- [FAU-USP, imagem 01 — Mike Peel, CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Architecture_and_Urbanism_College_of_University_of_S%C3%A3o_Paulo_2016_01.jpg)
- [Edifício J23-A — HVL, CC BY 4.0](https://commons.wikimedia.org/wiki/File:Vista_do_Edif%C3%ADcio_J23-A_no_B._Cariru,_Ipatinga_MG.JPG)

As imagens são usadas como referências visuais em um estudo fictício; não representam projetos da marca conceitual.

## Licença do código

Este repositório é destinado à apresentação em portfólio. As fotografias mantêm as licenças indicadas por seus autores nas páginas de origem.
