# Sistema visual e adaptadores

Use o contrato existente como fonte canônica. [06 — continuidade](06-aplicar-manter-padroes.md) preserva os caminhos, templates e regras de handoff PP. Escolha um dos modos abaixo; criar um sistema e aderir ao que existe são tarefas diferentes.

## Extrair padrões reutilizáveis

Localize componentes, tokens, documentação e convenções de importação já existentes. Identifique repetições e variantes que realmente precisam de uma fonte comum. Valor de reúso e custo de manutenção importam mais que extrair todo valor literal.

Defina quais diferenças são variantes do mesmo componente e quais representam funções distintas. Preserve APIs, semântica, teclado, foco, estados e tipos usados pelos consumidores. Separe tokens primitivos de papéis semânticos quando isso beneficiar a aplicação real.

Migre somente consumidores no alcance autorizado, conferindo paridade visual e funcional. Atualize catálogo e exemplos necessários. Um pedido de extração não autoriza apagar implementações ou alterar produtos fora do recorte; siga a política de preservação e recuperação do projeto.

## Normalizar para o sistema existente

Mapeie cada desvio para sua fonte: token ausente, literal isolado, variante inadequada ou comportamento diferente. Substitua pelo padrão canônico e preserve o que for exceção documentada. Aderência visual não deve reduzir acessibilidade.

Confira tipografia, cor/tema, espaçamento, componente, interação e adaptação relevantes à tela. Se o padrão existente não atender ao caso, registre o limite e uma mudança proposta ou já autorizada; não crie uma segunda paleta informal.

## Adaptar para Stitch ou outra ferramenta

Produza um contexto derivado do contrato real: atmosfera, papéis de cor, tipografia, componentes, layout, estados e movimento pertinentes. Registre origem e versão e confira correspondência com tokens executáveis.

Use o formato aceito pela ferramenta e versão disponíveis; um arquivo local não comprova importação nem aplicação às telas. Importar, publicar ou associar a um projeto remoto entra somente quando a ação fizer parte do pedido. Um adaptador não redefine marca ou contrato canônico.

Os templates PP existentes são pontos de partida quando solicitados; substitua campos e valide caminhos. Preserve uma estrutura canônica já presente em vez de renomear pastas para caber num exemplo.

## Completar

O mapa de componentes/tokens, seus consumidores e os documentos devem descrever a mesma implementação. Informe migração feita, exceções, verificação de paridade e limitações. Uma biblioteca é entregue no alcance pedido, não pelo volume de componentes criados.

Origens: extract, normalize, stitch-design-taste e rotas PP existentes. A organização semântica do adaptador foi preservada sem impor um estilo visual concorrente.
