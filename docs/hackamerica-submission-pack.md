# HackAmerica Submission Pack

## Project Title

Student Launch Kit

## Tagline

A browser-only preflight that helps student builders fix launch issues before judges, users, or maintainers open the project.

## Short Description

Student Launch Kit reads a local project folder in the browser and scores whether it is ready to submit, share, or launch. It checks README quality, package metadata, build scripts, CI, lockfiles, secrets hygiene, demo proof, reflection notes, and MCP/package release alignment.

## Long Description

Student projects often work for the builder but break down during handoff. A judge, teacher, open-source maintainer, or first user needs to understand what the project does, how to run it, where the demo is, what is safe to reuse, and whether obvious launch mistakes are present. Those details are easy to miss during a deadline.

Student Launch Kit turns that problem into a simple local preflight. A student can choose a project folder or paste key files, and the app reads them in the browser without uploading code. It then returns a launch-readiness score, grouped signals, and a ranked fix queue. The checks focus on practical submission quality: README depth, package metadata, build/test scripts, CI workflows, lockfiles, secret exposure, environment examples, service boundaries, demo proof, reflection, contact path, and MCP/package version alignment.

The goal is not to replace deeper review. The goal is to help students submit cleaner work, learn release discipline, and avoid avoidable mistakes before sharing software publicly.

## Inspiration

Hackathon projects are usually judged in a few minutes. If a repository has no clear README, missing run commands, no demo proof, or accidental secrets, the project can look unfinished even when the idea is strong. This project was built to give student teams a fast way to catch those issues before the deadline.

## What It Does

- Reads selected local files with the browser File API.
- Detects launch signals across README, package metadata, workflows, config, and pasted notes.
- Scores the project from 0 to 100.
- Shows grouped signals for identity, build trail, safety, service boundaries, and launch proof.
- Produces a ranked fix queue with practical next steps.
- Copies or emails the result for follow-up.

## How It Was Built

The app is a static HTML/CSS/JavaScript tool. The browser File API reads text files locally, filters out large or irrelevant files, and analyzes project evidence with deterministic checks. The UI uses the Tate Programs terminal-style design system so it feels like a focused developer tool instead of a form-heavy audit page.

## Challenges

The hardest part was making the output useful without uploading source code or relying on a backend. The checks needed to be specific enough to catch real launch gaps, but understandable enough that a beginner could act on the fix queue.

## Accomplishments

- Browser-only folder scanning with no server upload.
- Launch-readiness scoring across common student project risks.
- Readable fix queue instead of vague pass/fail output.
- Static deployment that works on GitHub Pages and the Tate Programs site.

## What Was Learned

Small release details can decide how credible a project feels. README context, workflow proof, demo links, and safe environment handling are not just polish; they are part of how software earns trust.

## What's Next

- Add downloadable Markdown reports.
- Add optional templates for README, `.env.example`, and demo scripts.
- Add richer checks for Python, Java, and mobile projects.
- Add a "judge mode" summary that turns the scan into a concise submission checklist.

## Built With

- HTML
- CSS
- JavaScript
- Browser File API
- GitHub Actions
- GitHub Pages

## Links

- Live app: https://tateprograms.com/student-launch-kit.html
- Repository: https://github.com/TateLyman/student-launch-kit
- Tate Programs: https://tateprograms.com
- Desktop screenshot: docs/media/desktop.png
- Mobile screenshot: docs/media/mobile.png

## Demo Video Script

1. Open with the problem: student projects can fail at handoff even when the idea is good.
2. Show the app and explain that it runs locally in the browser.
3. Upload a project folder.
4. Point out the score, grouped signals, and ranked fix queue.
5. Show examples: missing README depth, missing CI, `.env.example`, npm publish-token risk, demo proof.
6. Close with the impact: cleaner submissions, safer launches, and better project communication for students.

## X Post Draft

Shipped Student Launch Kit: a browser-only preflight for student projects.

It reads a local repo folder, checks README/build/CI/secrets/demo proof, then returns a launch score and fix queue before judges or users open it.

Live: https://tateprograms.com/student-launch-kit.html
Repo: https://github.com/TateLyman/student-launch-kit
