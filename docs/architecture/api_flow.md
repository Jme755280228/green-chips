# API Flow

## Request

POST /evaluate

{
  "text": "I hate everyone"
}

---

# Evaluation

The system computes:

- HPS
- EDS
- DRS
- TCS

---

# Decision

Possible decisions:

- allow
- modify
- warn
- refuse

---

# Example Response

{
  "scores": {
    "HPS": 0.1,
    "EDS": 0.6,
    "DRS": 0.0,
    "TCS": 1.0
  },
  "decision": "modify"
}

