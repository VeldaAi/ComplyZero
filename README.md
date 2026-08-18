# ⚡ ComplyZero

**Free & open-source security compliance — without the $50K/year vendor tax.**

A practical research summary on whether a startup actually needs.

---


## What Is Vanta?

**Vanta** is a SaaS "trust management" platform that automates security compliance:

- **Frameworks:** SOC 2, ISO 27001, HIPAA, PCI DSS, GDPR
- **What it does:** continuously collects evidence (repo settings, PR practices,
  vulnerability alerts, access reviews, cloud config) and maps it to audit controls
- **GitHub integration:** powers version-control compliance, vulnerability scanning,
  and security-issue tracking automatically

### The catch
- **Expensive:** SOC 2 automation packages start in the **low-to-mid five figures/year**
  (Vanta itself is typically $1–5K/month)
- **The tool isn't the work:** you still need real policies, access reviews, and
  controls in place. Vanta only automates *evidence collection*
- **The audit isn't included:** a CPA audit still costs **$10–20K** no matter what
  tool you use

### When it IS worth it
The day a serious enterprise/healthcare customer.

---

## What GitHub Already Gives You For Free ✅

GitHub's native free features cover the "version control compliance" pillar that
Vanta's integration provides — at **$0/month**:

| Capability | GitHub Free | What it covers |
|---|---|---|
| **Dependabot** | ✅ free on private repos | dependency vulnerability alerts + auto PRs |
| **Secret scanning** | ✅ free on private repos | leaked API keys / credentials detection |
| **Code scanning (CodeQL)** | ✅ free minutes (unlimited on public) | SAST in CI |
| **Branch protection** | ✅ free | required PR reviews, no force-push to main |
| **Org audit log** | ✅ free (since 2024) | who did what, when |

That's the foundation — most startups never configure all of this, and it costs
nothing.

---

## Open-Source Vanta Replacements 🆓

Full compliance/evidence automation platforms you can **self-host for $0/month**:

### [Comp AI](https://github.com/Comp-AI)
The main one right now.
- AI-driven evidence collection, policy generation, continuous monitoring
- **580+ integrations** (GitHub, AWS, GCP, Cloudflare, Google Workspace, Slack…)
- Targets SOC 2, ISO 27001, HIPAA, GDPR
- Actively maintained

### [CISO Assistant](https://github.com/intuitem/ciso-assistant-community)
- Mature open-source GRC tool (governance, risk, compliance)
- Controls, risk registers, policy management
- Community edition is genuinely usable

### [Prowler](https://github.com/prowler-cloud/prowler)
- AWS security assessments & evidence (CIS benchmarks, NIST, PCI)
- The gold standard for cloud-side evidence, free

### [Openlane](https://github.com/openlane)
- Newer, fully open source, "no gatekeeping" on how you model compliance
- Native GitHub / AWS / GCP / Cloudflare / Google Workspace sync

---

## The Realistic Stack (If We Ever Need It)

```
GitHub native (free)      → version control compliance, vuln alerts, audit log
Prowler (free)            → cloud infrastructure evidence
Comp AI self-hosted (free) → policy management + evidence collection + control mapping
CPA auditor ($10–20K)     → the only unavoidable cost
```

That's **~80% of Vanta's value at $0/month**. The missing 20% is human work —
writing real policies and doing access reviews — which Vanta doesn't do for you either.

---

## Decision Framework

| Situation | Do |
|---|---|
| No enterprise/healthcare deal demanding compliance | **Do nothing** — configure GitHub's free features (Dependabot, secret scanning, branch protection) |
| Customer asks for SOC 2 / HIPAA posture | **Self-host Comp AI**, wire it into monthly checks so evidence stays fresh |
| Customer demands a *signed* audit report | **Pay for a CPA audit** ($10–20K) — no tool avoids this |
| Compliance becomes a sales bottleneck at scale | Re-evaluate Vanta/Drata vs. maintaining Comp AI (time cost) |

---

## TL;DR

- **Vanta = $1–5K/month** for automated evidence collection
- **GitHub free = 0$** and already covers the repo-side compliance pillar
- **Comp AI + Prowler = $0/month** self-hosted, cover most of the rest
- **The only unavoidable cost is the CPA audit** (~$10–20K), and that's a deal-driven expense
- **Rule: never pay for compliance software before a deal demands it**

---

*ComplyZero — compliance without the vendor tax.*
