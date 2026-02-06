# Applied AI Engineering for the Enterprise
## Day 1 - Hands-on Labs

---

# LAB 1: Diagnose the Prompt
## Purpose: Identify what's wrong with problematic prompts and explain how to fix them.

### Instructions
1. Work in your team of 2-3
2. Review each "broken" prompt below
3. Identify ALL issues (there may be multiple per prompt)
4. Write a brief explanation of why it's a problem
5. Suggest a specific fix (you don't need to rewrite the whole prompt)

---

<details>
<summary>Prompt A: The Support Ticket Handler</summary>

```
You are helpful. Respond to customer emails professionally. 
Here's the email:

"Your software sucks. I've been trying to reset my password 
for 3 days and nothing works. Fix this NOW or I'm switching 
to your competitor."

Write a response.
```
</details>

<details>
<summary>💡 Prompt A: Issues</summary> 

1. **Vague role** — "You are helpful" provides no context about expertise, company, or communication style
2. **No context** — No information about what company, what product, what the password reset process actually is, or what resources are available
3. **No constraints** — No guidance on tone (empathetic vs. formal), what to offer (refund? expedited support?), or what NOT to say
4. **No format** — Should the response include steps? Links? A phone number?
5. **Missing de-escalation guidance** — Angry customer requires specific handling approach
</details>

<br><br>

<details>
<summary>Prompt B: The Report Generator</summary>

```
Make me a report about sales.
```
</details>

<details>
<summary>💡 Prompt B: Issues</summary> 

1. **No context** — What sales? What time period? What company? What business unit?
2. **No format** — Should this be a summary, a detailed analysis, a presentation, a spreadsheet?
3. **No task specificity** — What should the report accomplish? Who's the audience?
4. **No constraints** — Length, sections to include, data to focus on, comparative analysis?

</details>

<br><br>

<details>
<summary>Prompt C: The Code Reviewer</summary>

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
</details>

<details>
<summary>💡 Prompt C: Issues</summary> 

1. **Contradictory instructions** — "Don't be too technical" vs "explain all the computer science concepts"
2. **Contradictory formatting** — "Short but comprehensive"
3. **Contradictory formatting** — "Don't use bullet points but make it scannable"
4. **Vague success criteria** — What makes code "good" or "bad"? Performance? Readability? Security?
5. **No audience definition** — Is this for a junior developer or a CTO?
</details>

<br><br>

<details>
<summary>Prompt D: The Marketing Copy Writer</summary>

```
Write social media posts for our new product launch. Make them 
engaging and viral. They should work on all platforms. Our product 
is innovative and best-in-class. Target everyone who might be 
interested. Make it pop! Think outside the box and push the envelope.
```
</details>

<details>
<summary>💡 Prompt D: Issues</summary> 

1. **No specifics about the product** — Can't write good copy without knowing what we're selling
2. **Vague target audience** — "Everyone who might be interested" is not actionable
3. **Clichés instead of direction** — "Make it pop," "think outside the box," "push the envelope" are meaningless
4. **Platform mismatch** — "Work on all platforms" ignores that Twitter, LinkedIn, TikTok, etc. have different formats, audiences, and norms
5. **No constraints** — Character limits, hashtag requirements, CTA requirements, brand voice guidelines
</details>

<br><br>

---

# LAB 2: Prompt Transformation Challenge
## Purpose: Take weak prompts and transform them into effective ones using specific techniques.

### Instructions
1. Work in your team of 2-3
2. Each transformation challenge specifies a technique to apply
3. Rewrite the prompt using THAT SPECIFIC TECHNIQUE
4. **BONUS**: Test your rewritten prompt in ChatGPT and see the difference!

---

<details>
<summary>Challenge 1: Apply Few-Shot Learning</summary>

### Original Weak Prompt:
```
Summarize these meeting notes into action items.
```

### Your Task:
Rewrite this prompt using the **few-shot technique** (provide 2-3 examples of input→output pairs before the actual task).

### 
<details>
<summary>Challenge 1: Few-Shot Solution</summary>

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
</details>

<details>
<summary>Challenge 1: Test example</summary>

Paste your new prompt into ChatGPT with these sample meeting notes:

> "Team discussed Q3 roadmap. Sarah mentioned we need to finalize the API documentation by end of month. John said he'd set up a meeting with the security team. Budget review pushed to next week per Maria's request. Everyone agreed to test the new deployment pipeline before Thursday."
</details>

</details>

---

<br><br>

<details>
<summary>Challenge 2: Apply Chain of Thought</summary>

### Original Weak Prompt:
```
Our startup has $500K remaining runway, burns $80K/month, has 3 
enterprise deals in pipeline worth $150K each (60% close rate), 
and was offered $1M at a $5M valuation. Should we take the funding?
```

### Your Task:
Rewrite this prompt using the **chain of thought technique** (explicitly ask for step-by-step reasoning).

### 
<details>
<summary>Challenge 2: Chain of Thought Solution</summary>

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
</details>

---

<details>
<summary>Challenge 2: Test example</summary>
Run both the original and your improved version in ChatGPT. Compare:
- Does the improved version show clearer reasoning?
- Can you verify the logic more easily?
- Which would you trust more for an actual decision?
</details>
</details>

---

<br><br>

<details>
  
<summary>Challenge 3: Apply Role + Constraints</summary>

### Original Weak Prompt:
```
Explain machine learning to my team.
```

### Your Task:
Rewrite this prompt using **role-based + constrained** techniques (assign a specific expert role AND add clear constraints).

### 
<details>
<summary>Challenge 3: Role + Constraints Solution</summary>

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
</details>


<details>
<summary>Challenge 3: Test example</summary>
Try multiple roles with the same base task:
- What changes when you specify "data scientist explaining to marketing"?
- What about "tech lead explaining to executives"?
- How about "teacher explaining to high school students"?

</details>

---

<br><br>


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


</details>

<br><br>

# Lab #3 - Creating Your Own Intelligence Briefing

**Purpose: Use AI to help keep you up-to-date on AI.**

<br><br>

<details>

## Extended Prompt

```
"Please provide me with a structured AI intelligence briefing covering the last 7-14 days. Format your response as an executive briefing with the following sections:
1. CRITICAL DEVELOPMENTS (What I Must Know)

Major AI model releases or significant updates
Regulatory changes or policy announcements
Security/safety incidents or concerns
Industry game-changers or disruptions

2. TECHNICAL ADVANCES (What's New)

New capabilities or benchmarks achieved
Research breakthroughs (summarize in 1-2 sentences each)
Open source releases worth noting
Performance improvements in existing tools

3. BUSINESS IMPACT (What Matters for Work)

New enterprise AI tools or features
Case studies of successful AI implementations
ROI data or efficiency metrics published
Vendor announcements (Microsoft, Google, AWS, etc.)

4. PRACTICAL APPLICATIONS (What I Can Use Now)

New tools I can try immediately (with links)
Prompt engineering techniques or tips discovered
Workflow improvements or automations
Cost-effective AI solutions released

5. INDUSTRY MOVEMENTS (Market Dynamics)

Major funding rounds or acquisitions
Partnership announcements
Competitive landscape shifts
Job market or skill demand changes

6. LOOKING AHEAD (What's Coming)

Upcoming releases or announcements to watch
Scheduled conferences or events
Predicted trends gaining momentum
Emerging concerns or opportunities

For each item, please:

Include the DATE it was announced/published
Provide a direct LINK to the source
Keep descriptions to 2-3 sentences max
Bold the most important items I shouldn't miss
Flag anything requiring immediate action with 🚨

End with a 'THREE THINGS TO DO THIS WEEK' section with specific, actionable recommendations based on the updates.
Focus on practical, business-relevant developments over purely academic research. Prioritize information from the last 14 days, and clearly mark anything older as 'BACKGROUND' if it's essential context."

```

<br><br>

## 1: Try out the simple one-line prompt

Open claude.ai, chatgpt.com, gemini.google.com or your preferred AI assistant and copy and paste the simplified prompt below (substituting in your role and industry in the appropriate places):

```
What are the 5 most important AI developments from the last week that a [YOUR ROLE] in [YOUR INDUSTRY] needs to know, with links to learn more?
```

![simple query](./images/aia-0-13.png?raw=true "Simple query")

<br><br>

## 2: Review the output and note what is useful/not useful.

<br><br>

## 3: Try out the extended prompt.

Copy and paste the extended prompt from the start of the lab into the AI assistant. Submit it. This will take several minutes to run.

![full query](./images/aia-0-14.png?raw=true "Full query")

<br><br>

## 4: Review the output and notice differences and details vs the simpler prompt. 

![full query output](./images/aia-0-15.png?raw=true "Full query output")

<br><br>

## 5: Run the extended prompt again but add the appropriate section (or create your own) for your role.

For Technical Practitioners
```
Include code examples, GitHub repos, and technical implementation details. Focus on tools I can integrate into development workflows.
```

For Business Leaders
```
Emphasize ROI metrics, competitive advantages, and strategic implications. Include cost comparisons and vendor assessments.
```
For Specific Industries
```
Filter for developments specifically relevant to [YOUR INDUSTRY: healthcare/finance/retail/etc.]. Include industry-specific use cases and compliance considerations.
```

![adding specialization](./images/aia-0-16.png?raw=true "Adding specialization")

<br><br>

## 6: Review the output with the additional details.

![full report output](./images/aia-0-17.png?raw=true "Full report output")

<br><br>

## 7: What would you change/add/delete to make the results better for you? Try out any changes you want to make to fine-tune and make this most useful.


<p align="center">
<b>[END OF LAB]</b>
</p>
</br></br>

</details>
<p align="center">
<b>For educational use only by the attendees of our workshops.</b>
</p>

<p align="center">
<b>(c) 2025 Tech Skills Transformations and Brent C. Laster. All rights reserved.</b>
</p>
