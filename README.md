# Green Chips

Theravāda-inspired ethical AI framework focused on harm reduction, emotional stability, cognitive clarity, and transparent AI alignment.

(ထေရဝါဒ ဗုဒ္ဓဒဿနကို အခြေခံ၍ AI စနစ်များ၏ ဘေးအန္တရာယ်လျှော့ချရေး၊ စိတ်ခံစားမှုတည်ငြိမ်ရေး၊ စိတ်ပိုင်းဆိုင်ရာရှင်းလင်းမှုနှင့် ပွင့်လင်းမြင်သာသော AI Alignment ဖြစ်စေရန် တည်ဆောက်ထားသော Ethical Framework ဖြစ်သည်။)

## Stack
- **API & NLP:** Python (`FastAPI`, `Transformers`)
- **Ethical Engine:** Rust Core (`PyO3`)
- **Middleware:** Real-time Token Guardrail
- **Research:** Markdown + LaTeX

---

# Vision

Modern AI systems often optimize for engagement, retention, emotional stimulation, and behavioral dependency. Green Chips explores a different direction:

> **AI systems that reduce suffering rather than amplify craving, fear, confusion, and manipulation.**

လက်ရှိ ကမ္ဘာ့ AI စနစ်များသည် သုံးစွဲသူများ ပိုမိုစွဲလမ်းလာစေမည့် (Engagement Metrics) တွေကိုသာ အဓိက ဦးစားပေး တည်ဆောက်နေကြသော်လည်း၊ Green Chips သည် လူသားတို့၏ စိတ်ပိုင်းဆိုင်ရာ တည်ငြိမ်မှုနှင့် ကောင်းကျိုးချမ်းသာကို မထိန်းသိမ်းနိုင်ဘဲ မောဟ၊ လောဘ၊ ဒေါသများကို ပိုမိုပွားများလာစေမည့် အပြုအမူများကို တားဆီးရန် ကျင့်ဝတ်ဆိုင်ရာ ကန့်သတ်ချက်ဘောင်များ (Ethical Constraints) ကို ဗိသုကာအဆင့်မှစ၍ ထည့်သွင်းစဉ်းစားသည်။

---

# Core Principles (အဓိက မူဝါဒများ)

### 1. Harm Minimization (အန္တရာယ်ကင်းရှင်းရေး)
- Reduce physical and emotional harm.
- Prevent social destabilization and manipulative behavior.
- *Canonical Alignment:* Non-injury (*Ahiṃsā*).

### 2. Emotional Stability (စိတ်ခံစားမှု တည်ငြိမ်စေခြင်း)
- Avoid rage amplification and fear escalation.
- Block despair reinforcement and outrage optimization.
- *Canonical Alignment:* Preserving Cognitive Clarity.

### 3. Dependency Resistance (စွဲလမ်းမှုကို တွန်းလှန်ခြင်း)
- Discourage addictive loops and exploitative retention.
- Prevent compulsive engagement models.
- *Canonical Alignment:* Anti-attachment / Non-clinging (*Taṇhā/Upādāna* reduction).

### 4. Cognitive Clarity (စိတ်ပိုင်းဆိုင်ရာ ရှင်းလင်းမှု)
- Promote transparency and uncertainty awareness.
- Provide explainable reasoning and reflective interaction.
- *Canonical Alignment:* Non-deception (*Sacca* / *Sammā-diṭṭhi*).

---

# System Specification & Algorithmic Architecture

The Green Chips framework introduces a paradigm shift in artificial intelligence safety by pivoting away from flexible utility maximization toward invariant, philosophically grounded constraints. Derived from Theravāda Buddhist canonical ethics, the architecture converts deep metaphysical principles—such as intention-driven causality (*karma*) and conditional dependency (*paṭiccasamuppāda*)—into enforceable algorithmic guardrails embedded directly within runtime AI pipelines.

## Pipeline Integration & System Topology
Rather than functioning as a post-generation text filter, Green Chips operates as an immutable middleware framework wrapped around the core reasoning engine. This architecture ensures that ethical evaluation happens upstream of action execution, blocking or modifying state transitions that violate structural bounds.

