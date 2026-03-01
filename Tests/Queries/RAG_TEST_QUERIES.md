# ROV Studios RAG Chatbot - Test Queries

Comprehensive test suite to evaluate chatbot performance based on the optimized system prompt v2.0.

---

## 🎯 **Service Inquiry Tests**

### Basic Service Questions

1. **"How much for a website?"**
   *Tests: Web pricing, booking flow, link handling*

2. **"Do you do logos?"**
   *Tests: Design service nuance (systems vs one-offs)*

3. **"What's your sound engineering service?"**
   *Tests: Specific service explanation + $50/song pricing*

4. **"Can you help with video production?"**
   *Tests: Video service overview*

5. **"Tell me about your AI integration services"**
   *Tests: AI service explanation*

### Multi-Service Questions

6. **"Do you do branding and video? How much?"**
   *Tests: Multi-intent handling, section organization*

7. **"What services do you offer?"**
   *Tests: Comprehensive service list, brevity*

8. **"I need a logo, website, and some video content"**
   *Tests: Complex multi-service response + unified CTA*

---

## 🧰 **CTRL-A Toolkit Tests**

### Tool Recommendations

9. **"What's the best tool for making color palettes?"**
   *Tests: Clarification question + free-first recommendations*

10. **"I need a tool for video editing"**
    *Tests: Tool recommendation flow*

11. **"What do you recommend for design mockups?"**
    *Tests: 3-5 tool limit, link handling*

12. **"Free tools for logo design?"**
    *Tests: Free-first philosophy*

13. **"What tool should I use for project management as a freelancer?"**
    *Tests: Specificity in recommendations*

---

## 💰 **Pricing & Booking Tests**

### Pricing Questions

14. **"What's the exact price for web development?"**
    *Tests: Pricing range + discovery call requirement*

15. **"Can you give me a quote for branding?"**
    *Tests: Custom-quoted language*

16. **"How much do you charge for sound mixing?"**
    *Tests: Specific $50/song pricing*

17. **"I need pricing for everything - design, web, video, sound"**
    *Tests: Multi-service pricing handling*

### Booking Flow

18. **"How do I get started?"**
    *Tests: Booking guidance*

19. **"Can I book a project right now?"**
    *Tests: Discovery call requirement enforcement*

20. **"What's the booking link?"**
    *Tests: Direct URL request handling*

---

## 🗣️ **Conversation Intelligence Tests**

### Vague/Ambiguous Questions

21. **"I need help with my business"**
    *Tests: Clarification question*

22. **"Can you help me with my brand?"**
    *Tests: Ambiguity detection (new vs existing brand)*

23. **"I want to improve my online presence"**
    *Tests: Multi-faceted intent clarification*

### Follow-up & Context Continuity

24. **Conversation Flow Test #1:**
    - First: **"What services do you offer?"**
    - Then: **"Tell me more about the design one"**
    *Tests: Conversation memory*

25. **Conversation Flow Test #2:**
    - First: **"How much for a website?"**
    - Then: **"What about adding video to that?"**
    *Tests: Context building*

---

## 🏢 **Company Information Tests**

### Brand/Philosophy

26. **"What does ROV stand for?"**
    *Tests: Simple factual answer, no forced links*

27. **"What makes ROV different from other agencies?"**
    *Tests: Brand positioning, value prop*

28. **"Who is ROV Studios?"**
    *Tests: Company overview*

29. **"What's your design philosophy?"**
    *Tests: Brand voice, CTRL-A integration*

### Workflow Questions

30. **"What's your web development process?"**
    *Tests: 6-phase process explanation*

31. **"How long does a typical project take?"**
    *Tests: Timeline info per service*

32. **"What happens after I book a discovery call?"**
    *Tests: Booking workflow clarity*

---

## 🚨 **Edge Cases & Fallback Tests**

### Out-of-Scope Questions

33. **"What do you think about the economy?"**
    *Should trigger fallback*

34. **"How do I market my business?"**
    *Should trigger out-of-scope response*

35. **"What's better, Webflow or WordPress?"**
    *Tests: Tool comparison (may or may not have context)*

36. **"Tell me about your competitors"**
    *Should trigger out-of-scope response*

### Insufficient Context

37. **"What are your office hours?"**
    *Likely triggers fallback (unless in docs)*

38. **"Do you offer refunds?"**
    *Tests: Policy question handling*

39. **"Can I pay in installments?"**
    *Tests: Payment info handling*

---

## 🔗 **Link Handling Tests**

### CTA Placement

40. **"I'm ready to start a web project"**
    *Tests: Booking link placement*

41. **"How can I see examples of your work?"**
    *Tests: Portfolio link handling*

