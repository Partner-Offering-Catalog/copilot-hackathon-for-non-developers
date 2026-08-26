# Explore GitHub Copilot with custom agents

This template is a guided sandbox for non-developers to turn an idea into a
planned and implemented application with GitHub Copilot.

> [!IMPORTANT]
> Do not create issues or projects in this template repository. First create
> your own repository from the template, then do every exercise in that copy.

## What is included

| Customization | Purpose |
| --- | --- |
| **Backlog Analyst** | Asks discovery questions, creates an epic/feature backlog, milestones, and a Kanban project |
| **Developer** | Selects ready issues, coordinates isolated workers, implements changes, and opens pull requests |
| **Web Canvas** skill | Builds a local interactive design canvas for refining a web application's visual direction |
| **Private Gist** skill | Saves notes and samples as a secret (unlisted) gist, never a public gist |
| **Repository Knowledge Base** skill | Creates and maintains handover-ready setup, operation, maintenance, and deployment documentation |

Agent profiles live in `.github/agents/`; reusable skills live in
`.github/skills/`. Copilot discovers both from the checked-out repository.

## Before the workshop

You need:

1. A [GitHub account](https://github.com/signup) with access to
   [GitHub Copilot](https://docs.github.com/en/copilot/get-started/plans).
2. Permission to create a repository and, for the planning exercise, a
   GitHub Project in your account or training organization.
3. [Git](https://github.com/git-guides/install-git) installed.
4. The
   [GitHub Copilot desktop app](https://github.com/features/ai/github-app)
   installed for your operating system.

## 1. Create your training repository

1. On this repository's GitHub page, select **Use this template** >
   **Create a new repository**.
2. Choose your personal account or training organization as the owner.
3. Give the repository a unique name and choose the visibility required by
   your workshop.
4. Select **Create repository**.
5. Confirm that the address bar shows your new owner and repository name—not
   `Partner-Offering-Catalog/copilot-hackathon-for-non-developers`.

Creating a repository from the template, rather than forking it, gives your
exercise its own issues, milestones, projects, branches, and pull requests.

## 2. Install and sign in to GitHub Copilot

1. Download the latest installer from the
   [GitHub Copilot app page](https://github.com/features/ai/github-app).
2. Install and open the app.
3. Select **Sign in with GitHub** and complete authorization in the browser.
4. If prompted, allow the app to access the owner of your training repository.

The interface changes frequently. See
[Getting started with the GitHub Copilot app](https://docs.github.com/copilot/how-tos/github-copilot-app/getting-started)
for current installation and connection instructions.

## 3. Clone through the Copilot app

1. In the Copilot app, choose the option to add or clone a repository.
2. Select your new training repository from the GitHub list. If it is not
   listed, paste its HTTPS URL from GitHub's **Code** menu.
3. Choose an empty local folder and start the clone.
4. Open the cloned repository as the active workspace.
5. Confirm the workspace contains `.github/agents` and `.github/skills`.

## 4. Confirm custom agents are available

1. Start a new session in the cloned repository.
2. Open the agent picker. Confirm **Backlog Analyst** and **Developer** appear.
3. Select **Backlog Analyst** and ask:

   > Help me plan a small application for **[your idea]**. Ask me questions
   > before changing GitHub.

4. Check that it asks clarifying questions and proposes a plan before it
   creates anything.

If the agents do not appear:

- confirm the app opened the repository root, not its parent directory;
- confirm both `.agent.md` files are present on the checked-out branch;
- pull the latest changes, then close and reopen the workspace;
- update the Copilot app to its latest release; and
- verify your GitHub account and organization policies permit custom agents.

See GitHub's
[custom agent configuration reference](https://docs.github.com/en/copilot/reference/custom-agents-configuration)
for current compatibility details.

## Workshop walkthrough

### Plan the work

Use **Backlog Analyst**:

> Turn my idea into an implementation backlog. Ask questions first. Show me
> the proposed epics, features, milestones, and project layout, and wait for my
> approval before creating them.

Review the proposal carefully. The agent should create a small number of
outcome-focused epics, break them into independently deliverable features,
link every feature back to its epic and milestone, and place the work on a
Kanban board.

### Explore a visual direction

In the same or a new session, ask:

> Use the web canvas skill to create an interactive design canvas for the
> application. Let me compare and adjust the colors, typography, spacing, and
> component style before we choose a direction.

Keep the canvas as a disposable design aid unless you explicitly approve
moving selected tokens or components into the application.

### Implement one feature

Select **Developer**:

> Pick one ready, high-priority feature from the backlog. Confirm its scope,
> implement it in isolation, validate it, and open a pull request. Coordinate
> separate workers only where their file ownership will not overlap.

Review the pull request and its checks. The Developer keeps `main` evergreen
by rebasing on it, avoiding merge commits, and merging only validated work
without bypassing repository protections.

### Capture useful notes

Ask:

> Use the private gist skill to prepare workshop notes from this session.
> Show me exactly what will be shared before creating the gist.

GitHub calls non-public gists **secret gists**. They are unlisted rather than
access-controlled: anyone with the URL can read one. Never include credentials,
personal data, customer data, or other confidential material.

### Prepare a handover

Ask:

> Use the repository knowledge base skill to document the current application
> for an operations handover. Verify every command and clearly mark unknowns.

Review the generated documentation with the intended maintainers. The
knowledge base should make setup, use, repository navigation, maintenance,
deployment, troubleshooting, ownership, and security responsibilities clear.

## Safe workshop habits

- Read an agent's proposal before authorizing GitHub or file changes.
- Never paste passwords, tokens, production data, or other secrets into chat,
  source files, canvases, issues, or gists.
- Keep issues finite and acceptance criteria observable.
- Require tests or an appropriate manual check before merging.
- Keep `main` deployable and use short-lived branches.
- Stop an agent if it targets the upstream template instead of your copy.
