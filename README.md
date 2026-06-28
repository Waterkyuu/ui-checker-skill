# UI Checker Skill

[中文文档](README.zh-CN.md)

`ui-checker` is a Codex/agent skill for reviewing front-end UI quality when there is no designer in the loop. It helps an agent identify why a page feels messy, inconsistent, rough, or amateurish, then turn those observations into concrete fixes.

The skill is built around four practical UI principles:

- **Consistency**: typography, colors, buttons, icons, radius, shadows, borders, and component structure.
- **Spacing**: page padding, section spacing, item gaps, card padding, and density.
- **Alignment**: text, icons, buttons, forms, lists, tables, and headers.
- **Feedback**: hover, active, focus-visible, disabled, loading, empty, error, success, and permission states.

## When To Use

Use this skill when you want an agent to:

- Review whether a UI looks cluttered, inconsistent, or unfinished.
- Improve an AI-generated front-end project without a dedicated designer.
- Check screenshots, page implementations, Tailwind classes, CSS, or component files.
- Find concrete UI quality issues instead of giving vague feedback like “looks good” or “needs polish.”
- Produce a prioritized fix list and a copyable prompt for another coding agent.

Example prompts:

```text
Use ui-checker to review this page and tell me why it feels messy.
```

```text
Check whether the typography, buttons, icons, spacing, and page states are consistent.
```

```text
Generate a UI self-check prompt that another coding agent can use to fix this screen.
```

## What It Checks

The skill guides the agent through a broad UI audit, including:

- Typography hierarchy
- Button styles and states
- Icon color and sizing
- Backgrounds, borders, radius, and shadows
- Spacing, gaps, alignment, and density
- Primary color usage
- Inputs, forms, clickable feedback, and accessibility basics
- Empty, loading, error, permission, and success states
- Dropdowns, modals, cards, navigation, tabs, badges, and tables
- Responsive behavior at mobile, tablet, and desktop widths
- Text overflow, invalid data, date/number formatting, and fallback copy
- Component reuse and Tailwind token discipline

## Expected Output

When used to audit a UI, the skill instructs the agent to respond with:

1. **UI quality conclusion**: a short verdict on whether the interface feels clean, moderately messy, or rough.
2. **Main issues**: the top problems, why they hurt quality, and how to fix them.
3. **Fix priority**: P0/P1/P2 grouping for urgent, important, and nice-to-have improvements.
4. **Copyable fix prompt**: a practical prompt that can be handed to a coding agent.

## Installation

Place `SKILL.md` in a skill directory named `ui-checker` under your Codex skills folder.

Example:

```text
~/.codex/skills/ui-checker/SKILL.md
```

If your agent runtime uses a different skills directory, copy the same `SKILL.md` file into the equivalent location.

## Files

- `SKILL.md`: the actual skill instructions used by the agent.
- `README.md`: English overview and usage guide.
- `README.zh-CN.md`: Chinese overview and usage guide.

## Design Goal

This skill is intentionally practical rather than artistic. It does not try to replace a designer or create a brand system from scratch. Its job is to help an agent make everyday front-end UI feel cleaner, more coherent, and easier to use.
