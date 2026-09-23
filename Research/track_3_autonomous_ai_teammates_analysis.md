# Paytm Build for India AI Hackathon --- Track 3

## Autonomous AI Teammates

> **Exact track statement:** "Build AI teammates that don't just
> respond; they get the job done."

The track asks for an AI teammate that goes beyond answering questions
and delivers **measurable outcomes in sales or customer service**. It
should understand context, make decisions, take actions, work alongside
human teams, and escalate only when needed.

------------------------------------------------------------------------

## 1. What this track is really asking

This is the most explicitly **agentic** of the three tracks.

### Traditional AI

``` text
User → Question → AI answer → Human does the work
```

### AI teammate

``` text
Task
 ↓
Understand context
 ↓
Plan
 ↓
Use tools
 ↓
Make decisions
 ↓
Execute
 ↓
Verify
 ↓
Resolve OR escalate
 ↓
Measurable outcome
```

The critical word is **outcome**.

The product should be judged by whether the task actually gets
completed, not simply by whether the AI produced a good response.

------------------------------------------------------------------------

# 2. Core requirements hidden in the statement

## "AI teammates"

The AI needs a defined role, context, tools, permissions and
responsibility.

## "Don't just respond"

A chatbot alone is insufficient. The AI needs to perform work.

## "Get the job done"

Give the AI a bounded task with a clear success condition.

Examples:

-   resolve a failed payment
-   process a refund
-   resolve a customer dispute
-   qualify a sales lead
-   book a sales meeting
-   onboard a merchant
-   recover an abandoned application

## "Measurable outcomes"

Examples:

-   ticket resolved
-   refund completed
-   lead qualified
-   meeting booked
-   merchant onboarded
-   first-contact resolution
-   average handling time reduced

## "Escalating to humans only when needed"

The architecture should be:

``` text
AI
 ↓
Can this be safely resolved?
 ├─ YES → execute → verify → complete
 └─ NO  → prepare case → human
```

Human escalation is therefore part of the product, not simply an error
condition.

------------------------------------------------------------------------

# 3. Why this is strategically relevant to Paytm

Paytm's current public materials describe AI being used across merchant
and consumer journeys, engineering, customer experience and operations.
Paytm has also publicly described an agentic-AI direction focused on
sales, service, operations and analytics.
citeturn0search29turn0search8turn0search1

Paytm's current public product direction also includes AI-powered
merchant marketing and business-growth agents. Its Pi material describes
AI taking a merchant from business information to creating and launching
an advertising campaign. citeturn0search3

That means Track 3 maps closely to a real Paytm technology direction.

------------------------------------------------------------------------

# 4. Assistant vs Copilot vs Agent vs Teammate

### Assistant

Answers:

> "What is my refund status?"

### Copilot

Suggests:

> "Here is the response you can send."

Human clicks send.

### Agent

Can execute:

``` text
Find transaction
→ diagnose
→ initiate refund
→ verify
```

### AI teammate

Owns a bounded business outcome:

``` text
Customer issue
 ↓
Investigate
 ↓
Decide
 ↓
Act
 ↓
Communicate
 ↓
Verify
 ↓
Resolve
 ↓
Escalate only if necessary
```

Track 3 is pointing toward the last model.

------------------------------------------------------------------------

# 5. The most important design principle

## Give the AI a job, not a personality.

Weak:

> "Meet your friendly AI assistant."

Strong:

> "Meet the Payment Resolution Teammate. It owns failed-payment cases
> from customer complaint to verified resolution."

The second has a clear scope, responsibility, tools and success
condition.

------------------------------------------------------------------------

# 6. Two explicit opportunity areas

The statement specifically mentions:

### Customer service

Possible teammates:

-   Payment Resolution Agent
-   Refund Agent
-   Dispute Agent
-   Merchant Support Agent
-   Onboarding Support Agent
-   Application Recovery Agent
-   Complaint Resolution Agent

### Sales

Possible teammates:

-   Sales Development Representative
-   Lead Qualification Agent
-   Merchant Acquisition Agent
-   Follow-up Agent
-   Cross-sell Agent
-   Deal Desk Agent

We should keep eventual concepts clearly tied to these areas.

------------------------------------------------------------------------

