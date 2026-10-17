# 🏠 GoldenTellus

> Production-ready AI capabilities, extracted from real enterprise deployments.

We deploy **SNAO** (multi-tenant agent platform) for enterprises, extract reusable capabilities, and open-source them for developers worldwide.

**Live site**: https://goldentellus.github.io/goldentellus-home/

---

## 🎯 What We Do

1. **Deploy SNAO** in enterprises — a platform that governs AI, precipitates knowledge from work, and manages capabilities
2. **Extract patterns** — Tools, skills, knowledge packs, external roles that proved valuable in production
3. **Desensitize & vet** — Remove enterprise-specific details, verify quality
4. **Open source** — Package as universal formats (MCP, Claude Skill, OpenAPI, standalone)

---

## 🚀 Quick Links

| Role | Start Here |
|---|---|
| **Developer** | [Capabilities catalog](https://github.com/GoldenTellus/goldentellus-capabilities) → [Quick start](./docs/for-developers.md) |
| **Enterprise** | [What is SNAO?](./docs/snao-overview.md) → [Schedule demo](./docs/for-enterprise.md) |
| **Contributor** | [Contributing guide](./docs/CONTRIBUTING.md) |

---

## 📦 Repository Structure

```text
docs/
├── index.md            # Site homepage
├── for-developers.md   # How to use capabilities
├── for-enterprise.md   # SNAO deployment info
├── capabilities.md     # Capabilities catalog page
├── snao-overview.md    # Technical architecture summary
└── CONTRIBUTING.md     # How to contribute
```

---

## 🛠️ Local Development

```bash
# Install dependencies
pip install mkdocs-material

# Serve locally
mkdocs serve

# Build (strict mode catches broken links)
mkdocs build --strict
```

Push to `main` triggers GitHub Actions → deploys to Pages automatically.

---

## 📊 Current Status

- **Capabilities**: 0 public (first batch in progress)
- **Deployments**: 0 production (platform in development)
- **Contributors**: Open to the community

This is a **greenfield project** — we're building in public. Watch this space.

---

## 🤝 Contributing

All capability contributions go to **[goldentellus-capabilities](https://github.com/GoldenTellus/goldentellus-capabilities)**.

For documentation improvements to this site, see [CONTRIBUTING.md](./docs/CONTRIBUTING.md).

---

## 📄 License

This site: [MIT License](./LICENSE)

Individual capabilities may have different licenses — check each capability's directory.

---

## 💬 Connect

- **Issues**: [goldentellus-home/issues](https://github.com/GoldenTellus/goldentellus-home/issues)
- **Discussions**: [goldentellus-home/discussions](https://github.com/GoldenTellus/goldentellus-home/discussions)
- **Capabilities**: [goldentellus-capabilities](https://github.com/GoldenTellus/goldentellus-capabilities)
