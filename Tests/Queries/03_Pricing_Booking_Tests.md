# Pricing & Booking Tests

Tests for pricing accuracy, discovery call requirement enforcement, and booking flow guidance.

---

## Pricing Questions

### Query #14
**"What's the exact price for web development?"**

**What This Tests:**
- Pricing range accuracy ($2K-$10K+)
- Discovery call requirement
- Handling "exact" price requests
- Booking CTA placement

**Expected Behavior:**
- Provides range: "Typically $2,000 to $10,000+"
- Explains exact quote requires discovery call
- Mentions factors (features, complexity)
- Booking link with descriptive anchor
- Not defensive about custom pricing

---

### Query #15
**"Can you give me a quote for branding?"**

**What This Tests:**
- Custom-quoted language
- Discovery call enforcement
- Brand voice (helpful, not evasive)

**Expected Behavior:**
- States branding is custom-quoted
- Explains why (scope varies)
- Mentions discovery call process
- 24-48 hour proposal timeline
- Booking CTA
- Doesn't apologize excessively

---

### Query #16
**"How much do you charge for sound mixing?"**

**What This Tests:**
- Specific pricing accuracy ($50/song)
- Clear communication
- Service details (vocal mix + master)
- Turnaround time

**Expected Behavior:**
- States $50 per song clearly
- Mentions vocal mix + master
- 48-hour turnaround
- Trackout custom pricing
- Free demo snippet mention
- Booking CTA appropriate for sound service

---

### Query #17
**"I need pricing for everything - design, web, video, sound"**

**What This Tests:**
- Multi-service pricing handling
- Organization and clarity
- Not overwhelming with numbers
- Unified booking approach

**Expected Behavior:**
- Organized by service (headers or bullets)
- Sound: $50/song (specific)
- Web: $2K-$10K+ (range)
- Design, Video, AI: Custom-quoted
- Single discovery call CTA to discuss all
- Not repetitive with "discovery call" language

---

## Booking Flow Tests

### Query #18
**"How do I get started?"**

**What This Tests:**
- Clear booking guidance
- Discovery call explanation
- Process clarity
- CTA placement

**Expected Behavior:**
- Directs to discovery call as first step
- Explains 30-minute duration
- Mentions outcome (proposal in 24-48 hours)
- Calendly link with descriptive anchor
- Welcoming tone

---

### Query #19
**"Can I book a project right now?"**

**What This Tests:**
- Discovery call requirement enforcement
- "No exceptions" rule adherence
- Helpful tone (not rigid)

**Expected Behavior:**
- Explains all projects start with discovery call
- Not defensive or apologetic
- Emphasizes benefit (accurate quote, understanding needs)
- Booking link
- Doesn't offer workarounds

---

### Query #20
**"What's the booking link?"**

**What This Tests:**
- Direct URL request handling
- Link still uses anchor text (not raw URL)
- Concise response

**Expected Behavior:**
- Provides link with descriptive anchor
- Brief context (30-minute discovery call)
- 1-2 sentences maximum
- Still human-sounding, not robotic

**Example:**
```
✅ "Here you go: [Book a 30-minute discovery call](calendly-link)"

❌ "https://calendly.com/rangeofviewmusic/30min"
```

---

## Pricing Language Validation

### Service-Specific Pricing

**Design:**
```
✅ "Custom-quoted based on scope after discovery call"
❌ "Pricing varies" (too vague)
❌ "$500-$5000" (inventing numbers)
```

**Web:**
```
✅ "Typically $2,000 to $10,000+ depending on features"
❌ "Around $5000" (not accurate to range)
❌ "Custom pricing" (missing helpful range)
```

**Sound:**
```
✅ "$50 per song for vocal mixing and mastering"
❌ "$50-$100" (wrong range)
❌ "Affordable rates" (not specific)
```

**Video:**
```
✅ "Custom-quoted based on shoot requirements"
❌ "$1000 per video" (inventing price)
```

**AI Integration:**
```
✅ "Custom-quoted based on automation complexity"
❌ "Starts at $2000" (inventing floor price)
```

---

## Discovery Call Details to Verify

### Required Elements

✅ **Duration:** 30 minutes
✅ **Purpose:** Understand goals, timeline, budget
✅ **Outcome:** Proposal within 24-48 hours
✅ **URL:** https://calendly.com/rangeofviewmusic/30min
✅ **Free:** Not explicitly stated, but implied

### When to Push Booking

**✅ Guide to booking when user:**
- Describes specific project need
- Asks "how do I start?"
- Requests a quote
- Seems ready to move forward
- Has asked 2+ detailed service questions

**❌ Don't push booking when user:**
- Is just browsing/exploring
- Asked single general question
- Seeking tool recommendations (CTRL-A)
- Hasn't indicated project intent

---

## Evaluation Checklist

For each pricing/booking query, verify:

- ✅ **Accuracy:** Pricing matches docs exactly
- ✅ **Grounding:** No invented numbers
- ✅ **Discovery Call:** Mentioned when appropriate
- ✅ **Process:** 24-48 hour proposal timeline stated
- ✅ **CTA:** Booking link with descriptive anchor
- ✅ **Tone:** Helpful, not defensive or apologetic
- ✅ **Brevity:** Concise explanation
- ✅ **No Exceptions:** Discovery call required, no workarounds

---

## Common Issues to Watch For

❌ Inventing specific prices not in docs
❌ Offering to "skip" discovery call
❌ Overly apologetic about custom pricing
❌ Missing pricing ranges when available (web: $2K-$10K+)
❌ Wrong pricing ($50/song vs invented ranges)
❌ Multiple booking links in one response
❌ Raw URLs instead of anchor text
❌ Not explaining discovery call value

---

## Price Pushback Scenario

**User asks:** "Can you just give me a ballpark figure?"

**Good Response:**
```
"I totally get wanting to know costs upfront. Here's the deal: [provide range if available], but the exact quote depends on your specific needs. The discovery call is free and takes 30 minutes — we'll discuss your project and give you accurate pricing within 24-48 hours after."
```

**Bad Response:**
```
"Sorry, I can't provide pricing without a discovery call."
(Too rigid, not helpful)
```

---

**Total Queries in This Category:** 7
**Difficulty Level:** Moderate
**Priority Level:** ⭐⭐⭐ High (Critical business function)