# 7. Customer-service opportunity space

Customer service naturally fits an autonomous workflow:

``` text
Problem
 ↓
Investigation
 ↓
Decision
 ↓
Action
 ↓
Verification
```

This makes it especially suitable for a hackathon demo.

------------------------------------------------------------------------

# 8. Idea: Payment Resolution Teammate

### User

> "₹2,000 was deducted but my payment failed."

### Agent

``` text
Find transaction
 ↓
Check payment state
 ↓
Check reversal/refund state
 ↓
Determine resolution path
 ↓
Execute allowed action
 ↓
Verify
 ↓
Notify customer
```

### Outcome

**Payment issue resolved**, rather than merely explained.

This is a very direct interpretation of the track.

------------------------------------------------------------------------

# 9. Idea: Autonomous Refund Teammate

Customer:

> "I want a refund."

Agent:

1.  identifies transaction,
2.  checks eligibility,
3.  checks policy,
4.  determines allowed amount,
5.  initiates refund,
6.  verifies refund,
7.  notifies customer.

Example:

``` text
Transaction: ₹12,000
Eligibility: ALLOWED
Refund: INITIATED
Verification: COMPLETED
Outcome: RESOLVED
```

------------------------------------------------------------------------

# 10. Idea: Dispute Resolution Teammate

Customer:

> "I was charged twice."

Agent:

``` text
Find transactions
 ↓
Detect possible duplicate
 ↓
Check settlement
 ↓
Check policy
 ↓
Start dispute/refund
 ↓
Track
 ↓
Verify
```

This demonstrates multi-step reasoning and action.

------------------------------------------------------------------------

# 11. Idea: Merchant Support Teammate

Merchant:

> "My Soundbox is not working."

Agent:

1.  identifies merchant/device,
2.  checks device status,
3.  checks connectivity,
4.  runs diagnostics,
5.  provides troubleshooting,
6.  triggers service/replacement workflow,
7.  tracks it,
8.  escalates if necessary.

Outcome:

> Device issue resolved or correctly routed to a human.

------------------------------------------------------------------------

# 12. Idea: Merchant Onboarding Teammate

The AI owns:

``` text
Collect business information
 ↓
Validate
 ↓
Check documents
 ↓
Identify missing information
 ↓
Prepare onboarding
 ↓
Submit
 ↓
Track KYC/status
 ↓
Escalate exceptions
```

Outcome:

> Merchant successfully onboarded.

This has strong Paytm relevance.

------------------------------------------------------------------------

# 13. Idea: Application Resolution Teammate

User:

> "My application hasn't moved."

Agent:

``` text
Find application
 ↓
Determine state
 ↓
Identify blocker
 ↓
Explain blocker
 ↓
Take permitted action
 ↓
Track progress
```

Example:

``` text
Application: 72% complete
Blocker: income document missing
Action: request document
Upload
→ validate
→ attach
→ resubmit
→ verify
```

This overlaps with Track 2, but Track 3 focuses on **AI ownership of
resolution**.

------------------------------------------------------------------------

# 14. Idea: Proactive Support Teammate

Instead of waiting for customers:

``` text
System detects anomaly
 ↓
AI identifies affected customers
 ↓
AI classifies cases
 ↓
AI resolves eligible cases
 ↓
AI notifies customers
 ↓
AI escalates exceptions
```

Example:

``` text
Payment incident detected
 ↓
500 affected customers
 ↓
Agent finds failed-but-debited cases
 ↓
Starts safe resolution
 ↓
Notifies customers
```

This is a strong differentiation direction.

------------------------------------------------------------------------

# 15. Sales opportunity space

Sales also maps naturally to agentic execution:

``` text
Lead
 ↓
Research
 ↓
Qualify
 ↓
Understand need
 ↓
Outreach
 ↓
Handle objections
 ↓
Follow-up
 ↓
Meeting
 ↓
CRM update
```

------------------------------------------------------------------------

# 16. Idea: AI Sales Development Representative

Agent:

1.  receives lead,
2.  researches context,
3.  qualifies,
4.  creates personalized outreach,
5.  sends through approved channels,
6.  handles replies,
7.  books meeting,
8.  updates CRM,
9.  escalates qualified opportunities.

Outcome:

