# Skills Pack — 46 skills para Cursor

Pacote de skills extraídas do ambiente Claude, convertidas em arquivos `.md` independentes prontos para serem usados como **regras**, **docs** ou **context files** no Cursor.

---

## Como usar no Cursor

Existem três modos de consumir estes arquivos, dependendo do seu fluxo:

### 1. Como Cursor Rules (`.cursor/rules/`)
Para transformar uma skill em regra ativa no projeto, copie o `.md` para `.cursor/rules/` e adicione um cabeçalho YAML de regra. Exemplo:

```markdown
---
description: Arquitetura de soluções de IA end-to-end
globs: ["**/*.ts", "**/*.py"]
alwaysApply: false
---

<conteúdo original da skill aqui>
```

O Cursor aplicará a regra automaticamente quando os `globs` corresponderem, ou sob demanda via `@regra`.

### 2. Como Docs referenciáveis com `@Docs`
Cole a pasta em um diretório do projeto (ex: `docs/skills/`) e referencie diretamente no chat:
```
@docs/skills/02-usuario/rag-research-scientist.md aplique isso ao pipeline do Theia
```

### 3. Como `.cursorrules` único (legado)
Escolha 1–3 skills mais relevantes, concatene em um único `.cursorrules` na raiz do projeto. Útil para projetos focados.

---

## Estrutura do pacote

```
skills_pack/
├── 01-publicas/    (8 skills oficiais Anthropic)
├── 02-usuario/     (28 skills pessoais)
└── 03-exemplos/    (10 skills de referência)
```

---

## Índice completo

### 📦 01-publicas/ — Anthropic oficiais
Manipulação de arquivos, leitura e design.

- `docx.md` — Criação/edição de documentos Word
- `pdf.md` — Manipulação de PDFs (criar, merge, split, OCR, formulários)
- `pptx.md` — Apresentações PowerPoint
- `xlsx.md` — Planilhas (.xlsx, .csv, .tsv)
- `frontend-design.md` — UIs frontend de alta qualidade
- `file-reading.md` — Roteador de leitura de arquivos uploaded
- `pdf-reading.md` — Extração de conteúdo de PDFs
- `product-self-knowledge.md` — Conhecimento oficial Claude Code/API/Claude.ai

### 🎯 02-usuario/ — Skills pessoais (Rony)

**Estratégia de Produto & Negócio**
- `chief-ai-product-strategist.md`
- `business-model-unit-economics-designer.md`
- `economic-reality-engineer.md`
- `meta-strategic-thinker.md`
- `exponential-technology-strategist.md`
- `product-experimentation-and-decision-scientist.md`
- `research-to-product-translator.md`
- `executive-technical-synthesis-advisor.md`
- `reality-execution-warfare-specialist.md`

**Arquitetura & Engenharia de IA**
- `ai-solution-architect.md`
- `agentic-systems-designer.md`
- `rag-research-scientist.md`
- `llm-systems-engineer.md`
- `local-ai-ollama-infra-engineer.md`
- `machine-learning-applied-scientist.md`
- `software-engineering-lead-for-ai-products.md`
- `domain-driven-design-strategist.md`
- `observability-and-evaluation-engineer-for-ai.md`

**Governança, Segurança & Transformação**
- `ai-governance-risk-architect.md`
- `security-privacy-and-intellectual-property-guardian.md`
- `enterprise-innovation-digital-transformation-advisor.md`
- `safe-scaling-delivery-orchestrator.md`
- `especialista-licitacoes.md`

**Humano, Aprendizado & UX**
- `human-centered-ai-ux-designer.md`
- `neuro-decision-architect.md`
- `human-behavior-systems-thinker.md`
- `learning-architect-g4-cognitive-learning-systems.md`
- `meta-cognitive-learning-system-designer.md`

### 🧪 03-exemplos/ — Referência Anthropic
- `algorithmic-art.md`
- `brand-guidelines.md`
- `canvas-design.md`
- `doc-coauthoring.md`
- `internal-comms.md`
- `mcp-builder.md`
- `skill-creator.md`
- `slack-gif-creator.md`
- `theme-factory.md`
- `web-artifacts-builder.md`

---

## Observações

- Todos os arquivos preservam o **frontmatter YAML original** (`name`, `description`) usado pelo sistema de skills da Anthropic. Isso é compatível com o Cursor, que trata esse bloco como metadata.
- Algumas skills (`docx`, `pptx`, `xlsx`, `pdf`, `frontend-design`) originalmente referenciam scripts auxiliares em subpastas — essas referências internas **não foram incluídas**; apenas o `SKILL.md` principal. Para o uso típico no Cursor isso basta (o texto descreve o comportamento esperado).
- Para projetos específicos, recomendo combinar 2–4 skills por projeto em vez de carregar todas — evita ruído no contexto.

_Gerado em 18 de abril de 2026._
