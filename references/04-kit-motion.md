# Extensão do fluxo: kit de identidade para vídeo

Use quando a entrega solicitada for assets, SVG, motion graphics ou templates de vídeo. Preserve `BASE-DESING` e `design-system-export`. Uma biblioteca para vídeos não exige criar ou alterar um aplicativo de produto.

## Base

Use [briefing e decisões](00-briefing-e-decisoes.md) para definir o kit, seus formatos e a participação do usuário. Se houver logo próprio autorizado, preserve-o e seus traçados. Sem logo fornecido, use uma identificação provisória ou crie uma proposta somente quando isso estiver no escopo; logos de referências não se tornam a marca do kit. Para reproduzir um símbolo próprio existente, prefira seu original vetorial a uma recriação raster. Fontes devem ter licença e cobrir os caracteres do idioma.

Procure materiais de vídeo já usados pela marca: estúdio, manual de edição, thumbnails, vinhetas e peças prontas. A identidade da interface pode usar fonte, ritmo e acentos diferentes dos vídeos. Não transforme uma preferência inferida de uma página estática em proibição de marca. Separe o perfil institucional dos perfis de campanha e registre qual o template implementa. Um estilo descrito não comprova a existência de seus arquivos de projeto ou fontes.

## Entregas pertinentes

- Assinaturas da marca em layouts e versões de cor úteis, com SVG e PNG transparente.
- Ícones, padrões, fundos sem texto e overlays de identificação, capítulos, legendas, passos, citações, comparação, tela e encerramento.
- Tokens visuais e de motion, guias de área segura e formatos solicitados.
- Componentes tipados e composições reais na ferramenta escolhida. Não aplicar estados de UI sem função em um asset de vídeo.
- Fonte local, áudio original ou licenciado, proveniência e licenças.
- Catálogo navegável, instruções de edição, prompts reproduzíveis, inventário com hashes e relatório.

Dimensione a biblioteca pelo uso, não por uma contagem arbitrária. Não gerar fotos, vozes, músicas ou imagens de pessoas sem contexto autorizado. Se o uso for educacional, forneça exemplos fictícios e instruções para substituir a marca por materiais autorizados.

## Ferramentas e motion

Leia as skills das ferramentas realmente usadas. Em Remotion, derive animação do frame e fps, use fontes/assets locais e adapte cada formato. Motion/GSAP destinam-se à timeline do ambiente em que forem usados; não rodar uma segunda timeline como relógio de exportação Remotion.

Mantenha SVGs com grupos identificáveis. Converta textos de assinatura em traçados para portabilidade e preserve uma fonte editável no gerador ou componente. Inclua movimento reduzido para previews/interatividade quando pertinente.

## Validação

Verifique integridade dos caminhos originais, XML, referências, dimensões, alpha, caracteres da fonte, contraste e cobertura do inventário. Execute checks de código e bundle. Inspecione cada formato e tema com frames reais; corrigir cortes, sobreposição e texto pequeno.

Declare separadamente: catálogo funcionando, preview de composição, frames renderizados, vídeo completo exportado e publicação. Um build verde não comprova todos esses resultados. Só exporte o vídeo completo quando estiver no escopo do pedido e respeitando a skill da ferramenta.

Antes de empacotar e entregar, execute [a revisão final](05-revisar-corrigir-entregar.md) no contexto de motion/vídeo. Corrija os problemas encontrados nos formatos e frames reais, confira o ritmo e as transições pertinentes e revalide o resultado. A conferência do kit não inicia uma integração de aplicativo nem uma exportação de vídeo fora do pedido.

## Encerramento

Entregue o kit organizado; produza uma cópia portátil quando houver pedido de compartilhamento/empacotamento. Exclua dependências instaladas, caches e credenciais e inclua os manifests e comandos necessários à reprodução. Preserve base e export até uma integração posterior solicitada e validada.

Quando houver referências autenticadas ou mídias de pessoas para consulta autorizada, mantenha-as em subpastas locais explícitas e exclua-as do ZIP de distribuição. Verifique o conteúdo do ZIP após empacotar. Catalogar um link, baixar um arquivo, implementar um preset e ter direito de redistribuição são resultados distintos; declare qual foi alcançado para cada material.
