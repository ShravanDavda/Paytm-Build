# Paytm Build for India AI Hackathon --- Track 2 Analysis

## AI-Powered Financial Journeys

> **Exact track statement from the supplied hackathon screenshot:**\
> **"Make Insurance, Lending and Fintech simpler, faster and more
> human."**
>
> The track asks teams to reimagine customer-facing journeys across
> **Insurance, Lending and Fintech** using AI, with emphasis on removing
> friction, reducing complexity, and helping customers complete
> important financial journeys faster and with greater confidence.
>
> The organizer's example is a **health-insurance claims journey**
> covering policy understanding, document submission, claim tracking and
> customer queries.

------------------------------------------------------------------------

# 1. Executive Summary

Track 2 is fundamentally a **journey-design problem**, not simply a
financial chatbot problem.

The user may already have a financial need:

-   "I need money."
-   "Can I claim this expense?"
-   "What does my insurance cover?"
-   "Why is my loan application stuck?"
-   "Which financial product fits my situation?"
-   "What documents do I need?"
-   "What happens next?"

The problem is that financial journeys often involve:

``` text
Intent
  ↓
Product discovery
  ↓
Eligibility / coverage understanding
  ↓
Comparison
  ↓
Data entry
  ↓
Documents
  ↓
Verification
  ↓
Application / claim
  ↓
Status tracking
  ↓
Queries / corrections
  ↓
Decision
  ↓
Follow-up
```

A strong AI solution compresses this journey.

The ideal product pattern is:

``` text
User intent
    ↓
AI understands context
    ↓
AI determines journey
    ↓
AI gathers missing information
    ↓
AI explains options / requirements
    ↓
AI prepares documents / forms
    ↓
AI executes permitted steps
    ↓
AI tracks progress
    ↓
AI handles exceptions
    ↓
User gets a clear outcome
```

### The central insight

> **Don't build "AI that explains financial products." Build "AI that
> helps the customer finish a financial task."**

That distinction is extremely important for this track.

------------------------------------------------------------------------

# 2. What the Track Actually Asks

The screenshot gives four major signals.

## Signal 1 --- "Simpler"

Financial products can contain:

-   policy terminology
-   eligibility rules
-   exclusions
-   fees
-   interest
-   documentation requirements
-   multiple steps
-   multiple stakeholders

AI should translate complexity into understandable next steps.

------------------------------------------------------------------------

## Signal 2 --- "Faster"

AI should reduce:

-   form filling
-   document searching
-   repeated questions
-   manual status checking
-   support interactions
-   unnecessary back-and-forth

------------------------------------------------------------------------

## Signal 3 --- "More human"

This does not necessarily mean adding a friendly chatbot.

It means:

-   understand user intent,
-   remember context,
-   communicate naturally,
-   explain decisions,
-   recognize confusion,
-   guide the user through difficult moments.

------------------------------------------------------------------------

## Signal 4 --- "Complete critical financial journeys"

This is probably the most important phrase.

The product should have a measurable **journey completion**.

Examples:

``` text
Claim submitted
Loan application completed
Insurance purchased
Document correction completed
Financial product selected
Application resumed
```

The outcome should not merely be:

> "User had a conversation."

The outcome should be:

> "User successfully completed the task."

------------------------------------------------------------------------

# 3. Why Paytm Is a Natural Platform

Paytm already operates at the intersection of payments and consumer
financial services.

Its current consumer offering includes financial products such as
personal loans and access to multiple lending partners. Paytm's current
personal-loan page describes a digital journey involving eligibility,
amount/tenure selection, KYC, e-signing, lender partners and
application-status tracking. citeturn0search1turn0search2

That makes the track naturally compatible with an AI journey layer.

The opportunity is not necessarily to invent another financial product.

It is to make the **existing product journey easier to navigate and
complete**.

------------------------------------------------------------------------

# 4. The Fundamental User Problem

Consider a user who says:

> "Mujhe ₹2 lakh chahiye business expand karne ke liye."

They may not know:

-   which loan type is appropriate,
-   whether they qualify,
-   which documents are needed,
-   what EMI they can afford,
-   which offer is relevant,
-   what the interest/fees mean,
-   what happens after applying.

A traditional interface might respond:

``` text
Loans → Personal Loan → Enter Details → Check Eligibility
```

An AI journey could instead do:

``` text
User:
“Mujhe ₹2 lakh chahiye business ke liye.”

AI:
“Samajh gaya. Main aapko suitable financing journey
samajhne mein help karta hoon.”

→ asks only necessary questions

→ identifies required information

→ explains available options

→ shows relevant terms

→ prepares application

→ tracks application

→ handles next steps
```

The AI becomes a **journey orchestrator**.

------------------------------------------------------------------------

# 5. Three Major Domains

The track explicitly covers:

1.  Insurance
2.  Lending
3.  Fintech

Each has different opportunities.

------------------------------------------------------------------------

# 6. Domain A --- Insurance

