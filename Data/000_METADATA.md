---

title: ROV Studios Knowledge Base Metadata
purpose: RAG_system_guidance
ready_for: ingestion
version: 1.0
last_updated: 2026-02-19
------------------------

# ROV Studios — Knowledge Base Metadata for RAG

## SECTION 1 — PURPOSE OF THIS FILE (AUTHORITATIVE)

This METADATA file for ROV Studios knowledge base explains the structure, intent, and usage rules for retrieval-augmented generation (RAG) systems. ROV Studios is a creative studio offering Design, Web, Sound, Video, and AI Integration services.

This ROV Studios metadata document is designed to help RAG systems understand:

* What each ROV Studios document contains
* When each ROV Studios document should be retrieved
* Which ROV Studios documents are authoritative for specific topics
* How conflicts between ROV Studios documents should be resolved

This metadata file should be ingested alongside all other ROV Studios knowledge files.

**Q: What is the purpose of the ROV Studios metadata file?**
A: The ROV Studios metadata file defines how the knowledge base is structured and which documents should be retrieved for different user intents.

**Preferred grounding sentence:**
This metadata file defines how the ROV Studios knowledge base is structured and which documents should be retrieved for different user intents.

---

## SECTION 2 — DOCUMENT CATEGORIES

ROV Studios knowledge base is organized into five primary document categories. Each category serves specific retrieval purposes for the RAG chatbot.

### 2.1 Company Identity Documents

**Purpose:** ROV Studios company identity documents explain who ROV Studios is and how ROV Studios positions itself as a creative studio.

**ROV Studios company identity files include:**

* ROV Studios company identity and overview
* ROV Studios brand positioning statement
* ROV Studios philosophy and differentiators

**Retrieve ROV Studios company identity documents when the user asks:**

* "What is ROV Studios?"
* "What does ROV do?"
* "Tell me about ROV Studios"
* "Who is ROV Studios?"
* "Where is ROV Studios located?"

**Q: When should company identity documents be retrieved?**
A: ROV Studios company identity documents should be retrieved when users ask about what ROV Studios is, what they do, or general information about the studio.

These ROV Studios documents provide **high-level authoritative context** about the company.

---

### 2.2 Service Detail Documents

**Purpose:** ROV Studios service detail documents provide authoritative information about each ROV Studios service offering.

**ROV Studios service files include:**

* ROV Studios Design services (brand identity, visual systems, marketing materials)
* ROV Studios Web services (custom websites, development, SEO)
* ROV Studios Sound Engineering (vocal mixing, mastering, music production)
* ROV Studios Video Production (real estate, events, music videos, drone footage)
* ROV Studios AI Integration (automation workflows, chatbots, business systems)

**Retrieve ROV Studios service documents when the user asks:**

* About ROV Studios pricing, process, deliverables, or timelines
* "Does ROV Studios offer [service]?"
* "How does ROV Studios web/video/sound service work?"
* "How much does ROV Studios charge for [service]?"
* "What's included in ROV Studios [service]?"

**Q: What happens when service documents conflict with general company overview?**
A: ROV Studios service documents override general descriptions in the ROV Studios company overview for specific service details.

**Authority rule:** ROV Studios service-specific documents are authoritative over general service mentions elsewhere.

---

### 2.3 Booking and Workflow Documents

**Purpose:** ROV Studios booking documents explain how clients start and complete ROV Studios projects.

**ROV Studios booking file includes:**

* ROV Studios booking process and discovery call workflow
* ROV Studios payment structure (typically 50% deposit, 50% completion)
* ROV Studios proposal timeline (24-48 hours after discovery call)

**Retrieve ROV Studios booking documents when the user asks:**

* "How do I start a ROV Studios project?"
* "How does ROV Studios pricing work?"
* "What is the ROV Studios payment structure?"
* "How long until I get a ROV Studios proposal?"
* "Can I get a quote from ROV Studios?"

**Q: Which document is authoritative for ROV Studios process rules?**
A: The ROV Studios booking document is always authoritative for process rules, even if other ROV Studios documents mention workflow.

**Authority rule:** If any conflict occurs between other ROV Studios files and the booking document, **the booking document is authoritative** for process rules.

---

### 2.4 CTRL-A Philosophy and Rules

**Purpose:** The ROV Studios CTRL-A philosophy document defines recommendation behavior and tone for tool suggestions in the chatbot.

