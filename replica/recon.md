# Recon map: takeUforward (web)

Scope: the full platform. Learning sheets, the practice judge, core CS subjects,
aptitude, company prep, the AI assistant, the planner, gamification, community
and paid plans. The map covers all of it; the size (XL) means the build gets
phased (see Size).
For: Parikshaa, a placement-prep platform for Indian college students and
early-career developers (the same audience as the original).
Date: 2026-10-13

## How this map was made (read first)

- **takeuforward.org itself could not be opened.** This environment's network
  policy blocks the host, so no page was loaded directly and no reference
  screenshots exist yet (`replica/screens/` is empty). Everything here comes
  from the site's own pages as indexed by web search, plus a few third-party
  pages. Each finding carries a confidence:
  - **high**: stated on several of the site's own pages
  - **medium**: one of the site's own pages, or its own promotional post
  - **guess**: inferred, or not found at all; verify before building
- **No account was used.** The original's Terms of Service (operator:
  Moveforward Private Limited) prohibit scraping, bots, reverse engineering,
  copying or redistributing platform content, and "using the Platform for any
  commercial purpose" without written consent. Using an account to research a
  competitor falls under that last clause, so this recon stays on public pages
  only. When the network block is lifted, verify against **public, signed-out
  pages** only. Do not use a TUF account for this.
- Nothing of the original's code, copy, content or assets was read or saved.
  The map describes what the product does, in our own words.

## Sources

| # | source | URL | notes |
| --- | --- | --- | --- |
| 1 | release guide ("ZENKAI", the latest rollout) | https://takeuforward.org/community/posts/explore-zenkai-a-complete-guide-to-takeuforward-s-latest-rollout | the best single feature list; also the closest thing to a changelog |
| 2 | pricing page | https://takeuforward.org/pricing | passes, bundles, AI credit allowances: what is gated |
| 3 | older plans page | https://takeuforward.org/plus | earlier plan names (Sprint, Pinnacle), outdated prices |
| 4 | Prep Hub index | https://takeuforward.org/prep-hub | subject and sheet catalogue |
| 5 | A2Z DSA sheet | https://takeuforward.org/prep-hub/strivers-a2z-dsa-sheet | flagship sheet: modules, sections, lesson/practice items |
| 6 | other DSA sheets | https://takeuforward.org/prep-hub/blind-75 , https://takeuforward.org/prep-hub/strivers-75-sheet , https://takeuforward.org/prep-hub/strivers-150-master-patterns-in-dsa | sheet page with progress counter |
| 7 | subject sheets | https://takeuforward.org/prep-hub/dbms-databases-and-sql-explained-deeply , https://takeuforward.org/prep-hub/oops , https://takeuforward.org/prep-hub/low-level-design , https://takeuforward.org/prep-hub/sql-data-engineering-foundations , https://takeuforward.org/prep-hub/operating-system-by-striver | modules, lessons, quizzes per subject |
| 8 | DSA practice hub | https://takeuforward.org/practice/dsa | topic / pattern / company organisation, recency toggle |
| 9 | problem pages | https://takeuforward.org/practice/dsa/next-permutation , https://takeuforward.org/plus/dsa/problems/ninja's-training | problem workspace, editor stub, test cases |
| 10 | all-problems (paid) | https://takeuforward.org/plus/dsa/all-problems?subject=all-dsa-problems , https://takeuforward.org/plus/sql/all-problems | filters by company, topic, difficulty |
| 11 | aptitude practice | https://takeuforward.org/practice/quantitative , https://takeuforward.org/practice/logical , https://takeuforward.org/practice/verbal | topic tables with practice and mock-test links |
| 12 | Problem of the Day | https://takeuforward.org/potd | today's problem, coin reward, dated archive |
| 13 | online IDE | https://takeuforward.org/ide | custom input, tabs, save and share |
| 14 | dashboard | https://takeuforward.org/dashboard | daily tasks, timer, progress, interview-experience counts |
| 15 | planner (Planly) | https://takeuforward.org/planly | questionnaire to daily plan, auto-reschedule |
| 16 | lists | https://takeuforward.org/lists | custom problem lists (formerly bookmarks) |
| 17 | notes (NoteSpace) | https://takeuforward.org/notes | notes by subject, export |
| 18 | leaderboard | https://takeuforward.org/leaderboard | coins, trophies, titles, ways to earn |
| 19 | store | https://takeuforward.org/goodies | redeem coins |
| 20 | community | https://takeuforward.org/community | posts, interview experiences, success stories |
| 21 | interview experiences | https://takeuforward.org/interview , https://takeuforward.org/interview/popular-companies/Google | per-company, round-wise stories |
| 22 | editorial articles | https://takeuforward.org/blogs/data-structure-and-algorithm/two-sum | written solutions |
| 23 | terms of service | https://takeuforward.org/terms-and-conditions | prohibited uses (see above) |
| 24 | refund policy | https://takeuforward.org/cancellation-policy | all sales final; conflicts with the terms' carve-outs |
| 25 | privacy policy | https://takeuforward.org/privacy-policy | 16+, Indian law, 30-day deletion |
| 26 | founder post on the free tier | https://www.linkedin.com/posts/rajstriver_striver-takeuforward-activity-7316666912589930496-FOQK | free tier once limited to 3 code runs (since lifted, per source 1) |
| 27 | third-party value guide | https://tufpricing.vercel.app/guides/is-tuf-plus-worth-it | independent opinion on plan value |

