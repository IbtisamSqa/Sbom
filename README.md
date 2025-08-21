# OWASP + SBOM Vulnerability Demo (Python)

This repo contains a test suite of insecure Python code used for:

- ✅ OWASP LLM Top 10 testing
- ✅ CWE-based static analysis
- ✅ SBOM generation with known vulnerable packages

## Files
- `owasp_llm_vuln_demo.py` – Vulnerable Flask app
- `requirements.txt` – Includes vulnerable packages
- `Dockerfile` (optional) – Use for containerized SBOM testing

## How to Test SBOM (locally)
```bash
# Install Syft (Anchore SBOM tool)
curl -sSfL https://raw.githubusercontent.com/anchore/syft/main/install.sh | sh -s -- -b /usr/local/bin

# Generate SBOM in SPDX format
syft . -o spdx > sbom.spdx.json

# Or test directly on GitHub with Dependabot alerts
```
