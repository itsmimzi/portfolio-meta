# TESTING.md — [Project Name]

> Stack-agnostic testing strategy. Fill in framework specifics per project.
> Status: `draft` | `active`

---

## 🧪 Testing Framework

<!-- Fill in once stack is decided -->

| Type | Framework | Config file |
|---|---|---|
| Unit | [e.g., pytest / Jest / Vitest / Go test] | [e.g., pytest.ini / vitest.config.ts] |
| Integration | [e.g., pytest / Supertest / Testcontainers] | |
| E2E | [e.g., Playwright / Cypress / N/A] | |

**Run all tests:**
```bash
# fill in per project
```

**Run unit tests only:**
```bash
# fill in per project
```

**Run integration tests only:**
```bash
# fill in per project
```

---

## 🔬 Unit Tests

**What to test:**
- Core business logic and utility functions
- Data transformations and parsing
- Edge cases and error handling
- Pure functions with deterministic outputs

**What NOT to unit test:**
- Framework internals
- Simple getters/setters with no logic
- UI rendering in isolation (use integration for that)

**Coverage target:** <!-- e.g., 80% on core logic modules -->

### Test File Conventions
```
src/
├── lib/
│   ├── utils.ts
│   └── utils.test.ts       ← co-located unit test
├── components/
│   ├── Button.tsx
│   └── Button.test.tsx
```

---

## 🔗 Integration Tests

**What to test:**
- API endpoints (request → response contracts)
- Database read/write operations
- Multi-component or multi-module interactions
- External service integrations (mocked or sandboxed)

**Approach:**
- Use a test database or in-memory alternative when possible
- Mock external APIs — don't depend on live third-party services in CI
- Test the happy path + at least one failure/edge case per endpoint

### Key Integration Scenarios

| Scenario | Input | Expected Output | Status |
|---|---|---|---|
| [e.g., POST /api/items] | Valid payload | 201 + created item | ⬜ |
| [e.g., POST /api/items] | Missing required field | 400 + error message | ⬜ |
| [e.g., GET /api/items/:id] | Unknown ID | 404 | ⬜ |

---

## 🌐 E2E Tests (if applicable)

**When to add:**
- Only when there's a UI with meaningful user flows
- Focus on critical paths, not exhaustive coverage

**What to test:**
- The primary user journey from start to finish
- Error states the user would actually encounter

**Skip E2E if:** project is API-only, CLI tool, or data pipeline.

---

## 🚦 CI Integration

- [ ] Tests run automatically on push / PR
- [ ] Failing tests block merge
- [ ] Coverage report generated (optional)

**CI platform:** [e.g., GitHub Actions]

```yaml
# .github/workflows/test.yml — fill in per project
```

---

## 📋 Test Checklist (per feature)

Before marking any feature done:
- [ ] Unit tests written for core logic
- [ ] Integration test covers the happy path
- [ ] Integration test covers at least one failure case
- [ ] All tests passing locally
- [ ] No test is skipped without a documented reason
