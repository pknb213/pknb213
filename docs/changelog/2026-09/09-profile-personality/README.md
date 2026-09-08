# Restore the profile's personal identity

## Why

The previous refresh over-prioritized recruiter-facing evidence and removed the owner's photograph and friendly character. Reliability improvements should preserve personal identity, not replace it with a generic professional introduction.

## Scope and decisions

- Restore the exact previously used new1.png banner, unchanged. All original images survived the earlier change; only their README references had been removed.
- Use a repository-relative image reference and descriptive alternative text. Do not recreate, retouch, or substitute the owner's photograph.
- Restore a centered welcome and the existing Instagram destination as a text link. Keep unreliable external badge/counter services removed.
- Use warmer Korean section names and contact copy while preserving technical claims, measurement caveats, and the mobile-friendly repository list.
- Do not switch to another old banner or invent new decorative assets. This is a surgical restoration, not a new visual direction.

## Verification

- GitHub Markdown API renders the image, centered welcome, and links correctly. For pre-publication browser preview only, the relative image reference was resolved to the repository's raw image URL.
- Actual GitHub styling inspected in light/dark modes at 1440px and dark mode at 390px. Image decode succeeded with original width 900px; mobile document width equals viewport width (390px).
- git diff --check passes. The original image binaries are unchanged. Technical metrics and project summaries are unchanged.
- Publication follows as one restoration commit; live profile image resolution is checked after push.