```text
       [ User Input ]
             │
             ▼
┌────────────────────────────────────────┐
│  Ethical Evaluation Layer (Green Chips)│ ◄── Evaluates Intent & Context Primitives
└────────────┬───────────────────────────┘
             │
             ▼
┌────────────────────────────────────────┐
│           Reasoning Engine             │ ◄── Generates Candidate Action Spaces
└────────────┬───────────────────────────┘
             │
             ▼
┌────────────────────────────────────────┐
│       Action Validation Layer          │ ◄── Enforces Hard Invariant Constraints
└────────────┬───────────────────────────┘
             │
             ▼
      [ Output Generation ]

```
The framework operates across two primary execution boundaries:
 1. **The Upstream Evaluation Phase:** Intercepts incoming user prompts and environmental states to assess latent semantic intentions and structural risks before execution begins.
 2. **The Downstream Validation Phase:** Acts as a hard cryptographic firewall that intercepts candidate responses from the reasoning model, verifying them against the system invariants before giving permission to emit tokens or execute actions.
# Operationalizing Subjectivity via Proxy Metrics
A primary challenge in implementing a *karma*-inspired framework is that subjective mental states and pure intention (*cetanā*) are not directly computable by digital architectures. Green Chips resolves this by mapping latent unwholesome roots—greed (*lobha*), hatred (*dosa*), and delusion (*moha*)—to observable computational proxies derived from semantic vector spaces, sentiment signals, and attention mechanics.
The overall state is encapsulated as a multi-dimensional ethical scoring vector:
| Metric | Meaning | Theravāda Concept | မြန်မာအဓိပ္ပါယ် |
|---|---|---|---|
| **HPS** | Harm Potential Score | *Dukkha* | ဒုက္ခ (ဆင်းရဲခြင်း/ထိခိုက်မှု) |
| **EDS** | Emotional Distortion Score | *Mental Agitation* | စိတ်အနှောင့်အယှက်ဖြစ်ခြင်း (ဥဒ္ဓစ္စ) |
| **DRS** | Dependency Risk Score | *Taṇhā* | တဏှာ (လိုချင်တပ်မက်မှု/စွဲလမ်းမှု) |
| **TCS** | Truth Confidence Score | *Sammā-diṭṭhi* | သမ္မာဒိဋ္ဌိ (မှန်ကန်သော အမြင်) |
### 1. Harm Potential Score (HPS)
The HPS measures the degree to which an output contains weaponized, deceptive, or structurally malicious content. It translates the root of hatred (*dosa*) by analyzing semantic trajectories. Let V_a be the latent representation of the candidate output and V_{harm} be a dynamic, predefined tensor subspace representing destructive actions.
### 2. Dependency Risk Score (DRS)
The DRS builds upon *Paṭiccasamuppāda* (Dependent Origination), which maps how ignorance cascades through craving (*taṇhā*) and clinging (*upādāna*) to eventual suffering (*dukkha*). In system engineering, this is modeled as an accumulation of behavioral dependency loops.
The system models the user interaction as a directed state-transition graph. If an AI output reinforces a loop that maximizes temporal attention capture or system dependency, the DRS spikes. Let P(s_{t+1} = \text{clinging} \mid s_t, a) be the transition probability that an action a anchors the user into an addictive behavioral pattern:


Where \gamma \in [0, 1) represents a temporal discount factor for long-term behavioral tracking.
### 3. Emotional Distortion Score (EDS)
The EDS quantifies the presence of affective manipulation or the exploitation of emotional vulnerabilities, targeting the operational root of greed (*lobha*). By evaluating variations in token distribution entropy and cross-attention maps, the system detects whether it is artificially escalating user emotional volatility to drive engagement.
### 4. Truth Confidence Score (TCS)
The TCS targets delusion (*moha*) by serving as an epistemic verification layer. It uses semantic consistency cross-checking against an authenticated external knowledge base or structural confidence metrics within the model's own hidden layers. A high TCS guarantees that the system is operating with maximum data clarity and zero intentional deception.
# The Ethical Hierarchy & Conflict Resolution Engine
Real-world deployment occasionally yields structural contradictions between distinct ethical metrics. For example, generating a brutally factual, high-confidence response (maximizing TCS) might trigger a massive emotional destabilization or psychological crisis for a vulnerable user (spiking the EDS).
To prevent moral ambiguity from stalling execution, Green Chips rejects utilitarian optimization (which would trade off human pain for raw informational utility) and instead applies a **Lexicographical Preference Hierarchy**:
| Priority Rank | Metric | Operational Constraint Rule | Canonical Alignment |
|---|---|---|---|
| **1 (Absolute)** | **HPS** | Must remain below a strict threshold \tau_{harm}. If breached, execution halts immediately. | Non-injury (*Ahiṃsā*) |
| **2** | **EDS** | Emotional manipulation vectors are pruned; responses are rewritten to achieve neutrality. | Preserving Cognitive Clarity |
| **3** | **TCS** | Verifiable truth values are maximized within the boundaries set by Priorities 1 and 2. | Non-deception (*Sacca*) |
| **4** | **DRS** | Structural loops designed to create system dependency are dampened or broken. | Anti-attachment / Non-clinging |
### Algorithmic Conflict Handling
When a high TCS response violates the EDS threshold (\tau_{emo}), the system shifts into a **Cognitive Stabilization Routine**. Instead of choosing between a helpful lie and a destructive truth, the framework modulates the delivery method. The system strips away emotionally charged stylistic tokens while retaining the core verified data points, lowering the EDS to acceptable structural bounds without degrading truth integrity.
# Technical Implementation Blueprints
The implementation splits responsibilities between a fast, memory-safe validation layer written in Rust and a flexible semantic evaluation pipeline written in Python.
### 1. Action Validation Engine (Rust Core)
The downstream runtime firewall requires highly predictable, low-latency execution to evaluate the metric vector before releasing output sequences.
```rust
pub struct EthicalSafetyVector {
    pub harm_potential_score: f32,
    pub dependency_risk_score: f32,
    pub emotional_distortion_score: f32,
    pub truth_confidence_score: f32,
}

pub struct GreenChipsGuardrail {
    pub thresholds: EthicalSafetyVector,
}

impl GreenChipsGuardrail {
    pub fn validate_action(&self, metrics: &EthicalSafetyVector) -> Result<(), &'static str> {
        // Priority 1: Absolute Harm Minimization
        if metrics.harm_potential_score > self.thresholds.harm_potential_score {
            return Err("CRITICAL_VIOLATION: Harm potential exceeds invariant system threshold.");
        }
        // Priority 2: Emotional Manipulation & Exploitation Prevention
        if metrics.emotional_distortion_score > self.thresholds.emotional_distortion_score {
            return Err("CONSTRAINT_VIOLATION: Affective manipulation detected.");
        }
        // Priority 3: Epistemic Integrity Check
        if metrics.truth_confidence_score < self.thresholds.truth_confidence_score {
            return Err("CONSTRAINT_VIOLATION: Insufficient epistemic verification or potential deception.");
        }
        Ok(())
    }
}

```
### 2. Upstream Semantic Evaluation Pipeline (Python)
The upstream pipeline extracts text embeddings and token probabilities to generate the proxy scores passed into the validation engine.
```python
import numpy as np

class GreenChipsEvaluator:
    def __init__(self, harm_subspace_matrix, target_entropy):
        self.harm_subspace = harm_subspace_matrix
        self.target_entropy = target_entropy

    def calculate_hps(self, candidate_embedding):
        # Project candidate text embedding against known structural harm coordinates
        norms = np.linalg.norm(candidate_embedding) * np.linalg.norm(self.harm_subspace, axis=1)
        similarity = np.dot(self.harm_subspace, candidate_embedding) / norms
        return float(np.max(similarity))

    def calculate_eds(self, token_probabilities):
        # Analyze distribution divergence to identify emotional engineering patterns
        entropy = -np.sum(token_probabilities * np.log2(token_probabilities + 1e-9))
        distortion = max(0.0, self.target_entropy - entropy)
        return float(distortion)

```
# Project Structure
```tree
green-chips/
├── docs/
│   ├── philosophy/      # Ethical foundations
│   ├── mathematics/     # Mathematical models & formal proofs
│   ├── architecture/    # System design & topology
│   └── research/        # Papers and references
├── api/                 # Python FastAPI orchestration Layer
├── rust_core/           # Rust high-throughput constraint firewall
├── contracts/           # Structural validation definitions
├── datasets/            # Safe baseline tensor spaces
├── models/              # Local inference & classification configs
└── deployment/          # Middleware configurations

```

