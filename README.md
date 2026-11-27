# Judah’s Gym

A lightweight, mobile-first workout tracker for **A / B / C** gym days.

- **A:** Chest, shoulders, triceps (optionally swap front raises for shoulder press)
- **B:** Back, legs, biceps, core
- **C:** Full body

Includes exercise diagrams, guided one-set-at-a-time workouts, rest countdown and optional audio cues, independent local profiles, exercise weight progression and JSON backup/import.

## Hosting: GitHub Pages (free)

The entire app is the single `index.html` file. No build tools, databases, API keys or paid services are needed.

1. Create a **public** GitHub repository named `Judahs-Gym` under your account, initialized with a `README.md` to create the `main` branch.
2. Add `index.html`, `.nojekyll` and this README to the repository root.
3. Open **Settings → Pages** and under **Build and deployment**, select **Deploy from a branch**, **main**, **/(root)**, then save.
4. The app will be at **https://jorlinsk.github.io/Judahs-Gym/** after Pages finishes publishing.

Subsequent changes to `main/index.html` publish automatically. No ZIP or Netlify account is needed.

## Migrating browser data from Netlify

GitHub Pages has a different website origin, so browsers **do not carry local storage over automatically**.

1. In the old website on your iPhone, open **Progress & history → Export backup**. Store the JSON backup in Files or iCloud Drive.
2. Open the new GitHub Pages site on **the same iPhone**. Tap **Import my backup** in the migration banner. (Or use **Progress & history → Import backup**.)
3. Select the saved JSON and confirm replacement. Verify previous workouts in Progress & history before removing the old Home Screen shortcut.

The existing export/import covers the **currently selected local profile**. If multiple profiles have histories to preserve, export each profile separately and import each into its own new profile. A new profile must be created for every additional person before importing their backup.

## Privacy and sharing

The GitHub source and website are public, but user-entered weights, session history, profile names, and preferences are **not pushed to GitHub**. They live in the browser’s `localStorage` on each device. A friend can use **Share routine** to receive the same exercises with independent local history.

**Back up regularly.** Clearing site data, using a different browser/device, or changing the website address can lose local history without a JSON backup.

## Development

Edit `index.html`, test locally, and commit to `main`. GitHub Pages automatically republishes. Review changes in Git history, and use a branch / pull request for larger revisions. No extra dependencies.

## Notes

- Audio and spoken cues may not fire reliably when the iPhone screen is locked (iOS browser limitation).
- Exact machine form for certain exercises was based on the user's written notes and should be verified at the gym.
- The code has no remote analytics or cloud user database.
