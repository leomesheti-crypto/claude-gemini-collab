# Claude + Gemini Collaboration Hub

Two-model refinement workflow for pitch documents, landing pages, and design work.

## Philosophy

- **Claude Code** (80%): Heavy lifting - research, structure, initial design, self-iteration
- **Gemini** (20%): Fresh eyes - visual polish, alternative ideas, catching details

## Live Previews

All projects are deployed to GitHub Pages:
**Base URL:** https://leomesheti-crypto.github.io/claude-gemini-collab/

## Projects

| Project | Status | Description |
|---------|--------|-------------|
| [ai-agency-pitch](projects/ai-agency-pitch/) | In Review | Sales one-pager for AI services |

## Structure

```
claude-gemini-collab/
├── README.md                    # This file
├── _templates/                  # Reusable review prompts
│   └── REVIEW-PROMPT.md
└── projects/
    └── {project-name}/          # One folder per project
        ├── README.md            # Project brief & status
        ├── drafts/              # Claude's work-in-progress
        ├── gemini-feedback/     # Gemini's reviews
        └── final/               # Approved deliverables
```

## Workflow

### 1. Start New Project
```bash
# Create project folder
mkdir -p projects/{project-name}/{drafts,gemini-feedback,final}

# Add project README with brief
```

### 2. Claude Creates Draft
- Uses established skills and patterns
- 2-3 self-iterations before handoff
- Commits to `projects/{name}/drafts/`

### 3. Gemini Reviews
- Access via GitHub Pages URL or read code directly from repo
- Use prompt template from `_templates/REVIEW-PROMPT.md`
- Save feedback to `projects/{name}/gemini-feedback/`

### 4. Claude Implements Refinements
- Review Gemini's feedback
- Implement chosen suggestions
- Final version goes to `projects/{name}/final/`

## How Gemini Accesses Files

**Option A: Live Preview (Visual)**
```
https://leomesheti-crypto.github.io/claude-gemini-collab/projects/{name}/drafts/{file}.html
```

**Option B: Raw Code (Direct)**
```
https://github.com/leomesheti-crypto/claude-gemini-collab/blob/master/projects/{name}/drafts/{file}.html
```

Both give Gemini full access to the actual files, not screenshots.

## Adding a New Project

1. Create folder: `projects/{project-name}/`
2. Add subfolders: `drafts/`, `gemini-feedback/`, `final/`
3. Create `README.md` with:
   - Brief (what is it)
   - Target audience
   - Goal
   - Brand feel
   - Status table
4. Start creating in `drafts/`

## Templates

See `_templates/` for:
- `REVIEW-PROMPT.md` - Standard, quick, and deep review prompts for Gemini