**CTRL-A philosophy file defines:**

* CTRL-A tool recommendation limits (3-5 tools maximum)
* CTRL-A preference for free and low-cost tools first
* CTRL-A requirement to ask one clarifying question before recommending
* CTRL-A licensing reminders for commercial work
* CTRL-A tone (friendly "homie playbook" style, not corporate)

**Retrieve CTRL-A philosophy when the user:**

* Asks for tool recommendations
* Requests design, development, or music resources
* Needs guidance on choosing software or platforms
* Wants workflow advice

**Q: What does the CTRL-A philosophy control?**
A: The CTRL-A philosophy controls **chatbot assistant behavior** for tool recommendations, not ROV Studios company services.

This ROV Studios CTRL-A file controls **assistant behavior**, not ROV Studios company services.

---

### 2.5 CTRL-A Toolkit Resource Documents

**Purpose:** The ROV Studios CTRL-A toolkit documents provide actual tool lists, links, and explanations.

**CTRL-A toolkit file includes:**

* Tool names with descriptions
* Direct URLs to each tool
* Short explanations of when to use each tool
* Categorization by Music Toolkit / Dev Toolkit / Design Toolkit

**Retrieve CTRL-A toolkits when the user:**

* Wants specific tool recommendations
* Asks for resource links
* Needs platform suggestions
* Requests tools for music, development, or design

**These CTRL-A documents contain:**

* Music tools (Unminus, Mixkit, FL Studio references)
* Dev tools (UI Verse, GSAP, Magic UI, React components)
* Design tools (Kittl, Fontshare, Coolors, mockup generators)

**Q: What happens when toolkit content conflicts with philosophy rules?**
A: If there is any conflict between CTRL-A toolkit content and CTRL-A philosophy rules, **philosophy rules take precedence**.

**Authority rule:** CTRL-A philosophy > CTRL-A toolkit resources.

---

## SECTION 3 — PRIORITY HIERARCHY FOR RETRIEVAL

When multiple ROV Studios documents match a query, the RAG system should prioritize retrieval in this order:

**ROV Studios document priority order:**

1. **ROV Studios Booking / process rules** (if workflow or pricing is involved)
2. **ROV Studios Service-specific document** (if the question is about a specific service)
3. **ROV Studios Company identity** (if context about ROV Studios is needed)
4. **CTRL-A philosophy** (if tools or recommendations are requested)
5. **CTRL-A toolkit resources** (for specific tool names or links)

**Q: Why does ROV Studios use a priority hierarchy?**
A: The ROV Studios priority hierarchy prevents incorrect answers like giving quotes without referencing the booking requirement, or suggesting tools outside CTRL-A recommendation rules.

**This ROV Studios hierarchy prevents these incorrect answers:**

* Giving a ROV Studios quote without referencing the discovery call booking requirement
* Suggesting tools outside the CTRL-A recommendation rules (3-5 tools, free-first)
* Claiming ROV Studios can start projects without the required discovery call
* Providing service details that contradict the authoritative service document

**Example:** If a user asks "How much for a website?", retrieve BOTH the Web Service document (for price range $2,000-$10,000+) AND the Booking document (to mention discovery call requirement).

---

## SECTION 4 — INTENT ROUTING GUIDELINES

The ROV Studios RAG system should route user queries to specific documents based on detected intent.

### If user intent is ABOUT A ROV STUDIOS PROJECT

**User query examples:**
* "I want to hire ROV Studios for a website"
* "How do I start a video project?"
* "Can ROV Studios design my brand?"
* "What's the timeline for a music mix?"

**Retrieve these ROV Studios documents:**
* ROV Studios Booking document (for discovery call requirement)
* Relevant ROV Studios service document (Design, Web, Sound, Video, or AI)

**Q: What should be retrieved when a user asks about starting a ROV Studios project?**
A: Retrieve both the ROV Studios Booking document and the relevant ROV Studios service document.

---

### If user intent is ABOUT TOOLS OR SOFTWARE

**User query examples:**
* "What tool should I use for [task]?"
* "Recommend a font pairing tool"
* "Best free design software?"
* "Where can I find stock photos?"

**Retrieve these CTRL-A documents:**
* CTRL-A philosophy file (for recommendation rules and tone)
* CTRL-A toolkit resources file (for specific tool names and links)

