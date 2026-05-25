# Yiwei Zha Personal Page Design

Date: 2026-05-25
Status: Revised draft after user correction
Workspace: `/Users/zhayiwei/Desktop/personal workflow/personal-page`

## Goal

Build and deploy a clean academic personal website for Yiwei Zha. The page should make Yiwei easy to understand as a first-year PhD researcher at Vrije Universiteit Amsterdam whose current center of gravity is trustworthy AI, especially building safety into agentic systems. The site should introduce what Yiwei is working on now, what research directions he is interested in, and how his earlier work connects to that trajectory.

The site may refer to the Academic Pages template, but it does not need to be a literal clone. The strongest outcome is a lightweight, maintainable static site with the same academic information architecture: home/about, publications, research/projects, CV, and external profile links.

## Source Materials

- Historical PhD-application CV for background only: `/Users/zhayiwei/phd applications/research CV/CV_0919_trustworthy.pdf`
- Academic Pages reference: https://academicpages.github.io/
- Google Scholar: https://scholar.google.com/citations?user=IvimIBUAAAAJ&hl=en
- GitHub: https://github.com/JonathanZha47
- LinkedIn from historical CV: https://www.linkedin.com/in/yiwei-zha/

Important content rule:

- The historical CV is a reference for research history, projects, publications, and contact links. It should not be copied directly as current site content because Yiwei is now a first-year PhD student at Vrije Universiteit Amsterdam.
- Current research framing provided by Yiwei should override the old CV framing: the site is about present and future trustworthy AI work, with the CV used only to recover past projects and publication details.

Public context checked:

- Academic Pages is a GitHub Pages/Jekyll template with sidebar profile, publications, talks, teaching, portfolio, blog, and CV pages.
- GitHub profile shows the name Yiwei Zha, username JonathanZha47, affiliation text "BU CS | NEU MSCS", and research/code repositories including `SMARTFinRAG`, `PadBen-Paraphrase-Attack-Benchmark`, and `AutoDroid-Agent`.
- Public paper/project pages found for `MobileAgentBench` and `PADBen`.

## Audience

Primary audience:

- Potential collaborators in trustworthy AI, agentic-system safety, LLM evaluation/safety, AI-generated content detection, phishing detection, model compression, RAG, and agent benchmarks.
- Researchers, labs, and project teams deciding whether Yiwei's work aligns with their own.

Secondary audience:

- Technical collaborators who want a concise project and engineering overview.
- Prospective students or peers looking for papers, code, and ways to contact Yiwei.

## Recommended Approach

Use a GitHub Pages site based on the Academic Pages pattern first, then improve the visual design later if the baseline feels too plain.

1. **Academic Pages baseline**
   - Use the Academic Pages/Jekyll structure or a close lightweight equivalent.
   - Best if the goal is to deploy quickly to `JonathanZha47.github.io`.
   - Prioritize correct content, publications, links, and deployability over custom visuals.

2. **Visual redesign pass**
   - After the baseline is live, redesign typography, layout, spacing, and visual personality.
   - Keep the same GitHub Pages deployment target.
   - Treat this as a second iteration so deployment does not wait on visual exploration.

Recommendation: implement the Academic Pages-style baseline first and deploy it. Once Yiwei can review the live page, decide whether to keep the template look or upgrade the visual design.

## Site Structure

### Global Navigation

Top navigation:

- Home
- Research
- Publications
- Projects
- CV
- Contact

External links should be visible in the header or profile area:

- Google Scholar
- GitHub
- LinkedIn
- Email

### Home

Purpose: immediately state who Yiwei is and what research direction he works in.

Hero content:

- Name: Yiwei Zha
- Role: First-year PhD student at Vrije Universiteit Amsterdam.
- Research positioning: Trustworthy AI, with a focus on building safety into agentic systems.
- Primary call to action: See Research.
- Secondary call to action: View Publications, GitHub, or CV.

Suggested short bio:

> I am a first-year PhD student at Vrije Universiteit Amsterdam working on trustworthy AI, with a particular interest in building safety into agentic systems. My current work studies defenses against memory poisoning in agent context windows and the safety implications of model compression methods such as quantization and pruning. I have also worked on AI-generated text detection, phishing email detection, RAG systems, mobile-agent benchmarks, and earlier physics-guided learning for industrial systems.

Visual tone:

- Academic, precise, modern.
- White or near-white background with restrained accent color.
- Avoid a marketing-heavy hero. This should feel like a researcher's home page, not a product landing page.

