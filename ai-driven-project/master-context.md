# Master Context: RPK Beauty Clinic

## Projeto
Site Institucional e Landing Pages da Dra. Larissa Rapack (Biomédica Esteta).

## Tecnologias
- **Framework:** Next.js (App Router)
- **Estilização:** Tailwind CSS v4
- **Animações:**## Status do Projeto
- **Interface Front-end:** `index.html` (Vanilla JS + Tailwind CSS v4 CDN + Framer-like animations).
- **Design System:** Cores institucionais (#778cc2, #786659, Branco, Off-White), linhas finas, formas orgânicas SVG.
- **Componentes Chave:**
  - Header responsivo com navegação fluida.
  - Hero Section com foto sem fundo da Dra. Larissa Rapack e CTA em destaque.
  - Comparador de Resultados ("Antes e Depois") com interatividade touch/mouse, efeito mágico de borboletas azuis (#778cc2) e poeira estelar cintilante (*Magic Particle System*).
  - Galeria Mobile para a seção "Antes e Depois" com transição por scroll-snap, animação JS suave personalizada (easing Bezier) e navegação por setas ("Ver mais" / "Procedimentos" / "Voltar").
  - Dock Flutuante Mobile com efeito **Liquid Glass (Glassmorphism de alto padrão)** e abas deslizantes interativas.
  - Carrossel de Protocolos/Tratamentos com molduras orgânicas e ilustrações fine-line em SVG exclusivas.
  - Sobre a Especialista e Rodapé institucional.

- 04/09/2026: Atualização e padronização rigorosa do NAP Oficial em todo o site (`index.html`, páginas de serviços nível 2, `llms.txt` e schemas JSON-LD):
  - **Nome**: Dra. Larissa Rapack | Biomédica Esteta
  - **Endereço**: Edifício Fronteira - Av. Getúlio Vargas, 227 - Sl 19 - Centro, Araranguá - SC, CEP 88900-973
  - **Telefone / WhatsApp**: (48) 99961-6804 (`https://wa.me/5548999616804`)

- 13/09/2026: Implementação do **Silo SEO Hiperlocal (Método Farol) - Nível 3 (Bairro: Centro)**:
  - Criadas 5 novas páginas (`index-centro.html`, `harmonizacao-facial-centro.html`, `preenchimento-labial-centro.html`, `harmonizacao-corporal-centro.html`, `protocolo-bigode-chines-centro.html`).
  - Adaptações de Copy com ancoragem geográfica para locais do Centro de Araranguá (Calçadão, Av. Getúlio Vargas, Praça Hercílio Luz, etc.).
  - Schema JSON-LD LocalBusiness atualizado com `areaServed`.
  - Repositório Git local inicializado em preparação para Deploy/Automação Jules isolada do app de finanças.

- 24/09/2026: Ativação de Publicação 100% Automática do Jules (`AUTO_DIRECT_COMMIT`):
  - Mesclada a página Nível 3 `harmonizacao-facial-cidade-alta.html` no repositório.
  - Atualizado o workflow `.github/workflows/jules-scheduler.yml` para o modo `AUTO_DIRECT_COMMIT`.
  - Novas páginas Nível 3 agora são salvas diretamente na branch `main` e publicadas automaticamente pelo deploy sem dependência de aprovações manuais via PR.

- 25/09/2026: Correção do fluxo do Jules e avanço na Cidade Alta:
  - Corrigido o `automationMode` no `jules-scheduler.yml` para `AUTO_PULL_REQUEST` (pois a API rejeita `AUTO_DIRECT_COMMIT`), com a adição da flag `-f` no cURL para reportar falhas corretamente ao GitHub Actions.
  - Criada manualmente a página Nível 3 `preenchimento-labial-cidade-alta.html` com Injeção de Schema e Contexto Geográfico Hiperlocal, atualizando `state.json`, `sitemap.xml` e `llms.txt`.
