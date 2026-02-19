# Module 3 Handout — Portfolio-First Mindset

## GitHub, Storytelling, and Your First Data Science Logo

**Author**: Dr. Zheng Qu

## Overview

In this module, you will:

- Check and install Git (if needed) on macOS or Windows.  
- Set up GitHub with SSH.  
- Turn your Nightingale project into a clear **data story**.  
- Design a simple **personal logo** with AI.  
- Publish and pin your project on your GitHub profile.  


## What You Need Before Class

- A working **Python** installation.  
- Access to **Antigravity** (Gemini 3 Pro enabled).  
- Your completed Nightingale project files:
  - The digitization app code.  
  - Your computed data (JSON / CSV).  
  - Your final rose diagram PNG.  


## Target Project Structure

Inside your `nightingale-rose` folder, aim for:

```text
nightingale-rose/
├── README.md  
├── data/
│   ├── coordinates.json  
│   └── nightingale_computed.csv
├── src/
│   ├── digitize_app.py  
│   └── plot_rose.py
├── output/
│   └── nightingale_rose.png
└── assets/
    ├── nightingale_original.png  
    └── logo.png (or logo.svg)
```

## The Antigravity Pattern

**Key concept**: You will **never memorize commands**. Instead:

- Copy prompts from this handout into Antigravity.  
- Let Gemini 3 Pro:
  - Explain what is happening.
  - Give you the exact commands.  
- Type the commands into your own terminal or PowerShell window.

This pattern works for **any** new tool or workflow, not just Git.


## Step 0 — Check and Install Git (macOS and Windows)

Before doing anything with SSH, make sure Git is installed.

### 0.1 — Universal Check (Any OS)

Open:

- **Terminal** (macOS)  
- **PowerShell** or **Command Prompt** (Windows)  

Then paste this into Antigravity:

I am a beginner on [macOS or Windows].

Help me check whether Git is already installed.

Give me:
1) A one-sentence explanation of what we are checking.
2) The exact command I should type to check the Git version.

Type the suggested command (likely `git --version`) yourself and press Enter.

**If you see a version string** like `git version 2.x.x`, you are done with Step 0. Skip to Part 1.

**If you get an error** or "command not found", continue below for your operating system.


### 0.2 — macOS: Install Git (Command Line Tools)

Paste this into Antigravity:

I am on macOS and the command to check `git --version` did not work.

I want the simplest, safest way to install Git using Apple's Command Line Tools.

Give me:
1) A short explanation of what we are about to do.
2) The exact command I should type to start the installation.
3) Any follow-up steps I should expect (such as clicking "Install" in a popup).

Follow Antigravity's instructions. They should involve installing **Xcode Command Line Tools** (for example with `xcode-select --install`), which include Git.

When finished, run the Git version check again to confirm.


### 0.3 — Windows: Install Git

Paste this into Antigravity:

I am on Windows and the command to check `git --version` did not work.

Give me two beginner-friendly options to install Git:

1) Using the official Git for Windows installer (GUI):
   - Tell me what website to open.
   - Tell me what to click.
   - Tell me what choices to make in the installer (defaults unless needed).

2) Using the winget command in PowerShell (if winget is available):
   - Tell me the exact `winget install` command.
   - Explain briefly what it does.

For each option, keep instructions short and numbered so I can follow them.

**If you choose the GUI option**, Antigravity should direct you to **git-scm.com** to download the installer and follow the standard wizard.

- **Important**: During installation, choose **"Git from the command line and also from 3rd-party software"** so git works in all terminals, including Antigravity.

**If you choose the winget option**, expect a command like:

winget install --id Git.Git -e --source winget

Run it in **PowerShell as Administrator**. This will download and install Git with default settings.

When finished, open a **new** PowerShell window and run the Git version check again.


### 0.4 — Move On When Git Works

You are ready for the SSH section when:

- `git --version` prints a Git version without errors.  

Only then proceed to **Part 1 — GitHub SSH Setup (with Antigravity)** below.


## Part 1 — GitHub SSH Setup (with Antigravity)

