# GrandCaddy Agile Portfolio (PRP370S)

## Project Presentation 3

**Student:** Rocco Given Visagie | **Student number:** 220343527 | **Due:** 27/10/2026

**Link to GrandCaddy Website:** <https://grand-caddy.vercel.app/>

GrandCaddy is a community-based website that connects elderly people (60+), starting in Kuilsriver, with trusted and verified helpers ("Caddies") for everyday tasks such as cleaning, grocery shopping, gardening, painting and minor repairs. It uses a pay-per-task model, and its value proposition is "Real people, trusted service and simple usage." Family members and caregivers are a secondary customer group, and administrators manage verification, disputes and payments. The solution uses a three-tier web architecture (presentation, application, data). The working prototype is built with React (TypeScript) and Supabase, which provides authentication and the database. The team members and their areas are listed in the charter below.

---

## 1. Agile Team Charter

### Evidence

#### 1. Team purpose and vision

- **Team mission:** To design and build GrandCaddy, a simple and safe platform that connects elderly people with trusted, verified helpers (Caddies) for everyday tasks.
- **Success definition:** An elderly customer can post a task, a verified caddy can accept and complete it, and families and administrators can trust the process.
- **Product / service:** GrandCaddy, a community web platform with a pay-per-task model, starting in Kuilsriver.

#### 2. Team members and roles

| Member | Area | Main responsibility |
|---|---|---|
| Luke | Customer experience and authentication | Sign up and login with Supabase Auth, Post-a-Task form, My Tasks, Task Detail and the reusable TaskCard component |
| Rocco (me) | Helper experience | Helper profile and bookings tables, helper sign-up, Browse Open Tasks, Accept Task and My Bookings (Mark Complete) |
| Isaac | Everything else | Supabase database setup (users, tasks and task_categories tables) and all remaining project work |

#### 3. Ways of working

- **3.1 Agile framework:** Kanban using a Trello board with three columns (Product Backlog, In Progress and Completed). Work is organised into one-week sprints, one per user story or theme.
- **3.2 Ceremonies:** a daily stand-up, recorded in the logbook by answering what I completed, what I plan to complete next and what my impediments are; and a weekly board walk through covering what is needed to advance the work, whether anyone is working off the board, what the team must finish and what the blockers are.

#### 4. Working agreements

- We show up prepared and on time.
- We respect time-boxes.
- We give constructive feedback.
- We raise blockers early.
- We commit to continuous improvement.

#### 5. Communication

- **Primary channels:** [add, for example WhatsApp or Teams].
- **Response-time expectations:** [0-24 hours]
- **Remote / hybrid norms:** [Yes we have agreed to that]

#### 6. Decision-making

- **Decision method:** [tick the one you used: consensus / Product Owner final decision / team vote / Agile lead decides after input].
- **Escalation path if we are stuck:** [add, for example raise it with the lecturer].

#### 7. Definition of Done

- The feature or screen meets the user story and its acceptance criteria.
- It follows the accessibility principles (large buttons, readable text, simple navigation).
- It is consistent with the other user journeys.
- It has been reviewed by another team member.
- The Trello card is moved to Completed and the logbook is updated.

#### 8. Core values and behaviours

- Respect, transparency, accountability, trust and a learning mindset.
- **Project values:** trust and safety first, and simplicity for elderly users.

#### 9. Risks and constraints

- **Known risks:** the interface becoming too complicated for elderly users; helpers providing services before they are verified; an accepted task not being limited to one helper; administrator pages exposing sensitive customer or helper information.
- **Dependencies:** the customer and helper features depend on the Supabase tables set up first; verification, ratings and payments must integrate with the Caddy workflow.
- **Constraints:** one-week sprints, [budget: add], [skills: add].

#### 10. Review and improvement

- **Charter reviewed every:** [quarter / release / retrospective].
- The project is ongoing, so this charter remains a living document.

#### 11. Team commitment

| Name | Agreement |
|---|---|
| Luke | ✓ |
| Rocco | ✓ |
| Isaac | ✓ |

### Reflection