Insurance is particularly interesting because the track's own example is
a health-insurance claim journey.

## Typical insurance journey

``` text
Need insurance
    ↓
Understand products
    ↓
Compare coverage
    ↓
Purchase
    ↓
Policy management
    ↓
Claim
    ↓
Documents
    ↓
Claim tracking
    ↓
Queries
    ↓
Settlement / rejection
```

Every stage can have friction.

------------------------------------------------------------------------

# 7. Insurance Opportunity 1 --- AI Claims Assistant

This is the most direct interpretation of the organizer's example.

### User says:

> "Hospital ka bill hai, insurance mein claim ho sakta hai?"

AI can:

1.  Identify the policy
2.  Read relevant policy terms
3.  Explain coverage
4.  Identify likely requirements
5.  Ask for missing information
6.  Read uploaded documents
7.  Prepare claim information
8.  Submit through the permitted workflow
9.  Track status
10. Explain insurer queries
11. Tell the customer what to do next

### Example

``` text
USER
“I was hospitalized for 3 days.
Can I claim this?”

        ↓

AI

Policy found:
Health Plan A

Relevant coverage:
Hospitalization expenses

Potential issue:
The policy has a waiting-period clause
for certain conditions.

Next:
Upload discharge summary + final bill.
```

The AI should distinguish between:

-   **what the policy explicitly says**
-   **what is uncertain**
-   **what still needs insurer/TPA confirmation**

It should never invent coverage.

------------------------------------------------------------------------

# 8. Insurance Opportunity 2 --- Policy Explainer

Users often receive long policy documents.

AI can answer:

> "What exactly am I covered for?"

> "What is not covered?"

> "How much is my deductible?"

> "Do I need pre-authorization?"

> "What documents are required?"

The important technical component is **document-grounded generation**.

Architecture:

``` text
Policy PDF
    ↓
Document parser
    ↓
Chunking
    ↓
Embeddings / retrieval
    ↓
Relevant clauses
    ↓
LLM
    ↓
Answer + source clause
```

The answer should cite the relevant policy section in the UI.

------------------------------------------------------------------------

# 9. Insurance Opportunity 3 --- Claim Document Copilot

Users upload:

-   discharge summary
-   bills
-   prescriptions
-   ID
-   policy documents
-   diagnostic reports

AI:

``` text
Document
    ↓
OCR / extraction
    ↓
Classification
    ↓
Field extraction
    ↓
Validation
    ↓
Missing-document detection
```

Example:

> "I found 7 documents. Five are sufficient for the current step. The
> claim form and final discharge summary are still missing."

This directly reduces friction.

------------------------------------------------------------------------

# 10. Insurance Opportunity 4 --- Claim Status Agent

Instead of:

> "Your claim is under process."

AI explains:

``` text
Claim status:
Medical review

What happened:
Documents were received.

What's next:
The insurer is reviewing the claim.

Action required:
No action currently.

Next expected milestone:
Medical review completion.
```

The important improvement is **context + next action**, not merely
status.

------------------------------------------------------------------------

# 11. Insurance Opportunity 5 --- Claim Exception Agent

This can be more interesting.

Suppose the insurer requests:

> "Please provide additional hospital documentation."

Instead of forwarding a generic message, AI:

1.  Understands the request
2.  Explains it
3.  Checks existing documents
4.  Identifies exactly what is missing
5.  Helps the user obtain it
6.  Resubmits it

This transforms support into a **resolution workflow**.

------------------------------------------------------------------------

# 12. Insurance Regulatory Consideration

This domain needs strong guardrails.

IRDAI's published health-insurance guidance states that insurers/TPAs
should call for necessary claim documents in a non-piece-meal manner and
that claim decisions are governed by policy terms and applicable
regulations. citeturn0search0

This means an AI product should not casually invent document
requirements.

A safer architecture is:

``` text
Policy / insurer rules
        ↓
Grounded retrieval
        ↓
AI explanation
        ↓
Action
```

not:

``` text
LLM memory
    ↓
Claim advice
```

------------------------------------------------------------------------

# 13. Domain B --- Lending

Lending has a different journey.

``` text
Need money
    ↓
Discover loan
    ↓
Eligibility
    ↓
Offer
    ↓
Compare
    ↓
Application
    ↓
KYC
    ↓
Documents
    ↓
Verification
    ↓
Approval
    ↓
Agreement
    ↓
Disbursal
    ↓
Repayment
```

This creates many opportunities for AI.

------------------------------------------------------------------------

# 14. Lending Opportunity 1 --- AI Loan Navigator

User:

> "Mujhe ₹2 lakh chahiye. Kaunsa loan lena chahiye?"

AI can:

1.  Understand the need
2.  Ask relevant questions
3.  Identify candidate products
4.  Explain eligibility
5.  Explain costs
6.  Compare available offers
7.  Guide the application

This is better than forcing the user to understand the product catalogue
first.

------------------------------------------------------------------------