### Research

Purpose: group Yiwei's work into understandable research themes, with current interests first and past work presented as supporting background.

Themes:

- Safety for Agentic Systems
  - Memory-poisoning defense: defending agent context windows and memory mechanisms against injected or poisoned information.
  - Agentic safety evaluation: understanding how agents fail under adversarial or unreliable context.
  - Mobile-agent and mobile edge computing benchmarks as earlier experience in evaluating agent behavior.

- Model Compression and Safety
  - Study whether quantization, pruning, and other compression methods introduce, amplify, or hide safety issues.
  - Frame compression not only as an efficiency problem, but also as a reliability and trustworthiness problem.

- AI-Generated Content and Abuse Detection
  - PADBen: paraphrase attack detection benchmark for AI-generated text detectors.
  - Phishing email detection and related trustworthy AI tasks.
  - X-Domain JailBench and safety-aware semantic entropy probes as adjacent LLM safety/evaluation work.

- Retrieval, Evaluation, and Agent Benchmarks
  - RAG systems and financial RAG work as prior systems experience.
  - Nuclear Norm: unsupervised method to compare uses of LLMs.
  - MobileAgentBench: mobile LLM agent benchmark.

- Earlier AI for Science and Industrial ML
  - iTransPASOH: physics-aware battery state-of-health estimation.
  - Distribution-shift-aware soft sensing and industrial process prediction work.
  - Present this as preliminary past work that broadened Yiwei's ML background, not the main current research identity.

Each theme should include a concise paragraph and 2-3 highlighted project cards or list items. Current projects should appear before older work.

### Publications

Purpose: show research output with status, venue, links, and contribution area. The initial list may be drafted from the historical CV, but each item should be checked and lightly rewritten before publication so the page reflects Yiwei's current PhD-era profile.

Initial publication list from the historical CV:

- Zha, Y., Min, R., Shanu, S. PADBen: A Comprehensive Benchmark for the Robust Evaluation of Paraphrase Attack Detection. In preparation for 2026 ACL Rolling Review.
- Zha, Y. SMARTFinRAG: Interactive Modularized Financial RAG Benchmark. arXiv preprint, 2025.
- Wang, L., Deng, Y., Zha, Y., Mao, G., Wang, Q., Min, T., Chen, W. MobileAgentBench: An efficient and user-friendly benchmark for mobile LLM agents. AAAI MARW Workshop, 2025. Nominated for JMLR.
- Zha, Y., & Mao, G. Physics-aware fusion method in time series model for lithium-ion battery state-of-health estimation. Poster, NU IMPACT Symposium, Northeastern University, 2025.
- Zha, Y., Yan, F., Yang, C., & Mao, G. iTransPASOH: A physics-aware iTransformer framework for lithium-ion battery state-of-health estimation. Knowledge Based Systems, minor revision.
- Yan, F., Zha, Y., Zhao, Y., Wang, S., Yan, D., & Yang, C. Target-driven dynamic weighted joint distribution adaptation network for soft sensing of tumbler strength in sintering process. IEEE/ASME Transactions on Mechatronics, under review.
- Yan, F., Zha, Y., Wang, H., Zhao, Y., He, B., & Yang, C. When Sintering Process Meets Distribution Shift: Predicting Multi-step Burn-Through Point via Adversarial Domain Adaption. IEEE/CAA Journal of Automatica Sinica, under review.

Add links where verified:

- MobileAgentBench project page: https://mobileagentbench.github.io/
- MobileAgentBench arXiv: https://arxiv.org/abs/2406.08184
- PADBen arXiv: https://arxiv.org/abs/2511.00416
- PADBen GitHub: https://github.com/JonathanZha47/PadBen-Paraphrase-Attack-Benchmark

### Projects

Purpose: connect research output to code and systems work.

Highlighted projects:

- Memory-Poison Defense: defenses for poisoned information in agent context windows and memory.
- Model-Compression Safety: safety issues introduced by quantization, pruning, and related compression techniques.
- PADBen: benchmark for evaluating AI text detectors under paraphrase attacks.
- Phishing Email Detection: trustworthy AI work around detecting malicious or deceptive emails.
- X-Domain JailBench: safety evaluation framework across professional domains.
- SMARTFinRAG / FinRAGDemo: financial retrieval-augmented generation projects from GitHub.
- MobileAgentBench: benchmark architecture for mobile LLM agents.
- iTransPASOH: physics-aware battery SOH estimation; present as earlier industrial ML work rather than the main site focus.