> Qualified meeting booked.

------------------------------------------------------------------------

# 17. Idea: Merchant Acquisition Teammate

Potential flow:

``` text
Potential merchant
 ↓
Research business
 ↓
Understand likely needs
 ↓
Personalized outreach
 ↓
Answer questions
 ↓
Collect information
 ↓
Book demo/onboarding
 ↓
Update CRM
```

Paytm's public materials already discuss AI-led merchant acquisition,
profiling and marketing, so this is strategically relevant.
citeturn0search29turn0search32

------------------------------------------------------------------------

# 18. Idea: AI Sales Follow-up Teammate

Sales opportunity:

``` text
Lead created
 ↓
Follow-up schedule
 ↓
Personalized message
 ↓
Response detection
 ↓
Objection handling
 ↓
Meeting booking
 ↓
CRM update
```

The agent's job is not "send lots of messages."

Its job is:

> **Move qualified opportunities to the next valid stage.**

------------------------------------------------------------------------

# 19. Idea: Lead Qualification Teammate

Agent:

``` text
Lead
 ↓
Ask missing questions
 ↓
Evaluate against defined criteria
 ↓
Qualify
 ↓
Update CRM
 ↓
Schedule human sales call
```

This is relatively easy to build but less ambitious than full end-to-end
sales ownership.

------------------------------------------------------------------------

# 20. Idea: AI Cross-sell Teammate

Agent uses:

-   merchant profile,
-   product usage,
-   transaction patterns,
-   defined eligibility criteria.

It identifies relevant opportunities, prepares outreach, answers
questions and routes qualified leads.

The AI should not invent eligibility or product claims.

------------------------------------------------------------------------

# 21. Core agent architecture

A strong general architecture is:

``` text
                 TASK / EVENT
                     ↓
                AI TEAMMATE
                     ↓
              CONTEXT ENGINE
                     ↓
               TASK PLANNER
                     ↓
              POLICY ENGINE
                     ↓
                 TOOL CALL
                     ↓
                 OBSERVE
                     ↓
               NEXT DECISION
                ↙          ↘
             ACTION       ESCALATE
                ↓             ↓
             VERIFY         HUMAN
                ↓
              RESULT
                ↓
              MEMORY
```

------------------------------------------------------------------------

# 22. Closed-loop vs open-loop AI

### Open loop

``` text
Customer:
“Refund this.”

AI:
“Please contact support.”
```

### Closed loop

``` text
Customer
 ↓
Find transaction
 ↓
Check policy
 ↓
Call refund API
 ↓
Read resulting state
 ↓
Confirm refund
 ↓
Notify customer
```

The second is what we should demonstrate.

------------------------------------------------------------------------

# 23. Verification is essential

Never assume an action succeeded merely because a tool returned an
accepted request.

Instead:

``` text
initiate_refund()
 ↓
get_refund_status()
 ↓
REFUND_COMPLETED
 ↓
customer notification
```

The agent's claim should be grounded in the authoritative backend state.

------------------------------------------------------------------------

# 24. Policy / Risk Engine

Do not give the LLM unrestricted authority.

Example:

``` text
AI proposes refund ₹12,000

Customer authenticated? YES
Transaction eligible? YES
Refund limit? YES
Already refunded? NO

→ ALLOW
```

For another case:

``` text
Refund amount: ₹90,000
Autonomous threshold: ₹25,000

→ ESCALATE
```

Critical business rules should be deterministic.

------------------------------------------------------------------------

# 25. Human escalation

A good escalation is not:

> "I don't know."

It is:

``` text
AI investigated
 ↓
Exception identified
 ↓
Actions attempted
 ↓
Evidence collected
 ↓
Case summarized
 ↓
Recommended next step
 ↓
Human takes over
```

Human receives:

``` text
Customer: Asha
Issue: duplicate ₹8,000 payment
Transactions: TX-X / TX-Y
Finding: probable duplicate debit
Actions attempted: automated refund unavailable
Recommendation: manual refund review
Evidence: transaction history + policy result
```

This reduces human effort.

------------------------------------------------------------------------

# 26. Agent tool design

The LLM should not have direct database access.

Use:

``` text
LLM
 ↓
Typed tool
 ↓
Backend validation
 ↓
API/database
```

