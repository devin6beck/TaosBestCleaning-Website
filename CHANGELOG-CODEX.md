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

## 2026-05-20 - GitHub CLI helper setup

Purpose:
- Install and verify the GitHub CLI helper tool, also called `gh`, so future Codex sessions can check GitHub login, branches, pull requests, and other GitHub details from this project folder.

Commands run:
- `Get-Command gh -ErrorAction SilentlyContinue | Select-Object Source,Version`
- `winget --version`
- `git status --short --branch --untracked-files=all`
- `git branch --show-current`
- `winget install --id GitHub.cli -e --source winget --accept-package-agreements --accept-source-agreements`
- `Test-Path -LiteralPath 'C:\Program Files\GitHub CLI\gh.exe'`
- `Test-Path -LiteralPath "$env:LOCALAPPDATA\Programs\GitHub CLI\gh.exe"`
- `Get-ChildItem -Path 'C:\Program Files','C:\Users\edwar\AppData\Local\Programs' -Recurse -Filter gh.exe -ErrorAction SilentlyContinue | Select-Object -First 5 FullName`
- `& 'C:\Program Files\GitHub CLI\gh.exe' --version`
- `& 'C:\Program Files\GitHub CLI\gh.exe' auth status`
- `& 'C:\Program Files\GitHub CLI\gh.exe' repo view devin6beck/TaosBestCleaning-Website --json nameWithOwner,defaultBranchRef`

Results:
- GitHub CLI was installed successfully.
- Installed version verified: `gh version 2.92.0 (2026-04-28)`.
- Installed location verified: `C:\Program Files\GitHub CLI\gh.exe`.
- The current shell did not immediately recognize plain `gh`, likely because Windows had not refreshed the shell path yet.
- Directly running `C:\Program Files\GitHub CLI\gh.exe` worked.
- `gh auth status` reported that no GitHub account is logged in yet.

Items to review:
- A future Codex or PowerShell session may recognize plain `gh` after reopening the terminal/app.
- GitHub login still needs to be completed by the user through GitHub's normal browser approval flow.

## 2026-05-20 - Local project safety verification

Purpose:
- Verify this local project folder, branch, GitHub remote, clean working tree, `main` branch safety, and GitHub CLI login before doing any website work.

Commands run:
- `Resolve-Path -LiteralPath 'C:\Users\edwar\Files\AI\Business Projects\TBC Website'`
- Cloud-folder path checks for OneDrive, Dropbox, iCloud, and Google Drive.
- `git branch --show-current`
- `git status --short --branch --untracked-files=all`
- `git remote get-url origin`
- `git branch --list`
- `git ls-remote --heads origin main`
- `git ls-remote --heads origin codex/quiet-estate-care-draft`
- `git rev-parse HEAD`
- `Get-Command gh -ErrorAction SilentlyContinue`
- `Test-Path -LiteralPath 'C:\Program Files\GitHub CLI\gh.exe'`
- `& 'C:\Program Files\GitHub CLI\gh.exe' --version`
- `& 'C:\Program Files\GitHub CLI\gh.exe' auth status`
- `Get-Date -Format 'yyyy-MM-dd HH:mm:ss zzz'`

Results:
- Project path verified: `C:\Users\edwar\Files\AI\Business Projects\TBC Website`.
- The project path is outside OneDrive, Dropbox, iCloud, and Google Drive.
- Current branch verified: `codex/quiet-estate-care-draft`.
- Working tree was clean before this changelog entry was added.
- GitHub remote verified: `https://github.com/devin6beck/TaosBestCleaning-Website.git`.
- Remote `main` was checked read-only and still pointed to `4a45d2e9fe435055033f088264dd1a1dba147a3d`.
- Local HEAD and remote `codex/quiet-estate-care-draft` both pointed to `46c3dc19bb7f153be86575295e3ef614f96da6e0`.
- GitHub CLI verified at `C:\Program Files\GitHub CLI\gh.exe`, version `2.92.0`.
- GitHub CLI login verified for account `devin6beck`.

Archived items:
- None.

Items to review:
- Because this changelog entry was added after the clean-tree check, the only expected working-tree change after verification is `CHANGELOG-CODEX.md`.

## 2026-05-20 - Homepage and header PDF change list