# 15. Lending Opportunity 2 --- Eligibility Explainer

Users often ask:

> "Loan kyun nahi mila?"

Instead of a generic error:

> "Not eligible."

AI can explain the **available reason codes or verified facts**.

Example:

``` text
Application status:
Not approved

Available reason:
Current eligibility criteria were not met.

What you can do:
Review the following information...
```

The system should not invent hidden underwriting reasons.

If a lender does not expose a reason, the AI must say that it does not
have that information.

------------------------------------------------------------------------

# 16. Lending Opportunity 3 --- Loan Application Copilot

The agent guides the user through the complete application.

``` text
AI
 ↓
Collect information
 ↓
Validate
 ↓
Identify missing fields
 ↓
Prepare application
 ↓
KYC
 ↓
e-sign
 ↓
Submit
 ↓
Track
```

The user should not have to remember where they left off.

------------------------------------------------------------------------

# 17. Lending Opportunity 4 --- Document Copilot

For self-employed users especially, documentation can be difficult.

AI can:

-   classify documents,
-   extract fields,
-   identify missing pages,
-   detect inconsistent information,
-   explain what is needed next.

Example:

> "Your bank statement is uploaded, but the required period is
> incomplete. Please upload the remaining two months."

Again, this should be based on actual lender workflow requirements.

------------------------------------------------------------------------

# 18. Lending Opportunity 5 --- Loan Comparison Explainer

Instead of showing:

  Lender     Rate   Tenure   Fee
  -------- ------ -------- -----
  A             X        Y     Z
  B             X        Y     Z

AI explains:

> "At the same loan amount and tenure, Offer A has a lower nominal rate
> but a higher processing fee. The estimated total repayment difference
> is ₹X based on the displayed terms."

This is a **decision-support** use case.

The system should show the underlying numbers rather than making an
unsupported claim that one product is "best."

------------------------------------------------------------------------

# 19. Lending Opportunity 6 --- Application Recovery Agent

This is a strong agentic opportunity.

Suppose:

``` text
User started loan application
        ↓
Completed 70%
        ↓
Stopped
```

The AI knows:

-   where the application stopped,
-   what is missing,
-   what documents were already submitted,
-   what the next step is.

The user returns later:

> "Where was I?"

AI:

> "You completed KYC and income details. The remaining step is
> bank-account verification."

This reduces journey abandonment.

------------------------------------------------------------------------

# 20. Domain C --- Fintech

Fintech is broader.

Possible journeys include:

-   payments
-   bill payments
-   credit cards
-   investment-like products where applicable
-   financial planning
-   account/service management
-   transaction disputes
-   refunds
-   payment failures
-   recurring payments
-   merchant/user financial tools

The important principle is:

> Pick a **journey**, not a category.

------------------------------------------------------------------------

# 21. Fintech Opportunity 1 --- Transaction Resolution Agent

User:

> "Payment failed but money got deducted."

Instead of:

``` text
Payment failed.
Contact support.
```

AI:

1.  Finds the transaction
2.  Determines current status
3.  Explains the state
4.  Tells the user what happens next
5.  Initiates the correct workflow if permitted
6.  Tracks resolution

Example:

``` text
₹1,500 payment

Status:
Failed

Settlement status:
Reversal pending

What this means:
The payment did not complete.

Next:
No action required right now.

I'll track the reversal status.
```

This is a strong example of reducing support friction.

------------------------------------------------------------------------

# 22. Fintech Opportunity 2 --- Financial Task Agent

User:

> "Mera monthly financial kaam sort kar do."

The AI could identify pending tasks:

``` text
3 bills due
1 failed autopay
2 recurring payments
1 pending refund
```

Then:

> "I found four items that need attention."

The user can resolve them one by one.

------------------------------------------------------------------------

# 23. Fintech Opportunity 3 --- Financial Health Navigator

The AI helps users understand their financial activity.

Example:

> "Where did most of my money go this month?"

AI:

``` text
Food             ₹8,400
Travel           ₹5,200
Utilities        ₹4,100
Shopping         ₹3,700
```

Then:

> "Your utility spending increased 23% compared with your recent
> baseline."

This can become a broader financial-management journey.

However, avoid making unsupported financial predictions or presenting
personalized financial recommendations as guaranteed outcomes.

------------------------------------------------------------------------

# 24. Fintech Opportunity 4 --- Bill / Payment Assistant

User:

> "What bills do I need to pay this week?"

AI:

``` text
Electricity     ₹1,840   Due Friday
Mobile            ₹599   Due Sunday
Broadband         ₹799   Due Tuesday
```

Then the user can authorize payment actions.

This becomes:

``` text
Understand
 → Prepare
 → Confirm
 → Execute
 → Verify
```

------------------------------------------------------------------------

# 25. The Strongest Product Pattern

Across insurance, lending and fintech, the same architecture appears:

