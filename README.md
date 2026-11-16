# Awesome-Foundational-Contract-Large-Language-Models

# Top Foundational Contract Large Language Models Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Legal Domain Adaptation, Contract Reasoning & Self-Hosted Legal LLMs*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Foundational Contract Large Language Models**. These models and platforms help legal teams analyze contracts, extract clauses, assess risk, and answer questions over agreements—covering everything from general-purpose foundation models adapted for legal work to specialized open-source legal LLMs you can self-host for confidentiality and cost control.

**Examples** include Icertis Vera, OpenAI GPT-4, Anthropic Claude 3.5 Sonnet, Google Gemini, Meta Llama 3, Cohere Command, Mistral Large, Legal-Peace-7B, and LiTiL models (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted legal language models, open-source contract reasoning, and community-driven legal AI—ideal for organizations seeking data sovereignty and avoiding per-token API costs that compound with document volume. The open-source landscape is genuinely emerging: **Legal-Peace-7B** is a fine-tuned Mistral-7B for contract analysis , **LiTiL** provides a suite of task-specific legal models , and **Saul-7B** offers a legal-domain LLM trained on 30B+ tokens of legal corpus .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Icertis Vera](https://www.icertis.com/)** | Enterprise contract intelligence platform with AI copilot grounded in contract data. Vera uses foundation models adapted for contract reasoning, obligation tracking, and risk identification. | Quote-only (enterprise CLM contract) | No free tier; demo via sales |
| **[OpenAI GPT-4](https://openai.com/)** | General-purpose foundation model widely used for contract analysis via prompting. **GPT-4.1 pricing: $2/million input tokens, $8/million output tokens** . Strong at clause interpretation but not legal-specific; requires careful prompt engineering and human review. | Pay-per-token (usage-based) | No free tier for GPT-4; API trial credits available |
| **[Anthropic Claude 3.5 Sonnet](https://www.anthropic.com/)** | Foundation model with strong long-context reasoning, often used for contract review and document analysis. | Pay-per-token (usage-based) | No free tier; API trial available |
| **[Google Gemini](https://deepmind.google/technologies/gemini/)** | Multimodal foundation model family from Google, including Gemini 2.5 Pro for long-document analysis. | Pay-per-token (usage-based) | Free tier available via Google AI Studio |
| **[Meta Llama 3](https://llama.meta.com/)** | Open-weight foundation model family. **Llama 3.1 8B Instruct** is frequently evaluated for contract tasks and can be self-hosted . | Free (open weights); infrastructure costs apply | **Free weights**: self-host or use via cloud providers |
| **[Cohere Command](https://cohere.com/)** | Enterprise LLM with strong retrieval-augmented generation (RAG) capabilities, suited for contract Q&A over internal repositories. | Pay-per-token (usage-based) | Trial available |
| **[Mistral Large](https://mistral.ai/)** | Foundation model from Mistral AI, available via API or self-hosted (open-weight variants). | Pay-per-token or quote-only for enterprise | Trial available via API |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Legal-Peace-7B](https://huggingface.co/olaverse/legal-peace-v1.0)** | [![Stars](https://img.shields.io/github/stars/Olaverse-Labs/olaverse-legal?style=social&color=white)](https://github.com/Olaverse-Labs/olaverse-legal/stargazers) | **The most accessible open-source contract analysis model with a dedicated inference wrapper.** Fine-tuned from **Mistral-7B-v0.3** using SFT (4,800 cases) + DPO (419 legal reasoning examples). **Apache 2.0 licensed** . Claims **32.6% faster contract analysis** and **14% faster case predictions** vs. base Mistral, with more structured legal responses . Available via the `olaverse` Python package: `pip install olaverse[legal]` . **Critical caveat**: explicitly labeled a **beta model for research purposes only**—outputs must be reviewed by qualified legal professionals and it is **not recommended for production use** . Trained primarily on U.S. legal data . **Best for researchers and developers** wanting a self-hosted, fine-tuned contract model to experiment with and build upon . |
| **[LiTiL Open Intelligence Models](https://huggingface.co/collections/litillabs/litil-open-intelligence-models)** | — | **A suite of task-specific legal models, each with a defined job in legal workflows.** Includes: **legal request router (1.5B)** for routing incoming matters; **legal intake (4B)** for consistent matter triage; **PII finder (0.3B)** for pre-redaction detection; **clause check (1.5B)** for Yes/No presence queries; **clause tagger (4B)** for taxonomy labeling; **clause classifier (0.4B)** for category assignment; **contract extractor (1.7B)** for CUAD field extraction with `NOT_PRESENT` handling; **contract playbook (3B)** for applying playbook rules; and **financing review (9B)** for source-linked review . **Best for teams wanting composable, narrow models** that each do one contract task well, rather than a single general-purpose legal LLM . |
| **[Saul-7B-Instruct-V1](https://huggingface.co/Equall/Saul-7B-Instruct-V1)** | — | **Legal-domain LLM built on Mistral-7B, trained on 30B+ tokens of English legal corpus** (case law, statutes, briefs, scholarly articles). **MIT licensed** . Developed by Equall.ai, CentraleSupélec, Sorbonne Université, Instituto Superior Técnico, and NOVA School of Law . Claims **~0.61 average on LegalBench-Instruct**, an 11% relative improvement over previous best-in-class 7B models . Two-stage training: legal continued pretraining + instruction fine-tuning (~600K instructions) . **Trade-off**: can produce hallucinations; requires human review; 16GB+ VRAM recommended . **Best for legal professionals** wanting a transparent, self-hostable legal LLM with strong benchmark performance . |
| **[Awesome Legal AI (Chinese)](https://github.com/lilialla/awesome-legal-ai-zh)** | — | **Curated index of 200+ open-source legal AI tools** for Chinese lawyers and legal professionals. Covers contract review, Word document formatting, OCR, redaction, legal research, and more—each entry annotated with **data path (local/self-hosted/API), external dependencies, verification depth, and license** . **Best for Chinese-speaking legal teams** wanting a task-oriented map of the open-source legal AI landscape . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[ContractEval (Benchmark)](https://arxiv.org/abs/2508.03080)** | — | **Clause-level legal risk identification benchmark for commercial contracts.** Evaluates **19 LLMs** including GPT-4.1, Gemini 2.5 Pro, Claude Sonnet 4, and 15 open-source models (DeepSeek R1, Llama 3.1 8B, Gemma 3, Qwen3 series). **Key insight**: open-source models are attractive for legal work because **client confidentiality requires local deployment** and they avoid per-token costs . **Best as an evaluation framework** for selecting which model to self-host . |
| **[LegalBench](https://arxiv.org/abs/2308.11462)** | — | **Collaboratively built benchmark for measuring legal reasoning in LLMs.** Includes contract-specific tasks like `cuad_audit_right` (does a clause grant audit rights?) and `definition_classification` (does a sentence define a term?). **Best as the standard evaluation suite** for comparing legal LLM performance . |

**Frameworks for building custom systems**: Choose **Legal-Peace-7B** for a fine-tuned contract model to experiment with (research only) , **LiTiL models** for composable task-specific extraction and classification , or **Saul-7B** for a legal-domain LLM with stronger benchmark performance —all self-hostable without per-token API fees. For evaluation, use **ContractEval** and **LegalBench** to select and validate models against your actual contract corpus.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Contract LLMs process legally sensitive and privileged documents; **data residency is critical**—open-source self-hosted models are often preferred for legal work precisely because client confidentiality obligations restrict transmission to external servers . Enforce strict access controls and never rely on model output without qualified legal review.
- **Open-source legal LLMs are early-stage and carry significant limitations.** **Legal-Peace-7B is explicitly a beta research model**—not for production use, trained primarily on U.S. legal data, and outputs must be reviewed by attorneys . **Saul-7B** shows strong benchmark performance but can hallucinate and recommends 16GB+ VRAM . **LiTiL models** are narrow and task-specific, not general-purpose reasoners . **Proprietary foundation models** (GPT-4, Claude, Gemini) are stronger general reasoners but require sending documents to external APIs—a compliance risk for privileged legal work . **Validate model performance on your own contract corpus** using **ContractEval** or **LegalBench** before committing, and always maintain human-in-the-loop review for any legally consequential output.

---

**Made for legal engineers, contract AI researchers, and organizations building legal language model infrastructure.**  
Let's make foundational contract LLMs more open, verifiable, and legally sound.
