# AI Opportunity Navigator

AI Opportunity Navigator is a browser-based prototype for collecting, assessing, and governing potential AI use cases. It demonstrates how an organization could move from informal AI ideas to a transparent, repeatable prioritization process.

The project is designed as a portfolio example of AI enablement, transformation, product thinking, and responsible AI governance. It focuses on the operating model around AI decisions—not on building an AI model.

### 🚀 Live Demo

[Try AI Opportunity Navigator](https://harshita-ht.github.io/ai-opportunity-navigator/)

### Explore the Application

1. Submit a fictional AI opportunity.
2. Review the opportunity backlog.
3. Open an opportunity to explore the prioritization assessment.
4. Examine the governance review and decision-making workflow.

**Note:** This is a portfolio prototype using fictional data.
Changes are stored locally in your browser.

### My Role & Contributions

*Independent Portfolio Project | AI Enablement & Transformation*

I designed and developed AI Opportunity Navigator as a portfolio project exploring how organizations can systematically identify, evaluate, and prioritize potential AI use cases.

My contributions included:

- **Problem Definition:** Identified the need for a structured, transparent process for AI opportunity intake and prioritization.
- **Process & Workflow Design:** Designed separate workflows for opportunity submitters and reviewers, covering submission, screening, assessment, collaboration, and recommendations.
- **Prioritization Framework:** Developed a weighted assessment methodology incorporating business impact, technical feasibility, data readiness, and adoption readiness.
- **AI Governance:** Incorporated preliminary risk screening, specialist review, and human oversight into the opportunity evaluation process.
- **Product Development:** Translated business requirements into an interactive prototype using Codex for AI-assisted development.
- **Testing & Iteration:** Refined the user experience, assessment guidance, and workflows through scenario-based testing and iterative improvements.

**Tools:** Codex, HTML, CSS, JavaScript, GitHub, GitHub Pages.

## Business problem

Organizations often receive AI ideas through presentations, spreadsheets, emails, and informal conversations. Those ideas can be difficult to compare because:

- Submitters describe solutions before clearly defining the business problem.
- Benefits are expressed differently and are rarely supported by a sense of scale.
- Technical feasibility, data readiness, and organizational adoption are considered inconsistently.
- Risk questions may appear too late, after time has already been invested.
- Review ownership and decision reasoning are not always visible.
- A high-value idea can be confused with an idea that is safe and ready to deploy.

This creates a portfolio problem: decision-makers cannot easily see which opportunities deserve further investment, what evidence is missing, or which specialists should be involved.

## Solution

The application provides one structured workflow for both opportunity submitters and reviewers.

### For submitters

The submission experience helps a non-technical employee describe:

- The problem today and the information or systems involved.
- How AI could assist, using plain language.
- The expected value and the scale of the current workload.
- Whether the required data is available.
- The senior business sponsor and the people who would benefit.
- Initial data, autonomy, consequence, and regulatory risks.

The form explains how each section contributes to the assessment. It also calculates estimated current workload from monthly volume, people involved, and time per case.

Submitters can use **My opportunities** to follow progress, review details, respond when more information is requested, and edit an opportunity only when its workflow status allows it.

### For reviewers

The reviewer experience provides:

- A searchable and filterable review queue.
- Clear ownership through claim and assignment controls.
- A consistent four-part priority assessment.
- A separate governance gate for preliminary risk.
- Optional business, technical, data, or other specialist reviewers.
- Optional governance verification by an appropriate risk stakeholder.
- Recommendations such as pilot, further discovery, request more information, consider a non-AI solution, or defer.
- A visible rationale and audit-style history for important decisions.

One primary reviewer remains accountable for each opportunity. Additional expertise is requested only when the case requires it, avoiding unnecessary review overhead.

## Prioritization methodology

Each opportunity is rated from 1 to 5 across four dimensions:

| Dimension | Weight | What it considers |
| --- | ---: | --- |
| Business impact | 35% | Time, cost, revenue, quality, customer, or risk value supported by the scale of the problem |
| Technical feasibility | 25% | Whether current AI capabilities can address the need and the complexity of systems, integrations, and controls |
| Data readiness | 20% | Whether suitable information exists, is accessible, is of sufficient quality, and can be used appropriately |
| Adoption readiness | 20% | Whether there is a committed owner, user support, an appropriate human role, and a realistic change path |

The weighted result is normalized to a score from **0 to 10**. The score supports comparison and prioritization; it does not automatically approve or reject an opportunity.

### Why risk is separate

Risk is treated as a governance gate rather than another weighted scoring category. This prevents a high business-value score from cancelling out a serious legal, compliance, privacy, security, safety, or autonomy concern.

The initial screen assigns a preliminary Low, Medium, or High risk tier based on:

- Data sensitivity.
- The authority given to AI.
- The consequence if the output is wrong.
- Whether laws, regulations, or formal policies may apply.

Medium- and high-risk opportunities require additional verification before a reviewer can recommend a pilot. This is still a preliminary decision-support process, not deployment approval.

## Product methodology

The prototype was developed through an iterative, problem-first approach:

1. **Define the operating problem.** The initial focus was how to make AI opportunity intake consistent and understandable for non-technical users.
2. **Simplify the submission model.** Questions were rewritten in plain language and grouped around impact, feasibility, data, adoption, and initial risk.
3. **Connect intake to assessment.** Each form section explicitly shows which review dimension it informs.
4. **Create a transparent rubric.** Reviewers use the same weighted criteria and see how the overall score is calculated.
5. **Separate prioritization from governance.** Portfolio value and risk verification are shown together but serve different decisions.
6. **Design the end-to-end workflow.** The prototype covers submission, screening, ownership, assessment, specialist input, recommendation, and submitter follow-up.
7. **Iterate through UAT scenarios.** Example opportunities and reviewer journeys were used to test calculations, terminology, edit permissions, send-back behavior, ownership, and governance escalation.
8. **Reduce reviewer effort.** The review workspace was reorganized into focused Assess, Collaborate, and Decide activities, with the submitted evidence kept accessible in a scrollable area.

## Key design decisions

- **Use “opportunity,” not “idea.”** An opportunity implies a business problem and potential value, while an idea can be only a proposed tool.
- **Keep one accountable reviewer.** Specialist reviewers contribute expertise without making ownership ambiguous.
- **Make human oversight explicit.** The intake asks whether AI drafts, recommends, acts after approval, or acts autonomously.
- **Ask for estimates, not false precision.** Rough volumes and time estimates are enough to support an initial comparison.
- **Explain the scoring model up front.** Submitters can see what reviewers will evaluate and which questions provide the evidence.
- **Do not treat a score as approval.** A strong priority score can justify further discovery, but governance and pilot decisions remain separate.
- **Use progressive disclosure.** Collapsible submission sections and focused review tabs reduce cognitive load without hiding the overall process.

## Lessons learned

### 1. Clear questions matter more than complex scoring

The quality of the assessment depends on the evidence collected. Questions such as “What is the problem today?” and “How could AI help?” produced a clearer user experience than asking submitters to define technical solutions or detailed outcomes too early.

### 2. Data readiness deserves its own view

Data is related to technical feasibility, but it creates different questions about availability, access, quality, permission, and suitability. Keeping it visible prevents teams from assuming that technically possible means data-ready.

### 3. Adoption is a real delivery constraint

An opportunity may be valuable and technically feasible but still fail without a senior sponsor, willing users, process ownership, and a clear human role. Adoption readiness therefore belongs in the priority assessment.

### 4. Risk should not be averaged away

A weighted risk score could make a serious concern look acceptable when combined with strong business benefits. A separate gate makes escalation requirements more visible and defensible.

### 5. Review participation should be proportional

Requiring multiple reviewers for every opportunity would slow down early screening. A primary reviewer with optional business, technical, data, and risk specialists provides clearer accountability and scales better.

### 6. Workflow language must describe real actions

Labels such as “Request more information,” “Claim,” and “Governance verification” are more useful when they trigger a clear status change, identify who owns the next action, and preserve the reason.

### 7. Reviewer experience affects governance quality

If the review interface requires excessive scrolling or repeated data entry, reviewers are more likely to skip context. Keeping assessment, collaboration, and decisions focused while leaving evidence visible supports better judgment.

### 8. A prototype needs explicit boundaries

The current application is suitable for demonstrating the workflow, testing terminology, and gathering feedback. It is not a production governance system and should not be presented as one.

## Prototype architecture and data

The application is contained in a single HTML file with embedded styling and JavaScript:

- `index.html`

It runs entirely in the browser and does not require a server or build process. Opportunities, assessments, assignments, and workflow updates are saved in the browser's local storage. CSV export is available for the review queue.

Because the prototype has no backend or user authentication:

- Data is available only in the browser where it was entered.
- Clearing browser storage removes saved changes.
- Different users do not share a common queue.
- Reviewer identities and permissions are illustrative.
- Local storage should not be used for confidential or regulated information.

## Running the prototype

Open `index.html` in a modern browser. No installation is required.

The prototype includes fictional demonstration opportunities. Use **Restore demo scenarios** in the review queue to return to the sample dataset. Export the queue first if you need to preserve browser-local changes.

## What production implementation would require

A production version would need:

- Secure sign-in and role-based permissions.
- A shared database and reliable audit history.
- Encryption, retention rules, and approved data handling.
- Configurable scoring rubrics and governance policies.
- Notifications, service-level expectations, and workflow integrations.
- Ownership by an AI program or governance team.
- Accessibility, security, privacy, and compliance testing.
- Reporting that tracks opportunities from submission through realized business value.

## Project outcome

The result is a working prototype that demonstrates how responsible AI governance can be embedded into an approachable business workflow. It makes opportunity quality, review ownership, prioritization logic, specialist involvement, and governance escalation visible without expecting submitters to be AI experts.