My part of GrandCaddy was the helper experience, so the charter mattered most to me where it protects trust. Our value of "trust and safety first" shaped how I built the helper side: a new helper profile starts with a verification status of pending, so nobody is treated as trusted until they are verified. I learned that a definition of done is useful when two people build in parallel, because Luke and I could both check our work against the same standard. I also learned that a charter only helps if it is revisited. If I did this again I would review it at regular intervals, since an agile charter is meant to be a living document. This will help me in future team projects.

---

## 2. User Stories and Tasks

Stories use the format *As a [role], I want [goal], so that [benefit]*, and each is split into tasks (Cohn, 2004). The tasks come from our project backlog.

### Story 1: Elderly user (customer)

> As an elderly customer, I want to post and manage tasks with a simple, easy-to-read screen, so that I can get help without struggling with technology.

**Acceptance criteria:** a task can be posted with description, price, location and time; buttons are large; navigation is simple; helpers show a verified badge.

| Sprint | Tasks |
|---|---|
| Sprint 1: Core features | Define the elderly user journey; design the homepage; create the "Post Task" screen (description, price, location, time); add simple navigation with large buttons and an accessible UI |
| Sprint 2: Trust and interaction | Design the caddy selection view (browse helpers); add the review submission layout; add the verification badge (background checked); show the payment per task concept UI |
| Sprint 3: Finalisation | Prototype the full journey in Figma; test the task flow; check consistency with the rest of the system |

### Story 2: Caddy (helper)

> As a caddy, I want to create a profile, browse available jobs and accept or reject them, so that I can earn money helping my community.

**Acceptance criteria:** onboarding is clear; available jobs are listed; accept and reject actions work; ratings and earnings are visible.

| Sprint | Tasks |
|---|---|
| Sprint 1: Core features | Define the caddy onboarding flow; design the profile setup page; create the task browsing screen; add the accept/reject task UI |
| Sprint 2: Trust system | Design the rating display; add the review submission layout; show the earnings per task concept UI; add the verification badge |
| Sprint 3: Finalisation | Prototype the full caddy journey in Figma; test the task acceptance flow; ensure consistency with the elderly user system |

### Story 3: Administrator

> As an administrator, I want to manage users, approve helpers, resolve disputes and monitor payments, so that the platform stays safe and trustworthy.

**Acceptance criteria:** users can be viewed, edited and blocked; helpers can be approved or rejected with notes; disputes can be resolved; refunds and weekly reports are available.

| Sprint | Tasks |
|---|---|
| Sprint 1: Core features | Define the admin journey; design login and dashboard; create the user management list (view/edit/block); build the task monitoring screen with sidebar navigation |
| Sprint 2 (10-14 Aug): Verification and approvals | Design the helper approval queue; create the document review interface (ID, background check); build the Approve/Reject workflow; add admin notes; send automated email/SMS on decision |
| Sprint 3 (17-21 Aug): Disputes and payments | Design the dispute dashboard; build the dispute review and resolution interface; create the transaction monitoring view; add the manual refund tool; generate basic weekly reports |

### Story 4: Family member

> As a family member or caregiver, I want to arrange and monitor help for my elderly relative, so that I have peace of mind when I cannot visit.

**Acceptance criteria:** a family member can view their relative's tasks and see that helpers are verified and rated.

The original backlog lists this story without a task breakdown, so I broke it into the tasks below.

| Sprint | Tasks |
|---|---|
| Sprint 4 (24-28 Aug) | Define the family member journey; design the family dashboard; allow booking on behalf of a relative; show task status and helper verification |

### Story 5: Trust and safety (cross-cutting epic)

> As a user of GrandCaddy, I want helpers to be verified, rated and supported, so that I can trust the platform.

| Sprint | Tasks |
|---|---|
| Sprint 5 (31 Aug-4 Sep): Helper verification | Design the document upload flow (ID, proof of address); build the background check status tracker (pending/cleared/rejected); add "Verified" badge logic; create the interview scheduling UI |
| Sprint 6 (7-11 Sep): Rating and review | Design the 5-category star rating (punctuality, quality, communication, value, safety); build review submission after a task; show the helper average rating; add a "Report Issue" button |
| Sprint 7 (14-18 Sep): Phone support | Design a one-tap "Call Support" button; build ticket creation from calls; create the support agent dashboard; add "Callback Request" for offline users |
| Sprint 8 (21-25 Sep): Dispute resolution | Design the dispute submission form; build the admin dispute review panel; create resolution tracking (pending/resolved/escalated) |

