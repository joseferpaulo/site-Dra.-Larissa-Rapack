1. **Duplicate template**:
   - `cp preenchimento-labial.html preenchimento-labial-barranca.html`
   - Verify creation `ls -la preenchimento-labial-barranca.html`
2. **Update Title, Meta Description and H1 in N3 page**:
   - Title: `Preenchimento Labial na Barranca, Araranguá - SC | Dra Larissa Rapack`
   - Meta: `Preenchimento labial com sensibilidade artística e rigor anatômico na Clínica Dra Larissa Rapack para moradores da Barranca, Araranguá. Lábios hidratados, definidos e volumosos.`
   - H1: `Preenchimento Labial na Barranca para Hidratação e Volume`
3. **Rewrite Copy in N3 page (Antigravity Protocol)**:
   - Update text near `<h2 class="text-lg md:text-xl text-brand-taupe font-light mb-8 leading-relaxed">` to include "Lábios Hidratados e Definidos para quem vive na região da Barranca".
   - Update the paragraph under `A Arte do Preenchimento Labial Harmônico`: "Lábios volumosos nunca devem parecer artificiais. Na Clínica Dra. Larissa Rapack, o Preenchimento Labial é executado com sensibilidade artística e rigor anatômico para pacientes de toda a cidade, especialmente para quem mora próximo à Rua Paulino Luiz Pereira e pontos de referência históricos da Barranca, como a Antiga Estação Ferroviária. Priorizamos a simetria, a definição do arco do cupido e a hidratação profunda dos tecidos."
   - Update the italic text inside `<div class="p-6 rounded-2xl bg-brand-blue_light border line-blue">`: "Se você reside na região da Barranca e busca destacar a beleza do seu sorriso sem perder a naturalidade, valorizando sua expressão, nosso protocolo foi feito para você."
   - Update ALT texts on images to include "na Barranca, Araranguá".
4. **Update Schemas in N3 page**:
   - Inject `"areaServed": ["Barranca", "Araranguá"],` in LocalBusiness schema.
   - Inject `ImageObject` schema in HTML with `"caption"` and `"contentLocation": { "@type": "Place", "name": "Barranca" }` for the existing image.
5. **Internal Linking in Parent page**:
   - In `preenchimento-labial.html`, locate `<!-- LOCAIS ATENDIDOS (SILO NÍVEL 3) -->` and append `<a href="preenchimento-labial-barranca.html" class="border line-taupe px-6 py-2.5 rounded-full text-sm font-medium text-brand-dark hover:bg-brand-taupe hover:text-white transition-colors shadow-sm">Barranca</a>` to the list of neighborhoods.
   - Also update the newly cloned page to include this link so it inherits the correct footer. (Oh wait, if I update parent first, then clone, it will have the link!)
   Let's swap order: I will first update the parent page, then clone! No, the plan says duplicate first. If I duplicate first, I need to update both. Actually, I can just update the clone after cloning.
6. **Update SEO files**:
   - Add `<url><loc>https://dralarissarapack.com.br/preenchimento-labial-barranca.html</loc><lastmod>$(date +%Y-%m-%d)</lastmod><changefreq>monthly</changefreq><priority>0.9</priority></url>` to `sitemap.xml` before `</urlset>`.
   - Add `- Preenchimento Labial (Barranca): https://dralarissarapack.com.br/preenchimento-labial-barranca.html` to `llms.txt`.
7. **Update State**:
   - Run script to update `preenchimento-labial-barranca.html` status to `concluido` in `.jules/state.json`. (Check if Barranca should be fully concluded).
8. **Test**:
   - Run `npx htmlhint *.html` to validate HTML.
9. Complete pre-commit steps to ensure proper testing, verification, review, and reflection are done.
10. Submit.
