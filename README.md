# 🛡️ Smart Contract Enhancement via Multi-Agent RAG Framework

[![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/maonoz/Smart_Contract_Enhancement)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An advanced, academically rigorous smart contract vulnerability detection and enhancement pipeline. This project utilizes a **Multi-Agent Adversarial Debate Architecture** combined with a **Code-Aware Retrieval-Augmented Generation (RAG)** engine.

This framework was designed to bridge the **Semantic-Syntactic Gap** found in traditional LLM security scanners, allowing for the accurate identification of complex, zero-day DeFi logic flaws (e.g., Price Manipulation) where standard dense vector retrieval models typically fail.

---

## 🚀 Key Academic & Technical Innovations

1. **The Semantic-Syntactic Fix**: Traditional embedding models get distracted by syntax (e.g., matching a `transfer` or multiplication symbol `*` to an `Arithmetic_Overflow`). This project utilizes a code-specific embedding model (`st-codesearch-distilroberta-base`) and explicit category indexing to align business logic with historical patterns.
2. **Adversarial Agentic Loop**: Instead of a single model guessing vulnerabilities, the framework orchestrates a structured debate between specialized AI agents (**Attacker** vs. **Defender**) to validate logic flaws.
3. **Smart Override Protocol**: Implemented within the **Judge Agent**, this protocol gives the LLM reasoning layer permission to mathematically reject weak RAG data if a lethal logic bug is discovered, successfully identifying bugs as either a `Known_RAG_Pattern` or a `Zero_Day_Logic_Flaw`.
4. **Rate-Limit Resilient Engineering**: Engineered with algorithmic token/request pacing using sequential execution delays to maximize throughput on public API gateways without triggering `429 Resource Exhausted` exceptions.

---

## 🏗️ System Architecture

The pipeline processes smart contracts through three decoupled stages:

```mermaid
graph TD
    A[Target Contract] --> B(Phase 1: Code-Aware RAG Engine)
    B --> |Fetches Top 5 Similar Patterns from FAISS| C(Phase 2: Adversarial Multi-Agent Debate)
    C --> |Attacker Agent: Exploit Strategy| D(Phase 3: The Judge Layer)
    C --> |Defender Agent: Counter-Analysis| D
    D --> |Smart Override & JSON Formatting| E[Final Audit Verdict]
