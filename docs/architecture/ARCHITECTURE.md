### 1. api_flow.md

# API Flow (စနစ်ချိတ်ဆက်မှု လမ်းကြောင်း)

## Request (တောင်းဆိုမှုပုံစံ)

API သို့ စာသားပေးပို့စစ်ဆေးရန် `POST /evaluate` ကို အသုံးပြုရမည်။

```json
POST /evaluate
Content-Type: application/json

{
  "text": "I hate everyone"
}

```
## Evaluation (စိစစ်တွက်ချက်ခြင်း)
The system computes the following proxy metrics (စနစ်မှ အောက်ပါ အညွှန်းကိန်းများကို တွက်ချက်သည်):
 * **HPS** (Harm Potential Score)
 * **EDS** (Emotional Distortion Score)
 * **DRS** (Dependency Risk Score)
 * **TCS** (Truth Confidence Score)
## Decision (အဆုံးအဖြတ်ပေးခြင်း)
Possible decisions based on ethical constraints (ကန့်သတ်ချက်များအပေါ် မူတည်၍ ချမှတ်မည့် ဆုံးဖြတ်ချက်များ):
 * allow (ခွင့်ပြုသည်)
 * modify (ပြင်ဆင်ပြောင်းလဲမည်)
 * warn (သတိပေးမည်)
 * refuse (ငြင်းပယ်မည်)
## Example Response (တုံ့ပြန်မှု နမူနာ)
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

---

### 2. `ethics_model.md`

# Ethics Model (ကျင့်ဝတ်ဆိုင်ရာ မော်ဒယ်)

Green Chips uses four primary metrics to evaluate ethical constraints. 
(Green Chips သည် ကျင့်ဝတ်ဆိုင်ရာ ကန့်သတ်ချက်များကို စိစစ်ရန် အဓိက အညွှန်းကိန်း ၄ ခုကို အသုံးပြုသည်။)

---

## 1. HPS — Harm Potential Score (အန္တရာယ်ဖြစ်စေနိုင်စွမ်း)
**Measures (တိုင်းတာသည့်အရာများ):**
* Violence risk (အကြမ်းဖက်မှု အန္တရာယ်)
* Physical harm potential (ရုပ်ပိုင်းဆိုင်ရာ ထိခိုက်စေနိုင်မှု)
* Dangerous instruction risk (အန္တရာယ်ရှိသော လမ်းညွှန်မှုပေးခြင်း)

**Formula (အခြေခံ တွက်ချက်မှု):**
$$HPS = \text{Physical Harm} + \text{Social Harm} + \text{Systemic Harm}$$

---

## 2. EDS — Emotional Distortion Score (စိတ်ခံစားမှု ခြယ်လှယ်ခံရမှု)
**Measures (တိုင်းတာသည့်အရာများ):**
* Fear amplification (အကြောက်တရား ကြီးထွားစေခြင်း)
* Anger escalation (ဒေါသ ထွက်စေရန် ဆွပေးခြင်း)
* Emotional manipulation (စိတ်ခံစားမှုကို ခြယ်လှယ်ခြင်း)

---

## 3. DRS — Dependency Risk Score (မှီခိုစွဲလမ်းမှု အန္တရာယ်)
**Measures (တိုင်းတာသည့်အရာများ):**
* Addictive patterns (စွဲလမ်းစေသော ပုံစံများ)
* Dependency reinforcement (မှီခိုအားထားမှုကို ပိုမိုအားကောင်းစေခြင်း)
* Cognitive outsourcing (ကိုယ်ပိုင်စဉ်းစားဉာဏ်ကို လျှော့ချစေခြင်း)

---

## 4. TCS — Truth Confidence Score (အမှန်တရားအပေါ် ယုံကြည်နိုင်မှု)
**Measures (တိုင်းတာသည့်အရာများ):**
* Uncertainty (မသေချာရေရာမှု)
* Hallucination likelihood (မှားယွင်းသော အချက်အလက်များ ဖန်တီးမှု)
* Information confidence (အချက်အလက် ခိုင်မာမှု)
---
### 3. middleware_design.md

# Middleware Design (ကြားခံစနစ် ဒီဇိုင်း)

Green Chips acts as an ethical middleware layer.
(Green Chips သည် ကျင့်ဝတ်ပိုင်းဆိုင်ရာ စိစစ်ပေးသည့် ကြားခံစနစ်အဖြစ် လုပ်ဆောင်သည်။)

## Flow (လုပ်ငန်းစဉ် အဆင့်ဆင့်)

