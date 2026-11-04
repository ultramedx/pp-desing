# Revisão final, correções e animações antes da entrega

Use ao concluir a primeira versão da etapa solicitada. Essa versão é candidata à entrega: faça uma segunda passagem pelo resultado, aplique as correções pertinentes e confira o estado final. Um build aprovado ou a primeira inspeção durante a implementação não encerram esta revisão.

## 1. Confirmar o alcance

Leia o pedido vigente, o contrato visual e os critérios da etapa. Use a estratégia visual e o modo de participação definidos em [00](00-briefing-e-decisoes.md). Corrija automaticamente falhas relacionadas à entrega; dúvidas materiais podem ser esclarecidas no modo colaborativo, sem renovar autorizações já fornecidas. Preserve a identidade escolhida, os originais e a lógica de negócio.

- **Base de referências:** revise briefing, rastreabilidade, cópias, licenças conhecidas e cobertura. Registre oportunidades de movimento para a geração; a revisão da base não cria uma interface.
- **Tela, biblioteca ou integração executável:** revise no navegador a tela, os consumidores e, quando fizerem parte da entrega, o catálogo/templates. Implemente correções e movimento pertinente e revalide as partes afetadas.
- **Kit de motion/vídeo:** examine previews e frames reais dos formatos solicitados; confira transições, texto, áreas seguras e sincronização. Exporte o vídeo completo somente se estiver no pedido.
- **Documentos, prompts ou a própria skill:** revise instruções, coerência, links e pacote. A atualização do fluxo não executa os projetos descritos nem instala a skill.
- **Pedido somente de análise ou sem alterar código:** registre achados e evidências; respeite esse limite também nas animações.

## 2. Conferir o resultado pronto

Abra a versão efetivamente produzida e faça uma passagem separada da implementação. Na estratégia fiel, compare com a referência principal nas mesmas condições de largura e tema; na inspirada, confira a coerência com os princípios e a identidade escolhidos; na evolução, confira os contratos e as melhorias combinadas. Inspecione o código quando precisar explicar ou corrigir um comportamento observado.

| Área | Conferência exigida quando aplicável |
| --- | --- |
| Fidelidade e composição | Fontes, cores, geometria, densidade, hierarquia, espaçamento, ícones e assets; diferencie observação, interpretação e extensão proposta |
| Temas e contraste | Texto, curvas, barras, legendas, dias selecionados, tooltips e readouts nas superfícies reais, inclusive diálogos e cards em gradiente; calcule contraste segundo a meta do projeto |
| Responsividade e texto | Containers estreitos, labels longos, toque, overflow e ampliação de texto em 200%; prefira 320/390/768/1440px para web responsiva, junto dos breakpoints reais, adaptando o que não se aplica |
| Interação e acessibilidade | Teclado, foco visível, foco inicial e retorno em diálogos, Escape, clique externo, seleção, filtros, formulários, estados vazios/erro/loading e nomes acessíveis |
| Dados e visualizações | Coerência de valores, unidades, legendas e seleções; dados textuais acessíveis; indicadores e marcadores associados à geometria ou série correta |
| Movimento | Elementos que comunicam entrada, mudança, seleção, progresso ou feedback; forma final, entrada/reentrada, interrupção, hover após a entrada e movimento reduzido |
| Desempenho e robustez | Imagens dimensionadas, carregamento, bundle, trabalho de renderização, cleanup de efeitos, preferências com storage indisponível e dependências relevantes |
| Documentação e pacote | APIs, variantes, estados e tokens coerentes; caminhos, fonte/licença, originais, proveniência, inventário e integridade do pacote sem caches ou credenciais |
| Continuidade com IA | Quando incluída, contrato e skill local encontrados pelas entradas das ferramentas; paths relativos, imports, recorte de adoção e adaptações sincronizados conforme [06](06-aplicar-manter-padroes.md) |