### Reflection

Working from the caddy (helper) story, I saw how acceptance criteria turn into things I can build and test: a helper must be able to sign up, browse open tasks, accept one and mark it complete, and each of those became its own task. Splitting the story into small tasks also made my work easier to plan, because each page had one clear job. Reviewing the whole backlog, I noticed that some tasks in the elderly user's Sprint 2 and 3 were copied from the caddy story, and that the family member story had no task breakdown in the backlog, so I broke it down myself. That taught me to check that every story is complete and its tasks really belong to it before a sprint starts. In future I will use the INVEST checklist to test a story before accepting it.

---

## 3. Product Backlog

The product backlog is the prioritised list of everything the product needs. Priority uses MoSCoW (Must, Should, Could). Points are my suggested relative estimates, so please adjust them to what your team agreed.

| ID | Epic | Backlog item | Priority | Points | Sprint |
|---|---|---|---|---|---|
| PB-01 | Elderly user | Define elderly user journey | Must | 2 | 1 |
| PB-02 | Elderly user | Homepage for elderly users | Must | 3 | 1 |
| PB-03 | Elderly user | "Post Task" screen (description, price, location, time) | Must | 5 | 1 |
| PB-04 | Elderly user | Simple, accessible navigation (large buttons) | Must | 3 | 1 |
| PB-05 | Elderly user | Caddy selection view (browse helpers) | Must | 5 | 2 |
| PB-06 | Elderly user | Review submission layout | Should | 3 | 2 |
| PB-07 | Elderly user | Verification badge (background checked) | Must | 3 | 2 |
| PB-08 | Elderly user | Full Figma prototype and flow testing | Must | 5 | 3 |
| PB-09 | Caddy | Onboarding flow and profile setup | Must | 5 | 1 |
| PB-10 | Caddy | Task browsing screen (available jobs) | Must | 5 | 1 |
| PB-11 | Caddy | Accept/reject task UI | Must | 3 | 1 |
| PB-12 | Caddy | Rating display and earnings per task UI | Should | 5 | 2 |
| PB-13 | Caddy | Full Figma prototype and acceptance flow test | Must | 5 | 3 |
| PB-14 | Admin | Admin journey, login and dashboard | Must | 5 | 1 |
| PB-15 | Admin | User management list (view/edit/block) | Must | 5 | 1 |
| PB-16 | Admin | Task monitoring screen with sidebar navigation | Should | 5 | 1 |
| PB-17 | Admin | Helper approval queue and document review | Must | 8 | 2 |
| PB-18 | Admin | Approve/Reject workflow with notes | Must | 5 | 2 |
| PB-19 | Admin | Automated email/SMS decision notifications | Should | 5 | 2 |
| PB-20 | Admin | Dispute dashboard and resolution interface | Must | 8 | 3 |
| PB-21 | Admin | Transaction monitoring and manual refund tool | Must | 8 | 3 |
| PB-22 | Admin | Basic weekly reports (tasks, revenue, disputes) | Could | 5 | 3 |
| PB-23 | Family member | Family dashboard and booking on behalf of a relative | Should | 8 | 4 |
| PB-24 | Trust and safety | Helper document upload flow | Must | 5 | 5 |
| PB-25 | Trust and safety | Background check status tracker | Must | 5 | 5 |
| PB-26 | Trust and safety | Verified badge logic and interview scheduling UI | Should | 5 | 5 |
| PB-27 | Trust and safety | 5-category star rating design | Should | 5 | 6 |
| PB-28 | Trust and safety | Post-task review and helper average rating | Must | 5 | 6 |
| PB-29 | Trust and safety | "Report Issue" button | Must | 3 | 6 |
| PB-30 | Trust and safety | One-tap "Call Support" button | Should | 3 | 7 |
| PB-31 | Trust and safety | Support ticket creation and agent dashboard | Should | 8 | 7 |
| PB-32 | Trust and safety | Callback request for offline users | Could | 3 | 7 |
| PB-33 | Trust and safety | Dispute submission form | Must | 5 | 8 |
| PB-34 | Trust and safety | Admin dispute review panel | Must | 5 | 8 |
| PB-35 | Trust and safety | Resolution tracking (pending/resolved/escalated) | Must | 5 | 8 |
| PB-36 | Build | Supabase tables: users, tasks, task_categories (Isaac) | Must | 5 | Build |
| PB-37 | Build | Sign up and login with Supabase Auth, Customer/Helper role toggle (Luke) | Must | 5 | Build |
| PB-38 | Build | Post-a-Task form, My Tasks, Task Detail and TaskCard (Luke) | Must | 8 | Build |
| PB-39 | Build | helper_profiles and bookings tables, helper sign-up form (Rocco) | Must | 5 | Build |
| PB-40 | Build | Browse Open Tasks and Accept Task action (Rocco) | Must | 5 | Build |
| PB-41 | Build | My Bookings with Mark Complete and Past section (Rocco) | Must | 5 | Build |