Each project should include:

- Title.
- One-line summary.
- Research area tag.
- Optional links: paper, arXiv, code, project page.

### CV

Purpose: provide a direct CV download and a skim-friendly web summary. The deployed CV should be an updated current version, not necessarily the historical PhD-application PDF.

Include:

- Education.
- Research experience.
- Selected publications.
- Work experience.
- Skills if available from an updated CV or later user input.

Store the updated PDF in a public `files/` or `assets/` folder for deployment. The link label should be `Download CV`. If an updated CV is not available during first implementation, the site can include a CV section without a download link until Yiwei approves the file.

### Contact

Include:

- Email: `y.zha@vu.nl`
- GitHub: `JonathanZha47`
- Google Scholar link.
- LinkedIn link.
- Vrije Universiteit Amsterdam affiliation details once Yiwei confirms the preferred department/lab wording.

Do not display phone number on the public site by default. The historical CV includes it, but a public personal webpage should avoid exposing it unless Yiwei explicitly asks.

## Visual Design

Direction:

- First version should stay close to the Academic Pages template: clean sidebar/profile area, simple top navigation, list-first publications, and Markdown-editable content.
- Avoid spending first-version effort on a highly custom visual system.
- A later redesign can make the page more distinctive once the baseline content and GitHub Pages deployment are working.

Palette:

- Background: white or very light neutral.
- Text: deep charcoal.
- Accent: one calm research-oriented color such as deep teal, blue, or restrained green.
- Secondary accents can distinguish research areas, but avoid a one-color monochrome theme.

Typography:

- Serif or humanist font for name/headings if available.
- Sans-serif for body and navigation.
- Keep line lengths comfortable for reading publications and project summaries.

Layout:

- Desktop: two-column first viewport works well: profile/introduction on the left, highlighted research/projects on the right.
- Mobile: single column, navigation collapses to compact links.
- Publications should be list-first, not card-heavy, because academic readers scan authors/venue/status.
- Project cards can be compact and repeated, with stable dimensions and clear links.

## Content Priorities

The first screen should answer:

- Who is Yiwei Zha?
- What does he research?
- What are the strongest current outputs?
- How can a potential collaborator read the papers/code or get in touch?

Top three research signals:

- Trustworthy AI for agentic systems, especially memory-poisoning defense in agent context windows.
- Safety implications of model compression methods such as quantization and pruning.
- Detection and evaluation work around AI-generated text, phishing emails, RAG systems, and mobile-agent benchmarks.

Past-work signal:

- Physics-guided learning for industrial systems should remain visible as prior research experience, but it should not dominate the main site framing.

## Deployment Plan

Target:

- GitHub Pages.
- Ideal repository name: `JonathanZha47.github.io` for root deployment at `https://JonathanZha47.github.io/`.

If this local folder becomes the deployment repo:

1. Initialize git.
2. Build the static site.
3. Add an updated CV PDF to a deployable folder if approved.
4. Push to GitHub.
5. Enable GitHub Pages from the default branch or GitHub Actions depending on framework.

If using Vite/Astro:

- Configure base path only if deploying to a project page instead of the root user page.
- Add a deploy workflow if GitHub Pages does not auto-publish the built output.

## Testing And Verification

Before handoff:

- Build succeeds.
- Local dev server loads.
- Header links and external links work.
- CV download link works if an updated CV is included.
- Desktop and mobile screenshots show no text overflow or overlapping sections.
- Publications and project links open the intended pages.
- Page title, meta description, and social preview basics are set.
- No private information beyond approved email/profile links is exposed.

## Assumptions To Confirm

- Site should be in English.
- Current role should be first-year PhD student at Vrije Universiteit Amsterdam.
- The historical CV should be used for background and research-history extraction, not copied directly as current public content.
- Main research identity should center trustworthy AI and safety for agentic systems.
- Current projects should include memory-poison defense and model-compression safety.
- Past work should be visible, but it should be organized as prior experience rather than the main current direction.
- Public phone number should be omitted.
- `y.zha@vu.nl` is the preferred public email.
- Fast static implementation is acceptable instead of a direct Academic Pages fork.
- The current empty folder can become the site repository.
- Yiwei will provide or approve a profile photo later; implementation can initially use initials or a clean text-first profile area if no photo is available.

## Out Of Scope For First Version

- Blog system.
- Dynamic citation syncing from Google Scholar.
- Full CMS/editor workflow.
- Private analytics.
- Complex animations.
- Multi-language pages.
