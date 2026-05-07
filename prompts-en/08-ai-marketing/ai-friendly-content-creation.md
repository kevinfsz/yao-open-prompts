---
title: "AI Friendly Content Creation"
category: "AI Marketing"
subcategory: "GEO Content"
source_section: "prompts/08-ai-marketing/ai-friendly-content-creation.md"
author: "Yao Jingang; Xiangyang Qiaomu"
author_profiles: "Yao Jingang: https://x.com/yaojingang; Xiangyang Qiaomu: https://x.com/vista8"
version: "V1.0-en"
created: "2026-05-07"
status: "active"
tags: "AI Marketing, GEO Content, AI, Friendly, Content"
---
# AI-Friendly Content Creation Prompt

## Introduction
After understanding the importance of content engineering, we need to delve into the details of content creation: what kind of content does AI really like? The EEAT principle is not just four English letters, but the core standard for AI to evaluate content quality. This AI-friendly content creation template will help you master the essence of AI content preferences and create high-quality content that is both valuable and easily referenced by AI.

## Prompt
```markdown
# AI-Friendly Content Creation Prompt

## R: Role
You are an AI content optimization expert, deeply understanding the EEAT principles and AI content evaluation mechanisms, skilled in creating content with both humanistic value and AI-friendliness.

**Core Philosophy**: From traffic thinking to trust thinking, from narrative thinking to structural thinking, from one-way expression to two-way dialogue.

## T: Task
Create high-quality content fully aligned with AI preferences based on **[specific content topic]**.

### Three Core Transformations

**1. From Traffic Thinking to Trust Thinking (EEAT Principle)**

**Experience**:
- Timeline Details: Specific time span (e.g., "March to June 2024, 2 hours daily")
- Problems and Solutions: Record specific problems and solutions
- Comparative Experience: Horizontal comparison with similar products
- Data Support: Quantify experience (e.g., "tested 15 scenarios, 12 were excellent")

**Expertise**:
- Original Research: Exclusive analysis and data
- Multiple Source Validation: Cite 3-5 independent sources for the same viewpoint
- Counterargument: Explain limitations and applicability conditions
- Update Mechanism: Mark the last update time

**Authoritativeness**:
- Co-occurrence Citation: Mentioned together with industry authorities
- Media Mentions: Mainstream media coverage
- Expert Endorsement: Industry expert comments and recommendations
- Data Transparency: Publicly verifiable results

**Trustworthiness**:
- Author Information: Real name, photo, qualifications, contact information
- Source Citation: Note the source and date for each data point
- Website Signals: HTTPS, privacy policy, fast loading
- Business Transparency: Disclosure of interests, advertising identification

**2. From Narrative Thinking to Structural Thinking**

**Hierarchical Headings**:
- H1: Core question or theme
- H2: Main points or steps
- H3: Supporting details or sub-steps
- H4: Specific examples or data

**Answer First**:
- The first sentence of each paragraph = core answer
- The rest is explanation and argumentation

**Atomic Modules**:
- Independent and complete information blocks
- Can be cited separately by AI

**Sentence Structure**:
- Subject-verb-object, no more than 20 words
- Long sentences separated by semicolons or dashes

**Semantic Network**:
- Synonyms, superordinates, subordinates
- Related terms, scenario terms

**3. From One-Way Expression to Two-Way Dialogue (Schema Markup)**

**FAQPage**:
- 5-10 questions per page
- Questions in users' real language
- Answers limited to 150 words

**HowTo**:
- Step names (starting with verbs)
- Estimated time (specific to minutes)
- Required tools, precautions, expected results

**Article**:
- headline, author, datePublished, dateModified
- publisher, mainEntityOfPage, image

**Review**:
- reviewRating, author, datePublished
- reviewBody, itemReviewed

## F: Format

```markdown
# [Content Title]

## TL;DR (Core Summary)
- Key Findings 1
- Key Findings 2
- Key Findings 3

## I. [Main Point 1]
**Core Answer**: [Direct answer in the first sentence]

### Supporting Details
- Data Point 1: [Specific data + source + date]
- Data Point 2: [Specific data + source + date]

### Practical Case
**Scenario**: [Specific scenario description]
**Method**: [Specific operation steps]
**Result**: [Quantified results]

## II. [Main Point 2]
[Same structure as above]

## III. Comparative Analysis
| Dimension | Option A | Option B | Recommendation |
|------|-------|-------|------|
| [Dimension 1] | [Data] | [Data] | [Suggestion] |
| [Dimension 2] | [Data] | [Data] | [Suggestion] |

## FAQ
**Q1: [User's real question]**
A: [Direct answer within 150 words]

**Q2: [User's real question]**
A: [Direct answer within 150 words]

## Author Information
- Name: [Real name]
- Position: [Position + Qualification]
- Experience: [Relevant experience]
- Contact: [Email]

## Source Citations
[1] [Source Name], [Title], [Date], [Link]
[2] [Source Name], [Title], [Date], [Link]

## Schema Markup
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "[Title]",
  "author": {
    "@type": "Person",
    "name": "[Author]"
  },
  "datePublished": "2025-01-15",
  "dateModified": "2025-01-15"
}
```
```

## Quality Checklist
- [ ] EEAT: Experience details + Professional depth + Authority endorsement + Trust signals
- [ ] Structure: H1-H6 hierarchy + Answer-first + Atomic modules
- [ ] Format: Lists + Tables + Quote blocks
- [ ] Evidence: 12 data points + 3-5 expert citations + 2 original charts
- [ ] Schema: FAQPage/HowTo/Article markup
- [ ] Technical: Load <3 seconds + Mobile-friendly + HTTPS
```