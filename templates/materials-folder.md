# Materials Folder Template

Use this folder shape when preparing a full run.

```text
materials/
├── target_jd.txt                 # required
├── resume.md                     # preferred; text export from PDF is OK
├── projects/
│   ├── project-a.md              # project summary, README, links, screenshots
│   └── project-b.md
├── code/
│   └── README.md                 # links or notes for local repos
├── notes/
│   ├── interview-notes.md
│   └── learning-notes.md
├── papers/
│   └── papers-read.md
├── awards/
│   └── competitions.md
├── transcripts/
│   └── courses.md
└── other/
```

Minimum viable input:

```text
materials/
├── target_jd.txt
└── resume.md
```

Better input:

```text
materials/
├── target_jd.txt
├── resume.md
├── projects/main-project.md
├── notes/bad-cases.md
├── notes/metrics.md
└── awards/contests.md
```

Recommended project note format:

```markdown
# Project Name

## One-line Summary

## My Role

## What I Actually Did

## What Others / Platform / Open Source Did

## Tech Stack

## Evidence

- code:
- logs:
- screenshots:
- metrics:
- README:
- experiments:
- bad cases:

## Current Claims In Resume

## Risks / Things I Cannot Prove

## What I Can Still Improve
```