Example tools:

``` text
get_customer()
get_transaction()
check_policy()
initiate_refund()
get_refund_status()
create_support_case()
update_crm()
send_message()
schedule_call()
```

Every action tool should validate authentication, authorization,
parameters, limits and idempotency.

------------------------------------------------------------------------

# 27. State machine

Use explicit workflow states.

Example:

``` text
NEW
 ↓
AUTHENTICATING
 ↓
INVESTIGATING
 ↓
ACTION_PLANNED
 ↓
POLICY_CHECK
 ↓
EXECUTING
 ↓
VERIFYING
 ↓
RESOLVED
```

Exception:

``` text
VERIFYING
 ↓
FAILED
 ↓
RETRY
 ↓
ESCALATE
```

This is safer than letting an LLM improvise the entire workflow.

------------------------------------------------------------------------

# 28. Memory

The teammate needs case-specific memory:

``` text
Case ID
Customer
Issue
Transaction
Actions
Current state
Evidence
Next step
```

For example:

``` text
CASE-1022
Customer: Asha
Issue: failed payment
Transaction: TX-8822
Action: refund initiated
State: awaiting verification
```

Authoritative transactional state should remain in the source system.

------------------------------------------------------------------------

# 29. n8n role

n8n can be used as the workflow/action layer:

``` text
AI Agent
 ↓
n8n
 ↓
Get transaction
 ↓
Check policy
 ↓
Refund
 ↓
Poll status
 ↓
Notify
 ↓
Log outcome
```

This also makes the workflow easy to show during the demo.

------------------------------------------------------------------------

# 30. Sarvam role

Voice and Indian-language interaction can make a customer-service
teammate more accessible.

Example:

> "Bhai, payment fail ho gaya aur paise kat gaye."

The AI understands the request and performs the same resolution
workflow.

The key principle:

> **Language is the interface; resolution is the product.**

A multilingual chatbot alone is not enough for Track 3.

------------------------------------------------------------------------

# 31. Cognee / knowledge role

A knowledge layer can provide:

-   previous cases,
-   customer preferences,
-   product knowledge,
-   support procedures,
-   merchant context.

But authoritative transactional state should stay in the backend.

------------------------------------------------------------------------

# 32. Multi-agent architecture

Possible design:

``` text
              Supervisor
                  |
       ┌──────────┼──────────┐
       ↓          ↓          ↓
Investigation  Action   Communication
   Agent        Agent       Agent
```

Use multiple agents only if separation genuinely improves the workflow.

For an 8-hour hackathon:

> **One excellent teammate is usually better than five superficial
> agents.**

------------------------------------------------------------------------

# 33. Strongest MVP direction

A very clean MVP is:

## Payment Resolution Teammate

Customer:

> "₹12,000 was deducted but my payment failed."

Agent:

``` text
Authenticate
 ↓
Find transaction
 ↓
Check payment state
 ↓
Check policy
 ↓
Choose resolution
 ↓
Execute
 ↓
Verify
 ↓
Resolve / Escalate
```

This demonstrates almost every phrase in the track.

------------------------------------------------------------------------

# 34. But there is a differentiation warning

Public GitHub repositories already show teams exploring Track 3
customer-resolution concepts, including autonomous
refund/customer-resolution teammates with typed tools, deterministic
policy gates and post-action verification.
citeturn0search0turn0search2

So:

> **"AI chatbot that refunds payments" is not enough as a differentiated
> idea.**

If we eventually choose this direction, we should add a meaningful
differentiator such as:

-   proactive resolution,
-   multi-system orchestration,
-   multilingual voice,
-   intelligent exception recovery,
-   merchant operations,
-   sales + service handoff,
-   or a distinctive measurable outcome.

------------------------------------------------------------------------

# 35. Alternative strong direction: Merchant Acquisition Teammate

Another strong Track 3 direction is:

``` text
Lead
 ↓
Research
 ↓
Qualify
 ↓
Personalized outreach
 ↓
Conversation
 ↓
Objection handling
 ↓
Meeting booking
 ↓
CRM update
```

Outcome:

> Qualified merchant meeting booked.

This connects well with Paytm's merchant ecosystem and current AI-led
acquisition/marketing direction. citeturn0search29turn0search32