Not found: an Android or iOS app (no store listing turned up; treat as web only),
public API docs, a help centre or FAQ, the sign-in page.

## Core loop

A student picks a structured sheet, works through it item by item (read a
lesson, solve the linked problem in the in-browser judge, tick it off), and
comes back daily to keep progress and revision moving. Paid passes unlock
more subjects, company-tagged questions and AI credits.

## Screens

Routes are the original's public URL patterns, recorded as evidence only. The
clone picks its own.

| ID | screen | route / how to reach | purpose | key components | states seen | confidence |
| --- | --- | --- | --- | --- | --- | --- |
| S01 | Home | `/` | marketing entry: Prep Hub, practice, pricing | top nav, hero, sheet cards, CTA | signed out | medium |
| S02 | Pricing | `/pricing` | sell passes and bundles | plan cards with struck-through price, pass list, feature matrix, AI credit line items, "launching 2027" labels | signed out, signed in | high |
| S03 | Sign in / sign up | prompted from progress actions ("log in or sign up to track progress") | create account | auth form or modal, OAuth buttons | not seen | guess |
| S04 | Checkout | `/plus/checkout` | pay for a plan | order summary, coupon field, pay button | not seen | guess |
| S05 | Account / subscription | `/plus/account` | active plan, validity, credits | plan card, expiry, credit balance | not seen | guess |
| S06 | Prep Hub | `/prep-hub` | catalogue of subjects and sheets | subject tabs, sheet cards (module/lesson/quiz counts) | filled | high |
| S07 | Sheet page | `/prep-hub/{sheet}` | one sheet: modules, sections, items, progress | progress bar and counter ("0% 0/69"), module accordion, item rows with type/difficulty/status, lesson and practice links | empty progress, partial | high |
| S08 | Lesson page | `/{sheet}/learning/{slug}`, `/learning/{subject}/{slug}` | theory for one item | article body, code samples in several languages, video (likely), prev/next, mark done | filled | medium |
| S09 | Module quiz | inside subject sheets (DBMS: 14 quizzes, OOPs: 18) | check understanding per module | MCQ card, score | not seen | medium |
| S10 | Editorial article | `/blogs/{category}/{slug}` | written solution: approaches, complexity | article, multi-language code tabs | filled | high |
| S11 | Practice hub | `/practice/dsa` | browse problems | filters: topic, pattern, company, difficulty, asked-frequency toggle (30 / 90 / 180 days); company chips with counts | filled | high |
| S12 | Problem workspace | `/practice/dsa/{slug}`, `/{sheet}/practice/{slug}`, `/plus/dsa/problems/{slug}` | read, code, run, submit | split pane: statement / editor; language picker (C++, Java, Python, JavaScript); class stub; test-case panel; Run, Submit; verdict; hints; editorial; submissions; notes; add to list; AI panel | "You haven't submitted yet", submitted | high (layout), medium (tabs) |
| S13 | All problems (paid) | `/plus/{dsa,sql}/all-problems` | full problem bank | table, filters by company / topic / difficulty, premium locks | filled | medium |
| S14 | Aptitude practice hub | `/practice/{quantitative,logical,verbal}` | topic list per aptitude area | topic table with practice and mock-test links | filled | high |
| S15 | Aptitude lesson | `/learning/aptitude/{topic}` | theory and worked problems | article, worked examples, discussion | filled | medium |
| S16 | Aptitude mock test | from S14 topic rows | timed MCQ test | timer, question palette, MCQ card, submit, score | not seen | guess |
| S17 | Problem of the Day | `/potd` | daily challenge | today's problem card with coin reward (+20), calendar archive by date | filled | high |
| S18 | Online IDE | `/ide` | free-form coding | editor, language picker, custom input, output, multiple tabs, save, share link | filled | medium |
| S19 | Company prep | company collections in practice and paid plans | practise by company | company list, recency filter (30 / 60 / 180 days), tagged problems | not seen | medium |
| S20 | Dashboard | `/dashboard` | home after sign-in | daily task list, learning timer, progress tracker, sprint revision notes, planner link, POTD, popular paths, interview-experience stats | signed in only | medium |
| S21 | Planner | `/planly` | personal study plan | onboarding questionnaire (level, target, deadline, daily time, subjects), day-by-day plan, sprint quizzes | onboarding, active plan | medium |
| S22 | Lists | `/lists` | custom problem collections for revision | list cards, list detail table, create / rename / delete | empty, filled | medium |
| S23 | Notes | `/notes` | notes by subject, linked to items | note list by subject, editor, export | empty, filled | medium |
| S24 | Saved code ("CodeSpace") | not found | saved code for revision | code list per problem | not seen | guess |
| S25 | AI assistant ("TUFY") | panel inside S12 (guess) | doubts, progressive hints, code review, interview follow-ups | chat panel, credit balance, out-of-credits upsell | not seen | medium (features), guess (placement) |
| S26 | Profile | not found | learning journey, skills, projects, achievements | stats, badges, activity | not seen | medium |
| S27 | Settings | not found | account, preferences, delete account | forms | not seen | guess |
| S28 | Community feed | `/community?tab=...` (interview-experience, success-stories) | browse posts | tabs, post cards with counters | filled | high |
| S29 | Post detail | `/community/posts/{slug}`, `/community/interview-experiences/{slug}` | read a post | meta header (company, role, experience, location, result), body, upvote count, comments ("Be the first to add a comment") | no comments, with comments | high |
| S30 | New post / share experience | from S28 | contribute an experience | structured form + rich text | not seen | medium |
| S31 | Interview experiences by company | `/interview`, `/interview/popular-companies/{Company}` | stories by company, round-wise | company grid, story list | filled (409 stories, 221 companies at time of indexing) | high |
| S32 | Leaderboard | `/leaderboard?tab=coins` | rankings | tabs, ranking table, top 5 this month, "ways to earn coins" panel, trophies, titles | filled | high |
| S33 | Store | `/goodies` | redeem coins | item cards (merch, plan time, coupons, experiences), coin price, redeem | filled | medium |
| S34 | Contests | not found (the DSA pass lists "Built-in Coding Editor + Contests") | timed competitions | unknown | not seen | guess |
| S35 | Legal | `/terms-and-conditions`, `/privacy-policy`, `/cancellation-policy` | policies | long-form text | filled | high |

