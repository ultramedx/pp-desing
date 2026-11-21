# pp-desing

Skill para **Claude Code**, **Codex** e **Gemini** que transforma referências (links, prints, pastas ou exports HTML/Stitch) em telas, páginas, protótipos e design systems verificáveis — inclusive reprodução fiel a partir de um link — com briefing, decisões registradas e revisão antes da entrega.

**Mentoria MedMagno** · Mentor **Pedro P.**

Versão atual: **2.3.0** · Licença [MIT](LICENSE)

## Instalar

### Opção 1 — baixar o pacote

1. Baixe [`pp-desing.zip`](https://github.com/ultramedx/pp-desing/releases/latest/download/pp-desing.zip).
2. Extraia a pasta `pp-desing/` na pasta de skills da sua ferramenta:
   - Claude Code: `~/.claude/skills/pp-desing/`
   - Codex: a pasta de skills indicada na documentação atual do Codex (no repositório: `.agents/skills/pp-desing/`).
   - Gemini: a pasta de skills indicada na documentação vigente do Gemini.
3. Confirme que o arquivo final está em `.../pp-desing/SKILL.md` e abra uma sessão nova.

### Opção 2 — clonar

```bash
git clone https://github.com/ultramedx/pp-desing.git ~/.claude/skills/pp-desing
```

## Usar

Comece o pedido chamando a skill pelo nome:

```text
Use a skill pp-desing para criar uma página para [público] usando [URL] como referência.
Preserve a hierarquia visual e adapte o texto para ensinar [tema].
Entregue uma versão local e confira o resultado em 390 px e 1440 px.
```

A skill define a estratégia (**inspirado**, **fiel** ou **evolução**), o modo de participação (**colaborativo** ou **autônomo**) e segue a rota adequada à entrega.

| Rota | Guia | Entrega |
| --- | --- | --- |
| Briefing e decisões | `references/00-briefing-e-decisoes.md` | escopo, estratégia e participação |
| Preparar a base | `references/01-preparar-base.md` | `BASE-DESING/` |
| Gerar o design | `references/02-gerar-export.md` | `design-system-export/` |
| Integrar e validar | `references/03-integrar-validar.md` | integração com evidências |
| Kit de identidade e motion | `references/04-kit-motion.md` | assets e templates para vídeo |
| Revisar e entregar | `references/05-revisar-corrigir-entregar.md` | revisão, correções e movimento |
| Aplicar e manter | `references/06-aplicar-manter-padroes.md` | `DESIGN.md`, entradas de Claude Code, Codex e Stitch |

A reprodução fiel a partir de um link está em `references/reproducao-por-url.md`. O histórico da versão está em [CHANGELOG.md](CHANGELOG.md).

## Estrutura

```text
SKILL.md                     # ponto de entrada da skill
CHANGELOG.md                 # histórico de versões
ORIGEM.md                    # unificação 2.3.0 e decisões de merge
CREDITOS.md                  # créditos, inspirações e ressalvas
LICENSE                      # licença MIT
README.md                    # este guia
references/                  # guias de cada rota, módulos de organização, reprodução por URL e avisos
assets/project-handoff/      # templates de DESIGN.md, regras e skill local
agents/openai.yaml           # metadados para o Codex
```

## Licença e créditos

Criada por **Pedro P.** para a **Mentoria MedMagno** e distribuída sob a [licença MIT](LICENSE).

A skill se inspira nas documentações públicas do Claude Code (Anthropic), do Codex (OpenAI), do Stitch e da especificação `design.md` (Google) e nas WCAG 2.2 (W3C). As fontes, os créditos e as ressalvas sobre marcas e materiais de terceiros estão em [CREDITOS.md](CREDITOS.md).
