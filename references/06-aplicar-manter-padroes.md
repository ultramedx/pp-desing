# Aplicar e manter o design durante o desenvolvimento com IA

Use para iniciar um projeto com o design fornecido, adotá-lo num projeto existente ou preparar a continuidade por Codex, Claude Code, Stitch ou outra ferramenta. Combine com [02](02-gerar-export.md) para gerar código e [03](03-integrar-validar.md) para integrar. Prepare o material dentro do export quando a aplicação em outro repositório ainda não estiver solicitada.

## 1. Definir o contrato do projeto

Recupere as decisões de [00](00-briefing-e-decisoes.md). Identifique o destino, o recorte de adoção, as ferramentas escolhidas e os contratos existentes. A skill geral define o método; o contrato local define a identidade de cada projeto.

| Artefato | Autoridade e uso |
| --- | --- |
| `DESIGN.md` ou contrato existente | Direção visual, versão, alcance, princípios, fontes, layout, estados, motion, acessibilidade e exceções |
| Tokens executáveis | Valores normativos consumidos pela aplicação; exemplos no Markdown apontam para essa fonte e são sincronizados |
| Componentes e padrões canônicos | APIs e comportamento a reutilizar; catálogo/inventário quando existentes ou necessários |
| Regras compartilhadas de design | Procedimento de consulta, mudança e validação; não mantêm uma segunda paleta |
| Skill local de aderência | Entrada curta que leva o agente ao contrato e às regras específicas do projeto |
| Adaptadores de ferramenta | Entradas de contexto ou imports que apontam às mesmas fontes |

Registre caminhos relativos à raiz, versão/estado do contrato e quais rotas/componentes ele governa. Num monorepo, identifique o sistema por aplicação e use nomes de skills distintos quando necessário. Preserve caminhos canônicos existentes, sem impor a árvore ilustrativa abaixo:

```text
projeto/
  DESIGN.md
  AGENTS.md                         # Codex, quando escolhido
  CLAUDE.md                         # Claude, quando escolhido
  docs/design/DESIGN-RULES.md
  .agents/skills/project-design/SKILL.md
  .claude/skills/project-design/SKILL.md
  .stitch/DESIGN.md                 # derivado/importável, quando necessário
  tokens/                          # ou localização real da stack
  components/                      # ou biblioteca canônica existente
```

Crie apenas as entradas das ferramentas usadas ou explicitamente incluídas no pacote portátil. Skills locais são ponteiros ao contrato, sem valores visuais independentes. Quando houver duas cópias de um mesmo guard, mantenha o conteúdo equivalente e confira a sincronização. O funcionamento básico deve continuar sem a instalação global da skill geral nem caminhos para a máquina do autor.

## 2. Projeto novo ou existente

**Novo:** estabeleça o contrato e o mapa dos tokens/componentes a partir do design fornecido e prepare as entradas das ferramentas escolhidas. Quando a implementação estiver incluída, conecte os estilos/tema da stack, implemente os componentes necessários e uma tela representativa antes de expandir as telas; confira referência, dados, comportamento e resultado renderizado. Num pedido somente de handoff/documentação, prepare e confira os arquivos sem iniciar a implementação.

**Existente:** faça o diagnóstico de 03 antes de alterar. Mapeie tokens, componentes, estilos globais, rotas, temas e documentos; preserve stack, comportamento e alterações preexistentes. Integre incrementalmente no recorte solicitado. Dois componentes não autorizam redesenhar o aplicativo. Delimite o legado preservado e a convivência dos sistemas, evitando que novos tokens alterem telas fora do alcance. Ajuste aliases/imports/consumidores necessários e verifique regressões nas partes afetadas.

Se pedido e contratos ativos entrarem em conflito, confirme qual mudança material é desejada no modo colaborativo ou aplique a escolha já delegada no alcance autorizado. Um export ou prompt de geração não redefine automaticamente a identidade vigente. Uma solicitação explícita de mudança atualiza o contrato; preserve o histórico da decisão.

## 3. Entradas específicas por ferramenta

As convenções abaixo foram conferidas em documentação oficial em 14/10/2026. Confirme a configuração e a documentação vigente ao aplicá-las, especialmente se houver diferenças de versão. Use o [template de entradas](../assets/project-handoff/TOOL-ENTRYPOINTS.template.md) como ponto de partida e substitua os caminhos pelos reais.

