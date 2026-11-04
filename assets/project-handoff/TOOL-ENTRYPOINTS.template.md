# Entradas de ferramentas — template

Leia os arquivos existentes antes de incorporar os trechos. Substitua campos `{{...}}`, ajuste caminhos relativos ao arquivo de entrada e preserve instruções preexistentes. Estes exemplos pressupõem entradas na raiz; adaptação para arquivo aninhado deve corrigir os paths. Inclua somente ferramentas escolhidas.

## Codex — seção em AGENTS.md ou arquivo ativo

```markdown
## Design e alterações de UI

Ao criar/alterar telas, componentes, estilos, tema, motion ou assets, leia `{{RULES_PATH}}`, `{{PROJECT_DESIGN_PATH}}` e `.agents/skills/project-design/SKILL.md`. Reutilize os tokens/APIs indicados e confira aderência antes de entregar. Caminhos são relativos à raiz do projeto; siga o alcance e as decisões registrados no contrato.
```

Se houver override ativo, acrescente a seção nele em vez de confiar num `AGENTS.md` ignorado. Preserve a hierarquia e as instruções não relacionadas.

## Claude Code — seção/import em CLAUDE.md

```markdown
## Design e alterações de UI

@{{RULES_PATH}}

Ao trabalhar na interface, leia `{{PROJECT_DESIGN_PATH}}` e `.claude/skills/project-design/SKILL.md`. Reutilize as fontes canônicas e cumpra a verificação de aderência das regras compartilhadas.
```

Imports `@path` são relativos ao arquivo importador. Se criar um novo `CLAUDE.md` e as instruções de projeto estiverem em `AGENTS.md`, preserve esse contexto com `@AGENTS.md` na raiz ou o caminho relativo correto; não importe um arquivo ausente nem crie ciclos. Preserve imports/regras existentes. Quando usar `.claude/rules/`, escolha o escopo aplicável em vez de duplicar a identidade.

## Stitch — instrução para aplicação do sistema

```text
Use o design system {{DESIGN_SYSTEM_NAME}} na versão {{DESIGN_VERSION}},
derivado do contrato {{PROJECT_DESIGN_PATH}} e dos tokens {{TOKENS_PATH}}.
Considere as referências fornecidas e preserve os papéis de cor, tipografia,
layout, componentes/estados e motion especificados. A nova tela deve cumprir
{{SCREEN_TASK_AND_CONSTRAINTS}}. Registre extensões inferidas e confira
o resultado contra o sistema antes de exportar.
```

Prepare o documento no formato nativo vigente e importe/associe o sistema somente se essa ação estiver solicitada. Para telas novas, confira o sistema padrão; para existentes, confira cada tela do recorte solicitado. Anexe/upload os materiais pelo recurso disponível; um caminho local no prompt não fornece seu conteúdo. Registre se o material está apenas preparado, importado ou aplicado.
