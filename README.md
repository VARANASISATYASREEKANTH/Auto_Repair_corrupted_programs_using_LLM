# Auto_Repair_corrupted_programs_using_LLM
Automated Program Repair (APR), is a rapidly developing area of research and application where Large Language Models (LLMs) are being used with significant success.
# 🤖 Auto Repairing Programs with Large Language Models (LLMs)

This document outlines the emerging field of **Automated Program Repair (APR)**, where **Large Language Models (LLMs)** are used to autonomously detect and fix corrupted or buggy code.

---

## How LLMs are Used for Automated Program Repair 🛠️

LLM-based APR systems are highly sophisticated pipelines that go beyond simple code generation. They integrate various analysis tools and iterative feedback loops to find and fix defects with high precision.

### 1. Autonomous Agent and Iterative Repair 🔄

Modern LLM repair techniques treat the language model as an **autonomous agent** capable of reasoning and executing a sequence of actions, much like a human developer.

* **Autonomous Agents:** Systems like "**RepairAgent**" plan, execute actions, and autonomously decide which tools to use. They use a **dynamically updated prompt** format that guides the LLM through the entire bug-fixing process.
* **Feedback Loops:** A critical component is the **iterative repair cycle**. After the LLM generates a candidate patch, it's tested. The **failing/passing test results**, error messages, and runtime warnings are fed back to the model. This allows the LLM to refine its patch and avoid repeating past errors.
* **Chain-of-Thought (CoT) Prompting:** This technique forces the LLM to first **analyze the error** and **identify the root cause** in natural language *before* generating the final code patch, significantly improving fix quality.

### 2. Augmenting LLM Reasoning with Tools 🔬

The power of LLMs is amplified by integrating them with traditional software engineering tools and structured data.

| Tool/Artifact | Function in APR |
| :--- | :--- |
| **Fault Localization (FL)** | Tools like **Spectrum-Based Fault Localization (SBFL)** analyze test results to highlight the most **suspicious code lines**. This narrows the focus for the LLM. |
| **Code Artifacts** | The LLM uses failing test cases, stack traces, compiler error reports, and existing code comments to gain maximum context about the defect. |
| **Verification** | Generated patches are automatically compiled and executed against the test suite to ensure the fix is correct and doesn't introduce new issues (regressions). |

### 3. Repair Scenarios and Applications 🎯

LLM-based APR is applicable to a wide array of defects and corrupted code types:

* **Semantic Bugs:** Fixing logical errors that cause incorrect program behavior.
* **Security Vulnerabilities:** Automatically identifying and patching exploitable flaws.
* **Web UI Test Failures:** Repairing brittle locators (e.g., XPath expressions) in automated test scripts that break due to minor front-end changes.
* **Systemic Errors:** Successfully fixing complex **multi-function bugs** that require coordinated changes across multiple parts of the codebase.

The field continues to advance rapidly, with LLM-based systems demonstrating **superior repair performance** compared to older, more traditional APR techniques.