``` text
                 USER INTENT
                     ↓
             Context Understanding
                     ↓
              Journey Detection
                     ↓
             Missing Information
                     ↓
              Decision Support
                     ↓
              Document / Data AI
                     ↓
                Tool Actions
                     ↓
               Status Tracking
                     ↓
             Exception Handling
                     ↓
                 Completion
```

This is the **Financial Journey Agent** pattern.

------------------------------------------------------------------------

# 26. The Difference Between a Chatbot and a Journey Agent

## Chatbot

User:

> "What documents do I need?"

AI:

> "You need A, B and C."

Conversation ends.

------------------------------------------------------------------------

## Journey Agent

User:

> "I want to claim my insurance."

AI:

``` text
1. Finds policy
2. Checks relevant coverage
3. Explains likely requirements
4. Collects documents
5. Detects missing documents
6. Prepares claim
7. Submits through permitted API
8. Tracks claim
9. Explains insurer queries
10. Helps resolve exceptions
```

This is much closer to the track.

------------------------------------------------------------------------

# 27. Candidate Product Directions

## Idea 1 --- AI Insurance Claims Agent

### Journey

``` text
Policy
 ↓
Coverage
 ↓
Claim
 ↓
Documents
 ↓
Submission
 ↓
Tracking
 ↓
Resolution
```

### Strength

Directly aligned with the organizer's example.

### Challenge

Insurance integrations and realistic claim processing can be difficult
to simulate credibly.

------------------------------------------------------------------------

# 28. Idea 2 --- Universal Financial Journey Agent

One AI interface for:

``` text
Insurance
Lending
Fintech
```

User simply states the goal.

Example:

> "I need financial help after a hospital bill."

The agent determines whether the journey involves:

-   insurance claim,
-   financing,
-   payment,
-   reimbursement,
-   or support.

### Strength

Very strong vision.

### Risk

Too broad for an 8-hour build.

------------------------------------------------------------------------

# 29. Idea 3 --- AI Loan Application Agent

The AI completes a loan journey.

### Flow

``` text
Need
 ↓
Eligibility
 ↓
Offer
 ↓
Comparison
 ↓
Documents
 ↓
KYC
 ↓
Application
 ↓
Tracking
```

### Strength

Very demoable.

Paytm already publicly describes digital lending flows involving
eligibility, loan selection, KYC, e-sign and application tracking.
citeturn0search1turn0search2

------------------------------------------------------------------------

# 30. Idea 4 --- AI Loan Application Recovery Agent

Focus specifically on abandoned applications.

### Example

``` text
Application:
72% complete

Missing:
Income verification

AI:
“You stopped at income verification.
Would you like me to continue?”
```

The agent resumes the workflow.

### Why interesting

The problem is narrow enough for an MVP while still demonstrating
agentic behavior.

------------------------------------------------------------------------

# 31. Idea 5 --- AI Insurance Policy + Claims Navigator

A user uploads a policy.

AI creates:

``` text
Coverage summary
Important exclusions
Claim requirements
Key dates
How to claim
Current claim status
```

Then the user can say:

> "I want to claim for this hospital visit."

The AI starts the claim journey.

### Strength

Very close to the organizer's example.

------------------------------------------------------------------------

# 32. Idea 6 --- AI Document-to-Financial-Journey Agent

This is an interesting horizontal solution.

User uploads documents.

AI identifies:

``` text
Document types
Relevant financial context
Missing information
Possible next journey
```

For example:

``` text
Hospital bill
Discharge summary
Insurance policy
```

AI:

> "These documents appear related to a health-insurance claim. I can
> help you check the policy coverage and prepare the claim."

This turns documents into an actionable journey.

------------------------------------------------------------------------

# 33. Idea 7 --- Financial Application Concierge

A single assistant handles the user's application lifecycle.

``` text
“Where is my application?”

        ↓

AI finds it

        ↓

“What's pending?”

        ↓

AI identifies blocker

        ↓

“Fix it.”

        ↓

AI prepares next action
```

This could work across:

-   loans
-   insurance
-   financial services

------------------------------------------------------------------------

# 34. Idea 8 --- AI Financial Support Resolution Agent

Rather than generic customer support, focus on resolution.

Example:

> "My loan EMI was deducted twice."

AI:

1.  Finds transactions
2.  Identifies duplicate
3.  Checks status
4.  Creates dispute/refund workflow
5.  Tracks resolution

Another:

> "My insurance claim is asking for a document."

AI:

1.  Reads insurer request
2.  Explains it
3.  Checks uploaded documents
4.  Identifies missing item
5.  Helps submit it

This can be extremely practical.

------------------------------------------------------------------------

# 35. Idea 9 --- AI Financial Translator

This is more than translation between languages.

It translates:

``` text
Financial jargon
       ↓
Simple explanation
       ↓
Personal context
       ↓
Action
```

Example:

> "What does deductible mean?"

AI:

> "If your policy has a ₹10,000 deductible, you generally pay the
> covered eligible expense up to that amount before the insurer pays
> according to the policy terms."

