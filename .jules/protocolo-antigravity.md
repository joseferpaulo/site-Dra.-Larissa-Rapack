# Método Farol: Pilar de Engenharia Web (Protocolo Antigravity v1.0)

Este documento dita as regras estritas de SEO On-Page, Copywriting e Estruturação de Silos para a criação de sites e Landing Pages focados em dominância hiperlocal.

## 1. Arquitetura de Site em Silo  
A estrutura do site deve seguir rigorosamente a hierarquia de 3 níveis para transferir autoridade de SEO local de forma matemática:

*   **Nível 1 (Páginas Principais):** Home, Sobre Nós e Contato. Devem conter o panorama geral da autoridade da marca e links diretos para o Nível 2.  
*   **Nível 2 (Serviços/Produtos):** Páginas pilares detalhando cada serviço específico.  
*   **Nível 3 (Ataque Local/Bairros):** O grande motor do SEO. Páginas específicas de um serviço direcionadas a um bairro ou localização exata (Ex: "Limpeza de Pele no Bairro X").

## 2. Regras de Copy e SEO Hiperlocal (Nível 3 - OBRIGATÓRIO)  
Para gerar as páginas de Nível 3 (Ataque), o conteúdo DEVE seguir estas regras matemáticas e geográficas:  
*   **H1 Matemático e Único:** A tag H1 deve conter obrigatoriamente a fórmula: `[Serviço/Produto] + [Nome do Local/Bairro] + [Variação/Dor]`. NUNCA repita o mesmo H1 em páginas diferentes.  
*   **Densidade Mínima:** Cada página de serviço/bairro deve ter um mínimo de 2 parágrafos densos. Zero "Lorem Ipsum" ou placeholders.  
*   **Ancoragem Geográfica Obrigatória:** O texto DEVE contextualizar o porquê o serviço é útil para os moradores daquele local. É obrigatório extrair de 2 a 3 pontos de referência REAIS (ruas, hospitais, praças) da Base de Conhecimento da Cidade e diluí-los naturalmente no texto. Nunca invente distâncias ("a 5 minutos", "a poucos passos").

## 3. Regras de Engenharia e Código (Antigravity)  
*   **Zero Placeholders:** A copy final entregue deve ser persuasiva, otimizada e pronta para ser colocada no site.  
*   **Schema Markup (JSON-LD) Principal:** É OBRIGATÓRIO gerar o código de marcação de dados estruturados para a página. O script deve incluir a tag `LocalBusiness` e especificar a área de cobertura usando a tag `areaServed` com os bairros alvos.  
*   **Schema de Imagens (ImageObject - OBRIGATÓRIO):** Para **cada imagem** existente na página, você DEVE gerar um script JSON-LD do tipo `ImageObject`. Neste bloco, inclua a URL da imagem e, obrigatoriamente, as propriedades: `"caption"` (descrevendo o serviço no bairro) e `"contentLocation": { "@type": "Place", "name": "[Bairro Alvo]" }`. Isso é vital para ranquear as imagens no Google Images e Motores de IA (GEO) para pesquisas locais.
*   **Otimização de Imagens (Alt Text):** Para cada imagem na página, exija a criação de um texto alternativo (`alt text`) carregado de SEO Local (ex: "Paciente realizando [Serviço] na clínica em [Bairro]").
