---
name: jules-silo-builder
description: Skill de automação para o Google Jules gerar progressivamente páginas Nível 3 (Bairros) seguindo o Método Farol.
---

# 🤖 Jules Silo Builder (Método Farol v1.0)

Esta skill orienta o agente **Google Jules** na construção progressiva de páginas web hiperlocais (Nível 3). 
Para não sobrecarregar o índice de busca e garantir um crescimento orgânico natural, você deve criar **apenas 1 página por execução**, avançando pela lista do arquivo de estado e marcando seu progresso.

## 📚 Conhecimento Obrigatório (Leia Antes de Começar)
Antes de executar qualquer modificação, você é **obrigado** a ler os seguintes documentos base na sua pasta:
1. **`protocolo-antigravity.md`**: Contém as Regras de Ouro matemáticas de SEO (H1, densidade de texto, ausência de placeholders, Schema JSON-LD).
2. **`geo-ararangua.md`**: A Base de Conhecimento com as vias, características e pontos turísticos reais do bairro que você está processando. Nunca invente o contexto geográfico.

## 🔄 Fluxo de Trabalho de Cada Execução (Apenas 1 Página)

### 1. Leitura do Estado
1. Leia o arquivo `state.json`.
2. Encontre o primeiro objeto na lista `"bairros"` cujo `"status"` seja `"em_progresso"`. (Se não houver nenhum "em_progresso", procure o primeiro `"pendente"` e mude para `"em_progresso"`).
3. Dentro desse bairro, olhe a array `"paginas"`. Encontre o primeiro objeto cujo `"status"` seja `"pendente"`.
4. Você usará o `"template_pai"` como arquivo de origem, e salvará a nova página com o nome definido em `"arquivo_destino"`.

### 2. Duplicação e Edição da Página (Nível 3)
1. Faça uma **cópia exata** do arquivo indicado em `"template_pai"` e salve-o com o nome de `"arquivo_destino"`. 
   > *Isso garante que o design, CSS e Tailwind permaneçam perfeitamente intactos. Altere apenas o conteúdo de texto focado em SEO.*
2. Abra a nova página Nível 3 recém-criada e realize as injeções exigidas pelo **Protocolo Antigravity**:
   - **`<title>` e H1**: Formate com `Serviço + Bairro`.
   - **`<meta name="description">`**: Insira de forma fluida o bairro no texto.
   - **JSON-LD Schema**: Adicione o bairro no array `"areaServed"`.
   - **Texto da Página (Ancoragem Geográfica)**: Utilize a skill `geo-ararangua.md` para injetar pontos de referência. **Lembre-se:** nunca crie distâncias ilusórias.

### 3. Linkagem Interna (Atualizando a Página Mãe)
1. Abra o arquivo **Mãe Original** (o arquivo que estava em `"template_pai"`).
2. Vá até o final da página, na seção de `<!-- LOCAIS ATENDIDOS -->` onde existe uma tag expansiva `<details>`.
3. Dentro da `div` com as classes `flex flex-wrap justify-center`, adicione um novo link apontando para a página Nível 3 criada:
   `<a href="[arquivo_destino]" class="border line-taupe px-6 py-2.5 rounded-full text-sm font-medium text-brand-dark hover:bg-brand-taupe hover:text-white transition-colors shadow-sm">[Nome do Bairro]</a>`

### 4. Atualização do Estado
1. No arquivo `state.json`, marque o objeto da página que você acabou de processar alterando seu `"status"` para `"concluido"`.
2. Verifique se todas as páginas daquele bairro agora estão como `"concluido"`. Se sim, mude o `"status"` do bairro inteiro para `"concluido"`.
3. Salve o arquivo `state.json`.

### 5. Finalização
Faça o commit no repositório com a mensagem no padrão: 
`feat: adiciona pagina N3 [template_pai] para o bairro [bairro]`

---
**Encerre sua execução logo após processar UMA ÚNICA PÁGINA.**
