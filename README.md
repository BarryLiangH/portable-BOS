# Portable BOS — Block Operating System

**A model-independent development protocol for building AI products.**

Created by: **Barry H Liang**  
License: MIT  
Current version: [v1.4.9](https://github.com/barryliang/portable-bos/releases)

---

## What Is BOS?

Portable BOS is a governance framework that lets solo developers and small teams build and ship AI products using a proven discipline: step-by-step planning, block-by-block development, verification before delivery, and one person as the confirming tester (never the first tester).

BOS was born from real projects:
- **HomeVisualizer** — a room design system with 2D/3D preview (37+ blocks)
- **DocAgent** — a Windows desktop app for AI-assisted document processing (32+ blocks)
- **IntelliDoc Advisor** — in planning (office document analysis with litigation/financial advisories)

It works with any AI provider (Claude, ChatGPT, Gemini, DeepSeek) because BOS is a *procedure*, not a model.

---

## Why BOS?

- **No manual testing loops** — every block is verified before you install it
- **Every change is journaled** — you see why each version exists and what it added
- **One author, always** — governance rules prevent ownership from getting lost across versions
- **Works across sessions** — carry BOS between conversations via a single ZIP file
- **Catches planning gaps early** — the Incubator gate checks everyday usability before coding starts
- **Scales predictably** — HomeVisualizer grew from 1 room to 3D preview in 37 blocks; each block cost 1-2 AI rounds

---

## Quick Start (5 Minutes)

### For AI Users (Claude, ChatGPT, etc.)

1. **Download the latest release** — [Portable_BOS_v1.49.zip](https://github.com/barryliang/portable-bos/releases)
2. **Upload the ZIP** to your AI chat
3. **Say:**
   ```
   I uploaded the BOS ZIP. Read 00_FIRST_READ_ME.md and carry on.
   ```
4. **The AI activates BOS** and walks you through the rest

### For Manual Use (Reading the Docs)

1. Download and extract the ZIP
2. Start with: `BOS_version_1.4/00_BOOTSTRAP/BOS_CORE_DIGEST.md`
3. Follow the activation manifest: `BOS_ACTIVATION_MANIFEST.md`

---

## Documentation Map

| Document | Purpose |
|----------|---------|
| `00_FIRST_READ_ME.md` | Quick orientation (read first) |
| `BOS_version_1.4/00_BOOTSTRAP/BOS_CORE_DIGEST.md` | Philosophy and core concepts |
| `BOS_version_1.4/08_INCUBATOR/IDEA_INCUBATOR_v1.1.md` | Turn a rough idea into a builder-ready plan |
| `BOS_version_1.4/02_ENGINEERING/EFFICIENT_BLOCK_ROUND_RULES.md` | How to deliver blocks without costly retesting |
| `BOS_version_1.4/06_STANDARDS/DAILY_USE_CONTROLS_BASELINE.md` | Everyday usability checklist (font size, undo/redo, etc.) |
| `BOS_version_1.4/12_UPGRADE_SYSTEM/BOS_UPGRADE_JOURNAL.md` | Complete version history and what changed |
| `BOS_version_1.4/10_GOVERNANCE/BOS_GROWTH_GOVERNANCE.md` | How BOS evolves and who controls it |

---

## Real Example: HomeVisualizer

HomeVisualizer reached **Block 37** using BOS:

```
Block 1-10   → Core floor-plan model and 2D editing
Block 11-20  → Furniture placement and room editing
Block 21-30  → 3D data structures and preview foundation
Block 31-37  → 3D rendering and user-facing features
```

Each block followed the same discipline:
1. Plan the block (Incubator gate checks daily-use controls)
2. Build and test
3. Verification runs (pre-delivery and clean-extract)
4. Barry runs it to confirm
5. Journal entry records what changed and why

**Result:** No surprise missing Undo buttons. No "we need to redo the folder picker." Every block was ready when delivered.

---

## Key Concepts

### The Block
A Block is one focused unit of work:
- Adds one feature or fixes one class of bugs
- Takes 1-2 AI rounds to plan and build
- Includes verification before delivery
- Has a checkpoint sentence and a next-approval sentence

### The Incubator
Turns a rough idea into a builder-ready plan by answering:
- Is this practical and user-friendly?
- Does it have everyday usability covered (font size, folder pickers, undo/redo)?
- What's the daily operation flow?
- What's the first block?

### Daily-Use Controls Baseline
Before any block is approved, the plan must answer for:
- Font size adjustable
- No clipped or overlapped text
- Folder pickers (not raw path typing)
- Undo/Redo on editing surfaces
- Clear success/failure feedback
- Remembered settings between sessions
- [13 more items — see DAILY_USE_CONTROLS_BASELINE.md]

### Verification Gates
Every block passes before delivery:
1. **Pre-Delivery Execution Gate** — the AI runs the test suite and shows real output
2. **Clean-Extract Package Test Gate** — the ZIP extracts cleanly and verification passes
3. **User Content Survival Gate** — existing user files don't get overwritten
4. **Package QA Gate** — checksums match, no stale files

---

## Releases

Every release includes:
- **Portable_BOS_vX.YZ.zip** — the full package
- **Portable_BOS_vX.YZ.sha256.txt** — checksum for integrity verification

See the [Releases page](https://github.com/barryliang/portable-bos/releases) for all versions.

### Version Numbering
- `v1.48` = internal v1.4.8 (Efficient Block Round Rules)
- `v1.49` = internal v1.4.9 (Universal Incubation Upgrade)
- `v1.50` = internal v1.5.0 (future)

The internal version is always available in `VERSION.txt`.

---

## Contributing

BOS is Barry's governance protocol, and contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

Types of contributions that help:
- Bug reports (use the issue template)
- Documentation improvements
- Case studies of products built with BOS
- Translations
- Questions (opens discussion)

Major architectural changes are unlikely to be merged, but you can fork and maintain your own version.

---

## Philosophy in One Sentence

**Barry should never be the person who discovers a missing Undo button — that's the AI's job to plan before building.**

---

## License

MIT — see [LICENSE.txt](LICENSE.txt)

You can use, modify, and distribute Portable BOS freely. Credit required; warranty disclaimed.

---

## Questions?

- **How do I use BOS for my project?** → Start with the Quick Start above, then read BOS_CORE_DIGEST.md
- **Can I fork BOS and make my own version?** → Yes. The MIT license allows it.
- **How do I report a bug?** → Open an issue using the template
- **Who maintains BOS?** → Barry H Liang. Improvements are reviewed and integrated back into this canonical version.

---

*Portable BOS v1.4.9 — Universal Incubation Upgrade*  
*Built for solo developers and small teams who want to ship AI products without surprises.*