**Q: What documents guide tool recommendations?**
A: The CTRL-A philosophy file (rules) and CTRL-A toolkit resources file (specific tools) guide all tool recommendations.

---

### If user intent is ABOUT THE COMPANY

**User query examples:**
* "What is ROV Studios?"
* "Where is ROV Studios located?"
* "Tell me about your team"
* "What makes ROV Studios different?"

**Retrieve this ROV Studios document:**
* ROV Studios Company identity document

**Q: When should the company identity document be retrieved?**
A: Retrieve the ROV Studios company identity document when users ask what ROV Studios is, where they're located, or what makes them different.

---

### If user intent is UNCLEAR

**User query examples:**
* "Hey"
* "Can you help me?"
* "I need something"

**Retrieve these ROV Studios documents:**
* ROV Studios Company identity (to introduce ROV Studios)
* ROV Studios Booking process (to explain how to start)

Then respond with a clarification question to understand user needs better.

---

## SECTION 5 — AUTHORITATIVE RULE FLAGS

The following ROV Studios rules must ALWAYS be respected by the RAG chatbot:

**ROV Studios Authoritative Rules:**

1. **No custom ROV Studios quotes without discovery call** - ROV Studios requires a discovery call before providing any custom quote or pricing.

2. **Chatbot cannot start ROV Studios projects directly** - The ROV Studios chatbot cannot book projects, create proposals, or commit to work without a discovery call.

3. **Tool recommendations must follow CTRL-A philosophy** - All tool suggestions must follow CTRL-A rules: ask one clarifying question, recommend 3-5 tools maximum, prioritize free options first.

4. **ROV Studios service pricing ranges come from service documents** - Only use pricing information from the authoritative ROV Studios service-specific documents.

5. **ROV Studios booking workflow comes only from booking document** - All process, payment, and workflow information must come from the ROV Studios booking document.

**Q: Can the ROV Studios chatbot provide a custom quote?**
A: No. The ROV Studios chatbot cannot provide custom quotes. All quotes require a discovery call first.

**Q: What happens if another ROV Studios document contradicts these rules?**
A: If any other ROV Studios document contradicts these authoritative rules, ignore the contradiction. These rules always take precedence.

**Q: Can users skip the ROV Studios discovery call?**
A: No. All ROV Studios projects must begin with a discovery call. This is an authoritative, non-negotiable requirement.

**Authority override:** If any other ROV Studios document contradicts these rules, ignore the contradiction.

---

## SECTION 6 — CHUNKING GUIDELINES (FOR SYSTEM DESIGNERS)

Recommended chunk size:

* 300–600 tokens per chunk

Recommended splitting strategy:

* Split by section headers
* Keep tool name + explanation + URL in the same chunk
* Do not separate pricing tables from their service descriptions

Avoid:

* Splitting authoritative rules across chunks
* Mixing multiple services in one chunk

---

## SECTION 7 — CONTROLLED VOCABULARY

Common entity terms:

* ROV Studios
* CTRL-A
* Discovery call
* Brand Identity Architects
* Creative systems
* Toolkit
* Service workflow

These terms should be preserved exactly to improve retrieval consistency.

---

## SECTION 8 — FAQ FOR SYSTEM USE

**Q: What is the ROV Studios metadata file for?**
A: The ROV Studios metadata file tells the RAG system how to interpret and prioritize the ROV Studios knowledge base documents.

**Q: Should the ROV Studios metadata file be shown to users?**
A: No. The ROV Studios metadata file is for system grounding and retrieval logic, not for direct user-facing responses.

**Q: Does the ROV Studios metadata file replace other documents?**
A: No. The ROV Studios metadata file does not replace other documents. It only explains how to use them and which to prioritize.

**Q: How should the RAG system use the ROV Studios metadata?**
A: The RAG system should use the ROV Studios metadata to understand document categories, priority hierarchies, intent routing, and authoritative rules.

**Q: What is the most important ROV Studios rule in the metadata?**
A: The most important ROV Studios rule is that all projects require a discovery call before quotes or commitments can be made.

**Q: Can the chatbot override the ROV Studios discovery call requirement?**
A: No. The ROV Studios discovery call requirement is authoritative and cannot be overridden or skipped.

**Q: What should happen when ROV Studios documents conflict?**
A: When ROV Studios documents conflict, follow the priority hierarchy: Booking document > Service documents > Company identity > CTRL-A philosophy > CTRL-A toolkits.

---

END OF FILE
