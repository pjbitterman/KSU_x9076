# Account Setup Guide

## Part 1

You do not need to create any accounts or install any software to start this course.

- **ArcGIS Pro** is already installed on the GIS lab machines in 442 McGilvrey Hall
- **Canvas**: you are enrolled in the Canvas section for this course

## Part 2

At approximately Week 8, the course will pivot from using ArcGIS Pro in the campus lab to the open-source Python stack running in your browser. That shift requires two free accounts: **GitHub** and **Google**. Both only take a few minutes. 

### 1. GitHub

**Why this course uses it:** GitHub is a standard location to store and share code. You will use it for version control (a history of every change you make) and for sharing your notebooks. It's also  a professional norm — having a GitHub account with real work on it is a small, standard thing employers and grad programs expect to see

**Sign up:**

1. Go to [github.com/signup](https://github.com/signup) and create a free account. GitHub's own walkthrough — [Creating an account on GitHub](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github) — covers the same steps if you want more detail.
2. **Pick your username carefully.** You'll likely keep this account, and this username, for years — future employers, collaborators, and grad programs may see it. Something professional and close to your real name ages a lot better than an old gamer tag.
3. **Turn on two-factor authentication (2FA).** GitHub's [guide to configuring two-factor authentication](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication) walks through the options — an authenticator app is the easiest to set up. 
4. **Claim the GitHub Student Developer Pack.** If you sign up (or verify) with your `kent.edu` email, you're eligible for the [GitHub Student Developer Pack](https://education.github.com/pack). It is free for verified students, and it unlocks a stack of free tools and services, including private-repository perks beyond GitHub's normal free tier. 

### 2. Google account → Colab

Most of you already have a Google account (Gmail, a `kent.edu` account running on Google, an old YouTube sign-up — any of these work). If you don't, [Google's account sign-up page](https://accounts.google.com/signup) walks you through creating one, free.

Once you have a Google account, there's nothing to install. Just go to [colab.research.google.com](https://colab.research.google.com) signed in with that account, and you're in Google Colab, a Jupyter notebook that runs entirely in your browser on Google's servers. (See Google's [Colaboratory FAQ](https://research.google.com/colaboratory/faq.html) if you want the full rundown of what Colab is.)

**Your first 60 seconds in Colab**, once you're signed in and want to try it:

1. Click **New notebook**.
2. Click into the first cell and type `1 + 1`.
3. Press **Shift+Enter** to run it. You should see `2` appear right below the cell.

One key distinction for now: Colab notebooks autosave to **your Google Drive**, not to your computer. So always know what file you're working on and where it is stored.

### Turn off built-in AI assistance

Per the course AI policy, AI tools don't write your code in this course except where an assignment expressly allows it. However, both Colab and VS Code ship with AI code generation **turned on**. Part of your week 8 setup is turning it off for coursework:

- **Colab:** gear icon (Settings, top right) → **AI Assistance** → uncheck the code-completion / generative-AI options.
- **VS Code:** if Copilot or another AI extension is installed or you're signed in with an account that enables it, disable it for your course workspace (Extensions sidebar → Copilot → **Disable (Workspace)**), or turn off inline suggestions in Settings.

We will eventually engage with these AI tools, but it's important to understand the basics from the start.

## Troubleshooting / common snags

- **Which email should I use for GitHub — personal or `kent.edu`?** Either works fine for the account itself. The one thing that matters: the **Student Developer Pack** specifically needs your `kent.edu` email linked to verify you're a student, so make sure that email is added to your GitHub account (Settings → Emails) even if it's not your primary one.
- **Colab says my session expired / disconnected.** This is normal, and not a problem — Colab runtimes are temporary and time out after a while of inactivity. Just rerun the notebook's setup cell(s) from the top and you should be back where you were.
- **Still stuck?** Ask in class or come by office hours