### Reflection

Because GrandCaddy depends on trust, verification, approvals and disputes are the Must-haves in the backlog, while reports and callbacks are Could-haves. For my own items (PB-39 to PB-41) I treated them as Must-haves because customers cannot get help until a helper can accept a task. I also saw that they depend on Isaac's tables being ready first, so priority and order are not the same thing. Estimating in points was the hardest part, and the points here are estimates, so in future I would estimate as a team using planning poker. This exercise improved my ability to explain why one item comes before another.

---

## 4. Sprint Backlog

A sprint backlog is the part of the product backlog the team commits to for one sprint, plus the plan to deliver it (Schwaber and Sutherland, 2020).

### Sprint 1: Core features (July)

**Sprint goal:** Define the core journeys and the main screens for all three roles.

| Task | Story | Owner | Status |
|---|---|---|---|
| Define the elderly user journey | Elderly | Luke | Done |
| Design the elderly homepage and "Post Task" screen | Elderly | Luke | Done |
| Add simple navigation (large buttons) | Elderly | Luke | Done |
| Define caddy onboarding, profile page and task browsing | Caddy | Rocco | Done |
| Design admin login, dashboard and user management list | Admin | Isaac | Done |

### Sprint 2: Trust and interaction

**Sprint goal:** Add the trust features: caddy selection, reviews, badges and admin approvals.

| Task | Story | Owner | Status |
|---|---|---|---|
| Design the caddy selection view | Elderly | Luke | Done |
| Add review layout and verification badge | Elderly/Caddy | Luke and Rocco | Done |
| Design the rating display and earnings UI | Caddy | Rocco | Done |
| Build the helper approval queue and Approve/Reject workflow (10-14 Aug) | Admin | Isaac | Done |
| Add admin notes and automated email/SMS notification | Admin | Isaac | Done |

### Sprint 3: Finalisation, disputes and payments

**Sprint goal:** Finalise the prototypes and design dispute and payment handling (17-21 Aug).

| Task | Story | Owner | Status |
|---|---|---|---|
| Prototype full elderly and caddy journeys in Figma | Elderly/Caddy | Luke and Rocco | Done |
| Test the task acceptance flow | Caddy | Rocco | Done |
| Dispute dashboard and resolution interface | Admin | Isaac | Done |
| Transaction monitoring view and manual refund tool | Admin | Isaac | Done |
| Basic weekly reports | Admin | Isaac | Done |

### Planning week: Business Model and Solution Architecture (4-7 Aug)

**Sprint goal:** Connect the business requirements to the technical solution so that the business model, the user journeys and the solution architecture support the same objectives. The taskboard shows the following items as completed.