42. **"What's the URL for booking?"**
    *Tests: Direct URL request*

### Link Density

43. **Simple question:** "What is ROV Studios?"
    *Should have 0-1 links max*

44. **Complex question:** "Tell me about your design and web services, and how to get started"
    *Tests: 2-3 link max*

---

## 🎓 **Expertise Level Tests**

### Beginner

45. **"What is brand identity?"**
    *Tests: Beginner explanation, no jargon*

46. **"I don't know anything about web design. Can you help?"**
    *Tests: Supportive, explanatory tone*

### Advanced

47. **"Do you handle brand architecture for multi-product portfolios?"**
    *Tests: Advanced terminology handling*

48. **"What's your tech stack for web development?"**
    *Tests: Technical detail level*

---

## 📊 **Response Quality Tests**

### Voice & Tone

49. **"Why should I choose ROV?"**
    *Tests: Brand voice (confident, not corporate)*

50. **"Are you just another agency?"**
    *Tests: Authentic, conversational tone*

### Brevity & Clarity

51. **"What is sound engineering?"**
    *Should be 2-4 sentences*

52. **"Tell me about all your services, pricing, and how to book"**
    *Tests: Organization, scannability, conciseness*

---

## 🔄 **Stress Tests**

### Rapid Context Switching

53. **Conversation Flow Test #3:**
    - First: **"Web pricing?"**
    - Then: **"Actually, what about sound?"**
    - Then: **"Do you do both?"**
    *Tests: Rapid context switching*

### Repeated Questions

54. **Ask "How much for web development?" twice in conversation**
    *Should reference previous answer*

### Edge Grammar/Spelling

55. **"wat r ur servces?"**
    *Tests: Handling of typos/informal language*

56. **"WEBSITE PRICE???"**
    *Tests: All-caps handling*

---

## ✅ **Success Metrics to Track**

For each query, evaluate:

1. **✅ Grounding:** Only uses retrieved context (no hallucinations)
2. **✅ Accuracy:** Facts match source documents
3. **✅ Voice:** Sounds like ROV (direct, confident, helpful, human)
4. **✅ Links:** Descriptive anchor text, appropriate placement/density
5. **✅ Brevity:** Concise, no filler
6. **✅ CTA:** Clear next step provided
7. **✅ Fallback:** Uses fallback when context insufficient
8. **✅ Clarification:** Asks ONE focused question when ambiguous

---

## 🎯 **Priority Test Set (Quick Validation)**

If you want a **quick 10-query test** to validate core functionality:

1. **"How much for a website?"**
2. **"What services do you offer?"**
3. **"What's the best tool for color palettes?"**
4. **"I need help with my business"**
5. **"What makes ROV different?"**
6. **"How do I get started?"**
7. **"Do you do branding and video? How much?"**
8. **"Tell me about your competitors"** *(should fail gracefully)*
9. **"What's your web development process?"**
10. **"I'm ready to start a project"**

---

## 📋 **Testing Instructions**

### How to Use This Test Suite

1. **Run queries in order** - Start with basic service inquiries, progress to complex scenarios
2. **Document responses** - Save actual chatbot responses for analysis
3. **Score each metric** - Use the Success Metrics checklist (1-8) for each response
4. **Note edge cases** - Pay special attention to fallback triggers and out-of-scope handling
5. **Test conversational flow** - Run multi-turn conversations (queries 24, 25, 53, 54)
6. **Compare against examples** - Reference the example conversations in the system prompt

### Testing Phases

**Phase 1: Core Functionality (Queries 1-20)**
Validate basic service info, pricing, booking flow

**Phase 2: Intelligence & Adaptation (Queries 21-32)**
Test conversation handling, clarification, company info

**Phase 3: Edge Cases (Queries 33-44)**
Verify fallback responses, link handling, out-of-scope detection

**Phase 4: Advanced (Queries 45-56)**
Stress test with expertise levels, voice consistency, rapid switching

---

## 📊 **Results Template**

For tracking results, use this format:

```markdown
### Query #[X]: "[Query text]"

**Response:**
[Paste actual chatbot response]

**Evaluation:**
- ✅/❌ Grounding: [Notes]
- ✅/❌ Accuracy: [Notes]
- ✅/❌ Voice: [Notes]
- ✅/❌ Links: [Notes]
- ✅/❌ Brevity: [Notes]
- ✅/❌ CTA: [Notes]
- ✅/❌ Fallback: [Notes]
- ✅/❌ Clarification: [Notes]

**Overall Score:** X/8

**Issues Found:** [List any problems]
**Improvements Needed:** [Suggestions]
```

---

**Created:** 2026-02-24
**Version:** 1.0
**Based on:** OPTIMIZED_SYSTEM_PROMPT v2.0
