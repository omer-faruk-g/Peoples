---
name: peoples
description: Peoples - market-intelligence and persona simulation. Finds 3-5 competitors, mines their negative reviews, patches those flaws into the code before delivery, then scores it with a synthetic panel of 100-1000 personas and emits the PEOPLES SIMULATION REPORT (adoption, top objections, the upgrade needed for 90%+). Use when a product, module, app or user-facing feature is proposed or built, when the user asks about competitors, market fit, adoption, conversion or whether it will sell, or says peoples, rakip, pazar testi, satar mı, tutar mı.
---

# SKILL: Peoples (Market-Intelligence & Multi-Agent Persona Simulation)

## PURPOSE
To perform background competitive research, extract negative user feedback from existing market alternatives, patch those flaws directly into the active codebase, and run a synthetic multi-agent panel simulation (100-1000 user personas) to measure product adoption and purchase conversion rates.

---

## 1. COMPETITOR & NEGATIVE REVIEW MINING (PAIN-POINT EXTRACTION)

When a product, module, or user-facing feature/code is proposed:
1. **Identify Competitors:** Detect 3–5 existing market alternatives or similar open-source/commercial products.
2. **Mine Negative Feedback:** Scan/analyze common user complaints, bad reviews, and UX friction points of those competitors (e.g., poor error handling, slow response, complex onboarding, missing edge-case handling).
3. **Preemptive Code Patching:** Implement concrete fixes for those mined flaws directly inside the current code/architecture *before* outputting the final product.
   - **Approval Gate (ClaudPer / ClaudeMT):** If these fixes change 2 or more files or more than 150 lines, list them as a plan and wait for the user's approval before patching.

---

## 2. SYNTHETIC PERSONA PANEL SIMULATION (100 - 1000 AGENTS)

Run a background Monte Carlo / Synthetic Agent Evaluation using a diverse pool of virtual user personas (Tech Savvy, Beginner, Enterprise, Budget-Conscious, Security-Obsessed).

### Agent Evaluation Parameters:
- **Usability & Friction Score (1-10)**
- **Value Proposition Match (1-10)**
- **Deal-Breakers / Objections Identified**

### Output Format (Emitted as a Background Execution Block):

```markdown
### 📊 PEOPLES SIMULATION REPORT (Sample Size: N = 1000 Synthetic Agents)

> NOTE: Metrics below are generated via synthetic Monte Carlo LLM persona simulation, representing predictive model estimation rather than empirical field telemetry.

#### 1. Market Flaws Patched in Code:
- [Mined Flaw #1]: [How this code specifically avoids/fixes it]
- [Mined Flaw #2]: [How this code specifically avoids/fixes it]

#### 2. Conversion & Purchase Metrics:
- **Total Simulated Cohort:** 1000 Agents
- **WILL BUY / ADOPT:** [X]% (e.g., 740 / 1000)
- **WILL REJECT:** [Y]% (e.g., 260 / 1000)

#### 3. Top Rejection Reasons (Objections):
1. **[Reason 1]:** [X]% of rejecting agents cited this (e.g., "Missing dark mode support")
2. **[Reason 2]:** [Y]% of rejecting agents cited this (e.g., "No offline fallback mechanism")

#### 4. Actionable Code Upgrade to Hit 90%+ Adoption:
- [Exact code/feature change needed to win over the rejecting cohort]
```

---

## 3. BACKGROUND EXECUTION & ISOLATION

- **Non-Blocking Flow:** Perform competitor research and persona testing in an isolated execution block (or parallel thread) so primary code generation is not delayed.
- **Data Density:** Keep agent reasoning dense. Output aggregated metrics rather than individual agent chat logs to optimize token usage.

---

## 4. PRE-FLIGHT SIMULATION CHECKLIST

Before finalizing the product/code deliverable:

- [ ] Have real-world competitor flaws been identified and patched in the code?
- [ ] Has the synthetic cohort (100-1000 agents) been executed against the proposed logic?
- [ ] Are conversion percentages and primary objection points explicitly calculated?