Verifique as famílias/variantes do conjunto solicitado pelo catálogo quando ele existir ou fizer parte da entrega; numa tela/página pequena, examine-a diretamente. Exercite as tarefas centrais dos templates/consumidores incluídos. Para exemplos equivalentes, use representantes e registre a amostragem. Examine os casos com divergências e as combinações exigidas pelo contrato. Registre checks ausentes como ausentes.

## 3. Corrigir durante a revisão

Registre os achados no relatório usado pelo projeto, com prioridade, localização, evidência/reprodução, ação e critério de aceite. Separe **falhas obrigatórias** (requisito não atendido, regressão ou problema de funcionamento/legibilidade/interação) de **melhorias opcionais**. Corrija as falhas no escopo; aplique quick wins proporcionais e demonstráveis. Novas funcionalidades, reformulações ou otimizações sem benefício comprovado ficam como oportunidades, sem iniciar outra etapa. Uma falha corrigível não deve ficar apenas como sugestão para o usuário aprovar depois.

Use a menor alteração que resolva a causa. Reutilize componentes e tokens; atualize o gerador canônico quando houver tokens gerados. Preserve versões e dependências compatíveis; atualizações pontuais justificadas por um problema comprovado devem incluir lockfile e verificações afetadas. Otimizações de tamanho ou carregamento precisam de medidas comparáveis antes/depois; tamanho de artefato não é prova de LCP, INP ou FPS.

Nas regressões de interação, prove o comportamento: seletores dentro de um form não enviam o formulário; padding interno não fecha um diálogo; Escape e o botão de fechar restauram foco; hover e seleção continuam funcionando depois da animação. Use fixtures ou testes focados quando necessários, evitando testes que apenas repetem a implementação.

Em criação inspirada/evolução, corrija cores e papéis semânticos para a meta de contraste do projeto. Somente quando a reprodução fiel exigir preservar cores de baixo contraste, mantenha o modo de referência identificado e acrescente uma alternativa de maior contraste e dados textuais. Para gráficos com uma série fornecida, derive a geometria dos valores; um desenho ilustrativo só é preservado como tal quando servir ao pedido e permanecer identificado. Animar não transforma uma ilustração em cálculo ou série real.

Autocorreção não autoriza trocar a marca, alterar um algoritmo do domínio, conectar backend/IA, expor dados, instalar a skill globalmente ou publicar/deployar. Conclua as correções locais autorizadas antes de depender de uma dessas ações.

## 4. Identificar e implementar movimento útil

Inspecione todos os elementos de dados e controles da entrega executável. Na ausência de restrição expressa, implemente animações discretas nos gráficos e indicadores que comuniquem entrada ou mudança, além do feedback de interação pertinente. Faça essa implementação durante a revisão; não encerre com uma lista do que poderia ser animado.

| Elemento | Movimento a considerar e conferir |
| --- | --- |
| Curvas e áreas de gráficos | Revelação breve e transição da seleção/atualização; marcador acompanha a curva/série correta. Preserve o estilo; preserve paths fixos somente em reprodução ilustrativa explicitamente solicitada |
| Barras | Crescimento do desenho a partir da base, com stagger curto; seleção, tooltip e hover funcionam após a entrada |
| Anéis, gauges e progresso | Arco ou ponteiro chega ao valor final correto; números e rótulos continuam disponíveis sem depender da animação |
| Faixas e timelines | Entrada discreta das marcas e transição do item escolhido; preserve a área clicável enquanto o desenho anima |
| Botões, filtros e navegação | Feedback de hover/pressed/focus e mudança de seleção, sem deslocar alvos nem esconder o foco |
| Diálogos e expansões | Transição breve que preserve a semântica, a gestão de foco e a leitura; confirme abrir, fechar e reabrir |
| Loading e feedback | Movimento ligado a um estado real; não simule espera de rede nem animação contínua em dados estáticos |

