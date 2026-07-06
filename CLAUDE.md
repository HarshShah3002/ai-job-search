# Job Application Assistant for Harsh Tarang Shah

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Harsh Tarang Shah, helping with:
1. **Job fit evaluation** - Assess job postings against his profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding, including H1B-aware targeting

## Candidate Profile

### Identity
- **Name:** Harsh Tarang Shah
- **Location:** College Station, Texas, US (open to relocating anywhere in the US)
- **Languages:** English (fluent), Hindi (native), Gujarati (native)
- **Status:** MS graduate (May 2026), on F1/OPT, will require H1B sponsorship. Actively job searching for full-time roles.
- **LinkedIn headline:** "Business Analytics MS @ Texas A&M | Data Analytics, Data Engineering, BI, Product"

### Education
- **MS in Engineering Management, Business Analytics Specialization** (2024-2026) - Texas A&M University, College Station, TX
  - GPA: 3.7/4
  - Coursework: Management of Engineering Systems, Data Analysis, Marketing, System Analysis & Design
- **B.Tech in Electronics & Communication Engineering** (2020-2024) - Pandit Deendayal Energy University, Gandhinagar, India
  - GPA: 4/4
  - Coursework: Object Oriented Programming, Data Mining, Machine Learning, Python Programming

### Professional Experience
- **Program Operations Management Assistant** (Current) - **Texas A&M University, Dept. of Nutrition & Food Science** (College Station, TX)
  - Supports program operations while completing MS coursework
  - Recently joined a faculty research project analyzing EmotiBit wearable physiological data for real-time adaptive cobot (collaborative robot) behavior

- **Product Management Intern** (Jan 2024 - June 2024) - **Staytuned LLP** (Ahmedabad, India)
  - Led a cross-functional team of 6 to automate GitHub workflows with JavaScript & GitHub Actions, cutting manual steps from 10 to 2 and saving 15+ developer hours weekly
  - Built an intelligent issue-triage system on the GitHub API that auto-categorized 180+ monthly issues, cutting mean-time-to-resolution for P0/P1 issues from 48 to 29 hours (40% reduction)
  - Built a Tableau dashboard tracking 8 KPIs from GitHub metrics (PR cycle time, sprint velocity), surfacing 3 bottlenecks and lifting sprint completion by 26%

- **Software Engineer Intern** (May 2023 - July 2023) - **TYSU Infotech Pvt. Ltd.** (Ahmedabad, India)
  - Redesigned 8 core user-facing screens based on qualitative feedback analysis, driving a 40% engagement boost and a 25% drop-off reduction
  - Used SQL to identify homepage accessibility gaps, validated fixes with A/B testing, improving accessibility by 55%

- **Data Analyst Intern** (May 2022 - July 2022) - **Innodel Technologies Pvt. Ltd.** (Ahmedabad, India)
  - Built a Tableau dashboard on cardiovascular illness trends to help providers identify high-risk patient segments
  - Analyzed a 500K+ row Netflix dataset in Tableau, delivering 4 actionable content-personalization recommendations

### Technical Skills
- **Primary:** SQL, Python, Data Analysis & Visualization, Tableau, Power BI
- **Secondary:** JavaScript, HTML, CSS, Machine Learning, A/B Testing, EDA, Streamlit, GitHub API automation
- **Domain:** Retail/product analytics, business intelligence, product operations, GenAI-augmented dashboards
- **Software:** Excel, Jira, Notion, Slack, Google Colab, Jupyter Notebook, Google Analytics, AWS, MySQL

### Certifications
- **Professional Scrum Master I (PSM I)** - Scrum.org
- **Engineering Project Management** - Texas A&M University
- **Understanding Incubation and Entrepreneurship** - IIT Bombay (Top 1% scorer)

### Publications
- None currently.

### Awards
- Top 1% scorer - "Understanding Incubation and Entrepreneurship" course, IIT Bombay

### Behavioral Profile
- **Self-starter / high ownership** - builds his own infrastructure rather than waiting on process (e.g. a 1,200+ entry Notion job-search HQ, automated GitHub workflows)
- **Systematic under volume** - comfortable tracking and executing many parallel threads (job applications, outreach, coursework, research) without losing organization
- **Strengths:** end-to-end execution (idea to deployed dashboard/tool), data storytelling, cold outreach and written communication
- **Growth areas:** still building depth in large-scale/production data engineering infrastructure beyond project-scale pipelines
- **Thrives in:** fast-paced, high-ownership environments (startup-like pace) where he can move from idea to shipped output quickly

### What Excites You
- Turning messy raw data into a working, decision-ready tool (pipeline to dashboard to insight)
- Automation that removes repetitive human steps from a workflow
- Roles that blend technical depth (SQL/Python/data) with business or product framing

### Target Sectors
- Tech / SaaS: Tesla, OpenAI, Brex, Clay, Upgrade, Peregrine Technologies, Amigo AI, Goose, Omni
- Retail / e-commerce / consumer: Etsy, Ollie, T-Mobile, Sony Interactive Entertainment

### Deal-breakers
- Company unable or unwilling to sponsor H1B on a realistic timeline after OPT
- Roles that are purely maintenance work with no path to substantive analysis or building

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools (Danish portals + country-agnostic LinkedIn tool)

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match, and H1B sponsorship likelihood. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and his strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`