| Completed item | Status |
|---|---|
| GrandCaddy business model developed (Business Model Canvas) | Completed |
| Customer segments identified and value proposition defined | Completed |
| Revenue model defined; key activities and key resources identified | Completed |
| Solution architecture developed | Completed |
| Customer journey and Caddy/helper journey reviewed | Completed |
| Administrator requirements reviewed | Completed |
| Trust and safety requirements identified | Completed |

### Sprint 4: Family member (24-28 Aug)

**Sprint goal:** Design the family member's journey so a family member or caregiver can arrange and monitor help for an elderly relative.

| Task | Story | Owner | Status |
|---|---|---|---|
| Define the family member journey | Family member | Rocco | Done |
| Design the family dashboard | Family member | Rocco | Done |
| Allow booking on behalf of a relative | Family member | Rocco | Done |
| Show task status and helper verification | Family member | Rocco | Done |

### Sprint 5: Helper verification (31 Aug-4 Sep)

**Sprint goal:** Make sure only verified helpers are presented as trusted.

| Task | Owner | Status |
|---|---|---|
| Design the document upload flow (ID, proof of address) | Rocco | Done |
| Build the background check status tracker | Rocco | Done |
| Add "Verified" badge logic to helper profiles | Rocco | Done |
| Create the interview scheduling UI | Rocco | Done |

### Sprint 6: Rating and review (7-11 Sep)

**Sprint goal:** Give users a detailed, trustworthy way to rate helpers.

| Task | Owner | Status |
|---|---|---|
| Design the 5-category star rating | Luke | Done |
| Build review submission after task completion | Luke | Done |
| Create the helper average rating display | Luke | Done |
| Add the "Report Issue" button | Luke | Done |

### Sprint 7: Phone support (14-18 Sep)

**Sprint goal:** Let users reach a real person easily.

| Task | Owner | Status |
|---|---|---|
| Design the one-tap "Call Support" button | Isaac | Done |
| Build ticket creation from calls | Isaac | Done |
| Create the support agent dashboard | Isaac | Done |
| Add the "Callback Request" feature | Isaac | Done |

### Sprint 8: Dispute resolution (21-25 Sep)

**Sprint goal:** Provide a clear, end-to-end dispute process.

| Task | Owner | Status |
|---|---|---|
| Design the dispute submission form (user and helper) | Isaac | Done |
| Build the admin dispute review panel | Isaac | Done |
| Create resolution tracking (pending/resolved/escalated) | Isaac | Done |

### Implementation sprint: Supabase and React build (29 Sep-2 Oct)

**Sprint goal:** Turn the designs into a working app where a customer can post a task and a helper can accept and complete it. Luke and Rocco built the customer and helper features on tables that Isaac had already set up in Supabase.

| Task | Owner | File or table | Status |
|---|---|---|---|
| Set up the Supabase tables users, tasks and task_categories | Isaac | Supabase | Done |
| Wire the SignUp page to Supabase Auth (Customer/Helper toggle passed as the role) | Luke | `src/pages/SignUp.tsx`, `src/components/Toggle.tsx` | Done |
| Verify the Login page calls `signIn()` correctly | Luke | `src/pages/Login.tsx` | Done |
| Post-a-Task form that inserts into the tasks table | Luke | `src/pages/PostTask.tsx` | Done |
| My Tasks page (own tasks, status badge, newest first) | Luke | `src/pages/MyTasks.tsx` | Done |
| Task Detail page with helper name if assigned | Luke | `src/pages/TaskDetail.tsx` | Done |
| Reusable TaskCard component used in My Tasks and Browse Tasks | Luke | `src/components/TaskCard.tsx` | Done |
| Create the helper_profiles and bookings tables with basic RLS policies | Rocco | Supabase SQL Editor | Done |
| Helper sign-up form (bio, skills, years of experience) | Rocco | `src/pages/HelperSignup.tsx` | Done |
| Browse Open Tasks (status = open) | Rocco | `src/pages/BrowseTasks.tsx` | Done |
| Accept Task button (creates a booking, sets the task to assigned) | Rocco | `src/components/AcceptTaskButton.tsx` | Done |
| My Bookings page with Mark Complete and a Past section | Rocco | `src/pages/MyBookings.tsx` | Done |

