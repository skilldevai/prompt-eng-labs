# Prompt Engineering Labs
## Hands-On Exercises for Teams of 2-3

---

# 🧪 LAB 1: Diagnose the Prompt
## Time: 10 minutes

### Objective
Identify what's wrong with problematic prompts and explain how to fix them.
<div style="position: sticky; top: 0; background: white; z-index: 10;">
### Instructions
1. Work in your team of 2-3
2. Review each "broken" prompt below
3. Identify ALL issues (there may be multiple per prompt)
4. Write a brief explanation of why it's a problem
5. Suggest a specific fix (you don't need to rewrite the whole prompt)
</div>
---

## Prompt A: The Support Ticket Handler

```
You are helpful. Respond to customer emails professionally. 
Here's the email:

"Your software sucks. I've been trying to reset my password 
for 3 days and nothing works. Fix this NOW or I'm switching 
to your competitor."

Write a response.
```

### Your Analysis:

**Issues Found:**
- [ ] Issue 1: _______________________________________________
- [ ] Issue 2: _______________________________________________
- [ ] Issue 3: _______________________________________________

**Why These Are Problems:**

_________________________________________________
_________________________________________________

**Suggested Fixes:**

_________________________________________________
_________________________________________________

---

## Prompt B: The Report Generator

```
Make me a report about sales.
```

### Your Analysis:

**Issues Found:**
- [ ] Issue 1: _______________________________________________
- [ ] Issue 2: _______________________________________________
- [ ] Issue 3: _______________________________________________

**Why These Are Problems:**

_________________________________________________
_________________________________________________

**Suggested Fixes:**

_________________________________________________
_________________________________________________

---

## Prompt C: The Code Reviewer

```
Review this code and tell me if it's good or bad:

function processData(d) {
  var r = [];
  for(var i=0;i<d.length;i++){
    if(d[i].status == 'active'){
      r.push(d[i].value * 1.1);
    }
  }
  return r;
}

Don't be too technical. Keep it simple but also explain 
all the computer science concepts. Make it short but comprehensive.
And don't use bullet points but make it scannable.
```

### Your Analysis:

**Issues Found:**
- [ ] Issue 1: _______________________________________________
- [ ] Issue 2: _______________________________________________
- [ ] Issue 3: _______________________________________________

**Why These Are Problems:**

_________________________________________________
_________________________________________________

**Suggested Fixes:**

_________________________________________________
_________________________________________________

---

## Prompt D: The Marketing Copy Writer

```
Write social media posts for our new product launch. Make them 
engaging and viral. They should work on all platforms. Our product 
is innovative and best-in-class. Target everyone who might be 
interested. Make it pop! Think outside the box and push the envelope.
```

### Your Analysis:

**Issues Found:**
- [ ] Issue 1: _______________________________________________
- [ ] Issue 2: _______________________________________________
- [ ] Issue 3: _______________________________________________

**Why These Are Problems:**

_________________________________________________
_________________________________________________

**Suggested Fixes:**

_________________________________________________
_________________________________________________

---

## 💡 LAB 1 Answer Key (for facilitator / self-check)

### Prompt A Issues:
1. **Vague role** — "You are helpful" provides no context about expertise, company, or communication style
2. **No context** — No information about what company, what product, what the password reset process actually is, or what resources are available
3. **No constraints** — No guidance on tone (empathetic vs. formal), what to offer (refund? expedited support?), or what NOT to say
4. **No format** — Should the response include steps? Links? A phone number?
5. **Missing de-escalation guidance** — Angry customer requires specific handling approach

### Prompt B Issues:
1. **No context** — What sales? What time period? What company? What business unit?
2. **No format** — Should this be a summary, a detailed analysis, a presentation, a spreadsheet?
3. **No task specificity** — What should the report accomplish? Who's the audience?
4. **No constraints** — Length, sections to include, data to focus on, comparative analysis?

### Prompt C Issues:
1. **Contradictory instructions** — "Don't be too technical" vs "explain all the computer science concepts"
2. **Contradictory formatting** — "Short but comprehensive"
3. **Contradictory formatting** — "Don't use bullet points but make it scannable"
4. **Vague success criteria** — What makes code "good" or "bad"? Performance? Readability? Security?
5. **No audience definition** — Is this for a junior developer or a CTO?

### Prompt D Issues:
1. **No specifics about the product** — Can't write good copy without knowing what we're selling
2. **Vague target audience** — "Everyone who might be interested" is not actionable
3. **Clichés instead of direction** — "Make it pop," "think outside the box," "push the envelope" are meaningless
4. **Platform mismatch** — "Work on all platforms" ignores that Twitter, LinkedIn, TikTok, etc. have different formats, audiences, and norms
5. **No constraints** — Character limits, hashtag requirements, CTA requirements, brand voice guidelines

---

# 🧪 LAB 2: Prompt Transformation Challenge
## Time: 10 minutes

### Objective
Take weak prompts and transform them into effective ones using specific techniques.

### Instructions
1. Work in your team of 2-3
2. Each transformation challenge specifies a technique to apply
3. Rewrite the prompt using THAT SPECIFIC TECHNIQUE
4. **BONUS**: Test your rewritten prompt in ChatGPT and see the difference!

---

## Challenge 1: Apply Few-Shot Learning

### Original Weak Prompt:
```
Summarize these meeting notes into action items.
```

### Your Task:
Rewrite this prompt using the **few-shot technique** (provide 2-3 examples of input→output pairs before the actual task).

### Your Improved Prompt:

```
[Write your few-shot prompt here]

























```

### Test It! 
Paste your new prompt into ChatGPT with these sample meeting notes:

> "Team discussed Q3 roadmap. Sarah mentioned we need to finalize the API documentation by end of month. John said he'd set up a meeting with the security team. Budget review pushed to next week per Maria's request. Everyone agreed to test the new deployment pipeline before Thursday."

---

## Challenge 2: Apply Chain of Thought

### Original Weak Prompt:
```
Our startup has $500K remaining runway, burns $80K/month, has 3 
enterprise deals in pipeline worth $150K each (60% close rate), 
and was offered $1M at a $5M valuation. Should we take the funding?
```

### Your Task:
Rewrite this prompt using the **chain of thought technique** (explicitly ask for step-by-step reasoning).

### Your Improved Prompt:

```
[Write your chain of thought prompt here]

























```

### Test It!
Run both the original and your improved version in ChatGPT. Compare:
- Does the improved version show clearer reasoning?
- Can you verify the logic more easily?
- Which would you trust more for an actual decision?

---

## Challenge 3: Apply Role + Constraints

### Original Weak Prompt:
```
Explain machine learning to my team.
```

### Your Task:
Rewrite this prompt using **role-based + constrained** techniques (assign a specific expert role AND add clear constraints).

### Your Improved Prompt:

```
[Write your role + constraints prompt here]

























```

### Test It!
Try multiple roles with the same base task:
- What changes when you specify "data scientist explaining to marketing"?
- What about "tech lead explaining to executives"?
- How about "teacher explaining to high school students"?

---

## 💡 LAB 2 Sample Solutions

### Challenge 1: Few-Shot Solution

```
Convert meeting notes into a structured list of action items.

EXAMPLE 1:
Meeting notes: "We need to update the homepage copy before launch. 
Tim will handle the A/B testing setup. Follow up with legal on the 
new terms of service."

Action items:
- [ ] Update homepage copy before launch (Owner: Unassigned)
- [ ] Set up A/B testing (Owner: Tim)
- [ ] Follow up with legal on new terms of service (Owner: Unassigned)

EXAMPLE 2:
Meeting notes: "Design review scheduled for Friday. Make sure to get 
Sarah's input on the color scheme. Budget needs approval from finance 
first—James to send request."

Action items:
- [ ] Attend design review on Friday (Owner: Team)
- [ ] Get Sarah's input on color scheme (Owner: Unassigned)
- [ ] Send budget approval request to finance (Owner: James)

---

Now convert these meeting notes into action items:

"Team discussed Q3 roadmap. Sarah mentioned we need to finalize the 
API documentation by end of month. John said he'd set up a meeting 
with the security team. Budget review pushed to next week per Maria's 
request. Everyone agreed to test the new deployment pipeline before 
Thursday."

Action items:
```

---

### Challenge 2: Chain of Thought Solution

```
Our startup has the following situation:
- $500K remaining runway
- Burns $80K/month  
- 3 enterprise deals in pipeline worth $150K each (60% close rate)
- Offered $1M investment at a $5M valuation

Should we take the funding?

Please analyze this step by step:

STEP 1: Calculate our current runway without any new revenue
(How many months until we run out of cash?)

STEP 2: Calculate expected revenue from pipeline
(What's the probability-weighted value of those deals?)

STEP 3: Calculate runway with expected pipeline revenue
(How does the picture change if deals close?)

STEP 4: Analyze the funding offer
(What percentage are we giving up? Is this a fair valuation?)

STEP 5: Consider alternatives
(What other options exist besides this specific offer?)

STEP 6: Final recommendation
(Based on the above analysis, what should we do and why?)

Show your math at each step.
```

---

### Challenge 3: Role + Constraints Solution

```
You are a senior engineering manager who has successfully 
introduced ML initiatives to three non-technical teams. You're 
known for using relatable analogies and avoiding jargon.

Explain machine learning to our business development team.

CONTEXT:
- Audience: 8 people in business development, none with 
  technical backgrounds
- They've heard ML mentioned in client meetings and feel 
  unprepared
- They need to understand it well enough to discuss with 
  clients, not implement it

CONSTRAINTS:
- Use zero technical jargon (or define any term you must use)
- Include at least 2 real-world business examples they'd recognize
- Analogy requirement: Use at least one comparison to a familiar 
  business process
- Keep it under 300 words
- End with 3 simple questions they could ask a client to identify 
  ML opportunities

FORMAT:
1. One-sentence definition
2. The business value (why this matters)
3. Two examples with business impact
4. Everyday analogy
5. Three client discovery questions
```

---

# 🧪 LAB 3: Real-World Prompt Building (OPTIONAL/BONUS)
## Time: If time permits

### Objective
Build a complete, production-quality prompt for a realistic business scenario.

### Instructions
1. Work in your team of 2-3
2. Choose ONE scenario below
3. Build a complete prompt using ALL relevant elements (Role, Context, Task, Format, Constraints, Examples)
4. Test it in ChatGPT
5. Iterate at least once based on results
6. Be prepared to share your prompt and results

---

## Scenario Options

### Option A: Customer Email Triage
**Business Need:** Your support team gets 500+ emails daily. You need a prompt that categorizes emails and drafts initial responses.

Build a prompt that:
- Categorizes into: Urgent, Billing, Technical, General, Spam
- Flags emails needing human escalation
- Drafts a response template for non-urgent items
- Handles angry customers appropriately

---

### Option B: Interview Question Generator
**Business Need:** Your HR team needs to generate role-specific interview questions that assess both technical skills and culture fit.

Build a prompt that:
- Takes a job title and key requirements as input
- Generates behavioral and technical questions
- Includes what a "good" answer would cover
- Avoids legally problematic questions

---

### Option C: Competitive Intelligence Summary
**Business Need:** Your strategy team monitors competitor news but struggles to synthesize it into actionable insights.

Build a prompt that:
- Takes a collection of news snippets as input
- Identifies key competitive moves
- Assesses threat level to your business
- Suggests potential responses
- Outputs in executive-briefing format

---

## Your Complete Prompt

**Scenario Chosen:** _______________

```
[Write your complete prompt here]








































```

---

## Test Results

**First Attempt - What Worked:**
_________________________________________________
_________________________________________________

**First Attempt - What Didn't Work:**
_________________________________________________
_________________________________________________

**Changes Made for Second Attempt:**
_________________________________________________
_________________________________________________

**Final Results:**
_________________________________________________
_________________________________________________

---

# Quick Reference Card

## The Six Prompt Elements

| Element | Question It Answers | Example Start |
|---------|--------------------| --------------|
| **Role** | Who should the AI be? | "You are a senior..." |
| **Context** | What background is needed? | "Our company is..." |
| **Task** | What exactly should be done? | "Analyze and provide..." |
| **Format** | How should output look? | "Format as a table with..." |
| **Constraints** | What are the rules/limits? | "Do NOT mention..." |
| **Examples** | What does good look like? | "Example input/output..." |

## Prompt Types Quick Guide

| Type | When to Use | Key Feature |
|------|-------------|-------------|
| **Role-Based** | Need expertise or voice | Assign a persona |
| **Structured Output** | Need specific format | Define exact output structure |
| **Constrained** | Need guardrails | Set explicit limits |
| **Few-Shot** | Need pattern matching | Provide examples |
| **Chain of Thought** | Need reasoning | Ask for step-by-step |
| **Self-Consistency** | Need verification | Multiple angles |

## Red Flags Checklist
- [ ] Inconsistent output format
- [ ] AI asks for clarification often
- [ ] Outputs miss requirements
- [ ] Heavy editing needed
- [ ] Goes off-topic
- [ ] Contradictory results
- [ ] Wrong tone
- [ ] Makes things up

---

# Notes Page

Use this space for notes during the session:

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________

_________________________________________________________
