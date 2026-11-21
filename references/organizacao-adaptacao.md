# Adaptação de telas e contextos

Use quando a entrega precisa funcionar em outro espaço, entrada ou meio. Identifique o contexto de origem, o alvo e o que precisa permanecer acessível. Redimensionar não resolve por si só mudança de navegação, densidade ou uso.

## Interface web

1. Observe onde o conteúdo perde legibilidade, transborda ou dificulta a ação. Use essas quebras e o contrato do projeto para definir pontos de adaptação.
2. Preserve a tarefa principal e informações necessárias. Reordenação ou divulgação progressiva deve manter descoberta e sequência de leitura coerentes.
3. Use Flexbox para distribuição unidimensional e Grid quando linhas e colunas precisarem de coordenação. Prefira limites flexíveis e largura máxima a dimensões rígidas que causem overflow.
4. Use consultas de contêiner para componentes reutilizados em espaços diferentes e consultas de viewport para estrutura da página, conforme suporte real. Tamanhos fluidos com limites explícitos podem reduzir saltos de escala.
5. Preserve relação de aspecto e espaço reservado para imagens/vídeos; escolha recursos responsivos quando houver diferentes tamanhos de arquivo. Conteúdo importante deve continuar acessível com carregamento lento.

Não migre um projeto inteiro para mobile-first somente para corrigir um componente. Em uma nova estrutura, começar pelo menor contexto útil ajuda a priorizar conteúdo.

## Entrada, leitura e navegação

Inclua toque e teclado na decisão; informação essencial não pode depender apenas de hover. Mantenha foco visível e ordem compreensível. Escolha alvos e separação pelo contexto, com área confortável de toque e verificação dos requisitos de acessibilidade aplicáveis; não confunda recomendação de conforto com critério normativo universal.

Confira zoom, orientação, títulos longos, tabelas, formulários, menus e diálogos relevantes. Tabelas podem conservar leitura com rolagem localizada, prioridade de colunas ou outra apresentação compatível com a tarefa. Uma versão móvel não deve perder funções centrais.

Em aparelhos com recortes e barras do sistema, verifique safe areas e o espaço real disponível. Preserve navegação de retorno e o estado do usuário ao trocar orientação ou layout.

## Referência condicional Tailwind

Só use este ramo se Tailwind já fizer parte da stack ou estiver no pedido. Confira a versão, tokens e breakpoints configurados antes de aplicar receitas; sintaxe de uma versão não deve substituir a configuração de outra.

- Estilos de base definem o contexto menor; prefixos pertinentes acrescentam diferenças, sem repetir todo o estilo.
- Componentes embutidos podem precisar de container queries, enquanto a estrutura de navegação responde ao viewport.
- Use tokens e utilitários existentes para espaçamento, tipografia e dimensões. Safe areas e tamanhos fluidos podem usar valores CSS necessários ao projeto.
- Preserve espaço de mídia e sobreposições; em vídeo, mantenha controles dentro da área utilizável sem encobrir conteúdo essencial.

## Outros meios

**Impressão:** reveja quebras de página, margens, contraste, conteúdo recolhido e metadados necessários. Retire controles sem utilidade no papel; preserve informação, cabeçalhos ou rodapés que a peça exige. Confira visualmente a saída de impressão.

**E-mail:** escolha layout e CSS compatíveis com os clientes-alvo. Preserve leitura, CTA, texto alternativo e alternativa para recursos indisponíveis. Interações complexas podem apontar para a aplicação. Gerar ou visualizar um e-mail não autoriza enviá-lo.

**Outros dispositivos/entradas:** adapte densidade, distância de leitura, controles e feedback à tarefa. Não imponha automaticamente menu inferior, drawer ou número fixo de colunas só pelo nome do dispositivo.

## Verificação

Teste dimensões representativas e as transições onde o layout muda, incluindo conteúdo extremo aplicável. Confira leitura, foco, controles, overflow e persistência de estado. Emulação e teste físico são evidências diferentes; indique quando o dispositivo real não foi testado.

Origens: adapt, responsive-design e tailwindcss-mobile-first; detalhes de proveniência permanecem separados.
