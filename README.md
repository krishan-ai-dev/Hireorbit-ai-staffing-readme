# HireOrbit — AI-Native IT Staffing Platform

> Automated candidate screening, scoring, and routing for IT recruitment — processing **500+ resumes/month** with zero manual effort.

---

## The Problem

IT recruitment teams were drowning in resumes. Manually reading, scoring, and routing 500+ candidate profiles per month was taking 3–4 hours per recruiter per day — with inconsistent results and slow response times to candidates.

---

## The Solution

HireOrbit is an end-to-end AI staffing platform that captures resumes directly from Gmail, scores them using a LangGraph multi-step AI pipeline, and routes shortlisted candidates to the right recruiter — automatically. Recruiters only see pre-scored, pre-filtered candidates ready for interview.

**Architecture:**
```
Gmail (resume intake) → n8n (email trigger + parsing)
→ LangGraph AI Pipeline (skill extraction → scoring → routing)
→ Supabase PostgreSQL (candidate database)
→ Recruiter Dashboard (shortlist view + actions)
→ WhatsApp / Email (automated candidate notifications)
```

---

## Results

| Metric | Before | After |
|---|---|---|
| Manual screening time | 3-4 hrs/day/recruiter | 0 hrs |
| Resumes processed/month | 500+ (manual) | 500+ (automated) |
| Candidate response time | 2-3 days | Same day |
| Screening consistency | Variable | Standardized AI scoring |

---

## Tech Stack

| Layer | Tools |
|---|---|
| Workflow Orchestration | n8n |
| AI Scoring Pipeline | LangGraph (multi-step agent) |
| LLM | OpenAI API (GPT-4) |
| Database | Supabase (PostgreSQL) |
| Authentication | Firebase Auth (multi-tenant) |
| Resume Intake | Gmail API |
| Notifications | WhatsApp API (Wati), Email |
| Deployment | AWS EC2, Docker |

---

## Key Features

- **Gmail Resume Capture** — n8n watches inbox, auto-parses attached resumes
- **LangGraph Scoring Pipeline** — Multi-step AI agent: skill extraction → experience scoring → job match ranking
- **Multi-tenant Access** — Separate recruiter dashboards per client via Firebase Auth
- **Automated Candidate Notifications** — WhatsApp + email updates sent automatically on status change
- **Recruiter Dashboard** — Clean interface showing ranked candidates with AI-generated summaries
- **CRM Sync** — Candidate data synced to client CRM on shortlisting

---

## How the AI Pipeline Works

```
Step 1: Resume text extracted (PDF/DOCX parser)
Step 2: LangGraph Agent — skill extraction (Python, Java, AWS, etc.)
Step 3: LangGraph Agent — experience scoring (years, role match)
Step 4: LangGraph Agent — job description match scoring (0-100)
Step 5: Auto-routing to recruiter based on score threshold
Step 6: Candidate notified via WhatsApp/email
```

---

## Impact

- 500+ candidate profiles processed every month — fully automated
- Recruiter manual screening time reduced by **70%**
- Consistent, bias-free AI scoring across all candidates

---

## Built By

**Krishan Kumar** — AI Automation Engineer | n8n Developer | LangChain | Python  
📧 kk88987@gmail.com | 📍 Ghaziabad, India | Open to Remote

> Need an AI recruitment automation system for your team? Let's talk.
