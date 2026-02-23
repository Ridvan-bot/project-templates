# Troubleshooting log (LLM context)

**Use when:** You're debugging something – add information here continuously so everything is in one place. Update often during the troubleshooting.

Tips:
- Write short and concrete. Prefer bullets over long text.
- Do NOT store secrets. Use placeholders.
- Paste exact error messages and relevant log lines.

---

## 0) Quick status (update often)

- **Customer/environment:** *(name)*
- **Goal:** *(what needs to be resolved)*
- **Current problem:** *(short description of the issue right now)*
- **Status:** *(e.g. Active debugging / Waiting on X / Resolved / Paused)*
- **Last updated:** *(YYYY-MM-DD)*
- **Next steps:** *(what we'll test or check next)*

---

## 1) Environment overview

- **Platform:** *(e.g. Azure DevOps, application, OS)*
- **Affected components:** *(servers, services, versions)*
- **Network topology / dependencies (brief):** *(if relevant)*
- **Other context:** *(security, firewall, accounts – no secrets)*

---

## 2) Problem definition (what’s wrong)

- **Symptom:** *(what happens / what the user sees)*
- **Error messages:** *(paste exact messages and codes)*
  - *
  - *
- **Where it occurs:** *(which step, which environment, which server)*
- **How often:** *(always / sometimes / after X)*
- **When did it start:** *(if known)*

---

## 3) Hypotheses (prioritised)

1. **Hypothesis A** *(short)* – *(reasoning)*
2. **Hypothesis B** *(short)* – *(reasoning)*
3. *(Add/remove as we learn more.)*

---

## 4) Experiments and results (timeline)

One block per attempt. Update as you go.

### YYYY-MM-DD HH:MM – Short title
- **Change/test:**
- **Commands/config:**
- **Result:**
- **Conclusion:**
- **Next:**

### (example) 2026-02-16 – Artifact download test
- **Change/test:** Run "Download artifacts from file share" against given path.
- **Result:** scandir UNKNOWN (errno -4094).
- **Conclusion:** Likely path or permissions.
- **Next:** Check task order and read access.

*(Add more blocks as the troubleshooting progresses.)*

---

## 5) Known facts (verified)

- *(Things we know to be true – e.g. "Port 445 is open", "Works in env X but not Y")*
- *
- *

---

## 6) Open questions (need answers)

- *(What we still don't know or need to check)*
- *

---

## 7) Copy/paste – commands we use often

*(Relevant commands for this troubleshooting.)*

```bash
# example
```
