# Contributing to Portable BOS

Thank you for your interest in contributing to Portable BOS!

Portable BOS is Barry H Liang's governance protocol for building AI products. It reflects hard-won lessons from real projects (HomeVisualizer, DocAgent, IntelliDoc Advisor). Contributions are welcome, and the canonical version is maintained here.

---

## Before You Contribute

**BOS is opinionated.** Every rule and gate exists because it solved a real problem. Before suggesting a change, ask yourself:

- Does this improve the core philosophy? (One author stays in control. Barry is the confirming tester, never the first tester. Every change is journaled.)
- Does this help solo developers or small teams?
- Is this a bug fix, clarification, or new feature?

**Suggestions that align with BOS philosophy are much more likely to be accepted.**

Major architectural rewrites (removing governance rules, changing the block structure, overhaul of the upgrade system) will not be merged into the canonical version. You can fork and maintain your own branch.

---

## How to Contribute

### 1. Open an Issue First
**Before you code, open an issue.** Describe:
- What you want to change
- Why it helps BOS
- Which part of the philosophy it serves (or if it's a bug fix, what broke)

Examples of good issues:
- "DAILY_USE_CONTROLS_BASELINE.md is missing item X, which caused bug Y"
- "The Incubator Step 12B gate description is confusing; here's a clearer wording"
- "HomeVisualizer case study: how we used BOS to reach Block 37"

### 2. Fork the Repository
```bash
git clone https://github.com/YOUR_USERNAME/portable-bos.git
cd portable-bos
git checkout -b your-feature-branch
```

### 3. Make Your Changes
- Edit the markdown files you want to improve
- Test that your changes are clear and accurate
- If you're updating a module, update the version in `BOS_UPGRADE_JOURNAL.md`

### 4. Submit a Pull Request
```bash
git add .
git commit -m "Clear description of what changed and why"
git push origin your-feature-branch
```

Then open a pull request on GitHub. Link the issue you opened in step 1.

### 5. Barry Reviews and Merges (or Explains Why Not)
You'll get feedback. If the change aligns with BOS philosophy, it gets merged into the main version. If not, Barry will explain why and you keep your fork.

---

## What Kinds of Contributions Help

### Bugs & Clarifications ✓
- "The VERIFY_BOS_PACKAGE.ps1 script fails when X"
- "The Incubator Step 12B description says Y but means Z"
- "DELIVERY_PROFILE.md should mention Z"

### Documentation ✓
- Clearer wording for any module
- Better examples in the Incubator
- Corrections to the upgrade journal (if dates/versions are wrong)

### Case Studies ✓
- "Here's how I used BOS to build X"
- "HomeVisualizer taught us Y"
- "DocAgent benefited from BOS because Z"

### Translations ✓
- BOS in other languages (Spanish, Chinese, etc.)
- Professional proofreading

### Questions ✓
- "I don't understand Step 12B" → open a discussion
- "Does BOS work for X kind of project?" → we'll help figure it out

### New Domain Extensions ✓
- "I built a domain extension for data-intensive systems"
- "Here's what the Blockchain Extension looks like"
- These live in `08_INCUBATOR/domain_extensions/`

---

## What Won't Be Merged

### Version History Rewriting ✗
The `BOS_UPGRADE_JOURNAL.md` is append-only. You can:
- Add a new entry for v1.50, v1.51, etc.
- Correct a date or typo in an existing entry

You cannot:
- Delete old entries
- Rewrite why a version was released
- Change author attribution

### Removing Governance Rules ✗
Rules like the Daily-Use Controls Baseline, Efficient Block Round Rules, and the Package QA Gate exist because they prevented real bugs. Removing them will not be merged.

You can:
- Propose clarifications
- Add to the checklist if you found a gap
- Create your own fork with different rules

### Breaking Changes to Core Files ✗
- OWNER.md (creator attribution)
- MODULE_REGISTRY.md structure (breaking the activation system)
- VERSION.txt format
- BOS_ACTIVATION_MANIFEST.md structure

---

## The BOS Philosophy (For Reference)

If you want your contribution merged, understand these principles:

1. **One Author, Always** — the creator's vision stays intact through governance rules
2. **Barry Is the Confirming Tester, Not the First** — every block is verified before he runs it
3. **Every Change Is Journaled** — there is no silent patch; the upgrade journal explains everything
4. **Practical Over Perfect** — BOS solves real problems; it doesn't aim for academic purity
5. **Daily-Use Basics Are Planned, Not Patched** — the AI plans font size, undo/redo, folder pickers before building; Barry never discovers missing basics in testing
6. **Blocks Are Focused Units** — one feature, one round, one verification

---

## Example: How a Good Contribution Looks

**Issue:** "DAILY_USE_CONTROLS_BASELINE.md item 2.1 is missing 'remember folder history' — I had to keep re-browsing the same folder on every run"

**Your fork:**
- Updates DAILY_USE_CONTROLS_BASELINE.md to add item 2.1B
- Updates DOMAIN_EXTENSION_INDEX.md if the extension needs it
- Adds a journal entry note (if you're testing it)

**Your pull request:**
- Title: "Add 'remember folder history' to Daily-Use Controls Baseline"
- Description: "When users pick a folder repeatedly, the app should offer recent folders. This gap caused redundant clicks in DocAgent."
- Links the issue

**Barry reviews:** Merges it because it closes a real gap. The next version (v1.50) includes your improvement.

---

## Questions?

- **How long do reviews take?** — Usually 1-2 weeks
- **Can I request a review sooner?** — Yes, mention it in the PR; critical fixes get priority
- **What if my PR gets rejected?** — You keep your fork. You can maintain your version or help us understand the blocker
- **Can I become a maintainer?** — The canonical BOS is maintained by Barry. You can fork and maintain your own version; that's the point of open source

---

## Thank You

Every contribution helps solo developers and small teams build AI products better. We appreciate you.

— Barry H Liang & the BOS Community
