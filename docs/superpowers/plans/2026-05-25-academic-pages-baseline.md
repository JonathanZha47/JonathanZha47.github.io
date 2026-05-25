# Academic Pages Baseline Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build and deploy a first-version Academic Pages-style personal website for Yiwei Zha at a GitHub Pages URL.

**Architecture:** Use a Jekyll/GitHub Pages academic-site structure with Markdown-driven pages for home, research, publications, projects, CV, and contact. Keep the first version visually close to Academic Pages so deployment and content correctness come first; later visual redesign can reuse the same content.

**Tech Stack:** Jekyll, GitHub Pages, Markdown, YAML front matter, SCSS/CSS, GitHub repository `JonathanZha47.github.io` or equivalent Pages repo.

---

## File Structure

- `README.md`: local setup, edit instructions, and deployment notes.
- `_config.yml`: site title, author metadata, navigation, URL, theme/plugin configuration.
- `index.md`: homepage with current PhD role and collaborator-facing research summary.
- `research.md`: current and past research themes, led by trustworthy AI for agentic systems.
- `publications.md`: publication list drafted from Google Scholar/CV and checked links.
- `projects.md`: project summaries with code/paper links.
- `cv.md`: CV summary page; link to updated PDF only if approved.
- `contact.md`: public contact links.
- `assets/css/custom.scss` or `assets/css/custom.css`: small baseline style tweaks only.
- `files/`: optional deployable files such as an approved updated CV PDF.
- `.github/workflows/pages.yml`: only if the chosen Pages setup requires GitHub Actions.

## Task 1: Initialize Academic Pages Baseline

**Files:**
- Create/modify: repository root files from Academic Pages template or a close Jekyll equivalent.
- Create: `README.md`
- Create: `_config.yml`
- Create: `index.md`

- [ ] **Step 1: Confirm repository target**

Run:

```bash
pwd
ls -la
git status --short
```

Expected:

```text
/Users/zhayiwei/Desktop/personal workflow/personal-page
```

The directory may not be a git repository yet. If `git status` says `fatal: not a git repository`, initialize git in Step 2.

- [ ] **Step 2: Initialize git if needed**

Run only if Step 1 shows no git repository:

```bash
git init
```

Expected:

```text
Initialized empty Git repository
```

- [ ] **Step 3: Bring in the Academic Pages baseline**

Preferred command if network access is available and the user approves:

```bash
git clone https://github.com/academicpages/academicpages.github.io.git /tmp/academicpages-template
```

Then copy the template files into the current repository while preserving the existing `docs/` directory:

```bash
rsync -av --exclude='.git' --exclude='docs' /tmp/academicpages-template/ ./
```

Expected:

```text
_config.yml
_pages/
_publications/
_data/
assets/
```

Fallback if cloning is unavailable: create a minimal Jekyll structure manually with `_config.yml`, `index.md`, `research.md`, `publications.md`, `projects.md`, `cv.md`, and `contact.md`.

- [ ] **Step 4: Set site metadata in `_config.yml`**

Use these values as the source of truth:

```yaml
title: "Yiwei Zha"
name: "Yiwei Zha"
description: "First-year PhD student at Vrije Universiteit Amsterdam working on trustworthy AI and safety for agentic systems."
url: "https://JonathanZha47.github.io"
baseurl: ""
repository: "JonathanZha47/JonathanZha47.github.io"
author:
  avatar: ""
  name: "Yiwei Zha"
  bio: "First-year PhD student at Vrije Universiteit Amsterdam. Trustworthy AI, agentic-system safety, model-compression safety, and AI-generated content detection."
  location: "Amsterdam, Netherlands"
  employer: "Vrije Universiteit Amsterdam"
  googlescholar: "https://scholar.google.com/citations?user=IvimIBUAAAAJ&hl=en"
  github: "JonathanZha47"
  linkedin: "yiwei-zha"
  email: "y.zha@vu.nl"
```

- [ ] **Step 5: Commit baseline scaffold**

Run:

