# Capabilities Catalog

Browse production-tested AI building blocks extracted from real enterprise deployments.

All capabilities are available at **[goldentellus-capabilities](https://github.com/GoldenTellus/goldentellus-capabilities)**.

---

## 🔍 What You'll Find

Every capability includes:

- **README**: Usage examples, installation, configuration
- **Trust Block**: Declared scopes, egress, secrets, cost profile
- **Universal Format(s)**: MCP Server, Claude Skill, OpenAPI, standalone
- **Production Evidence**: Deployed where, for how long, success rate

---

## 📦 Current Status

**0 capabilities published** (first batch in progress)

We're in the early stages of extracting capabilities from our production SNAO deployments. Check back soon or **[watch the repo](https://github.com/GoldenTellus/goldentellus-capabilities)** for updates.

---

## 🧩 Capability Types

### Tools (Connectors)
External system integrations: CRM, database, file storage, APIs.

- **Execution**: Sandbox (gVisor, Firecracker, Docker)
- **Trust**: Requires scopes, egress whitelist, secret refs
- **Formats**: OpenAPI (preferred), MCP Server, standalone script

**Examples** (coming soon):
- Salesforce CRM lookup
- PostgreSQL query executor
- S3 file operations

### Skills (Orchestration)
Prompt engineering + RAG for specific tasks.

- **Execution**: RAG Adapter (retrieval → rerank → LLM)
- **Trust**: Read-only scopes, no egress
- **Formats**: Claude Skill manifest, YAML template

**Examples** (coming soon):
- Document summarization
- Meeting notes generation
- Data analysis prompt chains

### Knowledge Packs
Domain-specific knowledge for RAG.

- **Execution**: Vector indexing
- **Trust**: Read-only, no secrets
- **Formats**: Structured docs + schema

**Examples** (coming soon):
- Manufacturing SOPs
- Financial compliance rules
- Healthcare protocols

### External Roles
Customer-facing bot personas.

- **Execution**: Gateway Bot runtime
- **Trust**: Public context only, outbound filtering
- **Formats**: YAML role config

**Examples** (coming soon):
- Lead capture bot
- Customer service bot
- Partner portal bot

---

## 🔐 Understanding Trust Blocks

Every capability declares what it needs:

```yaml
trust:
  execution_class: executable  # declarative | executable | composite
  required_scopes: ["context:read", "crm:write"]
  egress: ["api.salesforce.com", "*.hubspot.com"]
  secret_refs: ["salesforce_api_key"]
  cost_profile:
    inference_cost: low
    task_tier: non_frontier
```

**Before using**:
- Check `required_scopes`: Do you want to grant these permissions?
- Check `egress`: Does it call domains you trust?
- Check `secret_refs`: Do you have these credentials?
- Check `cost_profile`: Does inference cost fit your budget?

---

## 🚀 Quick Start

### Browse on GitHub
Visit **[goldentellus-capabilities](https://github.com/GoldenTellus/goldentellus-capabilities)** and explore:

```text
capabilities.md
├── tools/          # External connectors
├── skills/         # Prompt orchestration
├── knowledge/      # Domain knowledge
└── external-roles/ # Customer-facing bots
```

### Install a Capability

**MCP Server** (Node.js):
```bash
npx @goldentellus/<capability-name>
```

**Claude Skill**:
```bash
cp capabilities.mdskills/<name>/manifest.yaml ~/.claude/skills/
```

**OpenAPI Tool**:
```bash
# Import spec into your HTTP client
curl -O https://raw.githubusercontent.com/GoldenTellus/goldentellus-capabilities.mdmain/capabilities.mdtools/<name>/openapi.yaml
```

**Standalone**:
```bash
git clone https://github.com/GoldenTellus/goldentellus-capabilities
cd capabilities.md<category>/<name>
./run.sh  # or python main.py, node index.js, etc.
```

---

## 🤝 Contribute a Capability

Have a production-tested capability? We'd love to include it!

**Requirements**:
1. **Production deployed** (not a demo or experiment)
2. **Universal format** (MCP / Claude Skill / OpenAPI / standalone)
3. **Trust block** declared
4. **README** with usage examples
5. **Quality checklist** passed

See **[Contributing Guide](https://github.com/GoldenTellus/goldentellus-capabilities.mdblob/main/CONTRIBUTING.md)** for full process.

---

## 📚 Learn More

- **[For Developers](for-developers.md)**: How to use capabilities in your projects
- **[SNAO Overview](snao-overview.md)**: Understand the platform that generates these capabilities
- **[For Enterprises](for-enterprise.md)**: Deploy SNAO to precipitate your own capabilities

---

## 💬 Get Help

- **Issues**: [goldentellus-capabilities.mdissues](https://github.com/GoldenTellus/goldentellus-capabilities.mdissues)
- **Discussions**: [goldentellus-capabilities.mddiscussions](https://github.com/GoldenTellus/goldentellus-capabilities.mddiscussions)

---

**Check back soon** — first capabilities coming Q4 2026!