Then:

> "For your current policy, the relevant deductible is ₹X according to
> section Y."

This is useful but weaker if it stops at explanation.

------------------------------------------------------------------------

# 36. Idea 10 --- Financial Journey Memory

The AI remembers the user's current financial processes.

Example:

``` text
Active journeys
-------------------------
Loan application     72%
Insurance claim      Awaiting document
Refund               Processing
Credit-card request  KYC pending
```

User:

> "What do I need to do today?"

AI:

> "Two financial tasks need your attention."

This makes the assistant feel persistent rather than stateless.

------------------------------------------------------------------------

# 37. A Potential Killer Concept

## "My Financial Journey"

Instead of organizing the app around products:

``` text
Loans
Insurance
Payments
Cards
```

organize around **user goals**:

``` text
I need money
I need protection
I need to claim
I need to resolve a payment
I need to complete my application
I need to understand my finances
```

AI determines which financial workflow is relevant.

This is a very important product-design shift:

### Traditional

``` text
PRODUCT → USER FIGURES OUT JOURNEY
```

### AI-native

``` text
USER GOAL → AI FIGURES OUT JOURNEY
```

That is one of the strongest conceptual directions inside this track.

------------------------------------------------------------------------

# 38. Recommended Architecture

``` text
                     User
                      ↓
               Chat / Voice UI
                      ↓
               Intent Agent
                      ↓
             Journey Orchestrator
                      ↓
        ┌─────────────┼─────────────┐
        ↓             ↓             ↓
    Insurance       Lending       Fintech
      Agent          Agent          Agent
        ↓             ↓             ↓
    Policy DB      Loan DB       Transaction DB
    Claims API     Lender API    Payment API
        ↓             ↓             ↓
        └─────────────┼─────────────┘
                      ↓
                 Tool Gateway
                      ↓
              Policy / Guardrails
                      ↓
                 User Approval
                      ↓
                 Execution
                      ↓
                Status Tracker
                      ↓
                  Completion
```

------------------------------------------------------------------------

# 39. AI Components

## 39.1 Intent Agent

Determines:

``` text
“What is the user actually trying to accomplish?”
```

Example:

> "Hospital mein 2 lakh kharch hua."

Possible intents:

-   insurance claim
-   reimbursement question
-   loan requirement
-   payment dispute

The agent should ask clarifying questions when necessary.

------------------------------------------------------------------------

# 40. 39.2 Journey Planner

Once intent is identified:

``` text
Goal:
Submit health insurance claim

Plan:
1. Identify policy
2. Check coverage
3. Collect required documents
4. Validate documents
5. Prepare claim
6. Submit
7. Track
```

This is where agentic planning becomes useful.

------------------------------------------------------------------------

# 41. 39.3 Document Intelligence

Use deterministic extraction wherever possible.

``` text
PDF/Image
   ↓
OCR
   ↓
Document classification
   ↓
Field extraction
   ↓
Validation
   ↓
LLM explanation
```

The LLM should not be the only validation layer.

------------------------------------------------------------------------

# 42. 39.4 Retrieval-Augmented Generation

For financial documents:

``` text
Policy / loan terms
       ↓
Chunk
       ↓
Index
       ↓
Retrieve relevant clauses
       ↓
LLM
       ↓
Answer + evidence
```

Every important financial explanation should ideally show:

> **Source: Policy document, Section X**

This reduces hallucination risk.

------------------------------------------------------------------------

# 43. 39.5 Tool Calling

Example tools:

``` text
get_user_profile()
get_policy()
search_policy_terms()
get_claim_status()
upload_claim_document()
submit_claim()
get_loan_offers()
get_application_status()
get_transaction()
create_dispute()
get_pending_tasks()
```

The LLM should call these tools through a controlled interface.

------------------------------------------------------------------------

# 44. 39.6 Status Engine

A major part of financial journeys is status.

Build a normalized state model:

``` text
NOT_STARTED
↓
IN_PROGRESS
↓
ACTION_REQUIRED
↓
SUBMITTED
↓
UNDER_REVIEW
↓
APPROVED / REJECTED / RESOLVED
```

The AI translates this machine state into human language.

------------------------------------------------------------------------

# 45. Guardrails

This track needs stronger guardrails than Track 1.

## Rule 1 --- Never invent financial terms

Every claim about:

-   coverage
-   interest
-   fees
-   eligibility
-   policy conditions
-   deadlines

must come from authoritative data.

------------------------------------------------------------------------

## Rule 2 --- Separate information from decision

Example:

``` text
Verified:
“Your displayed offer has an interest rate of X.”

Not acceptable:
“This is definitely the right loan for you.”
```

------------------------------------------------------------------------

## Rule 3 --- User confirmation

Require explicit confirmation for:

-   submitting an application
-   purchasing insurance
-   accepting loan terms
-   making payments
-   filing claims
-   sharing sensitive documents

