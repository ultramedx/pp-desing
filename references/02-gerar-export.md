# Prompt 2 — Gerar o design ou design system exportável

Use depois que a base estiver preparada. Em uma ferramenta sem acesso à pasta local, forneça os documentos e assets relevantes pelos mecanismos de anexos ou contexto que ela suporta.

---

Gere a entrega de design combinada usando as referências e o briefing disponíveis. Produza uma tela, página, protótipo, biblioteca ou kit coerente em `design-system-export` ou no destino solicitado. Uma criação independente não substitui a aplicação existente nem inicia uma integração.

## Contexto e escopo

Leia os registros existentes e os assets relevantes; use [briefing e decisões](00-briefing-e-decisoes.md). Se o usuário forneceu referências diretamente sem uma base formal, organize somente o contexto necessário com 01. Respeite a estratégia inspirado/fiel/evolução e o modo colaborativo/autônomo; decisões delegadas viram registros, não aprovação humana.

Se a ferramenta não tem acesso aos arquivos, use o material efetivamente disponível e registre o que faltou. Ausência de um formulário de briefing não obriga interromper uma tarefa com contexto suficiente; quando faltar informação essencial, esclareça-a conforme 00.

Para um projeto existente, confira sua stack e contratos antes de gerar código. Preserve suas versões e convenções. Não imponha Tailwind, shadcn/ui, React ou outra biblioteca por hábito. Em um projeto novo, use a stack solicitada; se ela não foi definida, registre a escolha de uma base mínima compatível com os recursos disponíveis.

## Entrega a produzir

Implemente a abrangência combinada. Numa tela/página, produza a composição e seus componentes, estados e layout necessários. Numa biblioteca reutilizável, cubra os grupos abaixo conforme os requisitos. Catálogo amplo, temas adicionais e templates extras precisam servir à entrega, sem inflar o escopo.

1. **Fundamentos:** paleta, tipografia, espaçamento, dimensões recorrentes, raios, bordas, sombras, camadas, iconografia, breakpoints e movimento. Use apenas as categorias necessárias ao produto.
2. **Tokens:** valores primitivos, tokens semânticos e tokens de componentes quando fizerem sentido. Defina papéis como fundo, superfície, texto, borda, ação, foco e feedback; os temas devem trocar valores sem mudar o significado desses papéis.
3. **Componentes:** todos os itens definidos no briefing, com APIs, variantes, tamanhos, estados e comportamento. Preserve as partes compostas sem inflar a contagem de componentes principais.
4. **Padrões:** composições e interações reutilizáveis do domínio, como formulários, busca, tabelas, navegação e feedback.
5. **Templates:** telas suficientes para demonstrar as tarefas centrais do produto e composições reais da biblioteca.
6. **Catálogo:** todos os componentes, variantes e estados pertinentes, nos temas solicitados e em layouts responsivos.
7. **Documentação e assets:** contrato visual, regras de uso, exemplos, fontes, ícones, logos e informação de origem/licença disponível.

Use conteúdo plausível e dados fictícios nos exemplos. Quando o usuário fornecer dados autorizados para a entrega, represente esses valores conforme solicitado, sem substituí-los por números inventados. A hierarquia, densidade e composição atendem às tarefas do briefing; efeitos, gradientes, cards e animações precisam de função na direção escolhida.

Na estratégia inspirada, crie combinações próprias e adapte os princípios das referências à marca e ao público; na fiel, preserve os elementos especificados e documente adaptações; na evolução, mantenha a identidade existente. Quando houver dados fornecidos para gráficos, derive sua geometria dos valores; desenhos ilustrativos devem permanecer identificados como tais.

## Estados e comportamento

Para cada componente, documente os estados aplicáveis: default, hover, active/pressed, focus-visible, disabled, loading, erro, vazio e selecionado. Não force estados sem sentido; vazio pode pertencer a uma lista, enquanto loading pode pertencer a uma ação ou região de conteúdo.