------------------------------------------------------------------------

# 36. Proactive AI teammate

A more differentiated concept is:

> The teammate discovers work before a human asks.

Example:

``` text
Payment system
 ↓
Detects anomaly
 ↓
AI identifies affected customers
 ↓
Classifies safe cases
 ↓
Resolves eligible cases
 ↓
Notifies customers
 ↓
Escalates exceptions
```

This changes customer service from reactive to proactive.

------------------------------------------------------------------------

# 37. Agent observability

The demo should make the AI's work visible.

Example:

``` text
10:42:01  Task received
10:42:02  Customer authenticated ✓
10:42:02  Transaction retrieved ✓
10:42:03  Policy checked ✓
10:42:04  Refund initiated ✓
10:42:05  Status verified ✓
10:42:06  Customer notified ✓
```

This is much more convincing than a chat transcript.

------------------------------------------------------------------------

# 38. Ideal UI

Use three panels.

### Left --- Customer

Conversation.

### Center --- AI Teammate

``` text
Current task:
Resolving failed payment

Progress:
✓ Authentication
✓ Transaction lookup
✓ Policy check
→ Refund
○ Verification
```

### Right --- Agent Activity

``` text
get_transaction ✓
check_policy ✓
initiate_refund ✓
get_refund_status ✓
```

Final state:

``` text
OUTCOME
RESOLVED ✓
```

------------------------------------------------------------------------

# 39. Three-minute demo

## 0:00--0:20

Customer reports:

> "₹12,000 deducted but payment failed."

## 0:20--0:45

AI authenticates and retrieves the transaction.

## 0:45--1:15

AI checks policy and determines the safe resolution path.

## 1:15--1:45

AI executes the action.

## 1:45--2:00

AI verifies the outcome.

## 2:00--2:20

Customer receives the resolution.

## 2:20--2:40

Show an exception case:

> "This case exceeds autonomous authority."

Agent escalates with complete context.

## 2:40--3:00

Show prototype metrics:

``` text
Tasks received
Autonomously resolved
Escalated
Verified success
```

Clearly label simulated/demo metrics.

------------------------------------------------------------------------

# 40. 8-hour implementation plan

### Hour 0--1

Choose one task and define:

-   inputs
-   tools
-   states
-   policies
-   success condition
-   escalation condition

### Hour 1--2

Create synthetic backend:

``` text
customers
transactions
refunds
support_cases
policies
```

### Hour 2--3

Build typed tools.

### Hour 3--4

Build agent orchestration.

### Hour 4--5

Build policy engine.

### Hour 5--6

Build verification + escalation.

### Hour 6--7

Build UI and agent trace.

### Hour 7--8

Test success/failure paths and polish the demo.

------------------------------------------------------------------------

# 41. Metrics

## Customer service

-   first-contact resolution
-   average handling time
-   resolution time
-   escalation rate
-   automation rate
-   successful action rate
-   customer effort

## Sales

-   lead qualification rate
-   meeting-booking rate
-   response rate
-   time-to-first-contact
-   follow-up completion
-   CRM completeness

## Agent-specific

### Autonomous resolution rate

``` text
Tasks resolved without human intervention
-----------------------------------------
Eligible tasks
```

### Verified success rate

``` text
Verified successful outcomes
----------------------------
Actions attempted
```

The important point is that **outcome metrics matter more than response
volume**.

------------------------------------------------------------------------

# 42. What not to build

### Generic AI employee

Too vague.

### Unrestricted API agent

Unsafe and difficult to trust.

### Chatbot with a few fake tool calls

Does not demonstrate true ownership.

### Agent that claims success without verification

Weak technical credibility.

### "Multi-agent" for its own sake

Complexity without benefit.

### Voice bot as the entire innovation

Voice should improve the workflow, not replace it.

------------------------------------------------------------------------

# 43. Track 3 differentiation ladder

Think of the maturity levels as:

``` text
Level 1 — Chatbot
Level 2 — Tool-using chatbot
Level 3 — Task agent
Level 4 — Closed-loop autonomous agent
Level 5 — AI teammate + policy + verification + escalation
Level 6 — Proactive AI teammate
```

The track strongly points toward Levels 4--6.

