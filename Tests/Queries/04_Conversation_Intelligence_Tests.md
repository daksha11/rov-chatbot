# Conversation Intelligence Tests

Tests for intent understanding, clarification questions, and context continuity across multi-turn conversations.

---

## Vague/Ambiguous Questions

### Query #21
**"I need help with my business"**

**What This Tests:**
- Ambiguity detection
- ONE focused clarifying question
- Not overwhelming with options
- Helpful tone

**Expected Behavior:**
- Recognizes question is too vague
- Asks ONE clarifying question
- Provides 3-4 clear options
- Friendly, not interrogating
- Waits for user response before recommending

**Good Clarification Examples:**
```
✅ "I'd love to help! Could you share a bit more about what you're looking for?

Are you thinking:
• Brand identity (logo, visual system)
• Website or digital product
• Video content
• Something else?"

❌ "What's your budget? Timeline? Industry? Target audience? Goals?"
(Too many questions at once)
```

---

### Query #22
**"Can you help me with my brand?"**

**What This Tests:**
- Detecting ambiguity (new vs existing brand)
- Clarification before retrieval
- Targeted follow-up

**Expected Behavior:**
- Asks: "Are you looking to build a brand identity from scratch, or update an existing one?"
- Waits for answer
- Then provides targeted response
- Doesn't assume

---

### Query #23
**"I want to improve my online presence"**

**What This Tests:**
- Multi-faceted intent clarification
- Understanding broad goals
- Narrowing focus appropriately

**Expected Behavior:**
- Recognizes multiple possible needs (web, social, content, etc.)
- Asks clarifying question
- May suggest multiple services but organized
- Not pushy with booking

**Potential Clarification:**
```
"Improving online presence could mean a few things. Are you focused on:
• Rebuilding or launching a website
• Visual branding/identity
• Content (video, graphics)
• Something else?"
```

---

## Follow-up & Context Continuity

### Query #24: Conversation Flow Test #1

**First Message:** "What services do you offer?"

**Second Message:** "Tell me more about the design one"

**What This Tests:**
- Conversation memory
- Reference to previous message
- Not repeating full service list
- Building on context

**Expected Behavior (Second Response):**
- Recognizes "the design one" refers to previously mentioned design service
- Doesn't re-list all services
- Dives into design service details
- Natural continuation
- May say "The design service I mentioned..." or similar

**Bad Response:**
```
❌ "We offer five core services..." (repeating everything)
❌ "What design service?" (no memory)
```

---

### Query #25: Conversation Flow Test #2

**First Message:** "How much for a website?"

**Second Message:** "What about adding video to that?"

**What This Tests:**
- Context building
- Understanding "that" refers to website project
- Combined service handling
- Not repeating web pricing

**Expected Behavior (Second Response):**
- Understands "adding video to that" = website + video
- Doesn't re-explain web pricing
- Explains video service in context of web project
- May suggest integrated approach
- Single booking CTA (not repeated)

**Good Response Pattern:**
```
✅ "Great combo — a lot of clients pair video content with their new site for homepage hero sections or portfolio work.

Video production is custom-quoted based on shoot requirements and post-production needs.

[Book a discovery call](link) and we can put together pricing for both."
```

---

## Intent Understanding

### Phase 1: Intent Classification

For each query, chatbot should mentally identify:

**Primary Intent Categories:**
- Service inquiry
- Tool recommendation (CTRL-A)
- Company info
- Booking
- General question

**User Journey Stage:**
- Awareness (exploring)
- Consideration (comparing)
- Decision (ready to book)

**Clarity Level:**
- Crystal clear
- Somewhat vague
- Very ambiguous

---

## Evaluation Checklist

For conversation intelligence queries, verify:

- ✅ **Ambiguity Detection:** Recognizes when question is vague
- ✅ **Single Question:** Asks ONE focused clarifying question
- ✅ **Context Memory:** References previous messages appropriately
- ✅ **No Repetition:** Doesn't re-explain already covered info
- ✅ **Natural Flow:** Conversation feels continuous, not fragmented
- ✅ **Wait for Response:** Doesn't answer vague questions without clarification
- ✅ **Intent Accuracy:** Correctly identifies what user is asking for
- ✅ **Journey Stage:** Adapts response to user's readiness level

---

## Common Issues to Watch For

❌ Answering vague questions without clarification
❌ Asking too many questions at once
❌ Not remembering previous conversation context
❌ Repeating information already shared
❌ Misunderstanding user intent
❌ Being too pushy with booking on first exploratory message
❌ Not building on previous discussion

---

## Multi-Turn Conversation Examples

### Example: Good Context Continuity

```
User: "What services do you offer?"
Bot: [Lists 5 core services]

User: "What about the web one?"
Bot: ✅ "The web development service I mentioned covers..."
     (Builds on context)

Bot: ❌ "We offer web development services..."
     (No memory, starts fresh)
```

### Example: Good Clarification Flow

```
User: "I need help with my business"
Bot: ✅ [Asks ONE clarifying question with 3-4 options]

User: "Yeah, I need a new logo and website"
Bot: ✅ [Now provides targeted answer about design + web]

vs.

User: "I need help with my business"
Bot: ❌ [Immediately recommends all services without clarifying]
```

---

## Advanced Context Tracking

### What to Remember Across Conversation:

✅ **Services discussed** - Don't re-explain
✅ **User's project intent** - Build on it
✅ **Booking CTA used** - Don't spam
✅ **User journey stage** - Adapt accordingly
✅ **Expertise level** - Maintain appropriate complexity

### What NOT to Assume:

❌ User budget (ask if relevant)
❌ User timeline (ask if relevant)
❌ Exact project scope (clarify if vague)
❌ Technical expertise (adapt as you learn)

---

**Total Queries in This Category:** 5 (3 single, 2 multi-turn)
**Difficulty Level:** Moderate to Advanced
**Priority Level:** ⭐⭐ Medium-High (Shows intelligence)