------------------------------------------------------------------------

## Rule 4 --- Sensitive data minimization

Don't send more data to an LLM than necessary.

Use:

``` text
PII vault
   ↓
Tokenized identifiers
   ↓
AI system
```

where possible.

------------------------------------------------------------------------

# 46. Regulatory / Trust Considerations

Financial journeys involve regulated entities and sensitive personal
information.

The product should be designed so the AI is an **interface and
orchestration layer**, while authoritative decisions remain with the
appropriate regulated system/entity.

For insurance, IRDAI's published material emphasizes that claims are
governed by the policy contract and applicable regulations, and its
published 2024 consolidated regulations include protections concerning
policyholder interests. citeturn0search0turn0search3

For lending, Paytm's current public loan journey explicitly identifies
lender partners and states that eligibility/terms depend on the user's
profile and the lending partner's terms.
citeturn0search1turn0search2

Therefore, the hackathon prototype should not pretend that an LLM itself
is the underwriter, insurer, lender, or final decision-maker.

------------------------------------------------------------------------

# 47. Data Strategy for the Hackathon

Real financial data may not be available.

Create a controlled synthetic environment.

## Example user

``` json
{
  "user_id": "U001",
  "name": "Asha",
  "city": "Mumbai",
  "language": "Hindi"
}
```

## Example policy

``` json
{
  "policy_id": "POL1001",
  "type": "health",
  "sum_insured": 500000,
  "deductible": 10000,
  "waiting_period": "...",
  "documents_required": [
    "discharge_summary",
    "final_bill",
    "claim_form"
  ]
}
```

## Example claim

``` json
{
  "claim_id": "CLM1001",
  "status": "ACTION_REQUIRED",
  "missing_documents": [
    "final_bill"
  ]
}
```

## Example loan application

``` json
{
  "application_id": "L1001",
  "status": "DOCUMENT_PENDING",
  "completed_percent": 72,
  "pending": "income_verification"
}
```

------------------------------------------------------------------------

# 48. Strong Demo Scenario --- Insurance

## Opening

User:

> "Mere hospital ka claim karna hai."

AI:

> "Sure. I found your active health policy. I'll first check what the
> policy says about hospitalization claims."

### Step 1

AI retrieves policy.

### Step 2

Shows:

``` text
Hospitalization:
Covered subject to policy terms

Deductible:
₹10,000

Required documents:
✓ Discharge summary
✓ ID
✗ Final hospital bill
```

### Step 3

AI:

> "One document is missing. Please upload the final bill."

### Step 4

User uploads it.

AI validates.

### Step 5

AI:

> "The required documents are now present. Would you like me to prepare
> the claim?"

### Step 6

User:

> "Yes."

### Step 7

Agent prepares/submits through simulated API.

### Step 8

Dashboard:

``` text
Claim submitted

Status:
Under review

Next:
No action required
```

This is a complete journey.

------------------------------------------------------------------------

# 49. Strong Demo Scenario --- Lending

User:

> "Mujhe ₹2 lakh chahiye."

AI:

> "What is the purpose?"

User:

> "Business expansion."

AI:

``` text
I found a financing journey that may fit
your stated need.

To continue I need:
✓ basic profile
✓ income information
✓ required KYC
```

Then:

``` text
Offer A
Amount: ₹2L
Rate: X
Tenure: Y
Fee: Z

Offer B
Amount: ₹2L
Rate: X
Tenure: Y
Fee: Z
```

AI explains the numerical differences.

User selects an option.

Agent continues the application.

------------------------------------------------------------------------

# 50. Strong Demo Scenario --- Fintech

User:

> "₹3,000 payment fail hua but account se paise kat gaye."

AI:

1.  Finds transaction.
2.  Checks transaction state.
3.  Explains it.
4.  Starts/records resolution workflow.
5.  Tracks the reversal.

UI:

``` text
Transaction
₹3,000

Status:
Failed

Amount:
Debited

Resolution:
Reversal pending

Action:
No action required

[Track resolution]
```

This is highly understandable in a demo.

------------------------------------------------------------------------

# 51. Three Strong MVP Candidates

After exploring the track, the most practical directions to carry
forward are:

## Candidate A --- AI Insurance Claims Agent

Focus:

> Policy → Documents → Claim → Tracking → Resolution

------------------------------------------------------------------------

## Candidate B --- AI Financial Application Agent

Focus:

> Intent → Eligibility → Documents → Application → Tracking → Completion

This can be demonstrated using a lending journey.

------------------------------------------------------------------------

## Candidate C --- Universal Financial Journey Agent

Focus:

> User goal → AI determines the correct financial journey → executes it.

This is the biggest vision, but also the highest scope.

------------------------------------------------------------------------

# 52. Narrow vs Broad Strategy

## Broad product

``` text
Insurance
+
Lending
+
Payments
+
Financial planning
```

### Advantage

Huge vision.

### Disadvantage

Likely shallow in an 8-hour hackathon.

