# Understanding RapidCMI5

RapidCMI5 is an open-source authoring and delivery ecosystem for creating CMI5-compliant training courses.
It solves a real problem: modern training standards like CMI5 and xAPI are powerful but complex to implement from scratch.
RapidCMI5 handles all of that complexity, letting instructional designers focus on content.

***

## The Two Core Components

RapidCMI5 is built around two distinct pieces that work together: an **authoring tool** and a **content player**.
Understanding the difference between them is key to understanding how the whole system works.

***

## rapid-cmi5 — The Authoring Tool

rapid-cmi5 is the course creation environment. It is published as an npm package (`@rapid-cmi5/react-editor`) and
embedded in the desktop application you are using right now.

It gives you three editing modes:

* **Designer View** — a visual editor for writing markdown-based course content without touching code
* **File View** — direct file editing for authors who prefer working closer to the source
* **Git View** — built-in version control for collaboration, history, and change tracking

Everything you create in rapid-cmi5 is stored as plain markdown files in a Git repository.
This means your courses are portable, version-controlled, and never locked to a proprietary format.

***

## cc-cmi5-player — The Content Player

cc-cmi5-player is a standalone React web application that learners use to take your courses.

When a learner launches a course through their LMS, cc-cmi5-player is what actually runs.
It handles everything the learner sees and everything the LMS needs to know:

* Rendering your markdown slides as interactive presentations
* Managing the CMI5 session with the LMS
* Sending xAPI statements to track progress, scores, and completion
* Playing back animations, videos, embedded activities, and scenarios

The player is a self-contained web app. It gets built once and packaged alongside every course you publish.

***

## How They Fit Together

The workflow moves in one direction — from authoring to delivery:

```
You write content in rapid-cmi5
        ↓
Course is saved as markdown in a Git repository
        ↓
You publish the course as a CMI5 package
        ↓
The package includes cc-cmi5-player as the runtime
        ↓
Learners launch the course through their LMS
        ↓
cc-cmi5-player renders the content and reports back to the LMS
```

rapid-cmi5 creates the content. cc-cmi5-player delivers it.
They share the same markdown format and the same slide components,
so what you see in the designer is what the learner sees in the player.

***

## Why CMI5?

CMI5 is the modern successor to SCORM. It is built on xAPI, which means:

* Courses can run anywhere — not just inside an LMS iframe
* Tracking is richer — you can record any learning event, not just pass/fail
* Content is portable — any CMI5-compliant LMS can run your courses
* Sessions are secure — each launch is authenticated

RapidCMI5 handles all CMI5 compliance automatically.
You do not need to write a single line of xAPI code to produce a fully standards-compliant course.

***

## Summary

<table class="rc5-table"><thead><tr><th style="background-color: transparent"></th><th style="background-color: transparent">rapid-cmi5</th><th style="background-color: transparent">cc-cmi5-player</th></tr></thead><tbody><tr><td style="background-color: transparent"><strong>Used by</strong></td><td style="background-color: transparent">Course authors</td><td style="background-color: transparent">Learners</td></tr><tr><td style="background-color: transparent"><strong>What it is</strong></td><td style="background-color: transparent">Authoring UI for Instructors</td><td style="background-color: transparent">Web application for students</td></tr><tr><td style="background-color: transparent"><strong>Runs in</strong></td><td style="background-color: transparent">Electron desktop app or Browser</td><td style="background-color: transparent">Browser</td></tr><tr><td style="background-color: transparent"><strong>Handles</strong></td><td style="background-color: transparent">Content creation, Git, structure</td><td style="background-color: transparent">Rendering, xAPI, CMI5 sessions</td></tr><tr><td style="background-color: transparent"><strong>Output</strong></td><td style="background-color: transparent">Markdown files in Git</td><td style="background-color: transparent">xAPI statements to LMS</td></tr></tbody></table>

Together they form a complete pipeline — from a blank page in the editor to a fully tracked, standards-compliant course delivered to a learner anywhere in the world.