## Flows

Click counts are guesses until verified on the live site.

```
F01 Student starts a sheet
    S01 home -> S06 prep hub -> S07 sheet -> S03 sign up -> S07 (progress now tracked) -> S08 lesson -> mark done
    happy path clicks: ~6 (guess)
    edge: signed out (progress prompt), paid sheet while on free tier (lock + upsell), resume where left off

F02 Solve a problem
    S07 sheet item -> S12 workspace -> write code -> Run (sample tests) -> Submit (hidden tests) -> verdict -> item marked solved on S07
    happy path clicks: ~4 (guess)
    edge: compile error, wrong answer on hidden test, time limit, switch language mid-way (stub swap), unsaved code on navigation, premium problem on free tier

F03 Get unstuck on a problem
    S12 -> hint 1 -> hint 2 (progressive) -> AI assistant (S25) or editorial / video -> retry
    edge: out of AI credits (upsell to S02), editorial gated by plan

F04 Daily Problem of the Day
    S20 dashboard or S17 POTD -> S12 -> submit -> +20 coins -> streak bonus
    edge: day rollover (time zone: IST), solving a past POTD from the archive

F05 Buy a plan
    S02 pricing -> S03 sign in (if needed) -> S04 checkout -> apply coupon -> pay -> S05 / unlocked content
    edge: coupon invalid or expired, payment failed, upgrading from a pass to a bundle, pass expiry (2-month and 12-month validity)

F06 Make a study plan
    S21 planner onboarding (level, target, deadline, daily time) -> generated plan -> S20 daily tasks -> sprint quiz
    edge: missed day (auto-reschedule), deadline too close for the syllabus, changing the target mid-plan

F07 Company-focused prep
    S11 practice or S19 company prep -> pick company -> recency filter (30 / 60 / 180 days) -> S12 -> solve
    edge: company list gated by plan, company with few tagged problems

F08 Revise
    S12 add to list / write note -> S22 lists / S23 notes -> revisit -> export notes
    edge: list deleted with items, duplicate add, export format

F09 Learn a core CS subject
    S06 -> S07 subject sheet (DBMS, OS, CN, OOPs, LLD, SQL) -> S08 lessons -> S09 module quiz -> progress
    edge: quiz retake, partially completed module

F10 Aptitude practice and mock test
    S14 aptitude area -> topic -> S15 lesson or practice -> S16 timed mock test -> score and review
    edge: timer expiry auto-submit, leaving mid-test, review of wrong answers

F11 Share an interview experience
    S28 community -> S30 new post (company, role, experience, location, result, rounds) -> publish -> S29 -> upvotes, comments
    edge: moderation queue, editing after publish, anonymous posting (unknown)

F12 Earn and redeem coins
    daily check-in (+1), solve (+10 to +20), quiz (+20), streak bonus, achievements (+100 to +5000) -> S32 leaderboard -> S33 store -> redeem
    edge: insufficient coins, out-of-stock item, abuse (farming coins)

F13 Contest (unverified)
    S34 -> register -> timed problem set in S12 -> ranking
    edge: everything unknown; verify before planning
```