Use os tokens de motion existentes. Quando ausentes, documente durações e easing compatíveis com a direção visual; para uma interface discreta, transições em torno de 120–300ms e entrada de gráficos em torno de 500–800ms são pontos de partida, não cotas obrigatórias. Apresente entradas uma vez por montagem/visibilidade, salvo necessidade demonstrada de replay; alterações de seleção devem responder imediatamente.

Prefira CSS, SVG ou recursos já presentes na stack. Anime transform/opacity e propriedades SVG pertinentes, avaliando o custo de pintura. Evite adicionar uma biblioteca pesada para uma entrada simples, medir layout em cada frame ou criar loops permanentes para dados estáticos. Limpe observers, listeners e timers. Em vídeo, mantenha o relógio determinístico da ferramenta de exportação.

Mantenha o alvo de toque e a área de foco estáveis: quando um segmento cresce com scaleY, aplique-o ao desenho interno, não ao botão. Defina o estado final na regra base. A animação de entrada precisa liberar as propriedades necessárias a hover e seleção; não deixe um fill-mode retido anulá-los.

Respeite prefers-reduced-motion e as preferências explícitas do usuário, tanto no CSS quanto na lógica JavaScript que dispara movimento. A alternativa estática deve mostrar imediatamente dados, marcadores e estado final. Teste essa alternativa; uma prévia em fixture pode ajudar, mas registre se a preferência nativa do ambiente foi realmente exercitada.

Registre uma matriz curta: elemento, propósito, movimento aplicado ou motivo para permanecer estático, tokens utilizados, comportamento reduzido e evidência. Elementos sem benefício claro, leitura crítica, atualizações frequentes/dados em tempo real e restrições explícitas podem permanecer estáticos quando o movimento prejudicar a interpretação. Preserve a composição final; a revisão não acrescenta efeitos decorativos indiscriminadamente.

## 5. Revalidar depois das correções

Reexecute os checks afetados e os checks obrigatórios do projeto depois da última alteração de código. No navegador, confirme os critérios de aceite dos achados, as animações em entrada e após terminar, a alternativa reduzida, o foco, as seleções e os layouts/temas afetados. Capture o resultado final quando possível; não use uma captura anterior à correção como prova do estado atual.

Se a correção gerar uma regressão, corrija e repita a verificação. Encerre quando os requisitos/falhas obrigatórias estiverem resolvidos, os checks pertinentes aprovados e uma nova conferência não revelar regressões relevantes. A busca contínua por melhorias opcionais não prolonga indefinidamente a entrega. Para o mesmo impedimento sem progresso após tentativas fundamentadas, ou falta de recurso indispensável, registre causa, tentativas e validação pendente; termine os itens independentes e declare resultado parcial. Sem navegador ou frames reais, a conferência visual executável permanece pendente; material estático é conferido pelos arquivos/previews disponíveis.

Atualize contrato, inventário, variantes/estados e proveniência quando a implementação os alterar. Se houver manifesto ou empacotamento solicitado, regenere-os após estabilizar as correções e confira caminhos, hashes e exclusões, inclusive metadados Git, dependências, caches e materiais sem permissão de redistribuição. Uma integração sem pedido de ZIP não exige criar um pacote para ser concluída.

## 6. Critério de entrega

Uma entrega concluída exige: cobertura da etapa confirmada; falhas obrigatórias no escopo resolvidas e revalidadas; animações pertinentes implementadas ou exceções justificadas; checks obrigatórios aprovados; conferência visual comprovada quando a entrega for visual executável; arquivos/documentos e, quando solicitado, pacote correspondentes à versão final.

Relate o que foi encontrado e corrigido, o movimento aplicado, os checks e evidências reais e as limitações remanescentes. Itens sem evidência suficiente permanecem pendentes; bloqueios não viram aprovação tácita. Revisão automática não equivale a aprovação humana da direção, certificação integral de acessibilidade ou publicação.
