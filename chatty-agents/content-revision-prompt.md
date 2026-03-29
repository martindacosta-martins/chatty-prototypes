# Chatty v3 — Content Revision Prompt

You are revising the copy in `chatty-prototype-v3/index.html` to align with Manychat's content guidelines. Every change below is grounded in one of three source documents:

- **Content Guidelines** (`content-guidelines.md`) — official word list, naming rules, formatting
- **Brand Voice** (`brand.md`) — direct, simple, outcome-focused, human, no idioms
- **Writing Style** (`writing-style.md`) — user-facing: 8th grade reading level, benefits before features, empathetic tone

---

## Voice Rule (apply everywhere)

**CTA buttons = creator's voice ("my").** The creator is the one tapping — buttons speak as them.
**Chatty messages = Chatty addressing the creator ("your").** Chatty is talking to the creator.
**Inside the inbox = Chatty uses "I" consistently.** If Chatty has a first-person personality in onboarding, it keeps it in the inbox. No switching to third person ("Chatty flagged these") or passive voice ("handled automatically").

Why: v3 currently mixes "your business" (Chatty's voice) in button labels with "my inbox" (creator's voice) in other buttons. This creates ambiguity that gets worse inside the inbox, where "your" could mean the creator OR the follower they're replying to. One voice per surface eliminates confusion.

---

## Changes

### 1. Step 1 (ObWelcome) — Promise accuracy

**Current:**
```
"I'm going to make sure none of them get ignored."
```

**Change to:**
```
"I'll help you stay on top of every conversation."
```

**Why:** Brand voice says "direct and clear." The current copy makes a guarantee Chatty can't keep (AI will misclassify some messages). The revision commits to helping, not to perfection. Avoids eroding trust when the inevitable miss happens.

---

### 2. Step 3 (ObAnalyzing) — Word list violations

**Current:**
```
'Learning your tone of voice...',
```

**Change to:**
```
'Matching your tone and voice...',
```

**Why:** Two violations in one line.
- Content Guidelines word list says ❌ "AI learns your (specific skill)" → use ✅ "AI matches/matched your tone"
- Content Guidelines word list says ❌ "Tone of voice" → use ✅ "Tone and voice"

---

### 3. Step 4 (ObInsights) — Overly polished, not direct

**Current:**
```
"I noticed a couple of things from your style.",
"You reply fast to lead inquiries. People trust you because of it.",
"Your tone is warm but direct. You always give a clear next step.",
"Your positive replies feel genuine, not copy-paste. That's rare.",
"I'll help you manage your conversations and ensure your style stays yours."
```

**Change to:**
```
"I looked at how you reply.",
"You're fast — especially with leads. And you always give people a next step.",
"Your replies don't sound templated. That matters.",
"I'll keep your tone and voice consistent across every conversation."
```

**Why:** Brand voice says "lead with the point" and "human writing — contractions, varied sentence length, occasional fragments." The current version reads like a LinkedIn endorsement — flattering but not direct. The revision is shorter, uses contractions, varies sentence length, and sounds like a tool that analyzed data.

Also: "ensure your style stays yours" → "keep your tone and voice consistent" uses the approved phrase ✅ "Tone and voice" and is more concrete.

Note: reduced from 5 messages to 4. Fewer typewriter messages = less forced waiting.

---

### 4. Step 4 (ObInsights) — CTA button voice

**Current:**
```
"About your business →"
```

**Change to:**
```
"About my business →"
```

**Why:** This is a CTA button. The creator taps it. It should speak in the creator's voice ("my"), not Chatty's voice ("your"). All other CTA buttons already use creator voice ("Open my inbox →", "Got it →", "Sounds good →"). This one is the outlier.

---

### 5. Step 4b (ObLeadDef) — Word list

**Current (Chatty message):**
```
"I've analyzed your business model.",
"Let's define what a lead looks like for you so I know who to prioritize."
```

**Change to:**
```
"I've looked at how your business works.",
"Let's define what a lead looks like so I know who to prioritize."
```

**Why:** "Analyzed your business model" is corporate language. Brand voice says "simple language, no jargon." "Looked at how your business works" is 8th-grade reading level per writing-style user-facing rules. Also removed "for you" — redundant, Chatty is already talking to the creator.

---

### 6. Step 5 (ObTrustFeel) — Kill idioms

**Current options:**
```
{ id: 'low', icon: '?!', label: 'I barely trust autocorrect', desc: 'No judgment — we\'ll go slow' },
{ id: 'mid', icon: '~', label: 'I\'ve dabbled. Cautiously optimistic', desc: 'You know the drill, just need proof' },
{ id: 'high', icon: '>>', label: 'I already talk to my toaster', desc: 'You\'re ready to let AI cook' },
```

**Change to:**
```
{ id: 'low', icon: '?!', label: 'I barely trust autocorrect', desc: 'No judgment — we\'ll go slow' },
{ id: 'mid', icon: '~', label: 'I\'ve tried AI. Cautiously optimistic', desc: 'You get it, just need to see it work' },
{ id: 'high', icon: '>>', label: 'I\'m comfortable with AI', desc: 'You\'re ready to let it handle things' },
```

