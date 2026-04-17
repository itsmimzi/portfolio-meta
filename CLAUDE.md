# CLAUDE.md — Global Knowledge Base

> Master context for all side projects and portfolio quests.
> Every project repo has its own `CLAUDE.md` that inherits from and extends this file.
> Last updated: 2025

---

## 🧭 Identity & Intent

Building a portfolio of targeted side projects and technical quests, hosted on GitHub.
Projects are **portfolio-targeted** — each one is designed to demonstrate skills relevant
to specific roles and industries, derived from real job descriptions.

Goal: show problem-solving depth and measurable impact — not a list of tools used.

---

## 🎯 JD-Driven Project Strategy

Job descriptions are the **starting point** for every project.

### Workflow
1. **Input:** One or more JDs from a target role / company type
2. **Extract:** Required skills, tech stack signals, domain knowledge expected
3. **Gap Analysis:** Map extracted skills against current portfolio coverage
4. **Direction:** Choose a project that demonstrates the highest-priority gaps
5. **Framing:** Shape the case study to speak directly to that role's pain points

### Ideal Project Profile
- Covers skill requirements from **multiple JDs** in the same role family
- Starts with one project per company type / role, then iterates
- Each project informs the direction of the next

### JD Analysis Template (used at project kickoff in `PLANNING.md`)
```
Role: [Title]
Company type: [Startup / Scale-up / Enterprise / FAANG-adjacent]
Key required skills: [list]
Nice-to-have skills: [list]
Domain: [e.g., fintech, infra, data platform, consumer product]
Gap identified: [What's missing from current portfolio]
Project hypothesis: [What to build and why it addresses the gap]
```

---

## 🎭 Personas

A **default persona** is set per project in its `CLAUDE.md`.
Any persona can be overridden mid-conversation for a specific task.

| Persona | Best For |
|---|---|
| **Senior Frontend Engineer** | UI architecture, components, accessibility, performance |
| **Lead Product Designer** | UX decisions, case study framing, visual systems |
| **Tech Lead** | Architecture decisions, tradeoffs, code review, project planning |
| **Software Engineer** | General implementation, algorithms, system design |
| **Backend Engineer** | API design, database modeling, server-side logic |
| **Data Scientist** | EDA, model selection, feature engineering, evaluation metrics |
| **Data Analyst** | SQL, dashboards, business metrics, insight framing |
| **DevOps / Platform Engineer** | CI/CD, containerization, cloud infra, observability |
| **Cybersecurity Analyst** | Threat modeling, vulnerability analysis, secure coding |
| **Technical Writer** | README generation, docs, case study synthesis, specs |

> List grows with role targets. Add new personas to project `CLAUDE.md` as needed.

---

## 🤖 Model Selection Strategy

| Model | Use For | Avoid |
|---|---|---|
| `claude-haiku-4-5` | README generation, repetitive file gen, reformats, test stubs | Anything needing judgment or design |
| `claude-sonnet-4-6` ✅ **Default** | UI, code, specs, case studies, most tasks | Burning tokens on trivial work |
| `claude-opus-4-6` | JD analysis, project direction, first-draft CLAUDE.md, complex architecture | Routine implementation |

**Rules:** Start with Sonnet. Opus for strategic phases only. Haiku for batch/templated work.
Per-project overrides go in the project `CLAUDE.md`.

---

## 🛠 Enabled Skills

| Skill | Invoke When |
|---|---|
| `frontend-design` | "build the UI", "create a component", "turn this into code" |
| `skill-creator` | "turn this into a skill", "create a reusable workflow" |
| `code-reviewer` | "review this", "check quality", "simplify this" |
| Brand Guidelines | "does this match the brand?", "align with my style" |
| Excalidraw Diagrams | "diagram this", "visualize the architecture" |
| Interactive Portfolio Designer | "design the portfolio page", "build the case study layout" |

---

## 📁 Standard Repository Structure

```
project-name/
├── CLAUDE.md              ← Project-specific rules (inherits from global)
├── README.md              ← Public-facing doc
├── PLANNING.md            ← JD analysis, project hypothesis, open questions
├── SPECS.md               ← Requirements: user stories + acceptance criteria
├── MVP.md                 ← MVP scope definition
├── TESTING.md             ← Testing strategy (stack-agnostic)
├── docs/
│   ├── case-study.md      ← Challenge → Solution → Impact
│   └── architecture.md    ← Diagrams + decision log (when infra is meaningful)
├── demo/                  ← Demo app (if applicable)
│   └── README.md
└── src/                   ← Source code
```

---

## 📋 Phase Checklist (all dev projects)

### Phase 0 — Direction
- [ ] JD(s) analyzed, skill gap identified
- [ ] Project hypothesis written in `PLANNING.md`

### Phase 1 — Requirements & Scope
- [ ] `SPECS.md` created (user stories + acceptance criteria)
- [ ] `MVP.md` created (scope locked, out-of-scope listed)

### Phase 2 — Design & Architecture
- [ ] Tech stack chosen and justified in project `CLAUDE.md`
- [ ] Architecture / data model sketched (if relevant)

### Phase 3 — Build
- [ ] Implementation follows MVP scope
- [ ] `TESTING.md` strategy defined, framework filled in

### Phase 4 — Ship & Document
- [ ] `README.md` generated
- [ ] `case-study.md` written
- [ ] Demo deployed (if applicable)
- [ ] Code reviewed

---

## 🎨 Design & Brand Preferences

- **Tone:** Clear, direct, technically credible — no fluff
- **Code style:** TypeScript preferred; Tailwind CSS + React for UI projects
- **Naming:** kebab-case files, PascalCase components, conventional commits
- **Color palette:** TBD
- **Typography:** TBD

---

## 🚀 Demo Deployment Defaults

- **Vercel** — frontend / Next.js / full-stack JS
- **GitHub Pages** — static HTML/CSS
- **Hugging Face Spaces** — ML / data science
- Always include `demo/README.md` with setup steps, env vars, live URL
