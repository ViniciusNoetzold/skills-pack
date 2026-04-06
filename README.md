# 🧠 Skills Pack — Claude Code

> Coleção curada de **39 skills** para o [Claude Code](https://claude.ai/product/claude-code), organizadas por categoria e prontas para uso imediato.

---

## 📦 O que são Skills?

Skills são arquivos de instrução (`SKILL.md`) que ensinam o Claude Code a seguir metodologias, padrões e boas práticas específicas durante o desenvolvimento. Ao instalar uma skill, o agente passa a aplicar aquele conhecimento automaticamente nos seus projetos.

---

## 🚀 Como instalar no Claude Code

### Requisito
- [Claude Code](https://claude.ai/product/claude-code) instalado
- Node.js 18+

### Opção 1 — Instalar skill direto deste repositório

```bash
npx skills add https://github.com/ViniciusNoetzold/skills-pack --skill nome-da-skill
```

**Exemplo:**
```bash
npx skills add https://github.com/ViniciusNoetzold/skills-pack --skill systematic-debugging
```

### Opção 2 — Clonar e instalar localmente

```bash
# 1. Clonar o repositório
git clone https://github.com/ViniciusNoetzold/skills-pack.git

# 2. Instalar uma skill específica apontando para a pasta local
npx skills add ./skills-pack --skill systematic-debugging
```

### Opção 3 — Instalar todas as skills de uma vez

```bash
git clone https://github.com/ViniciusNoetzold/skills-pack.git
cd skills-pack

# Instalar todas
for dir in */; do
  skill="${dir%/}"
  [ "$skill" != "skills-lock.json" ] && npx skills add . --skill "$skill"
done
```

---

## 📋 Skills disponíveis

### 🎨 Frontend & Design
| Skill | Descrição |
|-------|-----------|
| `frontend-design` | Interfaces production-grade com identidade visual forte, evitando padrões genéricos de IA |
| `vercel-react-best-practices` | Boas práticas React segundo a Vercel: componentes, performance e patterns modernos |
| `web-design-guidelines` | Diretrizes de design web: layout, hierarquia visual, responsividade e acessibilidade |
| `tailwind-design-system` | Sistema de design com Tailwind CSS: tokens, componentes e consistência visual |
| `shadcn` | Componentes acessíveis e customizáveis com Radix UI + Tailwind (shadcn/ui oficial) |
| `typescript-advanced-types` | Tipos avançados TypeScript: generics, utility types e discriminated unions |

### 📱 Mobile
| Skill | Descrição |
|-------|-----------|
| `building-native-ui` | Construção de UI nativa com Expo: componentes, navegação e animações |
| `expo-tailwind-setup` | Configuração de Tailwind/NativeWind em projetos Expo |
| `native-data-fetching` | Data fetching em apps nativos: caching, offline e error handling |
| `expo-deployment` | Deploy de apps Expo para App Store e Google Play |
| `expo-cicd-workflows` | Pipelines CI/CD para apps Expo: builds automáticos e publicação |
| `react-native-skills` | Skills de React Native: navegação, performance e padrões de desenvolvimento |
| `swiftui-expert-skill` | Desenvolvimento SwiftUI avançado para iOS/macOS |

### ⚙️ Back-end
| Skill | Descrição |
|-------|-----------|
| `nodejs-backend-patterns` | Arquitetura Node.js: clean architecture, middleware e estrutura de APIs |
| `api-design-principles` | Design de APIs RESTful: versionamento, idempotência e paginação |
| `better-auth-best-practices` | Autenticação moderna com Better Auth: sessions, OAuth e MFA |
| `next-best-practices` | Boas práticas Next.js: App Router, Server Components, caching e streaming |
| `python-performance` | Otimização de performance em Python: profiling, async e estruturas eficientes |

### 🗄️ Banco de Dados
| Skill | Descrição |
|-------|-----------|
| `supabase-postgres-best-practices` | PostgreSQL com Supabase: RLS, queries otimizadas e índices |
| `neon-postgres` | Postgres serverless com Neon: branching de banco e autoscaling |
| `database-schema-design` | Design de schemas: normalização, relacionamentos e estratégias de migração |

### 🔒 Segurança & Acessibilidade
| Skill | Descrição |
|-------|-----------|
| `security-best-practices` | Segurança em aplicações: OWASP Top 10, sanitização e headers de segurança |
| `web-accessibility` | Acessibilidade web (WCAG 2.1): ARIA, navegação por teclado e contraste |

### 🤖 Automação & DevOps
| Skill | Descrição |
|-------|-----------|
| `github-actions-docs` | Criação e documentação de GitHub Actions: workflows, jobs e secrets |
| `dispatching-parallel-agents` | Orquestração de agentes em paralelo para tarefas complexas |
| `executing-plans` | Execução estruturada de planos de desenvolvimento passo a passo |

### 🧪 Qualidade de Código
| Skill | Descrição |
|-------|-----------|
| `systematic-debugging` | Metodologia em 4 fases para debug: causa raiz → padrão → hipótese → fix |
| `test-driven-development` | TDD na prática: escrever testes que falham primeiro, depois implementar |
| `webapp-testing` | Testes de aplicações web: unitários, integração e E2E |
| `playwright-best-practices` | Testes E2E com Playwright: page objects, fixtures e paralelismo |
| `requesting-code-review` | Como solicitar e conduzir code reviews eficientes |
| `verification-before-completion` | Verificação sistemática antes de marcar uma tarefa como concluída |
| `skill-creator` | Como criar e otimizar novas skills para o Claude Code |

### 📝 Texto, Docs & Planejamento
| Skill | Descrição |
|-------|-----------|
| `writing-plans` | Planejamento estruturado antes de executar: estrutura e dependências |
| `doc-coauthoring` | Co-autoria de documentos: edição iterativa e consistência de estilo |
| `documentation-writer` | Geração de documentação a partir de código: JSDoc e wikis |
| `mcp-builder` | Criação de servidores MCP para integrar ferramentas ao Claude Code |
| `find-skills` | Localiza e sugere skills relevantes para a tarefa em andamento |
| `brainstorming` | Refinamento de ideias antes de escrever código: explora alternativas e valida design |

---

## 💡 Como usar uma skill no Claude Code

Após instalar, basta mencionar na conversa com o Claude Code:

```
Use a skill systematic-debugging para investigar esse erro
```

Ou o agente ativa automaticamente quando detecta que a situação se aplica.

---

## 🔄 Atualizar as skills

```bash
cd skills-pack
git pull
```

---

## 🤝 Contribuindo

Encontrou uma skill útil que não está aqui? Abra uma [issue](https://github.com/ViniciusNoetzold/skills-pack/issues) ou um Pull Request com o `SKILL.md` na pasta correta.

---

## 📚 Fontes

Todas as skills foram coletadas de [skills.sh](https://skills.sh) — o diretório oficial de skills para agentes de IA.

---

*Mantido por [@ViniciusNoetzold](https://github.com/ViniciusNoetzold)*