**Why:** Brand voice says "simple language — multicultural company, no idioms or jargon."
- "I already talk to my toaster" → culture-specific humor, won't land for non-English-native users (62% of ICP are global creators). Changed to plain "I'm comfortable with AI."
- "Let AI cook" → internet slang. Changed to "let it handle things" — direct, no idiom.
- "I've dabbled" → slightly obscure. "I've tried AI" is clearer.
- "You know the drill" → idiom. "You get it" is plainer.

---

### 7. Step 5 (ObTrustFeel) — Responses use approved language

**Current responses:**
```
low: "Totally fair. Here's what I'm thinking:\n\nI'll summarize your messages and draft replies, but you'll always review before anything gets sent. Nothing goes out without you.",
mid: "Love the open mind. Here's what I'm thinking:\n\nI'll handle your FAQs and qualify leads automatically. For everything else, I'll draft and you review.",
high: "Let's go. Here's what I'm thinking:\n\nI'll answer your comments, qualify your leads, and after some draft reviews, I'll start answering on your behalf."
```

**Change to:**
```
low: "Totally fair.\n\nI'll sort your messages and draft replies — but nothing gets sent without you. You review everything.",
mid: "Great.\n\nI'll handle common questions and sort your leads automatically. For the rest, I'll draft and you review.",
high: "Let's go.\n\nI'll reply to comments, sort your leads, and after a few reviews, start replying on your behalf."
```

**Why:**
- "Here's what I'm thinking" is repeated 3 times — feels templated, violates "replies don't sound copy-paste" (ironic given Step 4 praises the creator for exactly this).
- "Qualify leads" → "sort your leads." "Qualify" is Manychat internal jargon (the feature is called "Lead Qualification Skill" internally). Creators say "sort" or "filter." Writing-style says "8th grade reading level, no technical terms."
- "Love the open mind" → "Great." Brand voice: "lead with the point." The flattery adds nothing.
- Shortened overall — each response should be scannable, not a paragraph.

---

### 8. Step 7 (ObExamples) — Label naming

**Current:**
```
<div style={{ fontSize:11, ... }}>· AI draft</div>
```

**Change to:**
```
<div style={{ fontSize:11, ... }}>· Chatty's draft</div>
```

**Why:** Chatty is a character throughout the onboarding. "AI draft" is generic and breaks the personality. If the product has a name, use it. Also, the content guidelines say use specific feature names, not generic "AI" labels.

Also update the tag labels:

**Current:**
```
{ ..., tag: 'FAQ' },
{ ..., tag: 'Lead Qual' },
{ ..., tag: 'Positive' },
```

**Change to:**
```
{ ..., tag: 'Common question' },
{ ..., tag: 'Interested lead' },
{ ..., tag: 'Positive' },
```

**Why:**
- "FAQ" is a technical abbreviation. Creators think "common questions," not "frequently asked questions." Writing-style: "benefits before features, concrete examples not abstractions."
- "Lead Qual" is internal jargon. No creator knows what "Qual" means. "Interested lead" describes the person, not the process.

---

### 9. Step 8 (ObInboxPreview) — Match actual tab names

**Current preview labels:**
```
"Act Now"          → desc: "AI paused — needs your call"
"Review & Approve" → desc: "Draft ready — just approve it"
"Teach Me"         → desc: "Repetitive questions I could learn to handle"
"Handled"          → desc: "AI took care of it — nothing to do"
```

**Change to:**
```
"Important"        → desc: "I paused — these need your voice"
"Engagement"       → desc: "Draft replies ready — approve or edit"
"Questions"        → desc: "Repeated questions I can learn from"
"Handled"          → desc: "I took care of these — nothing to do"
```

**Why:**
- The preview labels ("Act Now", "Review & Approve", "Teach Me") don't match the actual inbox tabs ("Important", "Engagement", "Questions", "Handled"). This breaks the mental model before the creator even enters the inbox. The preview should be a 1:1 match.
- "Teach Me" → renamed to "Questions" to match the tab AND to avoid the ❌ "Teach AI" framing from the content guidelines word list.
- "AI paused — needs your call" → "I paused — these need your voice." Uses Chatty's first-person "I" and the language is warmer ("your voice" vs "your call").
- "AI took care of it" → "I took care of these" — consistent first-person.
- "Repetitive questions I could learn to handle" → "Repeated questions I can learn from." Content guidelines allow ✅ "AI gets smarter" framing but not ❌ "AI learns your (specific skill)." "Learn from" is general enough.

---

### 10. Step 9 (ObStats) — Active voice

**Current:**
```
"I sorted 142 messages and learned how you talk to people."
```

**Change to:**
```
"I sorted 142 messages and matched your tone and voice."
```