```bash
git add README.md _config.yml index.md docs/superpowers/specs/2026-05-25-personal-page-design.md docs/superpowers/plans/2026-05-25-academic-pages-baseline.md
git commit -m "chore: initialize academic pages baseline"
```

Expected:

```text
[main ...] chore: initialize academic pages baseline
```

## Task 2: Write Collaborator-Facing Homepage

**Files:**
- Modify: `index.md`
- Modify: `_config.yml`

- [ ] **Step 1: Replace homepage copy**

Use this content for the homepage body:

```markdown
---
layout: single
title: "Yiwei Zha"
permalink: /
author_profile: true
---

I am a first-year PhD student at Vrije Universiteit Amsterdam working on trustworthy AI, with a particular interest in building safety into agentic systems.

My current work focuses on two directions:

- **Memory-poison defense for agentic systems:** studying how poisoned information enters agent context windows or memory mechanisms, and how agents can defend against it.
- **Model-compression safety:** investigating whether quantization, pruning, and related compression methods introduce, amplify, or hide safety issues.

I have also worked on AI-generated text detection, phishing email detection, retrieval-augmented generation systems, mobile-agent benchmarks, and earlier physics-guided learning for industrial systems.

I am interested in collaborations around trustworthy AI, agentic-system safety, LLM evaluation, AI-generated content detection, and safety-aware deployment of efficient models.
```

- [ ] **Step 2: Run local Jekyll build**

Run:

```bash
bundle exec jekyll build
```

Expected:

```text
done in
```

If dependencies are missing, install with the repository's documented command, usually:

```bash
bundle install
```

- [ ] **Step 3: Commit homepage copy**

Run:

```bash
git add index.md _config.yml
git commit -m "feat: add collaborator-facing homepage"
```

Expected:

```text
[main ...] feat: add collaborator-facing homepage
```

## Task 3: Add Research Page

**Files:**
- Create: `research.md` or modify Academic Pages equivalent such as `_pages/research.md`
- Modify: `_data/navigation.yml` if the template uses data-driven navigation.

- [ ] **Step 1: Create research page**

Use:

```markdown
---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

## Safety for Agentic Systems

I am interested in how safety can be built into agentic systems rather than only evaluated after deployment. My current work studies memory poisoning in agent context windows and memory mechanisms: how poisoned or adversarial information enters an agent's working context, how it changes downstream behavior, and how defensive mechanisms can reduce that risk.

## Model Compression and Safety

Efficient models are increasingly deployed through quantization, pruning, and other compression methods. I am interested in whether these methods preserve safety behavior, introduce new failure modes, or make safety issues harder to observe.

## AI-Generated Content and Abuse Detection

My trustworthy AI work also includes AI-generated text detection, paraphrase-attack robustness, and phishing email detection. This direction connects detection systems with adversarial behavior, evaluation design, and practical abuse cases.

## Retrieval, Evaluation, and Agent Benchmarks

I have worked on retrieval-augmented generation systems and mobile-agent benchmarks. These projects inform my current interest in evaluating agent behavior under realistic and adversarial conditions.

## Earlier AI for Science and Industrial ML

Before my current PhD work, I worked on physics-guided learning for industrial systems, including battery state-of-health estimation and process prediction. I present this as earlier experience in scientific machine learning and robust modeling, not as the main focus of my current research agenda.
```

- [ ] **Step 2: Add navigation item**

If using `_data/navigation.yml`, include:

```yaml
main:
  - title: "Research"
    url: /research/
  - title: "Publications"
    url: /publications/
  - title: "Projects"
    url: /projects/
  - title: "CV"
    url: /cv/
  - title: "Contact"
    url: /contact/
```

- [ ] **Step 3: Build and commit**

Run:

```bash
bundle exec jekyll build
git add research.md _pages/research.md _data/navigation.yml
git commit -m "feat: add research overview"
```

Expected:

```text
[main ...] feat: add research overview
```

## Task 4: Add Publications And Projects

**Files:**
- Create/modify: `publications.md`
- Create/modify: `projects.md`