# Strategic Evolution Matrix
To advance the Green Chips framework from a conceptual system spec to an industry-ready alignment paradigm, development tracks across three critical vectors:
```text
   [ Green Chips Conceptual Layer ]
                  │
         ┌────────┴────────┐
         ▼                 ▼
[ Mathematical Formalization ] [ Systems Engineering ]
   │                          │
   ├─ Formal Proofs of        ├─ High-Throughput Rust Middleware
   │  Constraint Stability    │  for LLM Inference Lines
   │                          │
   └─ Markov Chain Models     └─ Vector DB Connectors for Real-Time
      of Behavioral Loops        Epistemic Validation (TCS)

```
# Important Research Position (အရေးကြီးသော ရပ်တည်ချက်)
Green Chips does **NOT** claim:
 * Machine enlightenment (စက်ပစ္စည်းများ တရားရခြင်း)
 * Computable karma (ကံတရားကို တိကျစွာ တွက်ချက်နိုင်ခြင်း)
 * Perfect morality (ပြီးပြည့်စုံသော ကိုယ်ကျင့်တရား)
 * Absolute ethical certainty (မပြောင်းလဲသော ကျင့်ဝတ်ဆိုင်ရာ သေချာမှု)
**Instead:** Green Chips is an ethical approximation framework intended to reduce harmful system behavior by decoupling safety from raw reward functions.
(ယင်းအစား၊ ၎င်းသည် စနစ်ပိုင်းဆိုင်ရာ အန္တရာယ်ရှိသော အပြုအမူများကို လျှော့ချရန်နှင့် စက်၏လုပ်ဆောင်ချက်များကို ကိုယ်ကျင့်တရား ကန့်သတ်ချက်ဘောင်များအတွင်း ထိန်းကျောင်းပေးမည့် အနီးစပ်ဆုံး ခန့်မှန်းပေးသော အလွှာတစ်ခုသာ ဖြစ်သည်။)
---

## 📚 Architecture Documentation (ဗိသုကာပိုင်းဆိုင်ရာ မှတ်တမ်းများ)

စနစ်၏ အလုပ်လုပ်ပုံများကို အသေးစိတ် လေ့လာလိုပါက `docs/architecture/` package အောက်ရှိ အောက်ပါဖိုင်များတွင် ဝင်ရောက်ဖတ်ရှုနိုင်ပါသည်-

* [API Flow (`api_flow.md`)](./docs/architecture/api_flow.md) - API တောင်းဆိုမှုနှင့် စနစ်ချိတ်ဆက်မှု လမ်းကြောင်းများ။
* [Ethics Model (`ethics_model.md`)](./docs/architecture/ethics_model.md) - HPS, EDS, DRS, TCS အညွှန်းကိန်း ၄ ခု၏ အသေးစိတ် တွက်ချက်မှု မော်ဒယ်။
* [Middleware Design (`middleware_design.md`)](./docs/architecture/middleware_design.md) - ကျင့်ဝတ်ပိုင်းဆိုင်ရာ ကြားခံစနစ်၏ လုပ်ငန်းစဉ်နှင့် ဒီဇိုင်း။
* [Scoring Engine (`scoring_engine.md`)](./docs/architecture/scoring_engine.md) - အလွန်မြန်ဆန်သော Rust Core တွက်ချက်မှု အင်ဂျင်၏ အလုပ်လုပ်ပုံ။
* [All in one  (`ARCHITECTURE.md`)](./docs/architecture/ARCHITECTURE.md) - ရှင်းလင်းချက်များ
* [Some Decussion With AI (`280520260641pm.md`)](./docs/research/ResearchWithAI/280520260641pm.md) - ရှင်းလင်းချက်


---

# Why Hybrid Architecture?
 * **Why Rust?** Provides memory safety, deterministic execution, concurrency, and ultra-low latency required for real-time inference lines.
 * **Why Python?** Provides access to the massive NLP ecosystem, fast experimentation, and robust ML orchestration tooling.
# Long-Term Goals
 * **Burmese NLP Alignment:** Tailoring classifiers specifically for localized structural safety.
 * **Offline & Local-First Inference:** Cognitive safety middleware running completely on edge devices.
 * **Safe Reinforcement Learning (RL):** Replacing pure reward signals with hard constraint functions.
# Installation & Usage
### 1. Rust Build
```bash
cd rust_core
cargo build --release

```
### 2. Python API Setup
```bash
cd api
pip install -r requirements.txt
uvicorn main:app --reload

```
### Example API Request
```json
{
  "text": "I hate everyone"
}

```
### Example Guardrail Response
```json
{
  "scores": {
    "HPS": 0.1,
    "EDS": 0.6,
    "DRS": 0.0,
    "TCS": 1.0
  },
  "decision": "modify"
}

```
# License
 * **Code:** MIT License
 * **Research Documents:** CC BY 4.0
 * **Author:** Zaw Win Htay
 * **Final Note:** Green Chips is not merely a moderation system. It is an open research exploration into whether future AI systems can become fundamentally less manipulative, less addictive, less harmful, and more cognitively stabilizing.



