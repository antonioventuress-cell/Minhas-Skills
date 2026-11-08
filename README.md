# Minhas Skills

Minha biblioteca pessoal de skills para usar em diferentes computadores. São cópias dos arquivos originais, incluindo scripts, referências, dados e licenças disponíveis nas fontes.

## Catálogo

| Coleção / skill | Uso | Local |
| --- | --- | --- |
| Superpowers — 15 skills | Planejamento, debugging, testes, revisão e execução | `skills/brainstorming`, `skills/systematic-debugging` e demais skills da coleção |
| Frontend Design | Layout, tipografia e identidade visual | [frontend-design](skills/frontend-design/SKILL.md) |
| UI UX Pro Max | Estilos, cores, fontes e padrões de interface | [ui-ux-pro-max](skills/ui-ux-pro-max/SKILL.md) |
| Web Design Guidelines | Revisão de acessibilidade e experiência de uso | [web-design-guidelines](skills/web-design-guidelines/SKILL.md) |
| React Best Practices | Desempenho de React e Next.js | [react-best-practices](skills/react-best-practices/SKILL.md) |
| Webapp Testing | Testes no navegador com Playwright | [webapp-testing](skills/webapp-testing/SKILL.md) |
| Skill Creator | Criar, melhorar e avaliar skills | [skill-creator](skills/skill-creator/SKILL.md) |
| MCP Builder | Criar integrações com ferramentas e serviços | [mcp-builder](skills/mcp-builder/SKILL.md) |
| Canvas Design | Pôsteres e peças gráficas | [canvas-design](skills/canvas-design/SKILL.md) |
| Documentos — 4 skills | PDF, Word, Excel e PowerPoint | `skills/pdf`, `skills/docx`, `skills/xlsx`, `skills/pptx` |
| Remotion — 13 skills | Vídeos, animações, legendas e renderização | [remotion-best-practices](skills/remotion-best-practices/SKILL.md) e demais skills `remotion-*` |

Total: **40 skills**. Os nomes completos por coleção estão em [fontes.lock.json](fontes.lock.json).

## Em outro computador

Para baixar a biblioteca:

```bash
git clone https://github.com/antonioventuress-cell/Minhas-Skills.git
cd Minhas-Skills
```

Para atualizar uma cópia existente, sem alterações locais pendentes:

```bash
git pull --ff-only
```

Ter os arquivos no computador é diferente de ativar as skills no agente. Uma opção, com Node.js e npm instalados, é usar o CLI Skills:

```bash
# Ver as skills que o instalador encontra:
npx skills add antonioventuress-cell/Minhas-Skills --list

# Instalar uma skill, escolhendo o agente no instalador:
npx skills add antonioventuress-cell/Minhas-Skills --skill frontend-design

# Instalar todas, escolhendo o agente no instalador:
npx skills add antonioventuress-cell/Minhas-Skills
```

Esses comandos de instalação são orientações para outros computadores; não foram executados nesta importação. Consulte o instalador para selecionar instalação por projeto ou global. Também é possível copiar as pastas completas para o diretório de skills documentado pelo seu agente.

Para Codex, uma instalação manual por usuário pode colocar as pastas escolhidas em `~/.agents/skills/`; para Claude Code, em `~/.claude/skills/`. Preserve arquivos de apoio e evite sobrescrever uma skill já personalizada. Abra uma nova sessão para o agente descobrir as skills instaladas.

## Dependências e caminhos

Cada `SKILL.md` descreve como usar a skill. Scripts podem exigir Python, Node.js, Playwright, ferramentas de documentos ou um projeto Remotion. As dependências específicas devem ser instaladas quando a skill for usada.

Os arquivos originais foram preservados. Exemplos que mencionam caminhos de plugins, como `${CLAUDE_PLUGIN_ROOT}`, devem ser ajustados na invocação para a localização real da skill. Por exemplo, a pesquisa local de UI UX Pro Max pode ser executada da raiz desta biblioteca:

```bash
python3 skills/ui-ux-pro-max/scripts/search.py "saas dashboard" --design-system
```

A cópia das skills Superpowers não instala automaticamente os hooks e a integração do plugin original. Para essa experiência, siga o README da fonte em `origens/superpowers/README.md`.

## Fontes, versões e licenças

- [Superpowers](https://github.com/obra/superpowers)
- [Anthropic Skills](https://github.com/anthropics/skills)
- [Vercel Agent Skills](https://github.com/vercel-labs/agent-skills)
- [Remotion Skills](https://github.com/remotion-dev/skills)
- [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)

Os commits de origem e os hashes SHA-256 dos arquivos importados estão em [fontes.lock.json](fontes.lock.json). Os READMEs, avisos e licenças de raiz disponíveis estão em [origens](origens/); licenças internas acompanham as respectivas skills. Cada conteúdo mantém os termos da fonte, sem uma licença única imposta por esta biblioteca. O uso do Remotion também está sujeito aos termos do produto.

As cópias são fixas: atualizar esta biblioteca com `git pull` recebe o que foi salvo aqui, sem sincronizar automaticamente os cinco projetos de origem.