## Components

| component | variants | states | used on |
| --- | --- | --- | --- |
| Top navigation | signed out, signed in (with coins / avatar) | dropdown open, mobile drawer | all |
| Button | primary, secondary, ghost, danger, upsell | default, hover, focus, disabled, loading | all |
| Sheet accordion | module > section > item rows | collapsed, expanded, locked (paid) | S07 |
| Item row | lesson, problem, quiz | not started, done, marked for revision, locked | S07, S13 |
| Progress bar + counter | percent + "done / total" | 0%, partial, complete | S06, S07, S20 |
| Difficulty badge | easy, medium, hard | n/a | S07, S11, S12, S13 |
| Tag chip | topic, pattern, company (with count) | selected, unselected | S11, S13, S19 |
| Filter bar | topic, difficulty, company, recency toggle | applied, cleared, no results | S11, S13, S19 |
| Code editor | per language with starter stub | empty, edited, read-only (submission view) | S12, S18 |
| Language picker | C++, Java, Python, JavaScript (verify list) | n/a | S12, S18 |
| Test-case panel | sample cases, custom input | idle, running, passed, failed | S12, S18 |
| Verdict panel | accepted, wrong answer, compile error, runtime error, time limit | n/a | S12 |
| Hint reveal | progressive (1, 2, 3...) | hidden, revealed | S12 |
| Tabs | description, editorial, submissions, notes | active, locked | S12, S28 |
| AI chat panel | doubt, hint, code review, follow-up | idle, streaming, out of credits | S25 |
| MCQ card | single answer, multiple answer (verify) | unanswered, selected, correct, wrong | S09, S16, S21 |
| Test timer + question palette | n/a | running, warning, expired | S16 |
| Calendar | POTD archive, plan days | today, solved, missed | S17, S21 |
| Daily task checklist | learn, practice, revise | pending, done, rescheduled | S20, S21 |
| Learning timer | n/a | running, paused | S20 |
| Plan card | pass, bundle | current plan, recommended, struck-through price | S02 |
| Coupon field | n/a | empty, applied, invalid | S04 |
| Coin toast / badge | +n coins | n/a | S12, S17, S32 |
| Leaderboard table | coins, trophies, titles tabs | you highlighted, empty period | S32 |
| Post card | interview experience, success story, post | n/a | S28, S31 |
| Comment thread | n/a | empty, filled | S29 |
| Upvote control | n/a | voted, not voted | S29 |
| Rich-text / markdown editor | post, note | empty, draft, saved | S23, S30 |
| "Add to list" modal | existing lists, new list | n/a | S12 |
| Paywall / lock overlay | n/a | locked, trial | S07, S12, S13 |
| Empty states | "You haven't submitted yet", "Be the first to add a comment", no lists, no notes | n/a | many |
| Toasts and modals | success, error, confirm | n/a | many |

## Inferred data model

