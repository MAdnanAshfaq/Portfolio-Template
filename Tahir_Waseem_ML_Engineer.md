# Tahir Waseem

Tahir Waseem  
Trenton, New Jersey, USA           • tahirwaseem .tk@gmail.com           • +15513362147  
PROFESSIONAL SUMMARY  
 
AI Full Stack Engineer with 6+ years of experience building production -grade, AI -powered web applications. 
Specialises in end -to-end product development  Next.js frontends, FastAPI backends, and LLM integrations using 
LangChain, RAG, and vector search. Comfortable across the full stack from streaming UI to async workers to 
model deployment, with a strong focus on scalability, observability, and shipping re liable AI features in regulated 
environments.  
 
TECHNICAL SKILLS
 
 Frontend   
 Next.js 14+ (App Router), React, TypeScript, Tailwind CSS, shadcn/ui, Vercel AI SDK  
 
Backend   
 FastAPI, Python, REST APIs, WebSockets, Server -Sent Events, Celery, Redis Queue  
 
AI & LLM  
 LangChain, LangGraph, Claude (3.5 Sonnet, Opus), GPT -4o, Mistral (7B, Mixtral 8x7B), 
Llama 3 (8B, 70B), Gemma 2, Ollama, HuggingFace, text -embedding -3-large, RAG, 
LangSmith  
 
LLM Engineering  
 Prompt engineering, structured outputs (Pydantic), streaming (SSE), prompt versioning, 
multi -provider fallback, model benchmarking, cost optimisation  
 
Vector & Search  
 pgvector (HNSW index), semantic similarity search, embedding pipelines, 
chunk_size/overlap tuning, top_k retrieval  
 
Databases   
 PostgreSQL, Redis, Supabase  
 
Auth & Security  
  JWT, OAuth 2.0, SOC 2 compliance, role -based access control (RBAC), data encryption at 
rest 
 
Scaling   
 AWS Auto Scaling Groups, pgBouncer (connection pooling), Redis caching, Celery async 
workers, token bucket rate limiting, Anthropic prompt caching  
 
Observability   
 Sentry, AWS CloudWatch, LangSmith (LLM tracing), Datadog, structured logging  
 
DevOps & 
Infrastructure  
 Docker, GitHub Actions, AWS (EC2, S3, ALB, Lambda, ASG), Vercel, blue -green 
deployments, canary releases, LaunchDarkly feature flags  
 
Testing   
 Pytest, Playwright, Jest, React Testing Library  
 

 
WORK EXPERIENCE  
 