**Why:** ❌ "learned" violates the word list ("AI learns your (specific skill)"). ✅ "matched your tone and voice" uses two approved terms.

---

### 11. Inbox — Tab descriptions (ImportantTab)

**Current:**
```
"Conversations that need your personal touch. Chatty flagged these for you."
```

**Change to:**
```
"Conversations that need your personal touch. I flagged these for you."
```

**Why:** Chatty used "I" throughout onboarding. Switching to third person ("Chatty flagged") breaks the voice. If the agent has a first-person personality, it keeps it.

---

### 12. Inbox — EngagementTab description

**Current:**
```
"Post comments grouped by post. Review and approve draft replies."
```

**Change to:**
```
"Comments on your posts. Review my drafts and approve or edit."
```

**Why:** "Post comments grouped by post" is redundant and reads like a database description, not a human. Brand voice: "direct and clear, human writing." The revision speaks in Chatty's voice ("my drafts") and tells the creator what to do.

---

### 13. Inbox — DailyReport

**Current:**
```
"91% handled automatically · 4 corrections today"
```

**Change to:**
```
"I handled 91% automatically · 4 corrections today"
```

**Why:** Passive voice ("handled automatically") hides the agent. Chatty should own its work: "I handled."

---

### 14. Inbox — SectionLabel icons

**Current:**
```
<SectionLabel icon="→" label="Interested in your services" />
<SectionLabel icon="◇" label="Needs a human" />
<SectionLabel icon="⬡" label="May want to collaborate" />
```

**Change to:**
```
<SectionLabel icon="→" label="Interested in your services" />
<SectionLabel icon="♡" label="Needs your voice" />
<SectionLabel icon="⬡" label="May want to collaborate" />
```

**Why:** "Needs a human" is clinical — it frames the creator as a fallback for when AI fails. "Needs your voice" is warmer and frames the creator as essential, not as a backup. This aligns with the writing-style rule "empathetic tone — acknowledge the struggle before the solution."

---

### 15. Inbox — Toast notification

**Current:**
```
"Learning from your answer"
```

**Change to:**
```
"Got it — I'll adjust for next time"
```

**Why:**
- ❌ "Learning" violates the word list.
- ✅ "adjust" is approved ("AI adjusts/adjusted").
- Adding "for next time" tells the creator what changed, per brand voice "outcome-focused."

---

### 16. Inbox — NARRATIONS object

**Current:**
```
1: "This person commented on your 12-week results post. They've been trying for 2 years — sounds like they need encouragement. Classic lead qualification moment.",
```

**Change to:**
```
1: "This person commented on your 12-week results post. They've been trying for 2 years — sounds like they need encouragement. This could be a strong lead.",
```

**Why:** "Classic lead qualification moment" is internal PM jargon. The creator doesn't think in "lead qualification moments." "This could be a strong lead" is plain and action-oriented.

Apply the same principle to all NARRATIONS — scan for jargon and replace with creator-native language.

---

### 17. ChatDetail — Draft reason text

**Current examples:**
```
reason: "High-intent lead showing vulnerability — encouragement + clear next step"
reason: "Direct product inquiry — matched from your FAQ knowledge base"
reason: "Price objection — addressed with your payment plan info"
```

**Change to:**
```
reason: "They're interested but hesitant — I went with encouragement and a clear next step"
reason: "Direct question about your product — I pulled from what you shared with me"
reason: "They're worried about the price — I mentioned your payment plan"
```

**Why:** The current reasons read like classification labels from a CRM ("High-intent lead showing vulnerability"). Brand voice: "human writing." The revisions:
- Use "They're" — about the person, not the category
- Use "I" — Chatty owns the decision
- ✅ "what you shared with me" instead of ❌ "knowledge base" (content guidelines: use "Details you shared" not technical terms)

---

## Summary of Rules Applied

| Rule | Source | Instances Fixed |
|------|--------|----------------|
| ❌ "AI learns your (specific skill)" | Content Guidelines word list | #2, #10, #15 |
| ❌ "Tone of voice" → ✅ "Tone and voice" | Content Guidelines word list | #2 |
| ❌ "Teach AI" / "Train AI" framing | Content Guidelines word list | #9 (Teach Me tab) |
| ✅ "AI adjusts" / "AI matches your tone" | Content Guidelines word list | #2, #10, #15 |
| ✅ "Details you shared" not "knowledge base" | Content Guidelines word list | #17 |
| No idioms (multicultural audience) | Brand Voice | #6 |
| Direct and clear, lead with the point | Brand Voice | #3, #7 |
| Human writing, contractions, varied length | Brand Voice | #3, #7, #12 |
| Simple language, no jargon | Brand Voice | #5, #7, #8, #16, #17 |
| 8th grade reading level (user-facing) | Writing Style | #5, #7, #8 |
| Empathetic tone | Writing Style | #14 |
| CTA buttons = creator's voice ("my") | Voice consistency rule | #4 |
| Chatty = first person "I" everywhere | Voice consistency rule | #9, #11, #12, #13, #17 |
