# Declarative WAF Policies

This repository contains **custom declarative WAF (Web Application Firewall) policies** for F5 BIG-IP Advanced WAF, managed in a version-controlled way. These policies are written in JSON and follow the **Declarative Security Policy** model provided by F5.

---

## 📖 What is a Declarative WAF Policy?

A **declarative policy** describes the desired security configuration in a single JSON document, rather than applying changes incrementally. This approach is:

- **Idempotent**: Applying the same policy multiple times results in the same state.
- **Versionable**: Easy to track changes in Git.
- **Automatable**: Ideal for CI/CD pipelines and Infrastructure-as-Code workflows.

For more details, see:
- [F5 Declarative WAF Policy Guide (v17.1)](https://clouddocs.f5.com/products/waf-declarative-policy/v17_1.html)
- [Getting Started with Declarative Security Policy](https://techdocs.f5.com/en-us/bigip-16-1-0/big-ip-declarative-security-policy/declarative-policy-getting-started.html#concept-4035)

---

## ✅ Features of This Repo

- **Custom WAF Policies** tailored for different application profiles.
- **Examples** for common use cases (e.g., OWASP Top 10 protection, bot defense).
- **Git-based workflow** for tracking changes and collaborating.

---

## 📂 Repository Structure

```
.
├── policies/
│   ├── base-policy.json        # Minimal baseline WAF policy
│   ├── strict-policy.json      # Strict security settings
│   ├── app-specific/
│   │   ├── graphql.json
│   │   └── webapp01.json
│   │   └── api01.json
├── references/                 # predefined configuration references
│   ├── base/                   # defaults
│   ├── app-specific/           # app-specific configurations
└── README.md
```

---


## 🛠 Best Practices

- **Start with a baseline policy** and extend it for specific apps.
- **Use Git branches** for testing new configurations.
- **Integrate with CI/CD** to automate deployments.

---

## 📚 References

- [F5 Declarative WAF Policy Documentation](https://clouddocs.f5.com/products/waf-declarative-policy/v17_1.html)
- [F5 BIG-IP Declarative Security Policy Guide](https://techdocs.f5.com/en-us/bigip-16-1-0/big-ip-declarative-security-policy/declarative-policy-getting-started.html#concept-4035)
