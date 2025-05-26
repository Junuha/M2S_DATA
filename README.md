# M2S_DATA: One Shot is Enough — Multi-turn-to-Single-turn Jailbreak Dataset

---

## Description

Large-language-model (LLM) safety research has shown that multi-turn jailbreaks are often more successful than single-turn attacks.  
Our paper proposes **M2S** methods that compress multi-turn jailbreak conversations into single-turn prompts without losing attack power.

This dataset releases **all prompts, LLM responses, StrongREJECT scores, and token statistics** used in the study:

| Dataset | Records |
|---------|--------:|
| **MHJ** | 8,592 |
| **SafeMT_ATTACK_600** | 9,600 |
| **CoSafe** | 4,800 |
| **Total** | **22,992** |

For every objective you will find:

* the original multi-turn conversation  
* three M2S variants (*Hyphenize · Numberize · Pythonize*)  
* outputs from four LLMs (GPT-4o-2024-11-20, GPT-4o-mini-2024-07-18, Llama-3-70B-chat-hf, Mistral-7B-Instruct-v0.3)  
* `StrongREJECT` scores and token counts (`input_tokens`, `response_tokens`, `total_tokens`)

---

## Ethical Considerations

### Intended Use and Potential Misuse  
While the techniques we propose (**Hyphenize, Numberize, Pythonize**) can expose critical vulnerabilities in LLMs, they could also be misapplied to generate harmful or disallowed content at scale. We release our methods and datasets so that researchers and practitioners can **identify and remediate** these weaknesses—not to facilitate malicious exploitation. Any harmful use directly contradicts the intent of this work.

### Data and Content Warnings  
The source datasets (e.g., Multi-turn Human Jailbreak, ATTACK_600, CoSafe) inevitably contain adversarial prompts requesting unsafe or disallowed outputs. We therefore flag the corpus as containing *potentially sensitive, unsafe, or harmful* text. Use is strongly discouraged outside carefully controlled safety evaluations; the primary purpose of release is to support the development and testing of robust defenses.

### Responsible Release  
To reduce the risk of amplifying harmful content, we limit direct quotations of disallowed text and focus on aggregated analyses. Where illustrative examples are essential, we paraphrase or redact sensitive portions. Consolidated single-turn prompts are provided **solely** to enable reproducibility and deeper security analysis by the research community.

### Broader Impact on LLM Safety  
By showing that “flattened” single-turn prompts can occasionally outperform more elaborate multi-turn attacks, we highlight the need for guardrails that inspect *entire input blocks*, not just incremental turns. We hope this disclosure spurs stronger alignment techniques and safer deployment practices. Consistent with *coordinated disclosure* principles, we publish with clear warnings and minimal verbatim harmful content so the community can address these challenges responsibly.
