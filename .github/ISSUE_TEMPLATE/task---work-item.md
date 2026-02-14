---
name: Task / Work item
about: Single work item for AI-Home
title: ''
labels: task
assignees: ''

---

name: "Task / Work item"
description: "Single work item for AI-Home (bug/feature/note) — sanitized."
title: "[TASK] "
labels: ["task", "triage"]
assignees: []
body:
  - type: dropdown
    id: kind
    attributes:
      label: Type
      options:
        - Bug
        - Feature
        - Docs
        - Idea
        - Chore
    validations:
      required: true

  - type: textarea
    id: goal
    attributes:
      label: Goal
      description: "What do we want as the outcome?"
      placeholder: "Example: Add minimal landing page under /docs with 1 button."
    validations:
      required: true

  - type: textarea
    id: context
    attributes:
      label: Context / Links
      description: "Relevant pages, files, screenshots (NO secrets)."
      placeholder: "- Repo path: docs/\n- Page: https://technik555.ru/\n- Related issue: #"
    validations:
      required: false

  - type: textarea
    id: steps
    attributes:
      label: Steps / Notes
      description: "If bug — how to reproduce. If feature — rough steps."
      placeholder: "1) ...\n2) ...\n3) ..."
    validations:
      required: false

  - type: textarea
    id: acceptance
    attributes:
      label: Done criteria
      description: "How we know it is done."
      placeholder: "- Works on GitHub Pages\n- README updated\n- No secrets in repo"
    validations:
      required: false

  - type: checkboxes
    id: safety
    attributes:
      label: Publish rules (MUST)
      options:
        - label: "No keys/tokens/passwords/personal data in text or screenshots"
          required: true
        - label: "No hardcoded local paths (C:\\, H:\\) unless it’s a public example"
          required: true
        - label: "Sensitive strings replaced with placeholders (e.g., <TOKEN>)"
          required: true