- [ ] **Step 1: Add publications page**

Use this initial page and refine any venue/status details against Google Scholar:

```markdown
---
layout: single
title: "Publications"
permalink: /publications/
author_profile: true
---

## Selected Publications

- **PADBen: A Comprehensive Benchmark for the Robust Evaluation of Paraphrase Attack Detection.** Yiwei Zha, R. Min, S. Shanu. In preparation for ACL Rolling Review 2026. [arXiv](https://arxiv.org/abs/2511.00416) [Code](https://github.com/JonathanZha47/PadBen-Paraphrase-Attack-Benchmark)

- **MobileAgentBench: An Efficient and User-Friendly Benchmark for Mobile LLM Agents.** L. Wang, Y. Deng, Yiwei Zha, G. Mao, Q. Wang, T. Min, W. Chen. AAAI MARW Workshop, 2025. [arXiv](https://arxiv.org/abs/2406.08184) [Project](https://mobileagentbench.github.io/)

- **SMARTFinRAG: Interactive Modularized Financial RAG Benchmark.** Yiwei Zha. arXiv preprint, 2025. [arXiv](https://arxiv.org/pdf/2504.18024) [Code](https://github.com/JonathanZha47/SMARTFinRAG)

- **iTransPASOH: A Physics-Aware iTransformer Framework for Lithium-Ion Battery State-of-Health Estimation.** Yiwei Zha, F. Yan, C. Yang, G. Mao. Under review / revision.

- **Physics-Aware Fusion Method in Time Series Model for Lithium-Ion Battery State-of-Health Estimation.** Yiwei Zha, G. Mao. Poster, NU IMPACT Symposium, Northeastern University, 2025.
```

- [ ] **Step 2: Add projects page**

Use:

```markdown
---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
---

## Current Projects

### Memory-Poison Defense

Defenses for poisoned information in agent context windows and memory mechanisms. This project studies how adversarial or unreliable information affects agent behavior and how system-level defenses can reduce those risks.

### Model-Compression Safety

Study of safety issues that may emerge when models are compressed through quantization, pruning, or related efficiency techniques.

## Trustworthy AI And Evaluation

### PADBen

A benchmark for evaluating AI text detectors against paraphrase attacks. [Code](https://github.com/JonathanZha47/PadBen-Paraphrase-Attack-Benchmark)

### Phishing Email Detection

Trustworthy AI work around detecting malicious or deceptive email content.

### MobileAgentBench

A benchmark for evaluating mobile LLM agents. [Project](https://mobileagentbench.github.io/) [arXiv](https://arxiv.org/abs/2406.08184)

## Systems And Earlier Work

### SMARTFinRAG / FinRAGDemo

Financial retrieval-augmented generation systems and demos. [GitHub](https://github.com/JonathanZha47)

### iTransPASOH

Earlier physics-guided learning work for lithium-ion battery state-of-health estimation.
```

- [ ] **Step 3: Build and commit**

Run:

```bash
bundle exec jekyll build
git add publications.md projects.md _pages/publications.md _pages/projects.md
git commit -m "feat: add publications and projects"
```

Expected:

```text
[main ...] feat: add publications and projects
```

## Task 5: Add CV And Contact Pages

**Files:**
- Create/modify: `cv.md`
- Create/modify: `contact.md`
- Optionally create: `files/Yiwei_Zha_CV.pdf`

- [ ] **Step 1: Add CV page without exposing stale CV as current**

Use:

```markdown
---
layout: single
title: "CV"
permalink: /cv/
author_profile: true
---

This page summarizes my academic background and selected research experience. An updated CV will be linked here once it is ready for public sharing.

## Education

- PhD student, Vrije Universiteit Amsterdam.
- M.S. in Computer Science, Northeastern University.
- B.A. in Computer Science and Mathematics, Boston University.

## Research Interests

- Trustworthy AI and safety for agentic systems.
- Memory poisoning and defenses for agent context windows.
- Safety implications of model compression.
- AI-generated content detection and phishing detection.
- LLM evaluation, RAG systems, and agent benchmarks.
```

