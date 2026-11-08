# Coleções adicionais

Os arquivos versionados destas sete fontes foram copiados com sua estrutura original, sem repositórios Git internos. Isso mantém scripts, referências, licenças, configurações de plugins e links simbólicos relativos juntos. As versões e os hashes estão em [fontes.lock.json](../fontes.lock.json).

| Coleção | Arquivos SKILL.md | Uso | Caminhos principais |
| --- | ---: | --- | --- |
| [Supabase](supabase/README.md) | 2 | Supabase e boas práticas de PostgreSQL | `supabase/skills/` |
| [Expo](expo/README.md) | 25 | Aplicativos Android/iOS, interfaces, animações, builds e publicação | `expo/plugins/expo/skills/` |
| [OpenAI](openai/README.md) | 44 | Inclui Playwright, implementação de Figma e segurança, além das demais skills da coleção | `openai/skills/.curated/` |
| [Trail of Bits](trailofbits/README.md) | 98 | Auditoria de segurança, revisão de código e testes especializados | `trailofbits/plugins/<plugin>/skills/` |
| [Marketing](marketing/README.md) | 53 | Copywriting, SEO, anúncios, conversão, preços e lançamentos | `marketing/skills/` |
| [Hugging Face](huggingface/README.md) | 26 | Modelos de IA, datasets, treinamento, execução local e Gradio | `huggingface/skills/` e `huggingface/hf-mcp/skills/` |
| [Microsoft](microsoft/README.md) | 210 | Azure, agentes, SDKs, arquitetura e integrações | `microsoft/.github/plugins/<plugin>/skills/` e `microsoft/.github/skills/` |

São **458 novos arquivos `SKILL.md`**, além dos 40 da seleção inicial. A contagem inclui a skill interna de avaliação do Expo e duas fixtures de testes do Trail of Bits; essas três definições auxiliares não são recomendações para instalação. Os demais arquivos podem incluir variações e skills especializadas em diferentes linguagens.

## Usar em outro computador

Clone esta biblioteca ou execute `git pull --ff-only` na sua cópia sem alterações pendentes. A organização dos plugins varia por fonte; siga o README da coleção para instalar a skill ou o plugin no agente escolhido. Arquivos ocultos, como `.github` e `.curated`, fazem parte dessas coleções e devem ser preservados.

Para consultar uma skill, abra seu `SKILL.md`. Para instalação manual, copie a pasta inteira com referências e scripts, verificando as dependências entre skills. Hooks e integrações de plugin precisam do procedimento da fonte; copiar arquivos não os ativa automaticamente.

O instalador genérico pode não descobrir todas as skills nas pastas ocultas ou nos plugins. Para esses casos, use as instruções da coleção ou a instalação manual do agente. Não instale as fixtures de testes.

## Limites desta cópia

- As skills foram arquivadas, sem ativação no ambiente ou execução dos seus instaladores e hooks.
- Os hashes e links simbólicos foram verificados; os fluxos de cada produto não foram testados nesta importação.
- Dependências, contas, ferramentas externas e serviços pagos podem ser necessários conforme a skill.
- O submódulo `expo/eval-harness`, usado pelo projeto de origem para avaliações, não foi baixado. Sua revisão está registrada no manifesto. Para desenvolver o avaliador do Expo, use um clone da fonte com esse submódulo.
- A fonte Microsoft contém 10 links simbólicos sem destino no plugin `microsoft-foundry`; foram preservados como na origem e estão registrados em `upstream_broken_symlinks` no manifesto. Esses atalhos não funcionam nesta versão; consulte as skills presentes no catálogo Microsoft em vez de usar esses atalhos.
- Os conteúdos mantêm as licenças e os termos das respectivas fontes. Arquivos de configuração e workflows dentro das coleções são referências das fontes.

## Fontes

- https://github.com/supabase/agent-skills
- https://github.com/expo/skills
- https://github.com/openai/skills
- https://github.com/trailofbits/skills
- https://github.com/coreyhaines31/marketingskills
- https://github.com/huggingface/skills
- https://github.com/microsoft/skills
