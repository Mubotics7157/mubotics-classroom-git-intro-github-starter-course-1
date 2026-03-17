# FRC 7157 Bootcamp — Course Intro & Assignment A1: Git Boot-Up

> **This course will throw you into the deep end.** We focus on **competition-grade code** with the exact stack you’ll use in season, using a progressive scaffolded approach. You’ll learn by doing, with a mix of theory and practice. You will not learn everything, but you will learn how to learn.
> We **will not** teach general Java syntax or fundamentals here. If you need that, use a Java 17 primer (Codecademy / Udemy / “Java Programming” on YouTube / Oracle tutorials) **in parallel**.

---

## What you’ll learn (high-level)

- Configure and drive a **swerve drive** robot (kinematics, odometry, field-centric).
- Log, replay, and diagnose with **AdvantageKit** + **AdvantageScope**.
- Build reliable, easily configurable autonomous routines with trajectory following and vision
- Create full-robot simulations (physics, sensors, and cameras), and create a workflow to test code without a robot.

### Expectations & ethos

- **Hands-on first.** You’ll implement features you don’t fully “get” yet, then we’ll unpack the math and control theory behind them.
- **Read the docs.** Weekly pre-reads are short and targeted. Do them.
- **Version control is your friend.** You’ll use Git + GitHub for every assignment. Learn to love branches and PRs. During season, **never** commit directly to `main`. This is a lesson you don't learn fully until you suddenly have broken robot code, ctrl-z is broken, your computer crashed, and you have a match in 10 minutes.
- **Logs or it didn’t happen.** Every feature ships with instrumentation and logging. You’ll learn to use logs to diagnose issues. We will focus heavily on the aspects of observability that are most useful for competition.

---

## Step 0: Setup (before class)

1. **Install WPILib**

   - Go to [WPILib Releases](https://github.com/wpilibsuite/allwpilib/releases).
   - Download the latest WPILib installer for your OS.
   - Run the installer and choose:

     - **Install VS Code** (our IDE).
     - If unsure, choose the option labeled _“fastest.”_

2. **Install Git**

   - Follow the [WPILib Git Setup Docs](https://docs.wpilib.org/en/stable/docs/software/basic-programming/git-getting-started.html).
   - Install Git for your OS and confirm it works:

   ```bash
   git --version
   ```

3. **Authenticate GitHub**

   - Make sure you can log in via HTTPS or SSH. (You’ll need this in A1.)

---

## Key Git Terms (you’ll use these constantly)

- **Repository (repo)** = project folder + full history.
- **Branch** = safe workspace off of `main`.
- **Commit** = a saved change (like a checkpoint).
- **Pull Request (PR)** = request to merge your branch into `main`.
- **Fork** = your own copy of someone else’s repo.
- **Issue** = a tracked task or bug.

You’ll always:

- Work on **branches**
- Open **PRs** to merge changes
- Never push straight to `main`

---

Note: the assignment below was written using AI, so feel free to utilize it heavily during these learning stages as well, for common workflows such as this it usually gives very accurate advice

# Assignment A1: Git Boot-Up

**Goal:** Learn the full GitHub workflow — fork → clone → branch → commit → push → PR → merge.

**Estimated Time:** 60–90 minutes

### You’re Done When:

✅ You created a branch named `a1/<your-handle>-intro`

✅ You added a file called `intro.md` with your student card

✅ You made one tiny edit to this README

✅ You pushed changes and opened a PR with:

- Title: `A1: <Your Name> — Git boot-up`
- Linked issue: `#A1` (make one if missing)
- Requested a reviewer

---

## Step-by-Step Guide

1. **Clone your fork**
   After accepting the assignment, you’ll see a repository called `git-intro-<your-handle>` under the organization's GitHub along with the URL. Clone it:

   ```bash
   git clone https://github.com/Mubotics7157/git-intro-<your-handle>.git
   cd git-intro-<your-handle>
   ```

2. **Make a new branch**

   ```bash
   git checkout -b a1/<your-handle>-intro
   ```

   (This creates and switches to your feature branch.)

3. Create an issue on GitHub using the web interface. Name it something like `Missing Intro`. You'll link to this in your PR. When you're done, you'll see one open issue in the repo.

4. **Add your student card**
   Create a new file:

   ```
   intro.md
   ```

   Paste in the **Submission Template** below.

5. **Make a tiny README edit**

   - Change one word in `README.md` (fix a typo, reword a sentence, etc.).

6. **Stage, commit, and push**

   ```bash
   git add .
   git commit -m "A1: add student card + small README change"
   git push -u origin a1/<your-handle>-intro
   ```

7. **Open a Pull Request (PR)**

   - Go to GitHub → Your repo.
   - Click **Compare & Pull Request**.
   - Base: `upstream/main` ← Compare: `origin/a1/<your-handle>-intro`
   - Title: `A1: <Your Name> — Git boot-up`
   - Link issue `#1` (or whatever number it is).
   - Add a reviewer.

8. **Respond to feedback**

   - If your reviewer requests changes:

     - Edit files locally
     - `git add . && git commit -m "fixes"`
     - `git push` (same branch)

   - Your PR updates automatically.

---

## Submission Template (intro.md)

```markdown
# A1 — Student Card

**Name:** Your Name  
**Handle:** @your-handle  
**OS:** (e.g., Windows 11)  
**GitHub URL:** https://github.com/your-handle  
**CS Experience:** (the coolest thing you’ve built with code)
```

---

Don’t worry if Git feels confusing now. By the end, you’ll be doing this workflow on autopilot.

---
