# Prompt 1 — Preparar a base de design

Copie o texto abaixo para a ferramenta que terá acesso ao projeto e às referências.

---

Prepare a base de referência para o design solicitado: tela, página, protótipo, biblioteca ou kit visual. Use [briefing e decisões](00-briefing-e-decisoes.md) para definir alcance, estratégia e participação. Nesta etapa, organize e analise os materiais, sem modificar a interface existente nem iniciar a integração.

## Entradas

- Empresa/produto: [nome ou nome provisório].
- Público, tarefas principais e tipo de produto: [descrição].
- Referências: [links, imagens, telas, arquivos ou pastas].
- Referência principal e papel das demais: [composição, tipografia, cor, interação ou outro].
- Tipo de entrega e etapas incluídas: [tela, protótipo, design system, kit visual; destino].
- Estratégia visual: [inspirado, fiel ou evolução].
- Participação: [colaborativo ou autônomo; conforme escolhas já fornecidas].
- Logo e assets próprios: [arquivos/caminhos, se houver].
- Direção desejada: [adjetivos úteis, exemplos e o que evitar].
- Plataformas/formatos: [os do pedido; para interfaces web, responsividade conforme o contexto].
- Temas: [os solicitados/existentes; sem indicação em projeto novo, um tema principal documentado].
- Restrições: [marca, fontes, stack, acessibilidade e outras exigências].

Use o contexto para preencher o que estiver disponível. Aplique o modo de decisão de 00: dúvidas relevantes podem ser esclarecidas com o usuário ou delegadas à IA; lacunas menores viram hipóteses explícitas. Se o nome não foi informado e não for indispensável, use um nome provisório identificado como tal. Preserve assets próprios; um logo novo só é proposto quando estiver no escopo.

## Execução

1. Confirme a raiz do projeto, leia suas instruções aplicáveis e verifique se `BASE-DESING` já existe. Atualize essa base sem substituir conteúdo alheio à tarefa.
2. Se houver aplicação, identifique sua identidade visual, estrutura e stack para orientar as próximas etapas. Nesta fase, não instale dependências nem altere código.
3. Examine os materiais realmente acessíveis. Para links, abra as páginas relevantes quando houver navegação disponível. Para imagens, inspecione os pixels; não conclua cores, layout ou estados só pelo nome do arquivo. Se uma fonte estiver inacessível, registre a limitação e prossiga com as demais.
4. Separe o que foi observado, o que é interpretação e o que é decisão proposta. Não declare uma fonte como analisada se você não conseguiu acessá-la.
5. Extraia princípios reutilizáveis: hierarquia, densidade, composição, navegação, tipografia, uso de cor, iconografia, espaçamento, superfícies, bordas e movimento. Diferencie estrutura e interação de elementos exclusivos da marca de referência.
6. Para projetos existentes, preserve a identidade vigente, salvo pedido de mudança. Para projetos novos, derive uma direção coerente das entradas. Não misture paletas, logos e tipografias de várias empresas indiscriminadamente.
7. Armazene em `BASE-DESING` os arquivos fornecidos e os registros da análise. Copie os originais locais, preservando seus nomes quando possível; não mova nem remova as fontes. Salve capturas e materiais remotos apenas quando as ferramentas e o uso autorizado permitirem. Um link com notas e localização é suficiente quando não for possível armazenar o conteúdo.

## Aquisição das referências

Para URLs, inspecione as páginas e identifique as telas, imagens e documentos relevantes ao pedido. Baixe esses materiais quando o acesso e as ferramentas permitirem, usando versões adequadas à comparação/extração; não baixe um site inteiro por padrão. Confira conteúdo real, formato, dimensões e integridade para detectar respostas HTML/erro salvas como imagem ou arquivo. Preserve o original e crie recortes/miniaturas separadamente, registrando sua origem e processamento.

Para anexos/pastas, confirme quais itens o ambiente consegue acessar, inventarie primeiro e selecione os relevantes. Inspecione imagens visualmente, documentos pelo conteúdo e exports por sua estrutura; mantenha cópias rastreáveis sem copiar caches, dependências ou conteúdo privado alheio ao pedido. Um caminho em outra máquina não torna seus arquivos acessíveis.

Se um link falhar, tente uma alternativa disponível, como a página renderizada, uma versão pública oficial ou outra referência fornecida. Registre o alcance real do acesso; não contorne controles nem declare material inacessível como analisado. Se a referência principal indispensável à reprodução fiel continuar ausente, peça o material necessário e mantenha a comparação como pendente; no modo autônomo, desenvolva o restante possível sem inventar a evidência.

## Cópia fiel a partir de um link

Para reproduzir uma seção, página ou site, use o [fluxo de reprodução por URL](reproducao-por-url.md) para delimitar rotas, capturar a referência e medir a composição antes de construir.

## Entregáveis

Crie somente as pastas necessárias; um pedido pequeno pode reunir os registros em um único documento. Para uma biblioteca, use esta organização como referência:

```text
BASE-DESING/
  BRIEF.md
  REFERENCIAS.md
  DIRECAO-VISUAL.md
  DECISOES.md
  assets/
    originais/
  referencias/
    capturas/
```

- `BRIEF.md`: produto, público, tarefas, tipo de entrega, estratégia visual, participação, plataformas, temas, restrições e hipóteses. Inclua os componentes, padrões e telas necessários ao alcance combinado.
- `REFERENCIAS.md`: identificador, URL ou caminho de origem, data de acesso, localização da cópia/captura, aspecto relevante, acesso confirmado ou pendente e licença/permissão quando conhecida. Não afirme direitos de reutilização que não conseguiu verificar.
- `DIRECAO-VISUAL.md`: direção escolhida para geração, hierarquia, densidade, tipografia, paleta proposta, composição, iconografia e movimento; associe as escolhas às referências. Valores estimados de imagens devem ser marcados como estimativas.
- `DECISOES.md`: decisões, alternativas descartadas, hipóteses, limitações e recursos ainda necessários. Diferencie direção proposta de direção explicitamente escolhida pelo usuário.

Na lista da biblioteca, separe componentes, padrões e templates. Para cada componente, indique variantes e estados pertinentes; use `não se aplica` quando necessário. Inclua comportamentos de teclado, foco, toque e responsividade que façam parte do produto.

Não inclua segredos, dados pessoais reais, arquivos privados sem relação com a tarefa ou dependências volumosas na base. Registre informações de licença disponíveis para logos, ícones e fontes.

## Critério de conclusão

A base deve permitir que outra ferramenta compreenda a direção visual sem depender desta conversa: briefing, referências rastreáveis, assets identificados, abrangência da entrega e decisões documentadas. A lista da biblioteca é necessária quando uma biblioteca estiver no escopo.

Antes de entregar, execute [a revisão final](05-revisar-corrigir-entregar.md) no alcance documental desta etapa: confira os materiais, links e a cobertura e corrija inconsistências. Registre onde animações serão úteis na geração, sem implementar a interface durante a preparação da base.

Entregue os caminhos dos arquivos, a direção proposta e as lacunas. Não afirme que a geração ou a integração foram executadas. Encerre esta etapa; a próxima começa quando for solicitada ou já estiver incluída na autorização do fluxo completo.
