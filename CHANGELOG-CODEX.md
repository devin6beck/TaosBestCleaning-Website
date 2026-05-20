## 2026-05-20 - Quiet estate branch migration setup

Purpose:
- Safely move the newer Taos Best Cleaning quiet-estate website work from the old OneDrive project folder to GitHub, then create a fresh local project folder under `C:\Users\edwar\Files\AI\Business Projects\TBC Website`.

Safety notes:
- No files or folders were deleted.
- No cleanup, reset, force push, or discard commands were run.
- `main` was inspected only and was not changed, merged into, or pushed.
- The old folder was inspected because the user explicitly approved outside-project inspection for comparison and recovery.

What was found before committing:
- GitHub remote: `https://github.com/devin6beck/TaosBestCleaning-Website.git`
- GitHub branches found:
  - `main` at `4a45d2e9fe435055033f088264dd1a1dba147a3d`
  - `gh-pages` at `4a45d2e9fe435055033f088264dd1a1dba147a3d`
  - `codex/luxury-redesign-implementation` at `1c0cfcadd289b93080b776b9a17001d31e442a04`
- Old local folder branch: `codex/quiet-estate-care-draft`
- Old local folder base commit: `1c0cfcadd289b93080b776b9a17001d31e442a04`
- The local quiet-estate branch did not have an upstream branch on GitHub yet.

Local-only work included:
- Modified tracked files:
  - `about.html`
  - `availability.html`
  - `contact.html`
  - `employment.html`
  - `index.html`
  - `services.html`
  - `styles.css`
- Untracked local files:
  - `Images/Logo Idea 1.png`
  - `Images/tbc-quiet-estate-hero.png`
  - `Images/tbc-quiet-estate-logo.svg`

Commands run for inspection and setup:
- `git ls-remote --heads https://github.com/devin6beck/TaosBestCleaning-Website.git`
- `git status --short --branch --untracked-files=all`
- `git branch --show-current`
- `git branch --list`
- `git remote -v`
- `git rev-parse HEAD`
- `git diff --stat`
- `git diff --name-status`
- `git ls-files --others --exclude-standard`
- `git rev-parse --abbrev-ref --symbolic-full-name '@{u}'`
- `git log --oneline --decorate --all -8`
- `gh --version`
- `gh auth status`
- `Test-Path -LiteralPath 'C:\Users\edwar\Files\AI\Business Projects\TBC Website'`
- `Get-Date -Format 'yyyy-MM-dd HH:mm:ss zzz'`

Items to review:
- `gh` was not installed or not available in this shell. This is not required for this branch push because Git can push directly to the configured GitHub remote.

Results:
- The quiet-estate work was committed in the old OneDrive folder as `bb00de52e3e2e014a9e51b2c532d251c7e41a9fb`.
- The branch `codex/quiet-estate-care-draft` was pushed to GitHub.
- GitHub verification showed:
  - `codex/quiet-estate-care-draft` at `bb00de52e3e2e014a9e51b2c532d251c7e41a9fb`
  - `codex/luxury-redesign-implementation` still at `1c0cfcadd289b93080b776b9a17001d31e442a04`
  - `main` still at `4a45d2e9fe435055033f088264dd1a1dba147a3d`
  - `gh-pages` still at `4a45d2e9fe435055033f088264dd1a1dba147a3d`
- The new local project folder was created by cloning from GitHub into `C:\Users\edwar\Files\AI\Business Projects\TBC Website`.
- The new local project is using branch `codex/quiet-estate-care-draft`.
- Expected files were verified in the new local project:
  - `CHANGELOG-CODEX.md`
  - `Images/Logo Idea 1.png`
  - `Images/tbc-quiet-estate-hero.png`
  - `Images/tbc-quiet-estate-logo.svg`
  - `about.html`
  - `availability.html`
  - `contact.html`
  - `employment.html`
  - `index.html`
  - `services.html`
  - `styles.css`

Additional commands run:
- `git add -- about.html availability.html contact.html employment.html index.html services.html styles.css CHANGELOG-CODEX.md "Images/Logo Idea 1.png" Images/tbc-quiet-estate-hero.png Images/tbc-quiet-estate-logo.svg`
- `git diff --cached --name-status`
- `git diff --cached --stat`
- `git -c user.name="Devin Beck" -c user.email="devin6beck@gmail.com" commit -m "Add quiet estate care draft"`
- `git push -u origin codex/quiet-estate-care-draft`
- `git clone --branch codex/quiet-estate-care-draft --single-branch https://github.com/devin6beck/TaosBestCleaning-Website.git "C:\Users\edwar\Files\AI\Business Projects\TBC Website"`
- `git status --short --branch --untracked-files=all`
- `git rev-parse HEAD`
- `git branch --show-current`
- `git remote -v`
- `git log --oneline --decorate -3`
- `git ls-files about.html availability.html contact.html employment.html index.html services.html styles.css CHANGELOG-CODEX.md "Images/Logo Idea 1.png" Images/tbc-quiet-estate-hero.png Images/tbc-quiet-estate-logo.svg`

Archived items:
- None.

Recovery notes:
- To keep using the newer quiet-estate site work, use `C:\Users\edwar\Files\AI\Business Projects\TBC Website` on branch `codex/quiet-estate-care-draft`.
- To view the old live-site style, use GitHub branch `main`.
- The old OneDrive folder was not deleted and can still be used as a recovery reference.

