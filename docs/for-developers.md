# For Developers

Ready to use production-tested AI capabilities in your projects? You're in the right place.

## ⚡ Quick Start

### 1. Pick Your Format

All capabilities are packaged in **universal formats** — choose what fits your stack:

| Format | Best For | Install Command |
|---|---|---|
| **MCP Server** | Claude Desktop, Code | `npx @goldentellus/<capability>` |
| **Claude Skill** | Claude CLI projects | Copy manifest to `.claude/skills/` |
| **OpenAPI** | Any HTTP client | Import spec from `capabilities.mdtools/<name>/openapi.yaml` |
| **Standalone** | Script in any language | Clone repo, run locally |

### 2. Browse the Catalog

Visit **[goldentellus-capabilities](https://github.com/GoldenTellus/goldentellus-capabilities)** to see what's available.

Each capability includes:
- **README** with usage examples
- **Trust block** declaring scopes, egress, secrets
- **At least 1 universal format** (usually multiple)
- **Production validation** evidence

### 3. Install & Use

Example: using an MCP-packaged tool:

```bash
# Add to your Claude Code MCP config
npx @goldentellus/crm-lookup
```

Example: using a standalone skill:

```bash
# Clone the repo
git clone https://github.com/GoldenTellus/goldentellus-capabilities
cd goldentellus-capabilities.mdskills/document-summary

# Copy to your Claude project
cp manifest.yaml ~/.claude/skills/goldentellus-doc-summary.yaml
```

## 🧩 Capability Types

### Tools (Connectors)
Connect to external systems: CRM, database, file storage, APIs.

- **Execution**: Runs in sandbox (gVisor, Firecracker, or your runtime)
- **Trust**: Requires explicit scopes, egress whitelist, and secret refs
- **Format**: OpenAPI (preferred), MCP Server, standalone script

### Skills (Orchestration)
Prompt engineering + RAG for specific tasks.

- **Execution**: RAG Adapter (retrieval → rerank → LLM)
- **Trust**: Read-only scopes, no egress
- **Format**: Claude Skill manifest, YAML prompt template

### Knowledge Packs
Domain-specific knowledge for retrieval-augmented generation.

- **Execution**: Vector indexing (Qdrant, pgvector, etc.)
- **Trust**: Read-only, no secrets
- **Format**: Structured documents + schema

### External Roles
Customer-facing bot configurations (lead capture, support, partner portal).

- **Execution**: Gateway Bot runtime
- **Trust**: Public context only, outbound filtering
- **Format**: YAML role config

## 🔐 Trust Model

Every capability declares a **trust block**:

```yaml
trust:
  execution_class: executable  # declarative | executable | composite
  required_scopes: ["context:read", "api:salesforce"]
  egress: ["api.salesforce.com", "*.hubspot.com"]
  secret_refs: ["salesforce_api_key"]
  cost_profile:
    inference_cost: low
    task_tier: non_frontier
```

This tells you:
- **Scopes**: What permissions it needs
- **Egress**: Which external domains it calls
- **Secrets**: What credentials you must provide
- **Cost**: Inference expense estimate

## 🧪 Testing Locally

Before using in production:

1. **Read the trust block** — know what it accesses
2. **Run in sandbox** — use gVisor, Docker, or your preferred isolation
3. **Test with fake data** — never use production secrets for first tests
4. **Check error handling** — does it fail gracefully?

## 🤝 Contribute a Capability

Have a production-tested capability? Share it!

**Requirements**:
- Must be deployed in production (not a demo)
- Must support at least 1 universal format
- Must include trust block and README
- Must pass quality checklist

See **[Contributing Guide](https://github.com/GoldenTellus/goldentellus-capabilities.mdblob/main/CONTRIBUTING.md)** for details.

## 📚 Learn More

- **[Capabilities Catalog](https://github.com/GoldenTellus/goldentellus-capabilities)** — Browse all available capabilities
- **[SNAO Overview](snao-overview.md)** — Understand the platform behind these capabilities
- **[For Enterprises](for-enterprise.md)** — Deploy SNAO in your organization

## 💬 Get Help

- **GitHub Issues**: [goldentellus-capabilities.mdissues](https://github.com/GoldenTellus/goldentellus-capabilities.mdissues)
- **Discussions**: [goldentellus-capabilities.mddiscussions](https://github.com/GoldenTellus/goldentellus-capabilities.mddiscussions)

---

**Next Steps**:
1. Browse the [capabilities catalog](https://github.com/GoldenTellus/goldentellus-capabilities)
2. Pick a capability and install it
3. Read its trust block
4. Test with sandbox + fake data
5. Integrate into your project
