# Origem da PP Desing unificada (2.3.0)

Unificação feita em 20/11/2026 a pedido do Pedro, para que Claude Code, Codex/ChatGPT e Gemini passem a usar uma única versão hospedada na BASE OS. As três instalações originais **não foram alteradas**; um snapshot fiel de cada uma está em `<BASE OS>/backups/pp-desing-2026-11-20/` (com `manifesto.json` de hashes SHA-256).

## Fontes comparadas

| Cópia | Caminho original | Arquivos | Última modificação | Observação |
| --- | --- | --- | --- | --- |
| A — Claude Code | `~/.claude/skills/pp-desing` | 13 | 15/10/2026 | 2.1.1 do Codex + adaptações para Claude (descrição ampla, `argument-hint`, seção "Execução no Claude Code"); CRLF |
| B — Codex/ChatGPT | `~/.agents/skills/pp-desing` | 27 | 03/11/2026 | 2.2.0 com `organization_revision` 2026-10-23, módulos `organizacao-*`, reprodução por URL e avisos de licença; LF. Idêntica à skill do pacote `pp-desing-github` |
| C — Gemini | `~/.gemini/config/plugins/migrated-settings/skills/pp-desing` | 13 | 14/11/2026 (só SKILL.md) | Cópia migrada de A. 12 arquivos idênticos por hash; `SKILL.md` difere apenas no fim de linha de 3 linhas do frontmatter (CRLF→LF) — conteúdo igual a A |

## Resultado da comparação A × B

| Classe | Arquivos |
| --- | --- |
| Idênticos | `assets/project-handoff/*` (4), `references/03-integrar-validar.md`, `04-kit-motion.md`, `06-aplicar-manter-padroes.md` |
| Só em B | `references/organizacao-{adaptacao,briefing,conteudo,evolucao,movimento,perfis,proveniencia,refinamento,sistema}.md`, `references/reproducao-por-url.md`, `references/avisos/*` (4) |
| Só em A | nenhum arquivo (só conteúdo dentro de `SKILL.md`) |
| Divergentes | `SKILL.md`, `agents/openai.yaml`, `references/00`, `01`, `02`, `05` — B é a mais recente (03/11) em todos |

## Decisões de merge

- **Base estrutural = B** (mais nova e mais completa). Todas as referências, módulos `organizacao-*`, `reproducao-por-url.md` e avisos de licença vieram de B sem alteração.
- **`references/01`, `02`, `05`:** versão B. Em 01 e 05, B é superconjunto de A (acrescenta a reprodução por link). Em 02 e 05, B trocou "sempre animar" por "movimento conforme a estratégia" (na reprodução fiel, só movimento observado ou pedido); é a regra mais nova e coerente com `reproducao-por-url.md`.
- **`references/00`:** texto de B + a frase de A "Inferir a estratégia de uma instrução clara evita repetir perguntas" e o exemplo "melhore este projeto" → evolução, que B tinha perdido.
- **`SKILL.md`:**
  - descrição nova cobre os dois usos (descrição ampla de A + reprodução por link de B; 657 caracteres);
  - `argument-hint` de A mantido (usado pelo Claude Code; os outros agentes ignoram);
  - estrutura de B (Contexto e decisão, tabela de rotas, módulos de interface);
  - rotas de A que B tinha condensado voltaram à tabela ("Fluxo completo", integração só quando pedida, handoff sem modificar outro repositório);
  - os 10 contratos de A e os 4 limites de B viraram 8 contratos sem perda de regra (ferramentas/versões reais, preservação da origem, política de arquivamento, continuidade via 06);
  - seção **"Execução no Claude Code"** de A mantida integralmente, como pedia a memória do Claude ("mesclar essa seção em vez de sobrescrever");
  - nova seção curta **"Na BASE OS"** (consultar os design systems registrados no catálogo);
  - entrega/verificação: B + critérios de A (segunda passagem sem regressões, resultado parcial).
- **`agents/openai.yaml`:** prompt e descrição curta combinam criar/aplicar (A) e reproduzir por link (B).
- **Fim de linha:** LF em todos os arquivos (padrão das edições de 03/11 e do pacote GitHub; os arquivos de 14/10 em B e toda a cópia A estavam em CRLF). Conteúdo conferido idêntico ignorando CR. Claude, Codex e Gemini leem ambos.
- **Versão:** 2.3.0; `organization_revision` 2026-10-23 preservada.

## Fora do pacote (referência)

O pacote GitHub de 03/11 (`pp-desing-github` e `pp-desing-2.2.0-github.zip`) tem também `README.md`, o exemplo `exemplos/oficina-da-dobra` e `scripts/verificar.py`. Eles não fazem parte de nenhuma instalação e não foram copiados; os links desta versão foram conferidos com a mesma lógica do `verificar.py` (55 links internos, nenhum ausente). Pendências herdadas de B: licença própria da PP Desing e conferência de atribuição de algumas fontes (ver `references/organizacao-proveniencia.md`).