Open your terminal and Antigravity side by side.

You will paste each prompt into Antigravity, read the explanation, and then **type the command** into your terminal.

### Prompt A — Generate SSH Key

I am a beginner setting up GitHub. 

What is GitHub in one simple sentence, and what is the first command I should run to generate a new SSH key? 

Give me:
1) One short explanation sentence
2) The exact command on its own line

Type the command in your terminal and press Enter.

### Prompt B — Start SSH Agent

I just generated my SSH key. 

What is the next command I should run to start the SSH agent, and what does it do? 

Again:
1) One short explanation
2) The exact command on its own line

Type the command in your terminal.

### Prompt C — Add Key to Agent

Now I need to add my new SSH key to the SSH agent. 

Explain what the command does, then give the command.

Run the command in your terminal.

### Prompt D — Show Public Key

How do I see my public SSH key so I can copy it into GitHub?

Explain briefly, then give the command.

Copy the key from your terminal and paste it into:

- GitHub → Settings → SSH and GPG keys → New SSH key  

### Prompt E — Test Connection

How do I test that my SSH connection to GitHub is working?

Explain in one sentence, then give the command.

You should see a message greeting you by your GitHub username.


## Part 2 — Local Repo Setup

Create and connect your project folder.

### Prompt F — Create and Connect Repo

I want to create a new project folder called 'nightingale-rose' on my computer, initialize it as a git repository, and connect it to a new GitHub repo called 'nightingale-rose' that I already created in the browser. 

Give me one command at a time, in order. For each command:
1) Briefly explain what it does
2) Then show the command

I will say 'next' when I'm ready for the next command.

Follow Antigravity's commands step by step.

When done, copy your existing Nightingale files into this folder, using the target structure shown at the beginning of this handout.


## Part 3 — README Template

Open `README.md` and use this template as a guide.

```markdown
# Florence Nightingale's Rose Diagram — A Replication

![Logo](assets/logo.png)

## The Story

[3-sentence paragraph generated and then edited by you.]

## How the Data Was Collected

[Describe your digitization app and how you got coordinates → radii → areas.]

## The Math and Visualization

- Briefly explain that you used distances from the center to compute radii.
- Mention that areas are proportional to r².
- Note that each wedge encodes deaths from different causes.

## The Visualization

![Rose Diagram](output/nightingale_rose.png)

## Key Insights

- [Bullet about the left diagram (before reforms).]
- [Bullet about the right diagram (after reforms).]
- [Bullet about what this shows about data and policy change.]
- [Your own extra observation.]

## Technical Details

- Language: Python  
- Libraries: [list your main libraries]  
- Files:
  - `src/digitize_app.py`  
  - `src/plot_rose.py`  
  - `data/coordinates.json`  
  - `data/nightingale_computed.csv`  

## How to Run

1. Clone this repository.  
2. Create and activate a virtual environment (optional).  
3. Install requirements (if you have a `requirements.txt`).  
4. Run the plotting script:  
   `python src/plot_rose.py`  

## What I Learned

[2–3 sentences written entirely by you: technical lessons and reflections.]

## References

- [Short list of sources or links you used.]

```

### Prompt G — Historical Context

Write a 3-sentence opening paragraph for a data science portfolio README about Florence Nightingale's rose diagram. 

Mention:
- The Crimean War
- The sanitary reform crisis
- How her visualization influenced British military policy

Write it in a clear, professional tone for a technical audience.

Paste the result into your **"The Story"** section and edit at least one sentence to match your voice.

### Prompt H — Data Collection Description

Write a 3-sentence paragraph for my README explaining how I collected the data for this project:

- I built a Python app that let me click 4 key points on each month in Nightingale's original diagram image.
- The app saved pixel coordinates as JSON.
- I then used Python to convert those coordinates into radii and proportional areas for different causes of death.

Write this in first person and make it understandable for someone new to data visualization.

Paste into **"How the Data Was Collected"** and adjust details if your implementation differed.

### Prompt I — Key Insights

Write 3 bullet points for my README that explain what Florence Nightingale's rose diagram reveals:

1) One bullet about what the left diagram (before reforms) shows.
2) One bullet about what the right diagram (after reforms) shows.
3) One bullet about what this visualization demonstrates about data-driven policy change.

Keep each bullet to one sentence.

Paste into **"Key Insights"** and add **one extra bullet of your own** based on your plot.

### Write "What I Learned" (No AI)

Add a **"What I Learned"** section.

Write 2–3 sentences **without using AI**:

- What did you learn technically?
- What did you learn about data and society?

This is your authentic voice.


## Part 4 — Logo Design with Gemini 3 Pro

### Step 1 — Choose a Simple Concept

Pick **one** of these:

- **Monogram**  
  - Your initials inside a circle or square.  
  - Maybe a tiny chart bar behind or under the letters.  

- **Data Icon**  
  - A minimalist bar chart, line chart, or node-link diagram.  
  - Your initials integrated into the design.  

- **Nightingale Theme**  
  - A radial "flower" shape made of bars or wedges.  
  - Your initials near or inside the shape.  

Make a 30-second sketch on paper.

### Step 2 — Turn Your Idea into a Prompt

In Antigravity, use this pattern and fill in the brackets:

You are Gemini 3 Pro, acting as a logo designer.

Create a simple, flat, vector-style logo for a data science student.

Concept:
- [Describe your chosen option: monogram / data icon / Nightingale theme]
- Include my initials: [YOUR INITIALS]
- Style: minimal, high contrast, works well at small sizes
- Background: transparent
- Output format: SVG or high-resolution PNG

First, describe the logo you will generate in 2–3 sentences. Then generate it.

Save the generated file as:

- `assets/logo.png` or `assets/logo.svg`  

### Step 3 — Add Logo to README

At the very top of `README.md`, add:

```
![Logo](assets/logo.png)
```

Adjust the filename if needed.


## Part 5 — Commit and Push

### Prompt J — Stage, Commit, Push

I am ready to publish my project.

Give me the git commands, one at a time, to:
1) See which files are changed.
2) Stage all files.
3) Write a good commit message for adding my Nightingale project, README, and logo.
4) Push to the main branch on GitHub.

Explain each command briefly.

Type each command in your terminal.

Check your repo in the browser when done.


## Part 6 — Profile README and Pinning

### Prompt K — Profile README

Write a GitHub profile README for a college freshman studying data science.

Include:
- A short About Me (2–3 sentences)
- A Skills section (Python, matplotlib, data visualization, git)
- A Projects section linking to my 'nightingale-rose' repository
- A Currently Learning section

Use clean markdown and a professional but friendly tone.

Create a repo named exactly your GitHub username and add the generated (and edited) README.

### Pin Your Project

On your GitHub profile:

- Click **Customize your pins**.  
- Pin the `nightingale-rose` repository.  


## Light Homework

- Add a new section to your profile README:
  - "What I'm Curious About in Data Science"

- Visit 2 classmates' profiles and leave them encouraging, specific feedback on their Nightingale project.


## Troubleshooting: Common Issues

### "git: command not found" after installation

- **macOS**: Open a new Terminal window after installing Xcode Command Line Tools.
- **Windows**: Open a new PowerShell window after installing Git for Windows.

### SSH connection test fails

Use this Antigravity prompt:

I got this error when testing my SSH connection to GitHub: [paste error].

What went wrong and what should I do to fix it?

### Git push rejected

Use this Antigravity prompt:

I tried to push to GitHub and got this error: [paste error].

I was trying to push my first commit to the main branch.

What went wrong and what commands should I run?

### Image not showing in README

- Check that the file path is correct relative to README.md
- Make sure the image file is committed and pushed to GitHub
- GitHub renders images after a few seconds — refresh the page


## Remember the Pattern

**Any time you face a new command-line task:**

1. Open Antigravity  
2. Describe what you want to do in plain English  
3. Ask for explanation + exact commands  
4. Type the commands yourself  
5. If there's an error, paste it back into Antigravity and ask for help  

This pattern works for Git, Python, databases, deployment — **everything**.