```
User          id, name, email, avatar, college?, grad_year?, created_at
              evidence: profile (S26), sign-up prompt (S03); fields beyond name/email are guesses
              confidence: medium

Plan          id, name (pass or bundle), price, list_price, currency, validity_days, ai_credits
              evidence: S02 (Company PASS 2 months, DSA PASS 12 months, Basic / Core / Max, credit allowances)
              confidence: high

PlanEntitlement  plan_id, subject_id | feature_key
              evidence: S02 feature matrix (which subjects and tools each plan unlocks)
              confidence: high

Subscription  id, user_id, plan_id, starts_at, ends_at, status (active | expired | cancelled)
              evidence: pass validity on S02, S05 account page
              confidence: medium

Order / Payment  id, user_id, plan_id, amount, coupon_id, provider_ref, status
              evidence: S04 checkout, coupon codes announced publicly
              confidence: medium (payment provider unknown)

Coupon        code, discount, valid_until, max_uses
              evidence: public coupon announcements
              confidence: medium

Subject       id, slug, name (DSA, DBMS, OS, CN, OOPs, LLD, SQL, Aptitude, ...)
              evidence: S06
              confidence: high

Sheet         id, subject_id, slug, title, is_free, item_count
              evidence: S06, S07
              confidence: high

Module, Section  id, sheet_id / module_id, title, position
              evidence: "19 modules and 95 sections" (A2Z), "14 modules" (DBMS)
              confidence: high

SheetItem     id, section_id, position, kind (lesson | problem | quiz), ref_id
              evidence: S07 item rows linking to learning and practice pages
              confidence: high

Lesson        id, slug, title, body, video_url?, languages_covered
              evidence: S08, S15
              confidence: medium

Problem       id, slug, title, difficulty, statement, constraints, topics[], patterns[], is_premium
              evidence: S11, S12, S13
              confidence: high

StarterCode   problem_id, language, stub
              evidence: S12 class stub
              confidence: high

TestCase      id, problem_id, input, expected_output, is_sample, is_hidden
              evidence: S12 test-case panel, "hidden test cases"
              confidence: high

Editorial     problem_id, body, video_url?
              evidence: S10, S12
              confidence: high

Hint          problem_id, position, body
              evidence: progressive hints (S12, S25)
              confidence: medium

Company       id, name, logo?
CompanyProblem  company_id, problem_id, last_asked_at, frequency
              evidence: company chips with counts, 30 / 60 / 180-day recency filter
              confidence: high (that it exists), guess (how recency is stored)

Submission    id, user_id, problem_id, language, code, verdict, runtime_ms, memory_kb, created_at
              evidence: S12 ("You haven't submitted yet"), saved submissions
              confidence: high

Run           user_id, problem_id, language, code, custom_input, output (not stored long-term?)
              evidence: Run vs Submit, unlimited runs on free tier
              confidence: medium

UserItemProgress  user_id, sheet_item_id, status (not_started | done), revision_flag, completed_at
              evidence: S07 counters, revision views
              confidence: high

Quiz, QuizQuestion, QuizAttempt   quiz_id, question, options[], answer, explanation; user score
              evidence: module quizzes (S09), sprint quizzes (S21)
              confidence: medium

MockTest, MockTestAttempt   subject (quant | logical | verbal), duration, questions[], score
              evidence: S14 mock-test links
              confidence: medium

Potd          date, problem_id, coin_reward
              evidence: S17
              confidence: high

List, ListItem  user_id, name; list_id, problem_id, position
              evidence: S22
              confidence: high

Note          id, user_id, subject_id, ref (problem | lesson)?, body, updated_at
              evidence: S23, notes on problems
              confidence: medium

SavedCode     user_id, problem_id, language, code
              evidence: "CodeSpace" in source 1
              confidence: guess

StudyPlan     user_id, level, target, deadline, minutes_per_day, subjects[]
PlanTask      plan_id, date, sheet_item_id, kind (learn | practice | revise), status, rescheduled_from
              evidence: S21 questionnaire and auto-reschedule
              confidence: medium

LearningSession  user_id, started_at, ended_at, item_id?
              evidence: learning timer (S20)
              confidence: medium

AiCreditLedger  user_id, delta, reason (grant | usage), created_at
AiConversation  user_id, problem_id?, messages[], credits_used
              evidence: credits per plan (S02), assistant features (source 1)
              confidence: medium

CoinTransaction  user_id, delta, reason (check_in | solve | quiz | streak | achievement | redeem), created_at
              evidence: S32 "ways to earn coins"
              confidence: high

Achievement / Trophy / Title  id, name, rule; UserAchievement user_id, achievement_id, earned_at
              evidence: S32
              confidence: medium (rules unknown)

StoreItem, Redemption  name, coin_cost, stock; user_id, item_id, status
              evidence: S33
              confidence: medium

Post          id, user_id, kind (interview_experience | success_story | post), company?, role?, experience?, location?, result?, body, upvotes, created_at
Comment       id, post_id, user_id, body, created_at
Vote          user_id, post_id
              evidence: S28, S29, S31
              confidence: high

Contest, ContestEntry  guess; nothing public found
```