------------------------------------------------------------------------

## Narrow product

``` text
Health insurance claim
```

### Advantage

Can build a polished end-to-end experience.

### Disadvantage

May appear less ambitious unless the underlying architecture clearly
generalizes.

------------------------------------------------------------------------

## Best compromise

Build:

> **One complete journey + reusable journey engine.**

For example:

``` text
Demo:
Health insurance claim

Underlying engine:
Intent
→ Plan
→ Documents
→ Tools
→ Approval
→ Status
→ Resolution
```

Then show:

> "The same engine can power lending and fintech journeys."

------------------------------------------------------------------------

# 53. Metrics

The track naturally supports strong metrics.

## Journey metrics

-   completion rate
-   abandonment rate
-   time to completion
-   number of steps
-   number of user interactions

## Support metrics

-   support contacts avoided
-   repeated questions reduced
-   resolution time

## Document metrics

-   documents correctly identified
-   missing-document detection
-   manual data entry reduced

## AI metrics

-   successful tool calls
-   correct intent classification
-   grounded-answer rate
-   human intervention rate

------------------------------------------------------------------------

# 54. Before / After Demo Metric

A powerful UI can show:

### Traditional journey

``` text
12 steps
8 document interactions
4 support questions
~30 minutes
```

### AI-assisted journey

``` text
5 guided steps
1 document interaction
0 repeated questions
~8 minutes
```

If these numbers are simulated, clearly label them as **prototype
estimates/simulated benchmark**, not production measurements.

------------------------------------------------------------------------

# 55. What Not to Build

## Don't build only a financial chatbot

``` text
User:
“What is deductible?”

AI:
“Deductible means...”
```

Useful, but insufficient.

------------------------------------------------------------------------

## Don't build only OCR

Document extraction is a component, not the whole product.

------------------------------------------------------------------------

## Don't build only a dashboard

The track is about journeys.

------------------------------------------------------------------------

## Don't make the LLM the financial decision-maker

Use authoritative rules, APIs and lender/insurer decisions.

------------------------------------------------------------------------

## Don't overclaim automation

If your prototype is simulated:

> "Claim submitted to simulated insurer API"

is more credible than:

> "We built real insurance claim processing."

------------------------------------------------------------------------

# 56. 8-Hour Hackathon Architecture

A realistic stack:

``` text
Frontend
React / Next.js

Backend
FastAPI

Database
PostgreSQL / SQLite

AI
LLM + structured tool calling

Document AI
OCR + parser

Knowledge
Vector DB / retrieval

Workflow
n8n

Language
Sarvam where useful

Memory
Cognee / retrieval layer where useful
```

The exact technology should depend on what the organizers provide.

------------------------------------------------------------------------

# 57. 8-Hour Build Plan

## Hour 0--1

Define:

-   one journey
-   one persona
-   five states
-   five tools
-   synthetic dataset

------------------------------------------------------------------------

## Hour 1--2

Build:

-   database
-   APIs
-   journey state machine

------------------------------------------------------------------------

## Hour 2--4

Build:

-   agent
-   retrieval
-   tool calling
-   document processing

------------------------------------------------------------------------

## Hour 4--6

Build:

-   frontend
-   timeline
-   document upload
-   AI chat

------------------------------------------------------------------------

## Hour 6--7

Integrate:

``` text
AI
→ API
→ workflow
→ state update
→ UI
```

------------------------------------------------------------------------

## Hour 7--8

Polish:

-   demo data
-   error states
-   animations
-   pitch
-   fallback demo

------------------------------------------------------------------------

# 58. Strong UI Concept

Instead of a standard chatbot, create a **Journey Workspace**.

### Header

``` text
Health Insurance Claim
```

### Progress

``` text
Policy ✓
Coverage ✓
Documents ✓
Submission →
Tracking
```

### AI panel

> "I found your policy and checked the hospitalization coverage."

### Evidence panel

``` text
Policy Section 4.2
Hospitalization coverage
```

### Action panel

``` text
Missing:
Final hospital bill

[Upload document]
```

### Timeline

``` text
10:42 Policy found
10:43 Coverage verified
10:44 Documents checked
10:45 Claim prepared
```

This visually communicates that the AI is **moving a journey forward**.

------------------------------------------------------------------------

# 59. Agent State Machine

A useful technical abstraction:

``` text
START
 ↓
UNDERSTAND_INTENT
 ↓
IDENTIFY_JOURNEY
 ↓
COLLECT_CONTEXT
 ↓
CHECK_REQUIREMENTS
 ↓
ACTION_REQUIRED
 ↓
USER_CONFIRMATION
 ↓
EXECUTE
 ↓
VERIFY
 ↓
TRACK
 ↓
COMPLETED
```

For exceptions:

``` text
VERIFY
 ↓
EXCEPTION
 ↓
EXPLAIN
 ↓
COLLECT_MISSING_INFO
 ↓
RETRY
```