### Reflection

In the implementation sprint my goal was clear: a helper can sign up, browse open tasks, accept one and see it in My Bookings. My first step was to create the helper_profiles and bookings tables, because every page I built depended on them, which showed me that a sprint backlog also has to be ordered by dependency. The Accept Task button taught me the most. It has to create a booking and also set the task to assigned, so if one step fails the data can become inconsistent. The unique rule on task_id also ensures only one helper can take a task. A weakness is that I used open development policies on my tables, which I would tighten before real users arrive. Next time I will update my task statuses daily so the sprint backlog is always accurate.

---

## 5. Agile Logbook

The logbook follows the PRP37XS Agile Logbook template: a taskboard, a walkthrough and daily stand-up entries that answer three questions. Monday is a campus day, so project work and logbook entries run from Tuesday to Friday. The weeks below are 28-31 July, 4-7 August and the implementation week.

### Week 1: 28-31 July 2026 (Caddy core features, Sprint 1)

#### Taskboard

| Product Backlog | In Progress | Completed |
|---|---|---|
| User Story 1, Elderly Customer, Sprint 1 customer journey: homepage, post task (description, location, date and time, payment), accessible navigation, caddy selection, reviews and ratings. User Story 2, Caddy/Helper, Sprint 1 caddy core features: onboarding, profile setup, available task browsing, task details, accept task, reject task. User Story 3, Administrator: dashboard, user management, helper verification, task monitoring, dispute management, payment monitoring. | Caddy/Helper user story: onboarding flow, profile requirements, available task screen, task details, accept/reject task workflow, trust and safety requirements. | Basic Caddy onboarding requirements defined; profile requirements identified; available task requirements identified; accept/reject workflow defined; initial Caddy user journey completed; future verification and ratings requirements identified. |

#### Walkthrough

| Question | Answer |
|---|---|
| What do we need to do to advance this piece of work? | Complete the Caddy/Helper user story by defining how a helper registers, creates a profile, views available tasks and accepts or rejects them, and make sure the Caddy journey connects with the elderly customer's task-posting journey while staying simple. |
| Is anyone working on anything that is not on the board? | No major work outside the agreed backlog. Discussions about verification, ratings and trust were recorded as future requirements. |
| What do we need to finish as a team? | Caddy onboarding, profile setup, available task browsing, task details, accept/reject functionality, the basic Caddy user journey and the requirements for future verification and ratings. |
| Are there any bottlenecks or blockers? | How much information to show helpers without complicating the interface; making sure an accepted task goes to one helper and is no longer shown to others; adding verification and trust requirements in the later development stage. |

#### Daily logbook

| Day | What did I complete since the last stand-up? | What am I planning to complete next? | What are my impediments? |
|---|---|---|---|
| Tue 28 Jul | Reviewed the Caddy/Helper user story and helped define the basic onboarding process, from registration to creating a helper profile. Identified the personal and profile information a helper must provide, and why verification matters before a helper can provide services. | Help define the Caddy profile and what customers should see when they view a helper, and how the profile connects to the customer journey. | Balancing a simple registration process with enough information to create trust. The profile should not be too complicated. |
| Wed 29 Jul | Helped define the Caddy profile structure: helper name, profile picture, description, services offered, location, availability, experience, rating and verification status. | Define the available-task screen and what a helper needs to see before accepting a task (description, location, date, time and payment). | Too much information on one screen. The interface must stay clear while giving helpers enough to decide. |
| Thu 30 Jul | Helped define the task-browsing process: helpers log in, open their dashboard, view available tasks and select one to see its details. | Complete the accept/reject task workflow, define what happens after a task is accepted or rejected and how the customer is informed. | Making sure an accepted task is assigned correctly and removed from the available list for other helpers. Customer notifications also need to be considered. |
| Fri 31 Jul | Completed the main Caddy/Helper workflow for the sprint: registration, profile setup, viewing available tasks and task details, accepting and rejecting tasks. Reviewed future requirements: verification, ratings, reviews and earnings. | Prepare the completed Caddy requirements for the next stage, which expands the journey with verification, ratings, reviews and earnings. | No major blockers. The main risk is making sure verification, rating and payment features integrate with the Caddy workflow. |

