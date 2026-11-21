# Briefing, estratégia visual e participação do usuário

Use no início da rota ou quando o usuário mudar a direção. Recupere primeiro o pedido, os arquivos acessíveis e as decisões da conversa/projeto. Registre somente as lacunas que realmente mudam o resultado; não transforme o briefing numa entrevista obrigatória.

## O que definir

| Decisão | Registro útil |
| --- | --- |
| Objetivo e público | Produto/peça, tarefas centrais, contexto de uso e conteúdo necessário |
| Tipo de entrega | Tela/página, protótipo executável, design system, material estático ou kit de motion; etapas incluídas e destino |
| Referências | URLs, anexos e pastas acessíveis; referência principal, complemento e papel de cada uma |
| Estratégia visual | Inspirado, fiel ou evolução; elementos a preservar, adaptar e criar |
| Marca e restrições | Assets próprios, direção desejada, stack/contratos existentes, plataformas, temas e limitações |
| Participação | Colaborativo ou autônomo; perguntas respondidas, decisões delegadas e hipóteses |
| Aplicação e continuidade | Projeto novo/existente, recorte de adoção e ferramentas usadas: Codex, Claude, Stitch ou outras |

Use `BRIEF.md` e `DECISOES.md` existentes. Numa entrega pequena, essas informações podem ocupar seções de um único documento; numa biblioteca ampla, mantenha os documentos separados e rastreáveis.

## Estratégia visual

- **Inspirado:** crie uma identidade/composição própria com os princípios escolhidos nas referências. Combine seus papéis com coerência; uma referência pode orientar o layout e outra a tipografia. Avalie o resultado pela direção definida, não por igualdade de pixels com outra marca.
- **Fiel:** quando solicitado, preserve os elementos visuais especificados e compare com a referência principal em condições equivalentes. Registre medidas inferidas, adaptações de acessibilidade e estados que a fonte não mostra. Fidelidade não comprova licença para reutilizar marcas ou arquivos.
- **Evolução:** preserve os contratos e a identidade existentes; use as referências para resolver problemas e melhorar as partes solicitadas.

Inferir a estratégia de uma instrução clara evita repetir perguntas. “Copie o design deste link” pede reprodução fiel do recorte indicado. “Copie o layout com a minha marca” mantém a composição como referência e trata logotipo, textos ou cores indicados pelo usuário como adaptações intencionais. “Use este site como inspiração” permite uma composição própria. “Melhore este projeto” indica evolução da identidade existente. Se “novo design” for ambíguo, esclareça no modo colaborativo. No autônomo, escolha a interpretação que melhor atende ao objetivo; sem pedido de cópia, priorize inspiração para um projeto novo e registre a escolha.

## Modo colaborativo

Este é o padrão quando o usuário não delegou decisões. Pergunte apenas sobre dúvidas que alteram materialmente objetivo, entrega, direção ou viabilidade e que o contexto não resolve. Se as entradas forem suficientes, prossiga diretamente.

Agrupe, em geral, uma a três perguntas curtas por rodada. Ofereça escolhas claras com seu efeito e permita a alternativa “Pode deixar a IA decidir”. Por exemplo: tela ou biblioteca; inspiração ou reprodução fiel; referência principal. Peça preferências, não aprovações repetidas de ações já incluídas no pedido. Questões de baixo impacto podem virar decisões documentadas.

Enquanto aguarda, avance em inventário, inspeção e outras tarefas que não dependam da resposta. Uma pergunta que decide um requisito essencial permanece pendente; silêncio não escolhe uma opção. Para informação opcional, dê oportunidade razoável de resposta e, se for necessário avançar, declare uma hipótese reversível sem apresentá-la como escolha do usuário.

## Modo autônomo

Ative quando o usuário escolher essa opção ou disser “decida por mim”, “pode escolher”, “sem perguntas” ou equivalente. Resolva decisões visuais e técnicas rotineiras dentro das restrições. Documente escolhas relevantes, hipóteses e alternativas descartadas, preservando a possibilidade de ajuste posterior. Não peça aprovação de cada cor, componente ou animação.

Interprete a delegação no alcance em que foi dada: “escolha a cor por mim” delega essa escolha, não todo o projeto. Uma delegação geral ativa o modo autônomo; delegações pontuais podem coexistir com o modo colaborativo nas demais decisões.

Autonomia não cria acesso a uma referência indisponível nem aprovação humana. Se faltar um recurso indispensável para cumprir o pedido, conclua o trabalho independente e peça apenas o recurso/informação necessário. Preferências e autorização já dadas persistem; uma resposta ou correção posterior do usuário atualiza as decisões afetadas sem reiniciar tudo.

## Alcance e tamanho

Gerar uma tela não obriga criar um catálogo completo, segundo tema, backend, vídeo ou integração. Para um design system, dimensione a biblioteca pelos usos e itens combinados; para uma tela, implemente seus componentes e estados relevantes. Preserve temas existentes; em um projeto novo sem indicação, escolha e documente um tema principal coerente. Temas adicionais entram quando solicitados ou justificados dentro da entrega.

Uma referência pode ser imagem/HTML/documento estático, export de código ou aplicação existente. Registre o que ela permite observar. Se houver apenas imagens, estados e comportamento serão propostas; se houver uma série de dados fornecida, a geometria dos gráficos deve representar essa série. Falta de briefing formal não impede uma criação quando o pedido e os materiais já dão contexto suficiente.
