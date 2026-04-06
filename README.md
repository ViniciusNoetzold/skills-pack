# 🧠 Skills Pack — Claude Code

> Coleção curada de **39 skills** para o [Claude Code](https://claude.ai/product/claude-code), organizadas por categoria e prontas para uso imediato.

---

## 📦 O que são Skills?

Skills são arquivos de instrução (`SKILL.md`) que ensinam o Claude Code a seguir metodologias, padrões e boas práticas específicas durante o desenvolvimento. Ao instalar uma skill, o agente passa a aplicar aquele conhecimento automaticamente nos seus projetos.

---

## 📂 Onde as Skills ficam na máquina?

As skills **não ficam dentro do projeto** — elas ficam em uma pasta da sua máquina. Existem dois locais:

| Local | Caminho | Disponibilidade |
|-------|---------|-----------------|
| **Pessoal** | `~/.claude/skills/` | Todos os seus projetos |
| **Por projeto** | `.claude/skills/` (dentro do repo) | Só aquele projeto |

**No Windows:**
```
C:\Users\SeuUsuario\.claude\skills\
```

**No Mac/Linux:**
```
~/.claude/skills/
```

> 💡 **Recomendação:** Use a pasta pessoal para ter as skills disponíveis em todos os projetos.

---

## 🚀 Como instalar no Claude Code

### Pré-requisito
- [Claude Code](https://claude.ai/product/claude-code) instalado
- Node.js 18+

---

### Método 1 — Instalar via npx (mais fácil)

```bash
npx skills add https://github.com/ViniciusNoetzold/skills-pack --skill nome-da-skill
```

**Exemplo:**
```bash
npx skills add https://github.com/ViniciusNoetzold/skills-pack --skill systematic-debugging
```

---

### Método 2 — Copiar manualmente para a pasta do Claude Code

**1. Clone este repositório:**
```bash
git clone https://github.com/ViniciusNoetzold/skills-pack.git
```

**2. Crie a pasta de skills (se não existir):**

Windows (Git Bash):
```bash
mkdir -p ~/.claude/skills
```

Mac/Linux:
```bash
mkdir -p ~/.claude/skills
```

**3. Copie as skills que quiser:**

```bash
# Copiar uma skill específica
cp -r skills-pack/systematic-debugging ~/.claude/skills/

# Copiar todas as skills de uma vez
cp -r skills-pack/*/  ~/.claude/skills/
```

**4. Reinicie o Claude Code** — ele detecta as skills automaticamente na próxima sessão.

---

### Método 3 — Instalar todas de uma vez via script

```bash
git clone https://github.com/ViniciusNoetzold/skills-pack.git
cd skills-pack
mkdir -p ~/.claude/skills
for dir in */; do
  skill="${dir%/}"
  [ -f "$skill/SKILL.md" ] && cp -r "$skill" ~/.claude/skills/
done
echo "✅ Skills instaladas em ~/.claude/skills/"
```

> No Windows use o **Git Bash** para rodar esse script.

---

## ✅ Como verificar se as skills foram instaladas

Abra o Claude Code e pergunte:

```
Quais skills você tem disponíveis?
```

O Claude vai listar todas as skills que encontrar na pasta `~/.claude/skills/`.

---

## 💡 Como usar uma skill

As skills são ativadas **automaticamente** quando o Claude detecta que a situação se aplica. Você também pode invocar manualmente:

```
Use a skill systematic-debugging para investigar esse erro
```

```
Aplique a skill test-driven-development nesse novo módulo
```

---

## 🗑️ Como remover uma skill

Basta deletar a pasta da skill:

```bash
rm -rf ~/.claude/skills/nome-da-skill
```

---

## 📋 Skills disponíveis

### 🎨 Frontend & Design
| Skill | Descrição |
|-------|-----------|
| `frontend-design` | Interfaces production-grade com identidade visual forte |
| `vercel-react-best-practices` | Boas práticas React: componentes, performance e patterns modernos |
| `web-design-guidelines` | Diretrizes de design web: layout, hierarquia e responsividade |
| `tailwind-design-system` | Sistema de design com Tailwind CSS |
| `shadcn` | Componentes com Radix UI + Tailwind (shadcn/ui oficial) |
| `typescript-advanced-types` | Tipos avançados TypeScript: generics e utility types |

### 📱 Mobile
| Skill | Descrição |
|-------|-----------|
| `building-native-ui` | UI nativa com Expo: componentes, navegação e animações |
| `expo-tailwind-setup` | Configuração de Tailwind/NativeWind em projetos Expo |
| `native-data-fetching` | Data fetching em apps nativos: caching e offline |
| `expo-deployment` | Deploy de apps Expo para App Store e Google Play |
| `expo-cicd-workflows` | Pipelines CI/CD para apps Expo |
| `react-native-skills` | Padrões e performance em React Native |
| `swiftui-expert-skill` | SwiftUI avançado para iOS/macOS |

### ⚙️ Back-end
| Skill | Descrição |
|-------|-----------|
| `nodejs-backend-patterns` | Arquitetura Node.js: clean architecture e APIs |
| `api-design-principles` | Design de APIs RESTful: versionamento e boas práticas |
| `better-auth-best-practices` | Autenticação com Better Auth: OAuth, sessions e MFA |
| `next-best-practices` | Next.js: App Router, Server Components e caching |
| `python-performance` | Otimização Python: profiling, async e estruturas eficientes |

### 🗄️ Banco de Dados
| Skill | Descrição |
|-------|-----------|
| `supabase-postgres-best-practices` | PostgreSQL com Supabase: RLS e queries otimizadas |
| `neon-postgres` | Postgres serverless com Neon: branching e autoscaling |
| `database-schema-design` | Design de schemas: normalização e estratégias de migração |

### 🔒 Segurança & Acessibilidade
| Skill | Descrição |
|-------|-----------|
| `security-best-practices` | OWASP Top 10, sanitização e headers de segurança |
| `web-accessibility` | WCAG 2.1: ARIA, navegação por teclado e contraste |

### 🤖 Automação & DevOps
| Skill | Descrição |
|-------|-----------|
| `github-actions-docs` | GitHub Actions: workflows, jobs e secrets |
| `dispatching-parallel-agents` | Orquestração de agentes em paralelo |
| `executing-plans` | Execução estruturada de planos de desenvolvimento |

### 🧪 Qualidade de Código
| Skill | Descrição |
|-------|-----------|
| `systematic-debugging` | Metodologia em 4 fases: causa raiz → padrão → hipótese → fix |
| `test-driven-development` | TDD: escrever testes antes de implementar |
| `webapp-testing` | Testes web: unitários, integração e E2E |
| `playwright-best-practices` | Testes E2E com Playwright: page objects e fixtures |
| `requesting-code-review` | Como conduzir code reviews eficientes |
| `verification-before-completion` | Verificação sistemática antes de concluir uma tarefa |
| `skill-creator` | Como criar e otimizar novas skills |

### 📝 Texto, Docs & Planejamento
| Skill | Descrição |
|-------|-----------|
| `writing-plans` | Planejamento estruturado antes de executar |
| `doc-coauthoring` | Co-autoria de documentos com consistência de estilo |
| `documentation-writer` | Geração de documentação a partir de código |
| `mcp-builder` | Criação de servidores MCP para integrar ferramentas |
| `find-skills` | Localiza skills relevantes para a tarefa em andamento |
| `brainstorming` | Refinamento de ideias antes de escrever código |

---

## 🔄 Atualizar as skills

```bash
cd skills-pack
git pull
cp -r */  ~/.claude/skills/
```

---

## 📚 Fontes

Todas as skills foram coletadas de [skills.sh](https://skills.sh) — o diretório oficial de skills para agentes de IA.

---

*Mantido por [@ViniciusNoetzold](https://github.com/ViniciusNoetzold)*
