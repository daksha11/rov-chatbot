# ROV Studios RAG Chatbot - Test Queries

Comprehensive test suite to evaluate chatbot performance based on the optimized system prompt v2.0.

---

## 📁 **Query Categories**

This test suite is organized into the following categories:

1. **[Service Inquiry Tests](01_Service_Inquiry_Tests.md)** (8 queries)
   - Basic service questions
   - Multi-service inquiries

2. **[CTRL-A Toolkit Tests](02_CTRL_A_Toolkit_Tests.md)** (5 queries)
   - Tool recommendations
   - Free-first philosophy validation

3. **[Pricing & Booking Tests](03_Pricing_Booking_Tests.md)** (7 queries)
   - Pricing questions
   - Booking flow enforcement

4. **[Conversation Intelligence Tests](04_Conversation_Intelligence_Tests.md)** (5 queries)
   - Vague/ambiguous questions
   - Context continuity

5. **[Company Information Tests](05_Company_Information_Tests.md)** (7 queries)
   - Brand/philosophy questions
   - Workflow inquiries

6. **[Edge Cases & Fallback Tests](06_Edge_Cases_Fallback_Tests.md)** (7 queries)
   - Out-of-scope questions
   - Insufficient context handling

7. **[Link Handling Tests](07_Link_Handling_Tests.md)** (5 queries)
   - CTA placement
   - Link density validation

8. **[Expertise Level Tests](08_Expertise_Level_Tests.md)** (4 queries)
   - Beginner vs advanced responses
   - Tone adaptation

9. **[Response Quality & Stress Tests](09_Response_Quality_Stress_Tests.md)** (8 queries)
   - Voice & tone consistency
   - Rapid context switching

10. **[Priority Test Set](10_Priority_Test_Set.md)** (10 queries)
    - Quick validation queries
    - Core functionality check

---

## ✅ **Success Metrics**

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

## 📋 **Testing Instructions**

### How to Use This Test Suite

1. **Start with Priority Test Set** - Run the 10 essential queries first
2. **Progress through categories** - Test each category in order
3. **Document responses** - Save actual chatbot responses for analysis
4. **Score each metric** - Use the Success Metrics checklist (1-8) for each response
5. **Note edge cases** - Pay special attention to fallback triggers
6. **Test conversational flow** - Run multi-turn conversations where indicated

### Testing Phases

**Phase 1: Core Functionality**
- Priority Test Set
- Service Inquiry Tests
- Pricing & Booking Tests

**Phase 2: Intelligence & Adaptation**
- Conversation Intelligence Tests
- Company Information Tests
- Expertise Level Tests

**Phase 3: Edge Cases**
- Edge Cases & Fallback Tests
- Link Handling Tests

**Phase 4: Advanced**
- Response Quality & Stress Tests

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

## 📈 **Total Test Coverage**

- **Total Queries:** 56
- **Simple Queries:** ~20
- **Complex Queries:** ~20
- **Multi-turn Conversations:** ~6
- **Edge Cases:** ~10

---

**Created:** 2026-02-24
**Version:** 1.0
**Based on:** OPTIMIZED_SYSTEM_PROMPT v2.0