This makes the agent much more reliable than an open-ended autonomous
loop.

------------------------------------------------------------------------

# 60. Key Differentiation

Many teams may build:

> "AI explains financial products."

A stronger solution says:

> **"AI completes financial journeys."**

Many teams may build:

> "Upload document → OCR."

A stronger solution says:

> **"Upload document → understand it → identify what's missing →
> complete the journey."**

Many teams may build:

> "Loan chatbot."

A stronger solution says:

> **"Tell us your financial goal → AI identifies the appropriate
> workflow → guides and executes the application."**

------------------------------------------------------------------------

# 61. The Most Interesting Strategic Insight

Track 2 can be understood as an **AI-native interface to financial
infrastructure**.

Traditional architecture:

``` text
PRODUCT
 ↓
FORM
 ↓
USER
```

AI-native architecture:

``` text
USER GOAL
 ↓
AI
 ↓
FINANCIAL JOURNEY
 ↓
TOOLS / APIs
 ↓
FINANCIAL SYSTEM
```

This is potentially more important than any single feature.

------------------------------------------------------------------------

# 62. Comparison of Track 2 Directions

  ---------------------------------------------------------------------------------------
  Direction                 AI depth      Agentic Demo clarity         Data        8-hour
                                        potential                difficulty   feasibility
  --------------------- ------------ ------------ ------------ ------------ -------------
  Insurance Claims              High    Very High    Very High       Medium          High
  Agent                                                                     

  Policy Explainer            Medium       Medium         High          Low     Very High

  Loan Application              High    Very High    Very High       Medium          High
  Agent                                                                     

  Loan Recovery Agent           High    Very High         High   Low/Medium     Very High

  Financial Support             High    Very High    Very High       Medium          High
  Resolution                                                                

  Document-to-Journey      Very High         High         High       Medium          High
  Agent                                                                     

  Universal Journey        Very High    Very High    Very High         High    Medium/Low
  Agent                                                                     

  Financial Translator        Medium          Low       Medium          Low     Very High

  Financial Journey             High         High         High       Medium   Medium/High
  Memory                                                                    
  ---------------------------------------------------------------------------------------

These are **hackathon-scoping estimates**, not organizer-provided
scores.

------------------------------------------------------------------------

# 63. Track 2 Shortlist

Carry these forward to the final three-track comparison:

### 1. AI Insurance Claims Agent

Policy → document → claim → tracking → resolution.

### 2. AI Loan Application Agent

Goal → eligibility → offer → documents → application → tracking.

### 3. AI Financial Support Resolution Agent

Problem → identify transaction/application → diagnose → execute
resolution → track.

### 4. AI Document-to-Journey Agent

Documents → understand context → identify financial journey → complete
next steps.

### 5. Universal Financial Journey Agent

User goal → determine journey → orchestrate the entire workflow.

------------------------------------------------------------------------

# 64. Final Takeaway

Track 2 is fundamentally about **reducing friction across high-value
financial workflows**.

The strongest mental model is:

``` text
OLD

Customer
 ↓
Find product
 ↓
Understand product
 ↓
Fill form
 ↓
Upload documents
 ↓
Call support
 ↓
Check status
 ↓
Repeat
```

versus:

``` text
AI-NATIVE

Customer
 ↓
Tell AI the goal
 ↓
AI understands context
 ↓
AI builds journey
 ↓
AI gathers information
 ↓
AI handles documents
 ↓
AI executes permitted actions
 ↓
AI tracks progress
 ↓
AI explains exceptions
 ↓
Customer completes journey
```

### The key question for Track 2 is:

> **"What painful financial journey can we make dramatically shorter,
> clearer and more reliable with AI?"**

That should be the question we use when generating the final solution
ideas.

------------------------------------------------------------------------

# 65. Sources / Further Reading

-   Paytm personal loans and current digital lending journey:
    https://paytm.com/loans-credit-cards/personal-loan/
    citeturn0search1turn0search2
-   IRDAI health-insurance regulations FAQ and claim-process guidance:
    https://irdai.gov.in/faqs-on-health-insurance-regulations
    citeturn0search0
-   IRDAI consolidated/gazette-notified regulations:
    https://irdai.gov.in/web/guest/consolidated-gazette-notified-regulations
    citeturn0search3
-   IRDAI document on insurance policy/claims information requirements:
    https://irdai.gov.in/document-detail?documentId=376507
    citeturn0search4

------------------------------------------------------------------------

# 66. Next Step

Do not select Track 2 yet.

After Track 3 is analyzed, compare the shortlisted concepts from all
three tracks using:

1.  **Problem severity**
2.  **Paytm fit**
3.  **AI necessity**
4.  **Agentic potential**
5.  **Differentiation**
6.  **Data availability**
7.  **8-hour feasibility**
8.  **Demo clarity**
9.  **Measurable outcome**
10. **Scalability**

Then narrow the entire hackathon to a small number of serious concepts
before choosing the final track.