- **Codex:** acrescente um ponteiro curto às regras e à skill local no arquivo de instrução efetivamente ativo: `AGENTS.md` ou override aplicável. Skills de repositório usam `.agents/skills/<nome>/SKILL.md`. Verifique a hierarquia, inclusive arquivos aninhados/overrides, para que o lembrete não fique em um arquivo ignorado. Preserve o restante das instruções. [AGENTS.md](https://learn.chatgpt.com/docs/agent-configuration/agents-md), [skills](https://developers.openai.com/codex/skills).
- **Claude Code:** mantenha `CLAUDE.md`/regras existentes e adicione o vínculo ao contrato compartilhado. Um import `@path` é relativo ao arquivo importador; `.claude/skills/<nome>/SKILL.md` fornece a skill de projeto. Ao criar um `CLAUDE.md` onde antes se usava `AGENTS.md`, preserve a leitura dessa base por import quando pertinente; a descoberta depende da hierarquia/versão e pode mudar com o novo arquivo. `.claude/rules/` é alternativa para regras pertinentes, sem duplicar o contrato. [Memória e imports](https://code.claude.com/docs/en/memory), [skills](https://code.claude.com/docs/en/skills).
- **Stitch:** prepare um `DESIGN.md` no formato aceito pelo recurso disponível. Quando o contrato canônico tiver outro formato, gere `.stitch/DESIGN.md` como adaptação dos tokens e regras reais, com origem/versão e conferência de correspondência; não mantenha valores independentes. Faça upload/importação e associe o sistema ao projeto somente quando essa ação externa estiver solicitada. Escolher o padrão governa telas novas; confira a aplicação por tela nas existentes. Um arquivo local pronto não comprova importação. A especificação `design.md` do Google Labs está em alpha: confira o schema antes de gerar o adaptador. [Importação](https://stitch.withgoogle.com/docs/design-md/get-instructions/), [uso e telas existentes](https://stitch.withgoogle.com/docs/design-md/usage/), [especificação](https://github.com/google-labs-code/design.md).
- **Outras ferramentas ou chat sem acesso ao repositório:** use o mecanismo de contexto documentado. Forneça contrato, material visual e instruções pertinentes como anexos/prompt; não presuma descoberta de `AGENTS.md`, `CLAUDE.md` ou arquivos do disco. Registre o alcance de acesso e valide o output contra o contrato antes de integrar.

O formato `design.md` permite frontmatter YAML opcional e Markdown. Para uma adaptação estruturada ao Stitch, tokens em YAML mais descrição visual são uma escolha útil de precisão, conforme o schema vigente; não declare YAML obrigatório para todo contrato. Se usar o CLI oficial, confira também warnings e os tokens realmente reconhecidos: um resultado sem erros pode conter um modelo vazio. Aceitação no importador e aplicação na tela continuam verificações separadas. [Spec](https://github.com/google-labs-code/design.md/blob/main/docs/spec.md), [comportamento do linter](https://github.com/google-labs-code/design.md/blob/main/packages/cli/src/linter/lint.ts).

Use os templates [DESIGN](../assets/project-handoff/DESIGN.template.md), [regras compartilhadas](../assets/project-handoff/DESIGN-RULES.template.md) e [skill local](../assets/project-handoff/project-design/SKILL.template.md). O template de skill usa o nome `SKILL.template.md` no pacote para evitar descoberta indevida; nos projetos preparados, sua saída é `SKILL.md`. Eles contêm campos `{{...}}` a substituir: não são um design preenchido. Leia antes de incorporar e una apenas as seções pertinentes aos arquivos existentes. Remova campos/seções inaplicáveis e confira que nenhum placeholder ou caminho inexistente reste no material entregue como pronto.

## 4. Consulta em cada tarefa de UI

Configure os ponteiros persistentes para alcançar a skill local e as regras ao criar/alterar telas, componentes, estilos, tema, motion ou assets. As regras mandam ler a versão vigente do contrato e localizar tokens/APIs antes de editar. Retome a consulta no início de uma nova tarefa, após compaction/handoff quando o contexto faltar e quando as fontes mudarem; não dependa só da memória da conversa.

Reutilize o que existir e escolha estados/layout/movimento dentro do contrato. Criar uma variante ou composição compatível é rotina; trocar marca, fonte principal, papéis de cor, tema global ou padrão transversal exige que a mudança faça parte do pedido ou da delegação. Esclareça apenas conflitos materiais ainda não resolvidos. Registre exceções locais com motivo, alcance e critério de revisão, em vez de aceitar desvios silenciosos.

Quando uma mudança material estiver autorizada, atualize a fonte canônica, os tokens afetados, os exemplos relevantes e os adaptadores gerados, com a versão/decisão registrada. Verifique os consumidores e o material de Stitch; o contrato não deve permanecer descrevendo a identidade anterior. Diretrizes de gosto genéricas de outra skill entram somente se forem compatíveis com esse projeto.

## 5. Verificar aderência

Instruções persistentes ajudam a manter a direção; complemente-as com checks reais do projeto. Se já houver lint de tokens, estilos, restrição de imports ou catálogo, reutilize-o. Crie uma regra proporcional somente quando houver um risco concreto e compatibilidade com a stack. Uma busca indiscriminada por todo número/hex não prova desvio: valores de dados, geometria e literais estruturais podem ser válidos. Registre checks ausentes sem simular sucesso.

Antes da entrega, faça a passagem de [05](05-revisar-corrigir-entregar.md) e confira:

- Caminhos do contrato, tokens, componentes, regras e skills realmente existentes; entradas ativas e imports resolvidos sem ciclos ou vínculos à máquina do autor.
- Regras específicas não conflitam com instruções preservadas; os adaptadores consultam a mesma versão e o recorte de adoção está claro.
- Fontes/papéis cromáticos/spacing/motion da implementação correspondem ao contrato; componentes reutilizados e exceções identificadas.
- Tarefas centrais, temas/layouts afetados, estados, dados e movimento reduzido continuam corretos; desvios involuntários são corrigidos e revalidados.
- Material portátil pode ser usado sem a conversa original; Stitch preparado, importado e aplicado são estados registrados separadamente.

Quando a ferramenta nativa estiver disponível, confirme a descoberta das instruções/skill numa sessão nova pelo mecanismo documentado. Sem essa execução, relate “arquivos preparados e conferidos”, não “integração nativa comprovada”. Uma skill ou documento sozinho não garante aderência visual absoluta; a entrega se apoia também na conferência do resultado.

Entregue contrato e versão, mapa dos caminhos/consumidores, entradas preparadas, decisões/exceções, checks e evidências. Mantenha a instalação global, publicação e importação externa separadas quando ainda não solicitadas.
