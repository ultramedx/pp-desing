# Movimento de interface e SVG

Use quando o pedido ou interação precisa de transição, orientação ou feedback. Identifique o evento, a informação comunicada e o estado final. Interface estática pode ser a solução correta; movimento não é requisito genérico de uma tela.

## Escolher o mecanismo

Use as ferramentas já adotadas e a complexidade necessária. CSS pode resolver transições simples; controle por código é pertinente quando interrupção, sequência ou estado exigirem. Confirme versão e API antes de adicionar uma biblioteca.

Prefira propriedades que evitem recalcular layout quando produzirem o efeito correto. Para expansão real de conteúdo, escolha conscientemente uma transição de layout, geometria ou apresentação que preserve leitura e foco; meça o efeito quando houver risco de custo relevante. A regra é adequar mecanismo e custo, não proibir toda animação de altura nem torná-la padrão.

Defina duração e curva pelo propósito e pelo contrato. Feedback não deve fazer a ação parecer lenta. Coordene entrada, saída, repetição e interrupção; mantenha o resultado correto se o usuário agir de novo durante a animação.

## Acessibilidade e estado

Respeite preferência de movimento reduzido com uma apresentação estável e funcional. Reduzir duração globalmente a quase zero pode quebrar lógica dependente de eventos; confira o fluxo alternativo.

Conteúdo, foco e ação principal devem continuar acessíveis sem a animação. Preserve semântica e estado ao montar/desmontar elementos. Controles de pausa ou limitação de movimento contínuo são pertinentes quando a experiência os exigir.

## SVG

Preserve viewBox e proporção; diferencie SVG embutido no DOM de recurso carregado por imagem. Escolha CSS, SMIL ou código segundo a integração e o suporte testado; CSS externo da página não controla internamente um arquivo SVG usado como imagem.

Para desenho de traço, meça o comprimento quando houver código disponível e use dasharray/dashoffset coerentes. Para morphing, confira compatibilidade de quantidade, tipo e ordem de comandos do path. Grupos podem separar movimento global de detalhes.

Mantenha IDs de gradientes/máscaras únicos quando houver várias instâncias. Ajuste origem e caixa de transformação; preserve título/descrição ou tratamento decorativo conforme a função da imagem. Geometrias complexas e filtros exigem inspeção de custo.

## Desempenho quando pertinente

Reproduza a animação com o conteúdo, dispositivo e condições relevantes. Localize custo de layout, pintura, composição ou trabalho em JavaScript antes de mudar mecanismo. Agrupe leituras e escritas de geometria para evitar ciclos de invalidação.

Use observação de visibilidade ou mecanismos de timeline quando adequados; se houver acompanhamento por eventos, limite trabalho e respeite o controle da biblioteca existente. Camadas, filtros, blur e will-change têm custo: aplique pelo problema observado e retire otimizações que não ajudarem.

Verifique início/fim, reversão, repetição, mudança de rota, foco e modo reduzido. Só declare ganho medido quando houver medição; uma escolha tecnicamente plausível continua hipótese até ser observada.

Vídeo determinístico HyperFrames, composição Remotion e edição Editonny mantêm contratos próprios. Não aplicar lógica de relógio interativo de UI a um render de quadros.

Origens: animate, svg-animations, fixing-motion-performance e princípios de interação/movimento Impeccable.
