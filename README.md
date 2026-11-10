# ⚡ Awesome Edge APIs — High-Performance Developer Microservices

[![Edge Network](https://img.shields.io/badge/Network-Cloudflare%20Edge-f38020?style=for-the-badge&logo=cloudflare)](https://workers.cloudflare.com)
[![RapidAPI](https://img.shields.io/badge/Marketplace-RapidAPI-0055ff?style=for-the-badge&logo=rapidapi)](https://rapidapi.com)
[![Latency](https://img.shields.io/badge/Latency-%3C50ms-emerald?style=for-the-badge)](https://rapidapi.com)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

A curated suite of enterprise-grade, ultra-low-latency Micro-APIs running on Cloudflare Workers edge nodes across 300+ cities worldwide. Zero cold starts, maximum deliverability, and developer-friendly documentation.

---

## 🚀 Quick Navigation

- [1. LeadGuard — Email Verification & Deliverability API](#1--leadguard--email-verification--deliverability-api)
- [2. MarkdownAI — Web to Clean Markdown for LLMs & RAG](#2--markdownai--web-to-clean-markdown-for-llms--rag)
- [3. VatGuard — EU VIES & Global Tax Intelligence API](#3--vatguard--eu-vies--global-tax-intelligence-api)
- [Free Tier & RapidAPI Access](#-free-tier--rapidapi-access)

---

## 1. 🛡️ LeadGuard — Email Verification & Deliverability API

Stop bounce rates, block disposable / burner emails, and protect your outbound sender reputation in real time.

- **Live Playground**: [https://leadguard-api.leadguard-api.workers.dev](https://leadguard-api.leadguard-api.workers.dev)
- **RapidAPI Hub**: [Subscribe on RapidAPI Hub](https://rapidapi.com/search/LeadGuard)

### Key Features
- **Real-Time MX Lookup**: Direct authoritative DNS check.
- **Disposable Detection**: 3,500+ constantly updated temporary domain blocklist.
- **Role Account Flag**: Flags `admin@`, `support@`, `sales@`, `info@`.
- **Smart Typo Auto-Suggest**: Detects `gmaill.com` -> `gmail.com`.
- **Deliverability Score (0-100)**: Instant algorithmic quality verdict.

```bash
# cURL Example
curl -X GET "https://leadguard-api.leadguard-api.workers.dev/v1/email/verify?email=alex.miller@gmail.com"
```

---

## 2. 📝 MarkdownAI — Web to Clean Markdown for LLMs & RAG

Turn any web page or messy HTML document into pristine, token-optimized Markdown ready for OpenAI, Claude, LangChain, or your vector database.

- **Live Playground**: [https://markdown-ai-api.leadguard-api.workers.dev](https://markdown-ai-api.leadguard-api.workers.dev)
- **RapidAPI Hub**: [Subscribe on RapidAPI Hub](https://rapidapi.com/search/MarkdownAI)

### Key Features
- **Save up to 85% on LLM Tokens**: Strips ads, navigation bars, SVG icons, scripts, and tracking pixels.
- **RAG & Agent Ready**: Returns structured headings, clean bullet points, code blocks, and markdown links.
- **Rich OpenGraph & Metadata**: Grabs title, meta description, cover image (`og:image`), favicon, author, and reading time in a single API call.
- **Sub-80ms Global Edge Latency**: Deployed worldwide on Cloudflare edge.

```python
# Python Example
import requests

res = requests.get(
    "https://markdown-ai-api.leadguard-api.workers.dev/v1/markdown",
    params={"url": "https://en.wikipedia.org/wiki/Artificial_intelligence"}
)
data = res.json()
print("Words:", data.get("word_count"))
print("Markdown:
", data.get("markdown", "")[:300])
```

---

## 3. 🏛️ VatGuard — EU VIES & Global Tax Intelligence API

Enterprise-grade European Union VAT validation, business lookup, and international tax rate calculation API for Stripe, Shopify, WooCommerce, and B2B SaaS checkouts.

- **Live Playground**: [https://vatguard-api.leadguard-api.workers.dev](https://vatguard-api.leadguard-api.workers.dev)
- **RapidAPI Hub**: [Subscribe on RapidAPI Hub](https://rapidapi.com/search/VatGuard)

### Key Features
- **Official EU VIES Integration**: Live validation across all 27 European Union member states.
- **Zero-Downtime Fallback**: Government VIES servers frequently fail (503). Algorithmic checksum & syntax validation ensures checkouts never abandon.
- **Company Information**: Retrieves legal entity names and registered addresses.
- **B2B Reverse Charge**: Automates 0% VAT exemption for cross-border transactions.

```javascript
// JavaScript / Node.js Example
const res = await fetch("https://vatguard-api.leadguard-api.workers.dev/v1/vat/validate?vat_number=DE122268496");
const data = await res.json();
console.log(`VAT Valid: ${data.valid} | Country: ${data.country.name}`);
```

---

## 🎁 Free Tier & RapidAPI Access

All APIs feature a generous **Free Tier (50 requests/month forever)** on RapidAPI. 

For higher production volume (5,000 to 50,000+ req/mo), subscribe via RapidAPI for instant API key activation, SLA monitoring, and automated billing.

---

## 📄 License
This documentation and open playground repository is open-sourced under the [MIT License](LICENSE).
