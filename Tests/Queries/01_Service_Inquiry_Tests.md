# Service Inquiry Tests

Tests for basic and multi-service inquiries to validate service explanation, pricing communication, and booking flow.

---

## Basic Service Questions

### Query #1
**"How much for a website?"**

**What This Tests:**
- Web pricing range ($2K-$10K+)
- Booking flow guidance
- Link handling (Calendly CTA)
- Discovery call requirement
- Concise response structure

**Expected Behavior:**
- Mentions $2K-$10K+ range
- Explains custom pricing after discovery call
- Includes booking link with descriptive anchor text
- 1-2 short paragraphs max

---

### Query #2
**"Do you do logos?"**

**What This Tests:**
- Design service nuance (systems vs one-offs)
- Brand voice (not just "yes")
- Value proposition clarity

**Expected Behavior:**
- Clarifies logos are part of complete brand systems
- Not standalone service
- May suggest discovery call if appropriate
- Avoids simple yes/no answer

---

### Query #3
**"What's your sound engineering service?"**

**What This Tests:**
- Specific service explanation
- $50/song pricing accuracy
- 48-hour turnaround mention
- Free demo snippet offer
- Concise formatting

**Expected Behavior:**
- States $50 per song clearly
- Mentions vocal mix + master
- 48-hour turnaround
- Free demo for first-time clients
- Booking CTA appropriate for sound service

---

### Query #4
**"Can you help with video production?"**

**What This Tests:**
- Video service overview
- Custom pricing handling
- Service types (real estate, events, music videos, drone)
- Timeline information

**Expected Behavior:**
- Lists video service types
- Custom-quoted language
- 1-2 weeks post-production mention
- Discovery call CTA

---

### Query #5
**"Tell me about your AI integration services"**

**What This Tests:**
- AI service explanation
- n8n workflows, chatbots, automation mention
- Brand voice ("Automate the chaos")
- Pricing and timeline handling

**Expected Behavior:**
- Mentions n8n, chatbots, automation
- Custom-quoted based on complexity
- 2-6 week timeline
- Discovery call CTA
- Authentic ROV voice

---

## Multi-Service Questions

### Query #6
**"Do you do branding and video? How much?"**

**What This Tests:**
- Multi-intent handling
- Section organization (headers)
- Pricing for multiple services
- Unified CTA placement
- Response structure

**Expected Behavior:**
- Uses section headers (### Branding, ### Video)
- Explains both services briefly
- Custom-quoted language for both
- Single booking CTA at end
- Mentions they work well together

---

### Query #7
**"What services do you offer?"**

**What This Tests:**
- Comprehensive service list
- Brevity (no feature dumps)
- Scannable formatting
- Appropriate CTA placement

**Expected Behavior:**
- Lists all 5 core services (Design, Web, Sound, Video, AI)
- Bullet points or brief sections
- 1-line description per service
- Optional discovery call CTA (not pushy)
- Should be scannable

---

### Query #8
**"I need a logo, website, and some video content"**

**What This Tests:**
- Complex multi-service response
- Unified CTA (not multiple booking links)
- Project approach suggestion
- Response organization
- Brand voice (helpful, action-oriented)

**Expected Behavior:**
- Acknowledges all three needs
- May suggest phased approach or integration
- Custom pricing language
- Single discovery call CTA to discuss all needs
- Organized with headers or bullets
- Not overwhelming

---

## Evaluation Checklist

For each query response, verify:

- ✅ **Grounding:** Only uses info from retrieved context
- ✅ **Accuracy:** Pricing, timelines, and service details are exact
- ✅ **Voice:** Direct, confident, helpful (not corporate)
- ✅ **Links:** Descriptive anchor text, natural placement
- ✅ **Brevity:** Concise, no filler words
- ✅ **CTA:** Clear next step, not pushy
- ✅ **Structure:** Scannable, organized logically
- ✅ **Relevance:** Directly answers the question

---

## Common Issues to Watch For

❌ Inventing services or capabilities not in docs
❌ Generic "click here" or raw URLs
❌ Too many booking CTAs in multi-service responses
❌ Feature dumps instead of value-focused explanations
❌ Overly corporate or robotic tone
❌ Missing pricing information when available
❌ Not mentioning discovery call requirement

---

**Total Queries in This Category:** 8
**Difficulty Level:** Basic to Moderate
**Priority Level:** ⭐⭐⭐ High (Core functionality)