Senior AI Full Stack Engineer  | Trustate                                                                                                              May  2022  – Present  
Trustate is a legal tech platform that consolidates the entire estate lifecycle — planning, trust funding, and probate administration — into 
a single AI -powered workspace built for attorneys, solo practitioners, and trust companies. The platform serves 1,0 00+ firms and financial 
institutions, has managed 11,000+ estates, and generated 249,000+ documents nationwide. Trustate holds SOC 2 compliance and h as 
been recognised on Inc.'s 2026 Female Founders 500 list.  
• Architected and led development of Trustate's AI document generation engine using LangChain and Claude 3.5 
Sonnet  fine-tuned for deterministic, legally precise output  enabling attorneys to auto -draft wills, trusts, and 
powers of attorney from 10,000+ vetted templates, reducing document preparation time by 70%  
• Built the Next.js 14 (App Router) frontend for the estate planning workspace, implementing token -by-token 
streaming using the Vercel AI SDK with Server -Sent Events (SSE) on the FastAPI backend, so attorneys see live 
document output with inline editing rath er than waiting for full generation  
• Designed and implemented a RAG -powered legal template search using FastAPI, pgvector with HNSW indexing, 
and OpenAI text -embedding -3-large  with chunking and retrieval parameters tuned for legal document precision  
allowing attorneys to semantically query 30+ years of attorney -vetted legal language in under 2 seconds  
• Developed the financial asset discovery UI and API layer, orchestrating 50+ financial database searches through a 
unified FastAPI backend with real -time result streaming to a Next.js dashboard, enabling attorneys to identify 
estate assets and liabilities i n a single workflow session  
• Built the estate administration task management system  a full -stack feature tracking 120+ post -death tasks per 
estate, with automated status updates, deadline alerts, and guided workflow prompts, reducing estate closure 
cycle times for client firms  
• Engineered a LangGraph -based AI agent for trust funding automation using Claude 3.5 Sonnet  orchestrating multi -
step document workflows (deed preparation, beneficiary change forms, account retitling, trust EIN acquisition) 
with structured tool calls, Pydantic -validated outputs, and exponential backoff retry logic for provider errors  
• Implemented end -to-end SOC 2 -compliant data architecture across the full stack  including field -level encryption 
for sensitive PII, immutable audit logs on all document actions, RBAC with attorney -level permission scoping, and 
secure document storage on AWS S3 with signed URL access  
• Integrated LLM -powered document Q&A using Claude 3.5 Sonnet  backed by a FastAPI RAG endpoint with multi -
turn conversation memory stored in Redis, enabling attorneys to ask natural language questions across documents, 
tasks, and client history with context retained across sessions  
• Led the redesign of the attorney -facing dashboard from a legacy monolith to a Next.js App Router architecture with 
React Server Components, reducing initial page load time by 55% and improving Lighthouse performance score 
from 61 to 94  
• Established CI/CD pipelines with GitHub Actions for the Next.js frontend (deployed to Vercel) and FastAPI backend 
(containerised with Docker on AWS EC2 behind an Application Load Balancer) — using blue -green deployment 
strategy for zero -downtime backend re leases, with automated Pytest and Playwright test suites cutting 
deployment errors by 60%  
• Designed and owned the LLM deployment and promotion strategy  new model versions (e.g., upgrading from GPT -4 
to Claude 3.5 Sonnet) released via canary rollout (10% → 25% → 100% traffic) with automated quality evaluation 
using LangSmith traces comparing output accuracy, latency, and user satisfaction scores before fu ll promotion; 
built multi -provider fallback routing (Claude → GPT -4o) to maintain 99.9% AI feature uptime during provider 
outages  
• Implemented a prompt versioning system storing all production system prompts in PostgreSQL with timestamps, 
author tracking, and one -click rollback  preventing silent prompt regressions that previously degraded document 
output quality without triggering any infrastructure alerts  
• Evaluated and benchmarked open -source LLMs (Mistral 7B, Mixtral 8x7B, Llama 3 8B) via Ollama for internal 
tooling, document classification, and non -PII intake tasks  replacing closed model API calls for lower -stakes 
workflows and reducing LLM API costs by an additional 30% on eligible request types; used HuggingFace model 

hub to compare embedding models (BGE -M3, all -MiniLM -L6-v2) against text -embedding -3-large before finalising 
the production embedding pipeline  
• Architected async document generation at scale using Celery workers backed by Redis Queue  offloading long -
running LLM document jobs (avg. 18 –45s) from the FastAPI request thread, with real -time progress pushed to the 
Next.js frontend via WebSocket, enabling the platform to handle 300+ concurrent document generation requests 
without timeouts or  blocked threads  
• Implemented LLM API rate limiting using a token bucket algorithm in Redis  tracking tokens -per-minute 
consumption per firm across concurrent requests and queuing overflow jobs gracefully, eliminating 429 
RateLimitError failures that previously caused a 12% job failure rate during peak usage hours  
• Optimised LLM API cost at scale by enabling Anthropic prompt caching on all long system prompts (estate 
templates, legal context blocks) reducing cached token costs by 90% and cutting average response latency by 40% 
on repeat prompt structures; combined with a Redis embedding cache for frequently retrieved document chunks, 
reducing pgvector query volume by 65% and saving ~$3,200/month in AP I and compute costs  
• Scaled the FastAPI backend horizontally using AWS Auto Scaling Groups (min 2, max 12 instances) behind the 
Application Load Balancer  configured to scale on CPU > 65%  and introduced pgBouncer for PostgreSQL connection 
pooling, reducing idle connection overhead and supporting a 4× increase in concurrent users without database 
exhaustion  
• Established full -stack observability across AI and application layers  integrated Sentry for real -time error tracking 
and stack traces on both FastAPI and Next.js, AWS CloudWatch dashboards for infrastructure metrics (CPU, 
memory, ALB latency), and LangSmith for LLM trace inspection, token usage, and latency breakdowns per c hain  
reducing mean time to diagnose production AI failures from hours to under 8 minutes  
• Collaborated directly with estate attorneys and trust company clients to define product requirements, translating 
complex legal workflows into intuitive UI/UX patterns that required minimal onboarding for non -technical legal 
professionals  
• Mentored two junior full stack engineers on LangChain integration patterns, FastAPI async best practices, and 
Next.js App Router data -fetching conventions  
 
