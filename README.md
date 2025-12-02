# Claude + Gemini Collaboration Workflow

Two-model refinement process for pitch documents and website designs.

## Philosophy

- **Claude Code** (80%): Heavy lifting - research, structure, initial design, self-iteration
- **Gemini** (20%): Fresh eyes - visual polish, alternative ideas, catching details

## Workflow

```
Claude Code → drafts/ → Gemini Review → gemini-feedback/ → Claude implements → final/
```

### Step 1: Claude Code Creates Draft
Claude uses established skills and patterns to produce a near-final version:
- `frontend-design` skill for aesthetics
- `library/patterns/` for proven templates
- 2-3 self-iterations before handoff

Output: `drafts/{project}-v{n}.html`

### Step 2: Gemini Reviews
Use the prompt template in `gemini-feedback/REVIEW-PROMPT.md`

Gemini provides:
- Visual critique (what feels off?)
- Micro-refinements (spacing, alignment, color)
- Alternative suggestions (what if we tried...?)
- Fresh ideas to consider

Output: `gemini-feedback/{project}-v{n}-review.md`

### Step 3: Claude Implements
Claude Code reviews Gemini's feedback and implements chosen refinements.

Output: `final/{project}-final.html`

### Step 4: (Optional) Alternative Explorations
If Gemini suggests interesting alternative directions, explore in:
`alternatives/{project}-{variation}/`

## Directory Structure

```
claude-gemini-collab/
├── README.md                 # This file
├── drafts/                   # Claude's near-final versions
│   └── {project}-v{n}.html
├── gemini-feedback/          # Gemini's reviews
│   ├── REVIEW-PROMPT.md      # Template for Gemini
│   └── {project}-v{n}-review.md
├── final/                    # Approved final versions
│   └── {project}-final.html
└── alternatives/             # Alternative directions
    └── {project}-{variation}/
```

## Current Projects

| Project | Status | Location |
|---------|--------|----------|
| AI Agency Pitch | In Review | `drafts/ai-agency-pitch-v1.html` |

## Tips for Good Gemini Reviews

1. **Share the screenshot**, not just the code
2. **Give context**: "This is for local service businesses"
3. **Be specific**: "Focus on visual polish, not content changes"
4. **Ask for 3 things**: Keeps feedback actionable
