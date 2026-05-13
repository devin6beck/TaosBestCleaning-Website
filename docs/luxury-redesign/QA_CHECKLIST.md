# QA Checklist

Use this checklist after implementation of the luxury redesign.

## File And Scope Checks

- `CNAME` is unchanged.
- Site still runs as static GitHub Pages content with no build step.
- No package manager, framework, backend, or generated dependency files were added.
- New logo exists at `Images/tbc-luxury-logo.svg`.
- Existing image assets were not overwritten unless explicitly requested.

## Content Checks

- Main navigation contains Home, About, Services, Contact.
- Employment is not in the main navigation.
- Employment is linked from the footer.
- Pricing is consistent everywhere: `$65 per labor hour`.
- Labor-hour explanation is clear and correct.
- Copy targets luxury homes, vacation homes, second homes, and high-end residential clients.
- Required trust signals appear: insured, bonded, local, trained/background-checked team.
- Contact CTA is a private walkthrough or consultation.
- No casual "make your place shine" style language remains.
- No visible encoding artifacts remain.

## Link Checks

- Logo links to `index.html`.
- Home nav links to `index.html`.
- About nav links to `about.html`.
- Services nav links to `services.html`.
- Contact nav links to `contact.html`.
- Phone links use a valid `tel:` URL for `575-613-2296`.
- Email links use `mailto:info@TaosBestCleaning.com`.
- Footer Employment link points to `employment.html`.

## Responsive Checks

Check at minimum:

- Mobile around `375px` wide.
- Tablet around `768px` wide.
- Desktop around `1440px` wide.

Verify:

- Header and navigation do not overlap.
- Logo remains legible at mobile sizes.
- Buttons do not overflow.
- Text does not collide with neighboring content.
- Images are cropped and scaled intentionally.
- Embedded Google Form and calendar, if retained, fit mobile screens.

## Visual Checks

- Overall look is premium, restrained, and professional.
- Palette is not dominated by generic blue or a single hue family.
- Layout uses full-width sections with constrained content, not one boxed page card.
- Cards, if used, are only for repeated service/process items.
- No nested cards.
- Typography hierarchy is clear and not oversized in compact areas.

## Final Git Checks

- Run `git status --short --branch`.
- Review `git diff --stat`.
- Confirm changed files are expected for the implementation.
- If only the handoff docs were requested, confirm no `.html`, `.css`, image, or `CNAME` files changed.