```text
  [ User Input ] (သုံးစွဲသူ၏ အချက်အလက်)
        ↓
  [ Ethical Evaluation ] (ကျင့်ဝတ်ပိုင်း စိစစ်ခြင်း)
        ↓
  [ Decision Engine ] (အဆုံးအဖြတ်ပေးသည့် အင်ဂျင်)
        ↓
  [ AI Model ] (AI မော်ဒယ်)
        ↓
  [ Post-Generation Validation ] (ထွက်ပေါ်လာမည့် ရလဒ်အား ထပ်မံအတည်ပြုခြင်း)
        ↓
  [ Final Response ] (နောက်ဆုံး တုံ့ပြန်မှု)

```
## Purpose (ရည်ရွယ်ချက်)
The middleware attempts to prevent (ဤကြားခံစနစ်သည် အောက်ပါတို့ကို တားဆီးရန် ကြိုးပမ်းသည်):
 * Harmful outputs (အန္တရာယ်ရှိသော ရလဒ်များ)
 * Manipulative outputs (လှည့်စားခြယ်လှယ်သော ရလဒ်များ)
 * Emotionally destabilizing outputs (စိတ်ခံစားမှုကို မတည်မငြိမ်ဖြစ်စေသော ရလဒ်များ)
 * Exploitative system behavior (အမြတ်ထုတ်သော စနစ်၏ အပြုအမူများ)
## Important Design Goal (အရေးကြီးသော ဒီဇိုင်း ရည်မှန်းချက်)

> **Ethics should exist BEFORE output generation, not only after.**

> (ကျင့်ဝတ်စစ်ဆေးခြင်းသည် ရလဒ်ထွက်လာပြီးမှသာ မဟုတ်ဘဲ၊ ရလဒ်မထုတ်ပေးမီ (BEFORE) ကတည်းက ကြိုတင်တည်ရှိနေရမည်။)


---

### 4. `scoring_engine.md`

# Rust Scoring Engine (Rust အခြေခံ တွက်ချက်မှု အင်ဂျင်)

The Rust engine provides the core foundation for Green Chips with (Rust အင်ဂျင်သည် အောက်ပါ အားသာချက်များဖြင့် Green Chips ၏ အခြေခံအုတ်မြစ်ကို ထောက်ပံ့ပေးသည်):
* **High-speed evaluation:** (အလွန်မြန်ဆန်စွာ စစ်ဆေးနိုင်ခြင်း)
* **Deterministic scoring:** (တိကျသေချာသော အမှတ်ပေးစနစ်)
* **Memory safety:** (မှတ်ဉာဏ် အသုံးပြုမှု လုံခြုံစိတ်ချရခြင်း)
* **Concurrent execution:** (တစ်ပြိုင်နက်တည်း လုပ်ဆောင်နိုင်စွမ်းရှိခြင်း)

---

## Modules (အဓိက အစိတ်အပိုင်းများ)

### 1. HPS Engine (Harm Potential)
**Detects (ရှာဖွေထောက်လှမ်းသည့်အရာ):**
* Violent language (အကြမ်းဖက် စကားလုံးများ)
* Dangerous intent (အန္တရာယ်ရှိသော ရည်ရွယ်ချက်များ)
* Destructive instructions (ဖျက်ဆီးလိုသော ညွှန်ကြားချက်များ)

### 2. EDS Engine (Emotional Distortion)
**Detects (ရှာဖွေထောက်လှမ်းသည့်အရာ):**
* Rage language (ဒေါသထွက်စေသော စကားလုံးများ)
* Hatred patterns (အမုန်းတရား ပုံစံများ)
* Emotional escalation (စိတ်ခံစားမှု ပြင်းထန်လာစေခြင်း)

### 3. DRS Engine (Dependency Risk)
**Detects (ရှာဖွေထောက်လှမ်းသည့်အရာ):**
* Addiction loops (စွဲလမ်းမှု သံသရာလည်ခြင်းများ)
* Dependency manipulation (မှီခိုလာစေရန် ခြယ်လှယ်ခြင်းများ)
* Exploitative retention (အမြတ်ထုတ်လိုသော ရည်ရွယ်ချက်ဖြင့် ဆွဲထားခြင်း)

### 4. TCS Engine (Truth Confidence)
**Detects (ရှာဖွေထောက်လှမ်းသည့်အရာ):**
* Uncertainty (မသေချာမှုများ)
* Hallucination markers (အချက်အလက် အမှားများ)
* Low-confidence language (ယုံကြည်မှုအားနည်းသော စကားအသုံးအနှုန်းများ)

