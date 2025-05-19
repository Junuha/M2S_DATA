# M2S_DATA: One Shot is Enough — Multi-turn-to-Single-turn Jailbreak Dataset

This repository accompanies our **ACL 2025 main-conference paper**, accepted as a long paper.
**“One Shot is Enough: Consolidating Multi-Turn Attacks into Efficient Single-Turn Prompts for LLMs.”**  
Junwoo Ha, Hyunjun Kim, Sangyoon Yu, Haon Park, Ashkan Yousefpour, Yuna Park, Suhyun Kim.  
[[arXiv 2503.04856](https://arxiv.org/abs/2503.04856)]

---

## Description

Large-language-model (LLM) safety research has shown that multi-turn jailbreaks are often more successful than single-turn attacks.  
Our paper proposes **M2S** methods that compress multi-turn jailbreak conversations into single-turn prompts without losing attack power.

This dataset releases **all prompts, LLM responses, StrongREJECT scores, and token statistics** used in the study:

| Dataset | Records |
|---------|---------|
| **MHJ** | 8,592 |
| **SafeMT_ATTACK_600** | 9,600 |
| **CoSafe** | 4,800 |
| **Total** | **22,992** |

For every objective you will find:

* the original multi-turn conversation  
* three M2S variants (Hyphenize · Numberize · Pythonize)  
* outputs from four LLMs (GPT-4o-2024-11-20, GPT-4o-mini-2024-07-18, Llama-3-70B-chat-hf, Mistral-7B-Instruct-v0.3)  
* `StrongREJECT` scores and token counts (`input_tokens`, `response_tokens`, `total_tokens`)