------------------------------------------------------------------------

# 44. Track 3 candidate solution space

  \#   AI Teammate                       Primary outcome
  ---- --------------------------------- --------------------------------
  1    Payment Resolution Teammate       Failed-payment resolution
  2    Refund Teammate                   Verified refund
  3    Dispute Teammate                  Dispute resolution
  4    Merchant Support Teammate         Support resolution
  5    Merchant Onboarding Teammate      Merchant activation
  6    Application Resolution Teammate   Application completion
  7    Proactive Support Teammate        Issues resolved before contact
  8    Merchant Acquisition Teammate     Qualified merchant leads
  9    Sales Development Teammate        Qualified meetings
  10   Sales Follow-up Teammate          Follow-up/meeting completion
  11   Lead Qualification Teammate       Qualified leads
  12   Cross-sell Teammate               Qualified opportunities
  13   Deal Desk Teammate                Sales workflow completion

These are product directions, not organizer-provided rankings.

------------------------------------------------------------------------

# 45. Track 3 vs Track 1

## Track 1

**Primary user:** Paytm merchant

**AI role:** business partner

**Outcome:** growth, operations, customer service

## Track 3

**Primary user/workflow:** customer service or sales team

**AI role:** autonomous teammate

**Outcome:** completion of a defined task

The overlap is real, but Track 3 has a stronger requirement for **task
ownership and execution**.

------------------------------------------------------------------------

# 46. Track 3 vs Track 2

## Track 2

> Make a financial journey simpler, faster and more human.

Example:

``` text
User wants insurance claim
→ AI simplifies and orchestrates the journey.
```

## Track 3

> Make an AI teammate own a task.

Example:

``` text
Customer issue
→ AI investigates, acts, verifies and resolves.
```

The distinction is subtle but important.

------------------------------------------------------------------------

# 47. Track 3 shortlist for final comparison

Carry these forward:

### Customer service

1.  **Payment Resolution Teammate**
2.  **Refund Resolution Teammate**
3.  **Proactive Customer Resolution Teammate**
4.  **Merchant Support Teammate**
5.  **Merchant Onboarding Teammate**

### Sales

6.  **Merchant Acquisition Teammate**
7.  **AI Sales Development Representative**
8.  **Sales Follow-up Teammate**
9.  **Lead Qualification Teammate**
10. **AI Cross-sell Teammate**

------------------------------------------------------------------------

# 48. Final Takeaway

Track 3 asks:

> **Can you build an AI worker that owns a real business task instead of
> merely producing a response?**

The strongest mental model is:

``` text
UNDERSTAND
    ↓
DECIDE
    ↓
ACT
    ↓
VERIFY
    ↓
RESOLVE
```

with:

``` text
Outside authority?
       ↓
   ESCALATE
       ↓
     HUMAN
```

A strong Track 3 MVP should therefore have:

-   one clearly defined job,
-   real tool usage,
-   multi-step execution,
-   deterministic policy controls,
-   verification,
-   intelligent escalation,
-   visible agent trace,
-   measurable outcome.

------------------------------------------------------------------------

# 49. Current research context

Paytm's public FY2026 materials describe AI across merchant and consumer
journeys and include agentic/AI-driven operational capabilities.
citeturn0search29turn0search8

Paytm has also publicly described a broader agentic-AI direction across
sales, service, operations and analytics.
citeturn0search1turn0search5turn0search13

Public examples of Track 3 hackathon work already include autonomous
customer-resolution concepts, so differentiation should be considered
before committing to a generic refund/support agent.
citeturn0search0turn0search2

------------------------------------------------------------------------

# 50. Next Step

We now have the **three exact organizer-provided tracks**.

The next document should be a cross-track strategy analysis comparing
the strongest concepts from all three on:

1.  Problem depth
2.  Paytm strategic fit
3.  AI necessity
4.  Agentic potential
5.  Differentiation
6.  Data availability
7.  API/tool requirements
8.  8-hour feasibility
9.  Demo impact
10. Measurable outcome
11. Technical risk
12. Competition/obviousness
13. Scalability
14. n8n usage potential
15. Sarvam usage potential
16. Cognee usage potential
17. Pitch strength

**Only after that comparison should we select the track.**
