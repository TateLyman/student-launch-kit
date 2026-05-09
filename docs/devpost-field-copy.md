# Devpost Field Copy

Use this to fill the HackAmerica project draft.

## Project Name

Student Launch Kit

## Elevator Pitch

A browser-only preflight that helps student builders fix launch issues before judges, users, or maintainers open the project.

## Inspiration

Hackathon projects are usually judged in a few minutes. If a repository has no clear README, missing run commands, no demo proof, or accidental secrets, the project can look unfinished even when the idea is strong. Student Launch Kit was built to give students a fast way to catch those issues before the deadline.

## What It Does

Student Launch Kit reads selected local files with the browser File API, detects launch signals across README, package metadata, workflows, config, and pasted notes, then returns a 0 to 100 launch-readiness score. It also shows grouped signals and a ranked fix queue so students know what to repair first.

## How We Built It

The app is a static HTML, CSS, and JavaScript tool. The browser File API reads project files locally, filters large or irrelevant files, and runs deterministic checks for README quality, package metadata, build/test scripts, CI workflows, lockfiles, secret exposure, environment examples, service boundaries, demo proof, reflection, contact path, and MCP/package version alignment.

## Challenges We Ran Into

The hardest part was making the output useful without uploading source code or relying on a backend. The checks needed to be specific enough to catch real launch gaps, but understandable enough that a beginner could act on the fix queue.

## Accomplishments

Student Launch Kit now has browser-only folder scanning, launch-readiness scoring, readable grouped signals, a ranked fix queue, screenshots, a public repo, passing CI, and static deployments through Tate Programs and GitHub Pages.

## What We Learned

Small release details can decide how credible a project feels. README context, workflow proof, demo links, and safe environment handling are not just polish. They are part of how software earns trust.

## What's Next

Next steps are downloadable Markdown reports, README and `.env.example` templates, richer language support for Python and mobile projects, and a judge-mode summary that turns the scan into a concise submission checklist.

## Built With

HTML, CSS, JavaScript, Browser File API, GitHub Actions, GitHub Pages

## Live Demo

https://tateprograms.com/student-launch-kit.html

## Repository

https://github.com/TateLyman/student-launch-kit

## Alternate Demo

https://tatelyman.github.io/student-launch-kit/

## Team Members

Tate Lyman