Full Stack  Engineer | Mento                                                                                                               Nov 2019 – Apr 2022  
Mento is an AI -powered career coaching and mentorship platform that connects professionals and executives with expert coaches for 1:1 
development programmes. The platform serves enterprise clients including Anthropic, Dropbox, Brex, Gusto, Intercom, DoorDa sh, Vercel, 
and SoFi. Mento reports 98% of users rate coaching as a worthwhile investment and 93% report stronger performance post -engagement  
 
• Built the coach -matching platform end -to-end a Next.js frontend intake flow paired with a FastAPI backend that 
collected user role, function, challenges, and growth areas, then generated profile embeddings using sentence -
transformers (all -MiniLM -L6-v2) stored in pgvector, surfacing the top 3 coach m atches ranked by cosine similarity 
score  
• Developed the AI session summary feature using GPT -3 Davinci with structured prompt templates enforcing JSON 
output  automatically generating summaries of coaching sessions (key insights, commitments, next steps) stored 
per-session in PostgreSQL and surfaced in coach and coachee dashboards  
• Built the Pulse Survey system a full -stack feature tracking 22 specific leadership behaviours across 500+ active 
coachees, with a FastAPI data pipeline aggregating psychometric survey responses and a Next.js dashboard 
rendering longitudinal progress charts for coaches and HR admins  shifting leadership reviews from quarterly 
snapshots to continuous measurement  
• Engineered the Peer Insights (360 -degree feedback) feature  designing the full data model, FastAPI survey 
collection APIs, anonymisation layer, and Next.js results dashboard delivering structured feedback from managers, 
peers, and direct reports to 800+ managers across 100+ enterprise accounts  
• Implemented AI -powered session prep using LangChain and GPT -3 Davinci a pre -session feature generating 
personalised agendas from a coachee's goal history, prior session summaries, and upcoming challenges via a chain -
of-thought prompt, delivered as a rendered Next.js page 24 hours before each meeting  
• Built the enterprise reporting dashboard used by HR and People teams  a Next.js data visualisation layer over a 
FastAPI aggregation backend surfacing anonymised engagement trends, leadership behaviour scores, and coaching 

ROI metrics across 100+ enterprise accounts; reduced manual HR reporting prep time by 60% by replacing 
spreadsheet exports with live, filterable dashboards  
• Developed the coach onboarding and profile platform  a multi -step Next.js form flow backed by FastAPI enabling 
credential submission, specialisation tagging, and availability management; onboarded 200+ coaches within 4 
months of platform launch with an admin review workflow that reduced manual vetting time by 50%  
• Integrated real -time session notifications using WebSockets in FastAPI and React state management on the 
frontend  supporting 1,200+ simultaneous active sessions at peak, delivering sub -100ms notification latency for 
session reminders, coach connection prompts, and async message threading  
• Contributed to frontend component library using Tailwind CSS and shared React components, establishing design 
system conventions that reduced UI build time for new features by 40% across the engineering team  
• Managed AI feature rollouts using LaunchDarkly feature flags  new model versions and prompt changes deployed 
to 5% of users in shadow mode first, with output quality compared against baseline using an internal evaluation 
harness before full promotion; enforced a minimum quality score of ≥ 4.5/5 on session summary co herence before 
any prompt change reached production  
• Wrote comprehensive Pytest test suites for all FastAPI endpoints and Jest/React Testing Library tests for critical 
frontend flows, maintaining >85% test coverage across the coaching session and matching modules  
 
 
Education  
 
Bachelor’s In Computer Science  — 2018  
National University of Science and Technology  
 
CERTIFICATIONS  
 
• AWS Certified Developer  Associate Amazon Web Services  
• LangChain & Vector Databases in Production  DeepLearning.AI  
• ChatGPT Prompt Engineering for Developers  DeepLearning.AI & OpenAI  
• Microsoft Certified: Azure Data Engineer Associate (DP -203)  Microsoft  
 


