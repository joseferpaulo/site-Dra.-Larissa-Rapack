# Implementação do Protocolo Método Farol e Setup para Integração com Google Jules

O objetivo deste plano é estruturar o site estático da Dra. Larissa Rapack seguindo rigorosamente o **Método Farol (Protocolo Antigravity v1.0)**, transformando-o em um gerador de tráfego orgânico hiperlocal, e isolá-lo num repositório Git autônomo. Esse repositório independente viabilizará futuramente o agendamento de tarefas recorrentes via **Google Jules**, sem qualquer interferência com o aplicativo de finanças do usuário.

## Open Questions
- Precisamos que você forneça o **Estudo de Mercado do cliente** (nicho, serviços, dores) e a **Base de Conhecimento Geográfica da cidade** (Araranguá e bairros alvos) para podermos definir os pontos de ancoragem real.
- O repositório no GitHub será criado por você para que possamos subir os arquivos, correto? Por favor, confirme quando criar e nos envie a URL.

## Proposed Changes

### Setup Inicial: Git & Isolamento (Google Jules)
Configurar a pasta do projeto como um repositório Git, garantindo total isolamento para futuras integrações do Jules via GitHub Actions ou API.
- **[NEW]** Repositório Local (inicialização via `git init` e commit inicial)

### Passo 1: Estrutura do Silo
Definir hierarquia de páginas:
- **Nível 1:** Institucional (Home, Sobre, Contato) - revisão do `index.html`.
- **Nível 2:** Serviços Raiz (Harmonização Facial, Corporal, Labial).
- **Nível 3:** Ataque Local (Páginas de serviço segmentadas por bairro/vias-chave).

### Passo 2 & 3: Copy Nível 1 e 2
Revisar e adaptar os textos do `index.html` e demais HTMLs de serviços para remover placeholders, garantir copy persuasiva e alinhar ao estudo de mercado.
- **[MODIFY]** `index.html`
- **[MODIFY]** `harmonizacao-facial.html`
- **[MODIFY]** `harmonizacao-corporal.html`
- **[MODIFY]** `preenchimento-labial.html`

### Passo 4: Copy Nível 3 (Ataque Local)
Criar as Landing Pages de ataque utilizando os dados de mercado e ancoragem geográfica.
Aplicação rigorosa do **H1 Matemático** e no mínimo **2 pontos de referência geográficos reais** em cada página.
- **[NEW]** Novos HTMLs focados em bairros (Ex: `protocolo-bigode-chines-centro.html`)

### Passo 5: Engenharia Final (SEO Técnico & Schemas)
Geração e injeção do `Schema JSON-LD` (`LocalBusiness` e `areaServed`) contendo todos os bairros de atuação, garantindo que o Google indexe corretamente a área de cobertura. Ajuste dos assets de SEO gerais e tags Open Graph.
- **[MODIFY]** `protocolo-bigode-chines.html`
- **[MODIFY]** `sitemap.xml`
- **[MODIFY]** `robots.txt`

## Verification Plan

### Manual Verification
- Validar a estrutura do Silo gerada (Passo 1) em texto e aguardar aprovação antes de gerar o código das páginas.
- Revisar as tags `<head>` para assegurar que os Schemas JSON-LD estão preenchidos com o NAP e `areaServed` corretos.
- Subir os arquivos para o repositório GitHub isolado e conferir se o deploy ocorreu corretamente pela Hostinger, deixando o terreno pronto para o Google Jules no futuro.