- [ ] **Step 2: Add contact page**

Use:

```markdown
---
layout: single
title: "Contact"
permalink: /contact/
author_profile: true
---

I am open to research conversations and collaborations around trustworthy AI, agentic-system safety, model-compression safety, AI-generated content detection, and LLM evaluation.

- Email: [y.zha@vu.nl](mailto:y.zha@vu.nl)
- Google Scholar: [Yiwei Zha](https://scholar.google.com/citations?user=IvimIBUAAAAJ&hl=en)
- GitHub: [JonathanZha47](https://github.com/JonathanZha47)
- LinkedIn: [yiwei-zha](https://www.linkedin.com/in/yiwei-zha/)
```

- [ ] **Step 3: Build and commit**

Run:

```bash
bundle exec jekyll build
git add cv.md contact.md _pages/cv.md _pages/contact.md files/Yiwei_Zha_CV.pdf
git commit -m "feat: add cv and contact pages"
```

Expected:

```text
[main ...] feat: add cv and contact pages
```

## Task 6: Verify Locally

**Files:**
- Modify only files required by verification fixes.

- [ ] **Step 1: Run build**

Run:

```bash
bundle exec jekyll build
```

Expected:

```text
done in
```

- [ ] **Step 2: Run local server**

Run:

```bash
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Expected:

```text
Server address: http://127.0.0.1:4000/
```

- [ ] **Step 3: Browser-check pages**

Open:

```text
http://127.0.0.1:4000/
http://127.0.0.1:4000/research/
http://127.0.0.1:4000/publications/
http://127.0.0.1:4000/projects/
http://127.0.0.1:4000/cv/
http://127.0.0.1:4000/contact/
```

Expected:

```text
Each page loads, navigation works, no phone number is visible, current role says first-year PhD student at Vrije Universiteit Amsterdam, and the homepage leads with trustworthy AI for agentic systems.
```

- [ ] **Step 4: Commit verification fixes**

Run if any fixes were needed:

```bash
git add .
git commit -m "fix: polish baseline site verification"
```

Expected:

```text
[main ...] fix: polish baseline site verification
```

## Task 7: Deploy To GitHub Pages

**Files:**
- Modify: `.github/workflows/pages.yml` only if needed.
- Modify: `_config.yml` if repository URL/baseurl differs.

- [ ] **Step 1: Confirm GitHub repository**

Preferred repository for user-site deployment:

```text
JonathanZha47/JonathanZha47.github.io
```

If it does not exist, create it on GitHub or ask Yiwei to create it.

- [ ] **Step 2: Add remote**

Run:

```bash
git remote add origin git@github.com:JonathanZha47/JonathanZha47.github.io.git
```

Fallback for HTTPS:

```bash
git remote add origin https://github.com/JonathanZha47/JonathanZha47.github.io.git
```

- [ ] **Step 3: Push main branch**

Run:

```bash
git branch -M main
git push -u origin main
```

Expected:

```text
branch 'main' set up to track 'origin/main'
```

- [ ] **Step 4: Enable Pages**

In GitHub repository settings:

```text
Settings -> Pages -> Build and deployment -> Source: Deploy from a branch -> Branch: main -> Folder: / (root)
```

Expected live URL:

```text
https://JonathanZha47.github.io/
```

- [ ] **Step 5: Verify live deployment**

Open:

```text
https://JonathanZha47.github.io/
```

Expected:

```text
The live site loads with the same content verified locally.
```

## Self-Review Notes

- Spec coverage: homepage, research, publications, projects, CV, contact, Academic Pages baseline, GitHub Pages deployment, privacy rule, and current research framing are all mapped to tasks.
- Placeholder scan: no `TBD`, `TODO`, or intentionally vague implementation steps remain.
- Risk: exact file paths may differ if the Academic Pages template keeps pages under `_pages/`; tasks name both root-page and `_pages/` variants so implementation can follow the template structure discovered after cloning.