Purpose:
- Create a safe working branch and implement the homepage/global-header revisions from `TBC_Website_Homepage_Change_List_2026-05-20.pdf`.

Branch:
- Created and switched to `codex/homepage-header-updates` from `codex/quiet-estate-care-draft` before editing website files.

Files changed:
- `index.html`
- `about.html`
- `services.html`
- `contact.html`
- `employment.html`
- `availability.html`
- `styles.css`
- `CHANGELOG-CODEX.md`

Changes made:
- Updated the global header CTA from `Schedule a private walkthrough` to `Request a consultation`.
- Updated the global header logo to use `Images/ChatGPT Image May 9, 2026, 09_05_54 AM (3).png`, the logo chosen by the user.
- Hid the duplicate typed brand text beside the header logo so the selected logo is the visible brand mark.
- Changed the homepage hero card label to `Thoughtful Home Oversight`.
- Made the homepage hero headline slightly smaller with more line spacing.
- Lightened the homepage hero photo card overlay while keeping text readable.
- Changed the homepage local credibility copy from `for years` to `almost 10 years`.
- Also changed the matching About page copy to `almost 10 years`, as approved by the user.

Archived items:
- Moved the temporary SVG draft created during this session to `_ARCHIVE_DO_NOT_DELETE/2026-05-21-homepage-header-logo-draft/tbc-header-logo-option-b.svg`.

Commands and checks run:
- `git status --short --branch`
- `git branch --list codex/homepage-header-updates`
- `git switch -c codex/homepage-header-updates`
- Text searches for old/new CTA text, logo references, hero card wording, and founder timeline wording.
- Local browser preview at `http://127.0.0.1:8787/index.html`.
- Multi-size layout check in Microsoft Edge at 1366x768, 768x900, and 375x812.

Verification notes:
- The selected PNG logo loaded in the header.
- The header CTA showed `Request a consultation`.
- The homepage hero card showed `Thoughtful Home Oversight`.
- The average laptop check showed the full hero headline above the fold.
- Laptop, tablet, and phone checks reported no horizontal scrolling and no header item overlap.
- Follow-up tweak: reduced the homepage hero card overlay opacity in `styles.css` from `0.78` to `0.68` so more of the photo shows through.
- Follow-up user tweak: user changed the homepage hero card overlay opacity to `0.45`; Codex then changed the hero card label, list text, and bullet dots to black for readability.
- Follow-up reversal: restored the homepage hero card overlay opacity to `0.78` and removed the temporary black text/bullet override so the card uses the original text and bullet colors again.

How to reverse:
- The safe starting point remains `codex/quiet-estate-care-draft`.
- To start over, switch back to `codex/quiet-estate-care-draft` and leave this `codex/homepage-header-updates` branch alone for reference.
- To undo only this work on the current branch, restore the changed HTML/CSS files from Git and move any archived draft back only if you want that unused SVG visible again.

## 2026-05-21 - Homepage branch merge preparation

Purpose:
- Remove the `Taos second-home care` eyebrow text from the top of the home page, then save the homepage/header update branch and merge it into `codex/quiet-estate-care-draft` without touching `main`.

Files changed:
- `index.html`
- `CHANGELOG-CODEX.md`

Changes made:
- Removed the small hero eyebrow line that said `Taos second-home care`.

Archived items:
- None.

Commands and checks run:
- `git status --short --branch`
- `Select-String` checks for `Taos second-home care`
- `git diff --name-status`
- `git diff --stat`
- `git diff --check`
- `Get-ChildItem -Recurse -File -Force '_ARCHIVE_DO_NOT_DELETE'`
- Project path check confirming this folder is on local `C:` and not inside OneDrive, Dropbox, iCloud, or Google Drive.
- `git add CHANGELOG-CODEX.md about.html availability.html contact.html employment.html index.html services.html styles.css _ARCHIVE_DO_NOT_DELETE`
- `git commit -m "Apply homepage header updates"` failed because this local copy did not have a Git commit name/email configured.
- `git log -1 --format="%an <%ae>"` was used to read the existing repo author.
- `git -c user.name="Devin Beck" -c user.email="devin6beck@gmail.com" commit -m "Apply homepage header updates"` saved the branch without changing global Git settings.

How to reverse:
- Use Git to revert the commit that records this branch merge work, or restore `index.html` from the previous commit if you only want that small homepage text back.

