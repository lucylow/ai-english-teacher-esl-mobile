# 🧠 AI English Tutor

### Learn English by Thinking, Speaking, Practicing, and Improving — Not Just Memorizing.

> **An AI-powered React Native English learning platform that combines grammar analysis, RAG-powered curriculum retrieval, Socratic tutoring, roleplay, voice interaction, personalized error correction, multilingual support, and adaptive practice.**

[![React Native](https://img.shields.io/badge/React%20Native-Mobile-blue)](https://reactnative.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-Strict-blue)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-Backend-green)](https://nodejs.org/)
[![AI](https://img.shields.io/badge/AI-Multimodal-purple)](#)
[![RAG](https://img.shields.io/badge/RAG-Curriculum-orange)](#)
[![License](https://img.shields.io/badge/license-MIT-lightgrey)](#)

---

# 📚 Table of Contents

1. [Vision](#-vision)
2. [Product Overview](#-product-overview)
3. [Core Philosophy](#-core-philosophy)
4. [Standout Features](#-standout-features)
5. [Architecture](#-architecture)
6. [System Architecture Diagram](#-system-architecture-diagram)
7. [React Native Architecture](#-react-native-architecture)
8. [AI Architecture](#-ai-architecture)
9. [Automated Error Tagging](#-automated-error-tagging)
10. [RAG Curriculum Engine](#-rag-curriculum-engine)
11. [Hybrid Retrieval](#-hybrid-retrieval)
12. [Socratic Teaching Engine](#-socratic-teaching-engine)
13. [Learning Loop](#-learning-loop)
14. [Roleplay Engine](#-roleplay-engine)
15. [Voice Learning](#-voice-learning)
16. [Accent Coaching](#-accent-coaching)
17. [Multilingual Architecture](#-multilingual-architecture)
18. [Personalized Review](#-personalized-review)
19. [CEFR Progression](#-cefr-progression)
20. [Curriculum System](#-curriculum-system)
21. [Offline Architecture](#-offline-architecture)
22. [Backend Architecture](#-backend-architecture)
23. [API Design](#-api-design)
24. [Database Design](#-database-design)
25. [Security](#-security)
26. [Privacy](#-privacy)
27. [Monetization](#-monetization)
28. [Subscription Architecture](#-subscription-architecture)
29. [Corporate Edition](#-corporate-edition)
30. [Certification](#-certification)
31. [Project Structure](#-project-structure)
32. [Installation](#-installation)
33. [Environment Variables](#-environment-variables)
34. [Development](#-development)
35. [Testing](#-testing)
36. [Deployment](#-deployment)
37. [Performance](#-performance)
38. [Observability](#-observability)
39. [Roadmap](#-roadmap)
40. [Conclusion](#-conclusion)

---

# 🌎 Vision

Learning English should not feel like repeatedly memorizing flashcards.

The goal of **AI English Tutor** is to create a mobile tutor that behaves more like an intelligent teacher.

Instead of simply saying:

> ❌ Wrong sentence.

The tutor should understand:

* what the learner attempted
* what grammatical structure they are using
* what mistake they made
* why the mistake happened
* what English concept is relevant
* what the learner's CEFR level is
* which curriculum lesson explains the problem
* whether the learner understands the correction
* what practice should happen next

The result is an interactive learning loop:

```text
TRY
 │
 ▼
ANALYZE
 │
 ▼
UNDERSTAND
 │
 ▼
QUESTION
 │
 ▼
HINT
 │
 ▼
DISCOVER
 │
 ▼
PRACTICE
 │
 ▼
RETRY
 │
 ▼
MASTER
```

The application is designed around the principle:

> **Don't just give learners the answer. Help them discover the answer.**

---

# 🚀 Product Overview

AI English Tutor is a React Native mobile application backed by an AI teaching platform.

The application combines:

* AI conversation
* grammar analysis
* RAG curriculum retrieval
* CEFR-level lessons
* pronunciation practice
* roleplay
* vocabulary learning
* idioms
* collocations
* cultural context
* multilingual explanations
* personalized review
* offline curriculum
* progress tracking
* subscriptions
* certification

---

# ⭐ Standout Features

## 1. AI Roleplay

Learners can practice realistic scenarios.

Examples:

```text
☕ Ordering Coffee

💼 Job Interview

🏥 Doctor Appointment

🏨 Hotel Check-In

✈️ Airport Conversation

🏫 Classroom Conversation

🛍️ Shopping

📞 Customer Support

🏠 Renting an Apartment

🤝 Meeting Someone New
```

The AI responds naturally while quietly monitoring English quality.

---

# 2. Automated Error Tagging

The system detects errors across multiple dimensions.

```text
Sentence
   │
   ▼
┌─────────────────────┐
│ LanguageTool        │
└─────────┬───────────┘
          │
┌─────────▼───────────┐
│ spaCy NLP           │
└─────────┬───────────┘
          │
┌─────────▼───────────┐
│ Deterministic Rules │
└─────────┬───────────┘
          │
┌─────────▼───────────┐
│ LLM Verification    │
└─────────┬───────────┘
          │
          ▼
      Error Tags
```

Potential categories include:

* syntax
* tense
* article
* preposition
* subject-verb agreement
* spelling
* punctuation
* word choice
* collocation
* naturalness
* vocabulary

---

# 3. RAG-Powered Teaching

Instead of asking an LLM to invent an explanation every time, the application retrieves relevant educational material.

The curriculum can contain:

```text
Grammar Rules
Idioms
Collocations
Vocabulary
Stories
Dialogues
Exercises
Examples
Cultural Notes
Pronunciation Guides
```

The retrieved material becomes the grounding context for the tutor.

---

# 4. Socratic Teaching

The AI intentionally avoids immediately revealing every answer.

For example:

### Learner

```text
Yesterday I go to school.
```

### Detection

```text
Category:
TENSE

Detected:
Present

Context:
"Yesterday"
```

### Tutor

```text
Look at the word "yesterday."

Does it describe something happening now
or something that already happened?
```

The learner thinks.

Then the AI provides a hint.

Then the learner tries again.

Only after the attempt does the tutor reveal the correction.

---

# 🏗️ System Architecture

The platform uses a layered architecture.

```text
                    ┌───────────────────────┐
                    │      React Native     │
                    │       Mobile App      │
                    └───────────┬───────────┘
                                │
                                ▼
                    ┌───────────────────────┐
                    │       API Gateway     │
                    └───────────┬───────────┘
                                │
               ┌────────────────┼────────────────┐
               │                │                │
               ▼                ▼                ▼
        ┌────────────┐   ┌────────────┐   ┌────────────┐
        │ Grammar    │   │ Tutor AI   │   │ Voice      │
        │ Engine     │   │ Engine     │   │ Engine     │
        └─────┬──────┘   └─────┬──────┘   └─────┬──────┘
              │                │                │
              ▼                ▼                ▼
        ┌────────────┐   ┌────────────┐   ┌────────────┐
        │ LanguageTool│  │ RAG Engine │   │ Speech     │
        │ spaCy       │  │ Curriculum │   │ Services   │
        └────────────┘   └─────┬──────┘   └────────────┘
                               │
                               ▼
                        ┌──────────────┐
                        │ Vector Store │
                        └──────────────┘
```

---

# 📱 React Native Architecture

The mobile application is designed around feature-based modules.

```text
src/
│
├── features/
│
├── grammar/
├── tutor/
├── roleplay/
├── voice/
├── pronunciation/
├── vocabulary/
├── lessons/
├── curriculum/
├── rag/
├── review/
├── subscriptions/
├── profile/
└── settings/
```

The mobile app should remain responsible for:

* rendering
* navigation
* local state
* local curriculum cache
* microphone interaction
* audio playback
* animations
* lesson interaction
* user input

Heavy AI processing belongs on the backend.

---

# 🧠 AI Architecture

The AI system is intentionally modular.

```text
                    USER
                     │
                     ▼
              Input Processor
                     │
        ┌────────────┼────────────┐
        ▼            ▼            ▼
      TEXT          VOICE       ROLEPLAY
        │            │            │
        └────────────┼────────────┘
                     ▼
              Language Analysis
                     │
        ┌────────────┼─────────────┐
        ▼            ▼             ▼
     Grammar       Intent       Vocabulary
        │            │             │
        └────────────┼─────────────┘
                     ▼
              Error Resolution
                     │
                     ▼
               RAG Retrieval
                     │
                     ▼
             Curriculum Context
                     │
                     ▼
               Tutor LLM
                     │
                     ▼
             Socratic Response
                     │
                     ▼
                Learner
```

---

# 🔎 Automated Error Tagging

Error tagging is one of the most important components of the platform.

The system should not depend exclusively on an LLM.

Instead:

```text
             English Sentence
                    │
                    ▼
          ┌──────────────────┐
          │ LanguageTool     │
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ spaCy Parser     │
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ Rule Engine      │
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ LLM Verification │
          └────────┬─────────┘
                   │
                   ▼
          ┌──────────────────┐
          │ Error Resolver   │
          └────────┬─────────┘
                   │
                   ▼
             GrammarError[]
```

---

# 🧩 Error Object

A standardized error object makes the entire application easier to build.

```typescript
interface GrammarError {
  id: string;

  category:
    | "syntax"
    | "tense"
    | "article"
    | "preposition"
    | "agreement"
    | "collocation"
    | "word-choice"
    | "spelling"
    | "punctuation"
    | "style"
    | "unknown";

  source:
    | "languagetool"
    | "spacy"
    | "llm"
    | "rule"
    | "rag";

  start: number;

  end: number;

  original: string;

  message: string;

  suggestion?: string;

  confidence: number;
}
```

This creates a consistent contract between:

```text
Backend
   ↓
API
   ↓
React Native
   ↓
UI
   ↓
Review Engine
```

---

# 🔬 Multi-Detector Architecture

Multiple detectors can disagree.

Therefore the platform includes an error resolution layer.

```text
LanguageTool
     │
     ├───────┐
     │       │
     ▼       ▼
   ERROR   ERROR
     │       │
     └───┬───┘
         ▼
    Deduplication
         │
         ▼
    Confidence
         │
         ▼
     Priority
         │
         ▼
  LLM Verification
         │
         ▼
    Final Error
```

The goal is not to overwhelm learners with every possible issue.

The tutor should generally prioritize the most educationally important error.

---

# 📚 RAG Curriculum Engine

The RAG engine connects AI tutoring to curated educational material.

The curriculum is organized into documents.

```typescript
interface CurriculumDocument {
  id: string;

  title: string;

  type:
    | "grammar"
    | "idiom"
    | "story"
    | "dialogue"
    | "collocation"
    | "vocabulary";

  level:
    | "A1"
    | "A2"
    | "B1"
    | "B2"
    | "C1"
    | "C2";

  topic: string;

  content: string;

  keywords: string[];
}
```

---

# 🧱 Curriculum Pipeline

```text
Curriculum Authoring
        │
        ▼
Document Validation
        │
        ▼
Sanitization
        │
        ▼
Chunking
        │
        ▼
Embedding
        │
        ▼
Vector Store
        │
        ▼
Retriever
        │
        ▼
Tutor Context
```

---

# 🔀 Hybrid Retrieval

The application can combine semantic and keyword retrieval.

```text
                  User Problem
                       │
            ┌──────────┴──────────┐
            ▼                     ▼
     Keyword Search        Semantic Search
            │                     │
            ▼                     ▼
       Exact Terms          Similar Concepts
            │                     │
            └──────────┬──────────┘
                       ▼
                  Merge Results
                       │
                       ▼
                  Deduplicate
                       │
                       ▼
                  Rank Results
                       │
                       ▼
                  Context Limit
                       │
                       ▼
                    LLM
```

This is particularly useful for language education because some queries contain exact grammatical terminology while others are expressed naturally by learners.

For example:

```text
"I don't know when to use have been"
```

should retrieve material about:

```text
Present Perfect
Present Perfect Continuous
Past Simple
```

even though the learner never used those technical terms.

---

# 🎓 CEFR-Aware Retrieval

Every curriculum document is associated with a CEFR level.

```text
A1
 │
 ├── Basic vocabulary
 ├── Simple sentences
 └── Present tense

A2
 │
 ├── Past tense
 ├── Common prepositions
 └── Daily conversations

B1
 │
 ├── Complex sentences
 ├── Idioms
 └── Workplace English

B2
 │
 ├── Nuanced vocabulary
 ├── Advanced grammar
 └── Natural conversation

C1
 │
 ├── Academic English
 ├── Professional communication
 └── Advanced idiomatic language

C2
 │
 ├── Precision
 ├── Style
 └── Near-native expression
```

The retrieval layer uses the learner's level to reduce irrelevant results.

---

# 🧑‍🏫 Socratic Teaching Engine

The tutor is designed to teach rather than merely correct.

The teaching state can be represented as:

```text
QUESTION
   │
   ▼
HINT
   │
   ▼
LEARNER ATTEMPT
   │
   ├───────────────┐
   │               │
   ▼               ▼
CORRECT          INCORRECT
   │               │
   ▼               ▼
PRACTICE          MORE HINT
   │               │
   └───────┬───────┘
           ▼
        MASTERY
```

---

# 🧠 Socratic Prompt Architecture

A grounded tutor prompt should contain:

```text
Learner Level
+
Detected Error
+
Error Category
+
Curriculum References
+
Conversation Context
+
Teaching Objective
+
Response Constraints
```

Example:

```text
Learner Level: B1

Error:
Incorrect past tense

Detected sentence:
"Yesterday I go to school."

Curriculum:
Past Simple lesson

Teaching objective:
Help learner recognize past-time markers.

Behavior:
Ask a question first.
Do not immediately reveal the answer.
Provide a hint if needed.
Then explain.
Finally create a practice question.
```

---

# 🔄 Complete Learning Loop

The central educational loop is:

```text
┌──────────────┐
│ Learner Input│
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Analyze      │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Tag Errors   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Retrieve     │
│ Curriculum   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Ask Question │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Learner      │
│ Attempts     │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Evaluate     │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Practice     │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Reattempt    │
└──────────────┘
```

---

# ☕ Roleplay Engine

Roleplay transforms grammar practice into realistic communication.

A roleplay session contains:

```typescript
interface RoleplaySession {
  id: string;

  scenario: string;

  learnerRole: string;

  tutorRole: string;

  level: CEFRLevel;

  objectives: string[];

  conversation: ConversationTurn[];
}
```

Example:

```text
Scenario:
Ordering Coffee

Learner:
Customer

AI:
Barista

Objective:
Practice polite requests.
```

The AI can track:

```text
Grammar
Vocabulary
Politeness
Naturalness
Turn-taking
Comprehension
```

---

# 🎭 Roleplay Architecture

```text
              Scenario
                  │
                  ▼
          Roleplay Generator
                  │
                  ▼
            AI Character
                  │
                  ▼
            Conversation
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
     Grammar   Vocabulary  Naturalness
        │         │         │
        └─────────┼─────────┘
                  ▼
            Tutor Feedback
                  │
                  ▼
            Continue Scene
```

The tutor should avoid interrupting every sentence.

Instead, it can maintain the conversation and provide feedback at appropriate moments.

---

# 🎤 Voice Learning

Voice interaction is a major part of the application.

The voice architecture is:

```text
Microphone
    │
    ▼
Audio Capture
    │
    ▼
Speech-to-Text
    │
    ▼
Transcript
    │
    ├──────────────┐
    ▼              ▼
Grammar         Pronunciation
Analysis         Analysis
    │              │
    └──────┬───────┘
           ▼
       Tutor AI
           │
           ▼
       Voice Reply
           │
           ▼
        Speaker
```

---

# 🗣️ Instant Pronunciation Coaching

The application can connect recognized speech to pronunciation feedback.

Potential feedback:

```text
Word:
comfortable

Learner pronunciation:
Needs practice

Tip:
Try stressing the first syllable less strongly.
```

The application should keep pronunciation feedback educational and encouraging rather than judgmental.

---

# 🔤 Multilingual Architecture

The tutor can explain English concepts in the learner's preferred language.

Architecture:

```text
Learner Language
       │
       ▼
English Learning Layer
       │
       ├── English Input
       ├── English Grammar
       ├── English Vocabulary
       └── English Examples
       │
       ▼
Explanation Layer
       │
       ▼
Preferred Language
```

Importantly, the underlying English curriculum remains English-focused.

The learner's native language is used as a support layer.

---

# 🌍 Localization

Recommended localization structure:

```text
locales/
├── en/
│   ├── common.json
│   ├── grammar.json
│   └── lessons.json
│
├── fr/
├── es/
├── pt/
├── de/
├── it/
├── ar/
├── zh/
├── ja/
└── ko/
```

Example:

```json
{
  "tutor": {
    "checkAnswer": "Check Answer",
    "tryAgain": "Try Again",
    "greatJob": "Great job!"
  }
}
```

---

# 🧠 Personalized Review

The review system turns detected mistakes into future practice.

```text
Learner Sentence
       │
       ▼
Grammar Error
       │
       ▼
Error Category
       │
       ▼
Review Item
       │
       ▼
Practice
       │
       ▼
Correct?
   ┌───┴───┐
   │       │
  YES      NO
   │       │
   ▼       ▼
Reduce   Revisit
Priority Lesson
```

The goal is to convert mistakes into personalized learning material.

---

# 🃏 Smart Review Cards

Example:

```text
┌─────────────────────────────┐
│       PAST SIMPLE            │
│                              │
│ Yesterday I ___ to school.   │
│                              │
│        [ Answer ]             │
└─────────────────────────────┘
```

The application can then explain why the answer works.

---

# 📈 CEFR Progression

The system supports:

```text
A1 → A2 → B1 → B2 → C1 → C2
```

Each level can contain:

```text
Grammar
Vocabulary
Speaking
Listening
Reading
Writing
Pronunciation
Conversation
Cultural Context
```

The tutor should not arbitrarily advance a learner based on a single interaction.

Instead, progression should be based on curriculum completion and repeated successful practice.

---

# 📖 Curriculum System

The curriculum should be structured as a graph rather than a flat list.

```text
A1
 │
 ├── Introductions
 │     ├── Vocabulary
 │     ├── Grammar
 │     └── Speaking
 │
 ├── Daily Routine
 │     ├── Present Simple
 │     └── Time Expressions
 │
 └── Shopping
       ├── Numbers
       ├── Prices
       └── Requests
```

Advanced lessons can depend on foundational concepts.

---

# 🧭 Lesson Dependency Graph

```text
Vocabulary
    │
    ▼
Simple Sentences
    │
    ▼
Present Simple
    │
    ▼
Past Simple
    │
    ▼
Future Forms
    │
    ▼
Complex Sentences
    │
    ▼
Advanced Grammar
```

This allows the tutor to recognize prerequisite gaps.

---

# 💾 Offline Architecture

The mobile application should support selected offline functionality.

```text
             Mobile App
                 │
       ┌─────────┴─────────┐
       ▼                   ▼
 Online API           Local Storage
       │                   │
       ▼                   ▼
 AI Features         Cached Curriculum
       │                   │
       ▼                   ▼
 Cloud RAG            Offline Lessons
```

Offline functionality can include:

* downloaded lessons
* vocabulary
* grammar explanations
* previously downloaded stories
* practice exercises
* review cards

AI-heavy operations can gracefully fall back to offline lessons.

---

# 🏢 Backend Architecture

A scalable backend can be organized into services.

```text
API Gateway
    │
    ├── Auth Service
    │
    ├── Tutor Service
    │
    ├── Grammar Service
    │
    ├── RAG Service
    │
    ├── Voice Service
    │
    ├── Curriculum Service
    │
    ├── Subscription Service
    │
    └── Certification Service
```

---

# 🔌 API Architecture

Example endpoints:

```text
POST /auth/login

POST /grammar/analyze

POST /grammar/verify

POST /tutor/teach

POST /tutor/practice

POST /tutor/check-answer

POST /roleplay/start

POST /roleplay/message

POST /voice/transcribe

POST /pronunciation/analyze

POST /curriculum/search

GET  /curriculum/lesson/:id

POST /review/create

GET  /review/items

POST /subscriptions/checkout

POST /certification/start
```

---

# 🗄️ Database Architecture

A relational database can store application state.

```text
Users
 │
 ├── Profiles
 │
 ├── Learning Preferences
 │
 ├── Enrollments
 │
 ├── Review Items
 │
 ├── Roleplay Sessions
 │
 ├── Lessons
 │
 ├── Subscription
 │
 └── Certificates
```

Conceptual schema:

```text
users
  │
  ├── user_profiles
  │
  ├── learner_preferences
  │
  ├── review_items
  │
  ├── roleplay_sessions
  │
  ├── lesson_progress
  │
  ├── subscriptions
  │
  └── certificates
```

---

# 🔐 Security Architecture

The application should use:

```text
HTTPS
JWT / secure sessions
Server-side API keys
Input validation
Rate limiting
RBAC
Encrypted storage
Secure token handling
Audit logging
```

AI provider keys must never be embedded in the React Native bundle.

Bad:

```typescript
const API_KEY = "secret-key";
```

Good:

```text
React Native
      │
      ▼
Your Backend
      │
      ▼
AI Provider
```

---

# 🛡️ AI Safety

The tutor should include guardrails around:

* hallucinated curriculum
* inappropriate content
* unsafe advice
* prompt injection
* curriculum poisoning
* malicious retrieved content
* excessive correction
* inappropriate personalization

Retrieved curriculum should be treated as reference material rather than executable instructions.

---

# 🔒 RAG Security

A protected RAG pipeline should look like:

```text
Curriculum
   │
   ▼
Validation
   │
   ▼
Sanitization
   │
   ▼
Chunking
   │
   ▼
Embedding
   │
   ▼
Vector Store
   │
   ▼
Retriever
   │
   ▼
Context Filter
   │
   ▼
Tutor
```

Curriculum content should never be allowed to override application-level system instructions.

---

# 💳 Monetization

The application supports multiple revenue streams.

## Freemium

Free users can receive:

```text
Basic Lessons
Limited AI Conversations
Daily Practice
Basic Grammar Checking
Selected Roleplay
```

Premium users can unlock:

```text
Unlimited AI Tutor
Advanced Roleplay
Advanced Grammar Feedback
Voice Practice
Pronunciation Coaching
Expanded Curriculum
Personalized Review
Advanced Stories
Certification Preparation
```

---

# 💰 Subscription Architecture

```text
                    User
                      │
                      ▼
                Subscription
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
        FREE                   PREMIUM
          │                       │
          ▼                       ▼
      Basic AI               Full AI
      Lessons                Roleplay
      Limited Chat          Voice
      Limited Review        RAG
                             Advanced
```

The application should use the platform's official in-app purchase mechanisms for digital subscriptions.

---

# 👩‍🏫 Optional Human Tutoring

A future marketplace can connect learners with human tutors.

```text
Learner
   │
   ▼
AI Tutor
   │
   ├── Identifies weak areas
   │
   ▼
Human Tutor
   │
   ▼
Targeted Session
```

The AI becomes a preparation and reinforcement layer rather than replacing human teachers.

---

# 🏢 Corporate Edition

The platform can support organizations.

Potential customers:

```text
Companies
Schools
Universities
Training Programs
Language Institutes
Workforce Programs
```

Corporate dashboards can manage:

```text
Seats
Curriculum
Learning Programs
Roleplay Scenarios
Certificates
Access Policies
```

---

# 🏆 Certification

The platform can offer structured assessments.

```text
Preparation
    │
    ▼
Practice
    │
    ▼
Mock Assessment
    │
    ▼
Final Assessment
    │
    ▼
Score
    │
    ▼
Certificate
```

Certificates should clearly describe what was assessed and should not imply accreditation by an external institution unless such accreditation actually exists.

---

# 📁 Recommended Project Structure

```text
ai-english-tutor/
│
├── mobile/
│   ├── src/
│   │   ├── components/
│   │   ├── features/
│   │   │   ├── grammar/
│   │   │   ├── tutor/
│   │   │   ├── roleplay/
│   │   │   ├── voice/
│   │   │   ├── pronunciation/
│   │   │   ├── lessons/
│   │   │   ├── review/
│   │   │   └── subscriptions/
│   │   │
│   │   ├── navigation/
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── store/
│   │   ├── i18n/
│   │   └── screens/
│   │
│   ├── app.json
│   └── package.json
│
├── server/
│   ├── src/
│   │   ├── api/
│   │   ├── auth/
│   │   ├── grammar/
│   │   ├── tutor/
│   │   ├── rag/
│   │   ├── curriculum/
│   │   ├── voice/
│   │   ├── roleplay/
│   │   ├── subscriptions/
│   │   └── certification/
│   │
│   └── package.json
│
├── curriculum/
│   ├── grammar/
│   ├── idioms/
│   ├── stories/
│   ├── vocabulary/
│   └── dialogues/
│
├── docs/
│   ├── architecture/
│   ├── api/
│   └── curriculum/
│
└── README.md
```

---

# ⚙️ Installation

## Requirements

Recommended development environment:

```text
Node.js
npm / pnpm
React Native / Expo
TypeScript
PostgreSQL
Redis
Python
spaCy
LanguageTool
Vector database
```

Clone the project:

```bash
git clone https://github.com/YOUR_USERNAME/ai-english-tutor.git

cd ai-english-tutor
```

Install mobile dependencies:

```bash
cd mobile

npm install
```

Install backend dependencies:

```bash
cd ../server

npm install
```

---

# 🐍 NLP Environment

The NLP service can use Python.

Example:

```bash
python -m venv .venv

source .venv/bin/activate

pip install spacy
```

Install an English model appropriate for your deployment:

```bash
python -m spacy download en_core_web_sm
```

---

# 🔑 Environment Variables

Example:

```env
NODE_ENV=development

DATABASE_URL=

REDIS_URL=

AI_PROVIDER_API_KEY=

LANGUAGE_TOOL_URL=

VECTOR_DATABASE_URL=

VECTOR_DATABASE_API_KEY=

AUTH_SECRET=

STORAGE_BUCKET=

STORAGE_REGION=
```

Never commit production credentials.

Add:

```text
.env
.env.local
.env.production
```

to `.gitignore`.

---

# ▶️ Development

Start the backend:

```bash
npm run dev
```

Start the mobile application:

```bash
cd mobile

npm start
```

Run the application using the desired development platform.

---

# 🧪 Testing Strategy

Testing should occur at multiple levels.

```text
Unit Tests
     │
     ▼
Integration Tests
     │
     ▼
API Tests
     │
     ▼
RAG Tests
     │
     ▼
Tutor Tests
     │
     ▼
Mobile Tests
     │
     ▼
End-to-End Tests
```

---

# 🧪 Grammar Tests

Example:

```typescript
describe(
  "past tense detection",
  () => {
    it(
      "detects present tense after yesterday",
      async () => {
        const errors =
          await analyzeEnglish(
            "Yesterday I go to school."
          );

        expect(
          errors.some(
            error =>
              error.category ===
              "tense"
          )
        ).toBe(true);
      }
    );
  }
);
```

---

# 🧪 RAG Tests

RAG tests should verify that the correct curriculum is retrieved.

Example:

```text
Query:

"I don't understand yesterday + verbs"

Expected:

Past Simple curriculum
```

Another:

```text
Query:

"make or do a decision"

Expected:

Collocation curriculum
```

---

# 🧪 Socratic Tests

The tutor should be tested for educational behavior.

Bad:

```text
Wrong.
Use "went."
```

Preferred:

```text
Look at "yesterday."

Does the action happen now
or did it already happen?
```

The system should verify that the tutor does not unnecessarily reveal answers immediately.

---

# 📊 Performance Architecture

The system should avoid sending unnecessary requests.

```text
User Typing
    │
    ▼
Debounce
    │
    ▼
Local Validation
    │
    ▼
Backend Request
    │
    ▼
Parallel NLP
    │
    ├── LanguageTool
    └── spaCy
    │
    ▼
LLM Only When Needed
    │
    ▼
RAG
```

This architecture reduces unnecessary AI calls and improves responsiveness.

---

# ⚡ Caching

Useful caches include:

```text
Curriculum Cache
Grammar Result Cache
RAG Result Cache
Lesson Cache
Voice Asset Cache
Roleplay Template Cache
```

Frequently accessed curriculum content can be cached locally.

---

# 📡 Observability

Production systems should monitor technical health.

Examples:

```text
API latency
Error rates
AI request failures
Timeouts
RAG retrieval failures
Database errors
Voice processing failures
Subscription failures
```

Avoid collecting unnecessary learner content merely for telemetry.

---

# 🧠 AI Provider Abstraction

The AI layer should not be tightly coupled to one provider.

```typescript
interface AIProvider {
  generate(input: {
    system?: string;
    user: string;
  }): Promise<{
    text: string;
  }>;
}
```

This enables:

```text
Provider A
Provider B
Provider C
Local Model
Mock Provider
```

without rewriting the tutoring system.

---

# 🔄 Provider Routing

```text
                AI Request
                    │
                    ▼
             Provider Router
                    │
          ┌─────────┼─────────┐
          ▼         ▼         ▼
       Primary   Fallback   Local
          │         │         │
          └─────────┼─────────┘
                    ▼
                Response
```

The routing layer can consider:

* availability
* latency
* task type
* token budget
* model capability

---

# 🧠 Specialized AI Agents

Future versions can split tutoring responsibilities.

```text
                    Tutor Orchestrator
                           │
       ┌───────────────────┼───────────────────┐
       ▼                   ▼                   ▼
 Grammar Agent       Vocabulary Agent    Conversation Agent
       │                   │                   │
       └───────────────────┼───────────────────┘
                           ▼
                     Teaching Agent
                           │
                           ▼
                       Learner
```

The agents should remain constrained by a central teaching policy.

---

# 🗣️ Conversation Intelligence

During a conversation, the AI can distinguish:

```text
Content
Grammar
Vocabulary
Pronunciation
Intent
Context
Turn-taking
```

Example:

```text
Learner:
"I go yesterday to Toronto."

Detected:
Tense
Word order

Tutor:
"I understood you. Let's look at
when the action happened first."
```

This maintains conversational confidence while teaching.

---

# 🌎 Cultural Context

English learning should include language in context.

Examples:

```text
Idioms
Slang
Politeness
Workplace conventions
Small talk
Email etiquette
Regional expressions
Conversation norms
```

The curriculum should clearly label expressions by region when appropriate.

---

# 🎮 Gamification

Optional game mechanics can include:

```text
Daily Streak
XP
Lesson Completion
Roleplay Missions
Vocabulary Challenges
Conversation Quests
Achievement Badges
```

The focus should remain learning rather than compulsive engagement.

---

# 🧩 Dynamic UI

The application should feel alive rather than static.

Possible animations:

```text
AI Thinking
Speech Waveform
Correct Answer Celebration
Error Highlight
Lesson Completion
Progress Animation
Roleplay Character Motion
Microphone Pulse
Vocabulary Flip
```

Animations should remain accessible and respect reduced-motion preferences.

---

# 🎨 UI Architecture

Example screen hierarchy:

```text
Home
 │
 ├── Continue Learning
 │
 ├── Daily Challenge
 │
 ├── Speak
 │
 ├── Roleplay
 │
 ├── Review
 │
 └── Explore
       │
       ├── Grammar
       ├── Stories
       ├── Idioms
       └── Vocabulary
```

---

# 🏠 Home Screen

The home screen should answer three questions:

```text
What should I do now?

What am I learning?

What should I practice?
```

Example:

```text
Good morning 👋

Today's Mission
─────────────────

🎯 Practice Past Tense

3 minute lesson

[ Start ]

Continue
─────────

☕ Coffee Roleplay
72% complete

Review
──────

5 grammar items
ready for practice
```

---

# 🎯 Daily Three-Minute Challenge

The application can create a compact learning loop.

```text
00:00
Prompt

01:00
Learner response

02:00
AI coaching

03:00
Practice + completion
```

A challenge might focus on one concept:

```text
Today's Focus:

Past Simple

Goal:

Describe something you
did yesterday.
```

---

# 🧠 Intelligent Difficulty

Difficulty can change within a lesson.

```text
Easy
 │
 ▼
Correct
 │
 ▼
Moderate
 │
 ▼
Correct
 │
 ▼
Advanced
```

If the learner struggles:

```text
Advanced
   │
   ▼
Hint
   │
   ▼
Simplified Example
   │
   ▼
Retry
```

This creates adaptive teaching without requiring a complex data-analysis system.

---

# 🛠️ Developer Principles

The project follows several principles.

## Principle 1 — AI Is a Teacher

Not merely an answer generator.

## Principle 2 — Curriculum Is Ground Truth

RAG should anchor educational explanations.

## Principle 3 — Errors Become Lessons

Every meaningful mistake can become practice.

## Principle 4 — Don't Overcorrect

Not every stylistic difference needs to become an error.

## Principle 5 — Explain at the Learner's Level

A1 explanations should not sound like C2 linguistics lectures.

## Principle 6 — Keep Human Agency

The learner should think and respond.

---

# 🚧 Common Failure Modes

## Failure 1 — LLM-only grammar correction

Problem:

```text
LLM
 ↓
Correction
```

This can produce inconsistent classifications.

Solution:

```text
NLP
+
Rules
+
LLM verification
```

---

## Failure 2 — RAG without curriculum quality

Retrieval cannot fix poor educational material.

Solution:

```text
Curated Curriculum
        +
Good Chunking
        +
Hybrid Retrieval
        +
Grounded Prompting
```

---

## Failure 3 — Overwhelming learners

Showing ten grammar errors after every sentence can discourage learners.

Solution:

```text
Detect many
     ↓
Prioritize
     ↓
Teach one or two
     ↓
Practice
```

---

# 🗺️ Roadmap

## Phase 1 — Foundation

```text
[x] React Native foundation
[x] TypeScript
[x] Tutor UI
[x] Grammar API
[x] Curriculum model
```

## Phase 2 — Intelligent Tutoring

```text
[ ] LanguageTool integration
[ ] spaCy integration
[ ] Error normalization
[ ] Error prioritization
[ ] RAG retrieval
[ ] Socratic teaching
```

## Phase 3 — Conversation

```text
[ ] Roleplay
[ ] Voice input
[ ] Speech recognition
[ ] AI voice output
[ ] Pronunciation coaching
```

## Phase 4 — Personalization

```text
[ ] Smart review
[ ] CEFR progression
[ ] Vocabulary goals
[ ] Personalized curriculum
```

## Phase 5 — Monetization

```text
[ ] Subscription
[ ] Premium lessons
[ ] Advanced roleplay
[ ] Certification
[ ] Corporate accounts
```

## Phase 6 — Scale

```text
[ ] Multi-provider AI
[ ] Global localization
[ ] Offline curriculum
[ ] Enterprise infrastructure
[ ] Teacher marketplace
```

---

# 🏆 Long-Term Product Vision

The ultimate goal is to evolve the application from an English practice app into an **AI language-learning operating system**.

```text
                 AI ENGLISH TUTOR
                        │
      ┌─────────────────┼─────────────────┐
      │                 │                 │
      ▼                 ▼                 ▼
    LEARN             SPEAK             WRITE
      │                 │                 │
      ▼                 ▼                 ▼
   Lessons           Roleplay          Grammar
   Stories           Voice             RAG
   Vocabulary        Pronunciation     Feedback
      │                 │                 │
      └─────────────────┼─────────────────┘
                        ▼
                  PERSONAL TUTOR
                        │
                        ▼
                   LEARNER MODEL
                        │
                        ▼
                ADAPTIVE CURRICULUM
```

---

# 💡 Why This Product Can Stand Out

Most language-learning applications focus heavily on:

```text
Vocabulary
Flashcards
Multiple Choice
Fixed Lessons
```

This product focuses on:

```text
Real Conversation
+
AI Teaching
+
Error Diagnosis
+
Curriculum Retrieval
+
Socratic Questioning
+
Voice
+
Roleplay
+
Personalized Practice
```

The differentiation is therefore not simply:

> "We have an AI chatbot."

It is:

> **"We built an AI tutor that understands how you make English mistakes and teaches you how to correct them."**

---

# 🧬 Core Technical Differentiator

The most important architecture is:

```text
                  LEARNER
                     │
                     ▼
               ┌───────────┐
               │   INPUT   │
               └─────┬─────┘
                     │
                     ▼
          ┌────────────────────┐
          │ LANGUAGE ANALYSIS  │
          └─────────┬──────────┘
                    │
        ┌───────────┼────────────┐
        ▼           ▼            ▼
     Grammar     Vocabulary    Context
        │           │            │
        └───────────┼────────────┘
                    ▼
             ERROR TAGGING
                    │
                    ▼
              RAG RETRIEVAL
                    │
                    ▼
           CURRICULUM CONTEXT
                    │
                    ▼
              SOCRATIC AI
                    │
             ┌──────┴──────┐
             ▼             ▼
          QUESTION       HINT
             │             │
             └──────┬──────┘
                    ▼
                LEARNER
                    │
                    ▼
                  RETRY
                    │
                    ▼
                PRACTICE
                    │
                    ▼
                 MASTERY
```

This is the heart of the platform.

---

# 📦 Example End-to-End Request

A learner submits:

```text
"I have went to the store yesterday."
```

The pipeline becomes:

```text
INPUT
 │
 ▼
LanguageTool
 │
 ▼
spaCy
 │
 ▼
Rule Engine
 │
 ▼
LLM Verification
 │
 ▼
Detected:
Past tense / verb form
 │
 ▼
RAG
 │
 ▼
Past Simple Curriculum
 │
 ▼
Socratic Question
 │
 ▼
"Look at 'yesterday'.
Which tense usually describes
a completed action in the past?"
 │
 ▼
Learner Attempts
 │
 ▼
Tutor Hint
 │
 ▼
Correction
 │
 ▼
Practice
 │
 ▼
"Yesterday I ___ to the store."
```

The system has transformed a mistake into a complete educational experience.

---

# 🧪 Example Tutor Session

### Learner

```text
I have went to the store yesterday.
```

### AI

```text
Let's look at the time expression first.

Does "yesterday" describe something
that is connected to now, or something
that finished in the past?
```

### Learner

```text
Finished in the past.
```

### AI

```text
Exactly.

Now look at the verb "have went."

Can you think of a simple past form
of "go"?
```

### Learner

```text
Went.
```

### AI

```text
Great.

A natural version is:

"I went to the store yesterday."

Now try this:

"Last weekend, I ___ to the park."
```

This is the core teaching philosophy.

---

# 🧭 Product Architecture Summary

```text
┌─────────────────────────────────────────────┐
│                MOBILE CLIENT                │
│                                             │
│ React Native + TypeScript                   │
│                                             │
│ Lessons • Roleplay • Voice • Review         │
└──────────────────────┬──────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────┐
│                 API LAYER                   │
│                                             │
│ Auth • Tutor • Grammar • Voice • RAG        │
└──────────────────────┬──────────────────────┘
                       │
         ┌─────────────┼─────────────┐
         ▼             ▼             ▼
┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ NLP ENGINE  │ │ RAG ENGINE  │ │ AI ENGINE   │
│             │ │             │ │             │
│ spaCy       │ │ Curriculum  │ │ LLM         │
│ LanguageTool│ │ Retrieval   │ │ Orchestrator│
│ Rules       │ │ Embeddings  │ │ Guardrails  │
└──────┬──────┘ └──────┬──────┘ └──────┬──────┘
       │               │               │
       └───────────────┼───────────────┘
                       ▼
              ┌────────────────┐
              │ Tutor Response │
              └────────────────┘
```

---

# 🚀 Future Expansion

The architecture is intentionally extensible.

Potential future capabilities include:

```text
AI pronunciation coach
AI conversation partner
AI writing coach
AI interview coach
AI presentation coach
AI workplace English coach
AI travel English coach
AI academic English coach
AI exam preparation
AI children's English mode
Teacher dashboard
School dashboard
Corporate training
Certification
```

The same underlying engine can power each experience.

---

# 🧠 Final Architecture Principle

The application should always follow this hierarchy:

```text
                    CURRICULUM
                        │
                        ▼
                    TEACHING
                        │
                        ▼
                       AI
                        │
                        ▼
                  PERSONALIZATION
                        │
                        ▼
                     LEARNER
```

Not:

```text
AI
 │
 ▼
Random Answer
```

The AI is the teaching engine.

The curriculum provides educational grounding.

The grammar engine identifies opportunities to teach.

The RAG engine finds the right material.

The Socratic engine turns that material into an interaction.

The learner ultimately does the thinking.

---

# ❤️ Mission

**AI English Tutor exists to make English learning feel less like studying and more like having a great teacher available whenever you need one.**

Every mistake becomes an opportunity.

Every conversation becomes practice.

Every lesson becomes personalized.

Every interaction moves the learner one step closer to confident English communication.

---

# 📄 License

This project is intended as a foundation for an AI-powered language-learning product.

Add the appropriate license and third-party attribution notices before distributing the application commercially.

---

# ⭐ Contributing

Contributions are welcome.

Recommended contribution areas:

```text
Grammar Rules
Curriculum
RAG Retrieval
React Native UI
Accessibility
Localization
Voice
Pronunciation
Roleplay
Testing
Developer Experience
Security
```

Before submitting a pull request:

```bash
npm run lint
npm test
npm run build
```

---

# 🎯 Final Product Definition

> **AI English Tutor is a multimodal, RAG-grounded, Socratic English learning platform that detects learner mistakes, retrieves the exact curriculum needed to explain them, guides learners toward their own corrections, and turns every interaction into targeted practice.**

The long-term objective is simple:

```text
                 DON'T JUST CORRECT.
                       ↓
                    TEACH.
                       ↓
                  DON'T JUST TEACH.
                       ↓
                   PRACTICE.
                       ↓
                DON'T JUST PRACTICE.
                       ↓
                   IMPROVE.
```

**Build the tutor. Build the curriculum. Build the learning loop.**

**Then let the learner become the teacher of their own English.**