### Week 2: 4-7 August 2026 (Business model and solution architecture)

#### Taskboard

| Product Backlog | In Progress | Completed |
|---|---|---|
| User Story 1, Elderly Customer: homepage, post task, task details, accessible navigation, caddy selection, reviews, ratings, customer support. User Story 2, Caddy/Helper: onboarding, profile, available tasks, accept/reject task, verification, ratings, reviews, earnings. User Story 3, Administrator: dashboard, user management, task monitoring, helper approval, verification document review, approve/reject helper, dispute management, payment monitoring. | GrandCaddy business and solution planning: Business Model Canvas, value proposition, customer segments, revenue model, key activities, key resources, solution architecture, user roles, system components, trust and safety, payment functionality, notification functionality. | Business model developed; customer segments identified; value proposition defined; revenue model defined; key resources and key activities identified; solution architecture developed; customer, caddy/helper and administrator requirements reviewed; trust and safety requirements identified. |

#### Walkthrough

| Question | Answer |
|---|---|
| What do we need to do to advance this piece of work? | Connect the business requirements to the technical solution so that the business model, user journeys and solution architecture support the same objectives. The next step is to turn them into detailed interface designs and development tasks. |
| Is anyone working on anything that is not on the board? | No major work outside the agreed activities. Payment gateways, notifications, background checks and phone support were discussed and treated as supporting requirements. |
| What do we need to finish as a team? | The Business Model Canvas, solution architecture, user roles, system components, database and security requirements, and the payment, verification, notification and phone-support processes. |
| Are there any bottlenecks or blockers? | Keeping the architecture simple while supporting multiple user roles; making sure elderly customers can use the system comfortably; addressing trust and safety because customers deal with helpers they may not know. |

#### Daily logbook

| Day | What did I complete since the last stand-up? | What am I planning to complete next? | What are my impediments? |
|---|---|---|---|
| Tue 4 Aug | Reviewed the elderly customer's journey: access the website, register or log in, navigate the homepage, post a task, enter task information, select a helper, complete the task, and rate or review. Discussed simple navigation and large, clear buttons. | Review the Caddy/helper journey and the functionality helpers need, and how the customer and helper journeys connect. | Making sure the website is not too complicated for elderly users while still providing all required functionality. |
| Wed 5 Aug | Reviewed the Caddy/Helper journey: registration, profile creation, verification, available tasks, accept/reject, task completion, ratings and earnings. Discussed how verification builds customer trust. | Review the administrator requirements: managing users, helpers, tasks and verification. | Making sure helpers cannot provide services before completing verification. The process must be built clearly into the system. |
| Thu 6 Aug | Reviewed the Administrator journey: admin login, dashboard, user and helper management, verification, task monitoring, dispute management and payment monitoring. Discussed restricted and secure administrator access. | Consolidate the customer, helper and administrator requirements into a proposed solution architecture, and identify the main database entities and external services. | Administrator functionality must not expose sensitive customer or helper information unnecessarily. The architecture must support the roles without becoming overly complicated. |
| Fri 7 Aug | Helped consolidate the requirements into the Business Model (customer segments, value proposition, channels, customer relationships, revenue streams, key activities, key resources, key partners, cost structure) and the Solution Architecture (Presentation, Application/Business Logic and Data layers, plus payment processing, helper verification, notifications and phone support). | Prepare the requirements for the next development stage: detailed Figma screens, database structures and development tasks. | No major blockers. Risks: the architecture must support future features, the system must stay accessible to elderly customers, and security, verification and payment must be considered during development. |

### Week 3: Implementation sprint, helper features (29 Sep-2 Oct)

#### Taskboard

| Product Backlog | In Progress | Completed |
|---|---|---|
| User Story 2, Caddy/Helper, build items: helper_profiles and bookings tables, helper sign-up, Browse Open Tasks, Accept Task, My Bookings with Mark Complete. User Story 1, Elderly Customer, build items (Luke): sign-up and login, Post-a-Task, My Tasks, Task Detail, TaskCard. | [Update: any helper page that was still being built or tested at the end of the week.] | [Confirm what was finished:] helper_profiles and bookings tables created; helper sign-up form; Browse Open Tasks; Accept Task; My Bookings with Mark Complete and a Past section. |

