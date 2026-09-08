# English profile translation

## Scope and decisions

Translate the profile README into natural English while retaining the original photograph, centered welcome, friendly tone, technical scope, dated metrics, and all link destinations. The linked portfolio and historical changelog documents are outside this translation's scope.

Use readable English rather than literal Korean phrasing. Keep learning projects distinct from professional work, and preserve the limitations on test counts and development measurements.

## Verification

- Automated assertions pass: no Korean text remains in README, all link destinations and the original image reference are unchanged, and all six project metrics plus the July 2026 qualifier are preserved.
- git diff --check passes.
- GitHub Markdown rendering succeeds. Browser preview confirms the English greeting, original image decoding at 900px natural width, no Korean article text, and no document overflow at a 390px mobile viewport. Screenshot visually inspected.
- Publication follows as one translation commit; confirm the live English heading after push.
