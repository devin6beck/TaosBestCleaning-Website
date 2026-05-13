# Implementation Guide For Codex 5.4

## Guardrails

- Keep the project static: HTML, CSS, SVG, and existing image assets only.
- Do not introduce a build step, JavaScript framework, package manager, backend form, or deployment workflow.
- Preserve `CNAME`.
- Use semantic HTML and a single shared stylesheet.
- Avoid unrelated refactors beyond what is needed for the redesign.

## Branch And File Expectations

Implement the redesign on a feature branch, not directly on `main`.

Expected files to update or add during implementation:

- `index.html`
- `about.html`
- `services.html`
- `contact.html`
- `employment.html`
- `availability.html`
- `styles.css`
- `Images/tbc-luxury-logo.svg`

Do not overwrite existing image assets unless the user explicitly asks. The new logo should be added as a new SVG file.

## Shared Site Structure

Use a consistent header and footer across all pages.

Header requirements:

- New logo linked to `index.html`.
- Primary nav: Home, About, Services, Contact.
- Phone link: `575-613-2296`.
- Primary CTA: private walkthrough or consultation.

Footer requirements:

- Business name.
- Phone and email links.
- Employment link moved here.
- Optional Availability link may live here if the page is kept public.
- Current copyright year.

## Page Expectations

### `index.html`

Build the homepage as the main high-end sales page.

Include:

- Premium hero focused on luxury home care, vacation homes, and second residences.
- Primary CTA to schedule a private walkthrough.
- Trust strip: insured, bonded, locally operated, trained/background-checked team.
- Service highlights: recurring home cleaning, vacation-home care, monthly check-ins, detailed first clean.
- Process section: walkthrough, tailored plan, detailed first clean, recurring upkeep.
- Short founder/local credibility section linking to About.
- Contact CTA section.

### `services.html`

Present services in a polished, scannable format.

Include:

- Recurring residential cleaning.
- Vacation-home and second-home care.
- Monthly one-hour minimum home check-ins.
- Detailed first clean before recurring service where appropriate.
- Starting rate: `$65 per labor hour`.
- Clear labor-hour explanation: 2 cleaners for 1 hour equals 2 labor hours.
- Note that final pricing depends on location, property size, access, condition, and service frequency.

### `about.html`

Rewrite the owner story in a polished trust-centered voice.

Include:

- Hannah Beck as local owner/operator.
- Locally owned and operated in Taos.
- Small trained team.
- Background-checked team members.
- Insured and bonded.
- Recurring care and attention to detail.

Use the existing Hannah photo if it supports the design, but improve layout and responsive behavior.

### `contact.html`

Make this the primary conversion page.

Include:

- Invitation to schedule a private walkthrough or consultation.
- Email: `info@TaosBestCleaning.com`.
- Phone: `575-613-2296`.
- Guidance for what to include when contacting: property type, location, desired frequency, access notes, and any vacation-home or check-in needs.

Do not add a backend form unless the user separately provides one and asks for it.

### `employment.html`

Keep the page functional but secondary.

Include:

- Shared redesigned header and footer.
- Existing Google Form embed unless the user asks to replace it.
- No primary-nav link to Employment.

### `availability.html`

Keep or lightly modernize this page as secondary content.

Include:

- Shared redesigned header and footer.
- Calendar embed may remain if still useful.
- Availability should not become the main conversion path.

## Logo Expectations

Create `Images/tbc-luxury-logo.svg`.

Direction:

- Premium `TBC` monogram or wordmark.
- Taos mountain cue.
- Subtle cleaning symbolism such as a sparkle, sweep, or polished line.
- Works in header, footer, and small mobile sizes.
- Prefer restrained colors that work with the site palette.
- Avoid cartoon, playful, busy, or handmade styles.

## Style Direction

Use a restrained luxury palette:

- Warm off-white background.
- Charcoal text.
- Deep green accents.
- Muted gold or brass highlights.

Layout direction:

- Full-width section bands with constrained inner content.
- Editorial but practical spacing.
- No card-heavy marketing clutter.
- No nested cards.
- Mobile-first responsive navigation and layout.

Typography direction:

- Elegant serif headings.
- Clean sans-serif body text.
- Avoid oversized text in compact panels.
- Ensure text never overflows buttons, cards, or narrow mobile containers.

## Cleanup Requirements

- Fix encoding artifacts such as `copyright mojibake`, `curly apostrophe mojibake`, and broken ellipsis text.
- Make pricing consistent across the site: `$65 per labor hour`.
- Make phone links consistently use `tel:5756132296` or another valid tel format.
- Make email links consistently use `mailto:info@TaosBestCleaning.com`.