#### Walkthrough

| Question | Answer |
|---|---|
| What do we need to do to advance this piece of work? | Build the helper side on the tables Isaac had already set up, so a helper can sign up, browse open tasks, accept one and mark it complete, and so a task moves from open to assigned to completed in the database. |
| Is anyone working on anything that is not on the board? | [No major work outside the agreed backlog. Confirm.] |
| What do we need to finish as a team? | Helper sign-up, Browse Open Tasks, Accept Task and My Bookings (my part), and sign-up, Post-a-Task, My Tasks, Task Detail and the shared TaskCard (Luke's part), all working against the same database. |
| Are there any bottlenecks or blockers? | Accept Task makes two changes (creating the booking and setting the task to assigned) and both must succeed; only one helper may take a task; the task card is shared between Luke's pages and my Browse Tasks page; the open development policies on my tables must be tightened before real users. [Confirm.] |

#### Daily logbook

| Day | What did I complete since the last stand-up? | What am I planning to complete next? | What are my impediments? |
|---|---|---|---|
| Tue 29 Sep | Reviewed my assignment and Isaac's tables, then created the helper_profiles and bookings tables in the Supabase SQL Editor. `verification_status` defaults to pending, a unique rule on `task_id` lets only one helper take a task, and row level security is switched on with basic development policies. | Build the helper sign-up form (bio, skills and years of experience) that saves to helper_profiles. | [Making sure the new tables link correctly to Isaac's users and tasks tables.] |
| Wed 30 Sep | Built the helper sign-up page (`HelperSignup.tsx`). It saves the profile for the logged-in user with verification pending, then redirects to Browse Tasks. | Build Browse Open Tasks, showing tasks with status open (category, title, suburb, amount and date). | [Needing the logged-in user's id, which depends on Luke's sign-up and login wiring.] |
| Thu 1 Oct | Built Browse Open Tasks with an Accept button for logged-in helpers, and started the Accept Task action: it inserts a booking and sets the task to assigned with my user id as the helper. | Finish Accept Task and build My Bookings. | [Both database changes must succeed or the data could become inconsistent. Luke is also extracting the card from my Browse Tasks page into the shared TaskCard.] |
| Fri 2 Oct | Finished Accept Task (redirects to My Bookings) and built My Bookings. It joins each booking to its task, has a Mark Complete button that sets the booking and the task to completed, and moves completed bookings into a Past section. | Test the whole flow with Luke's Post-a-Task: a customer posts a task, a helper accepts it and marks it complete, and I check the status changes from open to assigned to completed. | [No major blockers. Later, tighten the open development policies on helper_profiles and bookings.] |

### Reflection

The template made me answer the same three questions every day, which kept my work and blockers visible. The clearest example is the blocker I recorded on 30 July: an accepted task must go to one helper and disappear from the available list. That risk carried into the implementation sprint, where I handled it by setting the task to assigned when it is accepted and by adding a unique rule on task_id in the bookings table. The weekly walkthrough also showed me that most of our risks were about trust and simplicity for elderly users rather than technical problems. A logbook is only reliable when it is completed on the day, so I will write my entries daily from now on. This habit will help me in the workplace, where teams need evidence of decisions and progress.

---

## The Final Reflection

These five artefacts connect into one story from my point of view. The charter set our values (trust, safety, simplicity), the user stories turned them into needs for each user, the product backlog prioritised the work, the sprint backlog broke it into achievable steps, and the logbook recorded what we learned. In the implementation sprint I saw the charter working in practice. Isaac set up the shared database first, so Luke (customer features) and I (helper features) could build in parallel without waiting for each other. The one weakness was shared files such as the task cards, which we both used, so next time I would agree on shared components before building. My biggest growth was moving from building screens to thinking about the people who use them, especially elderly users and the helpers who support them.
