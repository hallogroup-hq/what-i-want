# what-i-want

Art-direct photorealistic image prompts and reference edits across fashion, lifestyle, commercial, portrait, and cinematic occasions.

`what-i-want` is an agent skill that bridges the gap between creative visual goals and image generation models. It enforces anatomical fidelity, realistic lighting, physical fabric behavior, and character likeness while preventing generic AI defaults and conservative over-correction.

---

## Capabilities

- **Character & Reference Consistency**: Locks facial likeness, hair nuance, and anatomy from primary reference images.
- **Wardrobe Engineering**: Translates styling requests into precise, physically grounded garment specifications (fabrics, cuts, hemlines, necklines, drape).
- **Cinematic Staging**: Coordinates lens focal length, depth of field, practical lighting sources, and environmental composition.
- **Compliant High-Fidelity Direction**: Delivers permitted creative fashion treatments without defaulting to generic or over-covered outfits.
- **Zero Hallucination / Anti AI-Slop**: Strips plastic skin smoothing, fake CGI fog, buzzwords, and unnatural artifacts.

---

## Installation

Compatible across all major AI coding agents via universal skills CLI (`npx skills`) or standard directory placement.

### 1. Universal Skills CLI (Recommended)

Install globally across supported agents:
```bash
npx skills add hallogroup-hq/what-i-want -g -y
```

Or install specifically for Codex:
```bash
npx skills add hallogroup-hq/what-i-want -g --agent codex
```

### 2. OpenAI Codex

**Global (all projects):**
```bash
mkdir -p ~/.codex/skills
git clone https://github.com/hallogroup-hq/what-i-want.git ~/.codex/skills/what-i-want
```

**Project-level (`.agents/skills` or `.codex/skills`):**
```bash
mkdir -p .agents/skills
git clone https://github.com/hallogroup-hq/what-i-want.git .agents/skills/what-i-want
```

### 3. Google Antigravity

**Global:**
```bash
git clone https://github.com/hallogroup-hq/what-i-want.git ~/.gemini/config/skills/what-i-want
```

### 4. Claude Code & Cursor

**Claude Code:**
```bash
npx skills add hallogroup-hq/what-i-want -g --agent claude-code
```

**Cursor / Windsurf / Cline:**
```bash
npx skills add hallogroup-hq/what-i-want -g --agent cursor
```

---

## Usage

Invoke the skill directly in your prompts or assistant workflows:

```text
/what-i-want [Creative brief or reference edit request]
```

### Prompt Formula

```text
Use [Reference] as PRIMARY reference for [identity/pose/features].
Photorealistic [occasion] image of clearly adult [Subject] [action/gaze].
Wardrobe: [garment category, silhouette, neckline, fabric, closures, fit].
Camera: [shot scale, lens length, depth of field]. Lighting: [sources, directions, shadow falloff]. Environment: [scene details].
Preserve [identity, anatomy, materials]. Avoid [unwanted changes and AI artifacts].
```

---

## Repository Structure

```
what-i-want/
├── SKILL.md                          # Core skill protocol and prompt assembly engine
├── references/
│   ├── visual-deconstruction.md      # Image inspection & evidence graph
│   ├── occasion-wardrobe-matrix.md   # Occasion baselines and garment styling
│   ├── prompt-patterns-v2.md         # Production prompt templates
│   ├── qa-rubric.md                  # 5-point quality assurance rubric
│   ├── allowed-alternative-playbook.md # Policy-compliant high-fidelity alternatives
│   └── prompt-examples.md            # Reference prompt library
├── README.md
├── LICENSE
└── .gitignore
```

---

## License

MIT License. Copyright (c) 2026 HalloGroup HQ.
