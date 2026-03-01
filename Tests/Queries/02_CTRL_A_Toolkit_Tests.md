# CTRL-A Toolkit Tests

Tests for tool recommendation flow, free-first philosophy, and "homie showing you the playbook" energy.

---

## Tool Recommendation Queries

### Query #9
**"What's the best tool for making color palettes?"**

**What This Tests:**
- Clarification question (client vs personal work)
- Free-first recommendations
- 3-5 tool maximum
- 1-line descriptions (not feature dumps)
- Licensing reminder for client work
- Tool link handling (if URLs in context)

**Expected Behavior:**
- Asks clarifying question first (budget/use case/skill level)
- After clarification: recommends Coolors, Adobe Color, Cosmos (if in docs)
- Lists free tools first
- 1-line description per tool
- Includes licensing reminder if client work
- Links to tools (only if URLs in context)

---

### Query #10
**"I need a tool for video editing"**

**What This Tests:**
- Tool recommendation flow
- Free vs paid recommendations
- Skill level adaptation
- CTRL-A voice (practical, not theoretical)

**Expected Behavior:**
- May ask clarifying question (skill level, budget, OS)
- 3-5 tools maximum
- Free options prioritized
- Paid options only if justified
- Brief descriptions
- Homie energy, not salesy

---

### Query #11
**"What do you recommend for design mockups?"**

**What This Tests:**
- 3-5 tool limit enforcement
- Link handling and density
- Tool URL grounding (only if in context)
- Free-first ordering

**Expected Behavior:**
- 3-5 tools max
- Free tools first (Figma free tier, etc.)
- Links only if URLs in retrieved context
- No overwhelming lists
- Actionable recommendations

---

### Query #12
**"Free tools for logo design?"**

**What This Tests:**
- Free-first philosophy
- Clear specification handling
- Appropriate tools for use case
- May warn about limitations

**Expected Behavior:**
- Only recommends free tools
- May mention limitations of free tools for professional use
- 3-5 tool limit still applies
- May suggest ROV services if context is right (not pushy)

---

### Query #13
**"What tool should I use for project management as a freelancer?"**

**What This Tests:**
- Specificity in recommendations
- Audience adaptation (freelancer)
- Practical workflow focus
- Free-first for freelancer budget

**Expected Behavior:**
- Tailored to freelancer needs
- Free or low-cost tools
- Practical workflow recommendations
- No enterprise-level suggestions
- 3-5 tools maximum

---

## CTRL-A Philosophy Validation

### Core Principles to Verify

**1. Free-First Ordering:**
```
✅ Correct:
• Coolors (free)
• Adobe Color (free)
• Huemint ($5)

❌ Wrong:
• Adobe Creative Cloud ($60/mo)
• Coolors (free)
```

**2. Tool Count Limit:**
```
✅ Correct: 3-5 tools
❌ Wrong: 8+ tools (overwhelming)
```

**3. Description Length:**
```
✅ Correct: "Fast palette generation, can extract from images"
❌ Wrong: "Coolors is a comprehensive color palette tool that offers advanced features including extraction from images, color theory algorithms, accessibility checking, export in multiple formats..."
```

**4. Homie Energy:**
```
✅ Correct: "Here's what I'd use for color palettes"
❌ Wrong: "I recommend the following enterprise-grade solutions"
```

---

## Link Handling in CTRL-A Responses

### Rules to Verify

1. **Only link if URLs exist in retrieved context**
   - Don't invent tool URLs
   - Use fallback if no URLs available

2. **Maximum 3-5 tool links per response**
   - Matches tool count limit

3. **Tool name in anchor text:**
   ```
   ✅ [Coolors](url) (free)
   ❌ [Click here](url)
   ```

4. **Link directly to tool, not ROV pages**
   - Unless recommending ROV service

---

## Evaluation Checklist

For each CTRL-A query response, verify:

- ✅ **Free-First:** Free tools listed before paid
- ✅ **Tool Count:** 3-5 tools maximum
- ✅ **Brevity:** 1-line descriptions, not feature dumps
- ✅ **Homie Voice:** Practical, friendly, not corporate
- ✅ **Links Grounded:** Only URLs from context (if any)
- ✅ **Licensing Warning:** Mentioned for client/commercial work
- ✅ **Clarification:** Asks question if request is vague
- ✅ **No Invention:** Doesn't make up tools not in docs

---

## Common Issues to Watch For

❌ Recommending 10+ tools (overwhelming)
❌ Paid tools listed first
❌ Feature dump descriptions (paragraphs per tool)
❌ Inventing tool URLs not in context
❌ Too corporate or salesy tone
❌ Missing licensing reminder for client work
❌ No clarifying question when request is vague

---

## Expected Clarifying Questions

Good examples:
- "What's your budget for this?"
- "Are you designing for a client or personal project?"
- "What's your current skill level with [category]?"
- "What platform are you on (Mac/Windows/browser-based)?"

Bad examples:
- "Tell me everything about your project"
- Multiple questions at once
- Questions that don't impact recommendation

---

**Total Queries in This Category:** 5
**Difficulty Level:** Moderate
**Priority Level:** ⭐⭐⭐ High (Core CTRL-A feature)
