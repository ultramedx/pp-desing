# Evoluir um projeto existente

Use com [03 — integrar e validar](03-integrar-validar.md) quando a entrega muda uma interface já existente. Preserve o contrato de [06 — continuidade](06-aplicar-manter-padroes.md).

## Diagnóstico do recorte

Identifique rotas, componentes, estilos, tokens, temas e dados locais afetados. Observe uma situação representativa antes da mudança e registre alterações preexistentes. Diferencie defeito observável, divergência do sistema e preferência estética.

Avalie apenas o necessário para o pedido:

- Hierarquia, densidade e legibilidade do conteúdo real.
- Fluxo até a ação principal, retorno e orientação de localização.
- Estados de foco, interação, carregamento, vazio, falha e sucesso.
- Semântica, rótulos, contraste e comportamento em diferentes entradas/telas.
- Consistência entre tokens, componentes, contrato e implementação.

Escolha mudanças pelo problema e resultado esperado. Trocar fontes, bibliotecas, cores de marca ou padrões de navegação não é uma etapa padrão de atualização visual.

## Implementação incremental

Reutilize a stack e os componentes canônicos. Concentre a mudança em uma parte verificável e expanda somente pelo recorte autorizado. Identifique consumidores antes de alterar token compartilhado, variante ou API de componente.

Preserve dados, ações e estados que já funcionam. Reescrever conteúdo, eliminar informação de domínio, inventar depoimentos ou datas e alterar integrações não decorre automaticamente de um pedido de melhoria visual.

Quando código antigo se tornar dispensável, trate limpeza segundo o pedido e a política do projeto. Preservar versões e recuperação vem antes de qualquer ação destrutiva; a organização desta biblioteca não exige excluir nada.

## Verificar

Compare condições equivalentes antes/depois e percorra o fluxo afetado. Confira identidade, dados, teclado, conteúdo extremo e telas pertinentes. Use os checks do repositório e acrescente uma verificação quando ela esclarecer risco real introduzido pela mudança.

Registre o que foi melhorado e quais partes do legado continuam. Atualize o contrato apenas se o comportamento ou padrão realmente mudou, preservando o histórico da decisão.

Origem conceitual: Redesign Existing Projects e PP Desing. As listas estéticas do material original foram contextualizadas; não há prioridade universal de troca de fonte ou paleta.