Implemente interações quando a ferramenta gerar código executável. Um desenho do estado de foco não substitui navegação por teclado; uma imagem de modal não comprova gestão e restauração do foco.

Inclua semântica, nomes acessíveis, contraste, legibilidade, toque, foco visível e suporte a movimento reduzido conforme o componente. Use uma meta de acessibilidade explícita, por padrão WCAG 2.2 AA, sem afirmar conformidade integral a partir de uma inspeção parcial.

## Contrato e export

Em bibliotecas, mantenha o contrato visual existente ou crie `DESIGN.md` numa estrutura nova, com direção e regras de uso ligadas aos tokens executáveis. Preserve nomes/caminhos canônicos adequados. Numa entrega menor, documente as decisões relevantes no contrato existente ou junto dos arquivos finais. Se houver um documento de design de outra ferramenta, preserve suas informações relevantes e sua origem.

O export deve conter, quando a ferramenta permitir:

```text
design-system-export/
  DESIGN.md
  INVENTARIO.md
  tokens/
  components/
  patterns/
  templates/
  assets/
  references/
```

Adapte a estrutura às capacidades reais da ferramenta. Não crie pastas vazias apenas para imitar o exemplo. Preserve HTMLs de referência e suas dependências. Não coloque `node_modules`, caches, segredos ou bundles descartáveis no export limpo; preserve os manifests e configs necessários para reproduzir o código.

Para uma biblioteca, registre em `INVENTARIO.md` uma matriz com:

| ID estável | Tipo | Nome | Fonte | Variantes | Estados aplicáveis | Temas | Implementação disponível |
|---|---|---|---|---|---|---|---|

Use uma linha por item principal. Identifique telas, padrões e partes compostas separadamente. Informe quantos componentes únicos existem e onde estão os exemplos.

O export executável pode ser a biblioteca canônica e a entrega final, com instruções de uso. A integração posterior é opcional e usa 03 quando solicitada; não duplique nem migre uma estrutura já adequada apenas para seguir os nomes das pastas.

Para design systems destinados ao desenvolvimento com IA, prepare o contrato e o material portátil de [aplicação e continuidade](06-aplicar-manter-padroes.md). Se as ferramentas de destino forem conhecidas, gere suas entradas e a skill local de aderência. Num export independente, mantenha esse material dentro do export; escreva instruções em outro repositório somente quando sua aplicação estiver no pedido. Uma imagem ou referência estática não exige instalar entradas de agentes.

Distinga claramente o que foi entregue: biblioteca funcional, código ainda não executado, HTML de referência, imagem ou guideline. Se a ferramenta produz apenas desenhos ou HTML, exporte esse material e declare quais componentes ainda precisam ser implementados na integração. Não anuncie código funcional sem que ele exista.

Se já houver um export, atualize-o de forma rastreável. Não acumule cópias com nomes como `final-2` ou `novo-final` sem necessidade; registre diferenças relevantes e preserve o material anterior de forma recuperável.

## Verificação desta etapa

Confira a cobertura entre briefing e inventário; não reduza a biblioteca a tokens. Verifique consistência visual dos temas, hierarquia, legibilidade, responsividade e estados disponíveis. Se houver código executável e ambiente compatível, valide-o e registre os comandos e resultados; se não houver, declare essa limitação.

Após a primeira versão pronta, execute [a revisão final com correções e animações](05-revisar-corrigir-entregar.md). Quando o export for executável, confira o resultado renderizado, aplique os ajustes e o movimento útil nos gráficos/controles e revalide antes da entrega. Quando a ferramenta só produzir material estático, confira esse material e documente o movimento a implementar posteriormente, sem declarar que ele foi executado.

Entregue o export, a matriz de cobertura, referências visuais e um resumo das escolhas. Separe validação técnica de revisão humana da direção visual. Não execute a migração para o projeto nem apague as fontes nesta etapa.