Relationships: Subject 1-n Sheet 1-n Module 1-n Section 1-n SheetItem; SheetItem
-> Lesson | Problem | Quiz; Problem 1-n TestCase, StarterCode, Hint, Submission;
Problem n-n Company; User 1-n Submission, UserItemProgress, List, Note,
CoinTransaction, Post; User 1-n Subscription n-1 Plan n-n Subject (entitlements);
User 1-1 StudyPlan 1-n PlanTask.

## Feature matrix

See `features.csv`: 79 rows. Must: 36, should: 23, could: 12 (one of them,
the high-level design track, is not in the original yet), skip: 8.

## Out of scope (cannot or should not be cloned)

- **Their content.** The A2Z sheet's curriculum and sequencing, the other
  sheets, 600+ videos, editorials, lessons, problem statements, test cases,
  hints and quizzes all belong to the original. Its terms forbid copying any of
  it. Parikshaa needs its **own** curriculum, problems, test cases and
  editorials. That is the biggest single cost of this project, bigger than the
  code. Classic problems (two sum and the like) are fair game as ideas, but the
  statements, test data and solutions must be written fresh.
- **Their company-question data.** Which company asked what, and when, is
  their dataset. Build yours from your own users' reports.
- **Their community.** The interview experiences and success stories are their
  users' posts, and the audience is theirs.
- **The founder's brand and audience.** "Striver", "takeUforward", "TUF+",
  "TUFY", "ZENKAI", "Planly", "NoteSpace", "CodeSpace" and "Prep Hub" are their
  names. None of them go into Parikshaa. (They belong in `replica/brand.json`'s
  avoid list when you get to `/replica-brand`.)
- **Store merch and partner rewards.** Physical goods and "real experiences"
  depend on their partnerships.
- **The founder's YouTube channel**, which drives most of their traffic.

## Size

Screens 35, flows 13, entities about 35.

Hard parts:

1. **The code judge.** Sandboxed execution of untrusted code in four or more
   languages, with time and memory limits, queueing, and hidden test cases.
   Use a hosted or self-hosted judge (for example Judge0) rather than building
   one. Must be isolated from everything else.
2. **Content.** Hundreds of problems, each with a statement, starter code in
   four languages, sample and hidden tests, hints and an editorial, plus lessons
   for six or more subjects and aptitude question banks. Months of authoring.
3. **Payments in India.** Rupee pricing, UPI, GST invoices, pass validity and
   entitlements by subject. Stripe's India support is limited; Razorpay or
   Cashfree are the usual choice. `/replica-architect` decides.
4. **The AI assistant.** LLM costs, credit metering, progressive hints that do
   not leak the full answer, code review grounded in the actual submission.
5. **The planner.** Turning level, deadline and daily time into a schedule,
   and rescheduling missed days without breaking the deadline.
6. **Gamification and community.** Anti-abuse on coins and leaderboards,
   moderation for posts and comments.

Size: **XL. Rescope it.** Suggested phases:

1. **Phase 1 (L):** sheets with progress, lessons, the practice judge, POTD,
   lists, auth, dashboard. This is the core loop.
2. **Phase 2 (M):** core CS subjects with quizzes, aptitude with timed mock
   tests, notes, pricing, checkout and plan gating.
3. **Phase 3 (M):** company prep, AI assistant with credits, planner.
4. **Phase 4 (M):** community, interview experiences, coins, leaderboard,
   profile, contests.

## Verify on the live site (signed out) once the host is allowed

- sign-in methods (Google? GitHub? email OTP?) and whether sign-in is a page or a modal
- lesson page controls: video placement, "mark done", how revision is flagged
- problem workspace tabs and where the AI assistant sits
- full language list in the editor
- contests: format, schedule, rating
- mock-test format: question count, timer, negative marking
- prices in INR and which payment methods checkout offers
- dark mode, mobile layout
- then take reference screenshots of public pages into `replica/screens/` (S01, S02, S06, S07, S11, S12, S14, S17, S28, S32)
