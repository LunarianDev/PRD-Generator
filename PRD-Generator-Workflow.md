# PRD Generator Workflow Script

**Version 1.0** | For use with IDE AI agents (Cursor, Windsurf, Antigravity, GitHub Copilot, etc.)

---

## Purpose

This workflow script automates the generation of a complete, client-specific Product Requirements Document (PRD) from questionnaire responses. Feed this script to your IDE agent along with the completed questionnaire data.

---

## How to Use

### Step 1: Collect Client Information
Complete the client discovery questionnaire (Section 1 of the main template) with your client. Save responses in a text file or paste directly into this workflow.

### Step 2: Prepare the Workflow
Copy this entire workflow script and paste it into your IDE's AI agent chat (Cursor Composer, Windsurf Agent, etc.)

### Step 3: Provide Client Data
Replace the `[CLIENT_DATA]` section below with actual questionnaire responses

### Step 4: Execute
The AI agent will generate a complete `[BusinessName]_PRD.md` file in the `/plans` directory.

---

## Pre-Generation Validation Checklist

**Before running the workflow, verify these mandatory questionnaire fields are complete:**

**Section A - Business Fundamentals:**
- [ ] Legal business name
- [ ] Industry/sector
- [ ] Years in operation
- [ ] Physical locations and service area
- [ ] Core services offered

**Section A2 - Business Goals:**
- [ ] Elevator pitch (one-sentence value proposition)
- [ ] Top 3 business goals for 2026

**Section A3 - Target Audience:**
- [ ] Primary customer description
- [ ] Geographic location of target customers
- [ ] Key pain points or objections

**Section C1 - Conversion Goals:**
- [ ] Primary conversion objective (form, call, booking, etc.)

**Section D1 - Competitors:**
- [ ] At least 2 competitor URLs

**Section E1 - Pain Points:**
- [ ] Pain points scored (0-5 scale) for business processes

**Section F2 - Budget:**
- [ ] Budget range for website project

**If any mandatory fields are missing**, the AI will insert `<<CLIENT_INPUT_REQUIRED>>` markers. Complete missing fields and re-run workflow.

---

## Workflow Script

# TASK: Generate Complete PRD Document

## Instructions for AI Agent

You are tasked with generating a comprehensive Product Requirements Document (PRD) for a website design project. 

**Output Requirements:**
1. Create a new file named: `plans/[BusinessName]_PRD.md` (replace spaces with underscores)
2. Use the PRD framework structure provided below
3. Fill in all sections using the client data provided
4. Never invent data - use `<<CLIENT_INPUT_REQUIRED>>` for missing required inputs
5. Calculate realistic estimates where needed
6. Identify automation opportunities from questionnaire pain points
7. Format as clean, readable Markdown

**PRD Framework Structure:**

---

# [Business Name] Website & Digital System - Product Requirements Document

**Version**: 1.0
**Date**: [Current Date]
**Project Manager**: [Your Name]
**Client Stakeholder**: [Client Contact Name]
**Industry**: [Industry/Sector]
**Location**: [City, State]

---

## Table of Contents

1. Project Overview
2. Target Audience & User Personas
3. Feature Requirements
4. Technical Architecture
5. Content Strategy
6. Design Requirements
7. AI/Automation Opportunity Matrix
8. Success Criteria & KPIs

---

## 1. Project Overview

### 1.1 Business Context

**Business Name**: [Legal name] (DBA: [Trading name if different])

**Industry**: [Industry/sector from questionnaire A1]

**Years in Operation**: [From questionnaire A1]

**Locations**: [Physical locations and service area from A1]

**Business Description**: 
[From questionnaire A2 - expand the one-sentence pitch into 2-3 paragraphs]

**Current Situation**:
[Analyze from questionnaire Section B - describe current digital presence, what's working, what's not]

**Top Business Goals for 2026**:
1. [Goal 1 from questionnaire A2]
2. [Goal 2 from questionnaire A2]
3. [Goal 3 from questionnaire A2]

### 1.2 Problem Statement

**Current Pain Points**:
[Analyze questionnaire Section E1 - list specific pain points with time investment scores]

- [Pain point 1]: Currently consuming [X hours/week] of team time
- [Pain point 2]: [Impact on business]
- [Pain point 3]: [Impact on business]

**Desired Future State**:
[Based on questionnaire C1 - describe what success looks like]

### 1.3 Success Metrics

**Primary KPI**: [Based on top-ranked objective from C1]
- Baseline: [Current state if known, or "TBD at launch"]
- Target: [Realistic goal based on industry benchmarks]
- Measurement: [How we'll track this]

**Secondary KPIs**:
- [KPI 2 from C1]: Target [X], measured by [method]
- [KPI 3 from C1]: Target [X], measured by [method]

**Timeline to Achieve**: [30/60/90 days based on complexity]

---

## 2. Target Audience & User Personas

### 2.1 Primary Persona

**Persona Name**: [Create descriptive name like "Busy Homeowner Sarah" or "Small Business Owner Mike"]

**Demographics**:
- Age range: [Infer from questionnaire A3]
- Location: [From questionnaire A3]
- Income level: [From questionnaire A3]
- Family/business status: [Context from A3]

**Goals**:
[From questionnaire A3 - what do they need solved?]
- Primary goal: [Main problem they need solved]
- Secondary goal: [Additional need]

**Pain Points**:
[From questionnaire A3 - their objections/hesitations]
- [Pain point 1]
- [Pain point 2]
- [Pain point 3]

**Behavior Patterns**:
- How they search: [From questionnaire A3 - Google, referrals, etc.]
- Device preference: [Mobile-first, desktop, both - infer from industry]
- Decision factors: [What influences their choice]
- Urgency level: [Immediate need vs. planning ahead]

**Current Journey**:
[From questionnaire A3 - how they currently find businesses]
1. Awareness: [How they discover options]
2. Research: [What information they seek]
3. Evaluation: [How they compare options]
4. Decision: [What triggers final choice]

**Objections to Overcome**:
[From questionnaire A3]
- [Objection 1]: [How website will address]
- [Objection 2]: [How website will address]
- [Objection 3]: [How website will address]

### 2.2 User Journey Map (Website-Specific)

**Stage 1: Landing (First 5 seconds)**
- Entry point: [Most likely: Google search, social media, referral link]
- First impression goal: [Immediate clarity on what business does]
- Success metric: Bounce rate <40%

**Stage 2: Exploration (1-3 minutes)**
- Information seeking: [What pages they visit - Services, About, Portfolio]
- Questions to answer: [Key questions from questionnaire A3 and E1]
- Success metric: 3+ pages viewed, session duration >1:30

**Stage 3: Evaluation (3-10 minutes)**
- Comparison factors: [Price, credibility, location, expertise]
- Trust indicators needed: [Reviews, credentials, years in business]
- Success metric: Time on key pages (Services, Portfolio)

**Stage 4: Conversion**
- Desired action: [From questionnaire C1 - form, call, booking]
- Path to action: [How we make it easy]
- Success metric: Conversion rate 2-5% (industry standard for local services)

---

## 3. Feature Requirements

### 3.1 Core Features (MVP - Must Have)

#### F1: Homepage

**Purpose**: Immediate clarity, build trust, drive conversion

**Key Sections**:

1. **Hero Section**
   - Headline: [Craft from questionnaire A2 elevator pitch - value proposition]
   - Subheadline: [Expand on unique differentiators from A2]
   - Primary CTA: [Based on C1 top objective - "Get a Quote", "Book Now", etc.]
   - Secondary CTA: [Lower commitment - "Learn More", "View Services"]
   - Background: [Image or gradient - based on D2 style preference]
   - Trust indicators: [Years in business, certifications, review count]

2. **Services Overview**
   - Section title: "Our Services" or [Industry-specific heading]
   - Services to feature: [List from questionnaire A2]
     - [Service 1]: [Brief description, icon, link to detail page]
     - [Service 2]: [Brief description, icon, link to detail page]
     - [Service 3]: [Brief description, icon, link to detail page]
     - [Continue for all services]
   - Layout: [3-column grid on desktop based on service count]

3. **Social Proof Section**
   - Type: [Based on C2 - testimonials, reviews, portfolio, case studies]
   - Content: [From questionnaire C3 - existing testimonials or note to collect]
   - Display: [Slider showing 3 at a time on desktop, 1 on mobile]
   - Elements per testimonial: Quote, name, location/title, [optional: photo, rating]

4. **About/Why Choose Us**
   - Content: [Summarize differentiators from questionnaire A2]
   - Format: [2-3 paragraphs + image, or bullet points with icons]
   - CTA: [Link to full About page]

5. **Service Area / Location**
   - [If physical location is important from A1]
   - Map embed: [Google Maps]
   - Service radius: [From questionnaire A1]
   - Cities/areas listed: [Specific areas from A1]

6. **Final CTA Section**
   - Headline: [Action-oriented based on C1]
   - CTA button: [Primary conversion action]

**Success Criteria**:
- Visitor understands business offering in <5 seconds
- All core services visible above fold or in first scroll
- Clear conversion path with CTA in hero and footer minimum
- Mobile responsive (hero image may hide on mobile, use background)
- Load time <3 seconds

**Technical Notes**:
- Full viewport height hero on desktop
- Lazy load images below fold
- Schema markup: LocalBusiness, WebSite

---

#### F2: Services Pages

**Number of pages**: [Count distinct services from questionnaire A2]

**Template structure** (replicate for each service):

1. **Hero/Header**
   - Service name as H1: [Specific service]
   - Value proposition: [Why choose this service]
   - Quick CTA: [Phone or form]

2. **Service Description**
   - What's included: [Detailed list from questionnaire A2]
   - Process overview: [How it works - 3-5 steps]
   - Benefits: [4-6 key benefits, client-focused language]

3. **Pricing Section**
   - Display: [If client provided pricing from questionnaire F2, show ranges or starting prices]
   - Alternative: "Request Custom Quote" CTA with form
   - Context: [What affects price, typical range without specific numbers if client prefers]

4. **FAQ Section**
   - Questions: [From questionnaire E1 - common questions for this service]
   - Format: Accordion (expand/collapse)
   - Count: 5-7 questions per service

5. **Related Services**
   - Display 2-3 complementary services
   - Links to those service pages

6. **Conversion Section**
   - CTA: "Get Started with [Service Name]"
   - Form or booking link

**Service-Specific Content** (generate for each):

[For EACH service from questionnaire A2, create subsection:]

**Service: [Service Name]**

*Target keyword*: [Service name] + [Location from A1]

*Content outline*:
- Description: [Expand from questionnaire A2]
- Process: [3-5 steps - standardize or infer from industry]
- Benefits: [Client-focused outcomes]
- Ideal for: [Customer scenarios]
- FAQ topics: [Based on E1 common questions]

*Call-to-action*: [Primary conversion goal for this service type]

[REPEAT FOR EACH SERVICE]

**Success Criteria**:
- Each service page ranks for "[service] [location]" keyword
- Answers top customer questions identified in questionnaire
- Conversion opportunity on each page (form or phone)
- FAQ reduces inquiry volume for common questions
- Load time <3 seconds

**Technical Notes**:
- Schema markup: Service, LocalBusiness, FAQPage
- Internal linking between related services
- Breadcrumb navigation

---

#### F3: About Page

**Purpose**: Build trust, humanize business, establish credibility

**Content Sections**:

1. **Origin Story**
   - Founding: [From questionnaire A1 - years in operation, why started]
   - Mission: [Infer from questionnaire A2 differentiators]
   - Growth: [Key milestones if provided]

2. **Team**
   - [If team bios available from C3]
   - Format: Photo + name + role + brief bio
   - Alternative: Owner/founder focus if solo operation

3. **Credentials & Trust**
   - Years in business: [From A1]
   - Certifications: [If mentioned in questionnaire]
   - Awards/recognition: [If mentioned]
   - Community involvement: [If mentioned in A2]

4. **Values/Differentiators**
   - [From questionnaire A2 - what makes you different]
   - Format: 3-4 value statements with explanations

5. **Call to Action**
   - "Work With Us" or "Get Started"
   - Link to contact/services

**Content Details**:
- Word count: ~400-600 words
- Tone: [Based on questionnaire D2 - playful/serious, traditional/modern]
- Images needed: [From C3 - team photos, facility photos]

**Success Criteria**:
- Builds emotional connection
- Establishes credibility
- Supports SEO for brand name searches
- Average time on page >1 minute

**Technical Notes**:
- Schema markup: AboutPage, Organization
- Link to social profiles

---

#### F4: Contact Page

**Purpose**: Make it easy to reach out, capture leads, provide location info

**Layout**:

**Left Column (60%): Contact Form**

Form fields [based on questionnaire E3 - what client needs to collect]:
- Name (required, text input)
- Email (required, email validation)
- Phone (required, format: (XXX) XXX-XXXX)
- [Custom field from E3 if needed - e.g., "Property Type", "Service Needed"]
- Service Interested In (required, dropdown):
  [List all services from A2]
- Message (required, textarea, minimum 10 characters)
- [Honeypot field]: "website" (hidden, spam prevention)

Form behavior:
- Real-time validation (instant feedback on errors)
- Submit button disabled until all required fields valid
- On submit: Loading state, disable button, show spinner
- Success: Replace form with thank you message
- Error: Display error above form, preserve filled data

**Right Column (40%): Contact Information**

- **Address**: [From questionnaire A1]
- **Phone**: [From A1] (click-to-call link)
- **Email**: [From E2 or A1]
- **Hours**: [From E2 or typical for industry]
- **Social Media**: [From questionnaire B2]

- **Map Embed**: [Google Maps with address from A1]

**Success Criteria**:
- 100% of form submissions captured and routed correctly
- Client receives notification within 1 minute
- User receives auto-reply confirmation
- Mobile-optimized (large touch targets, single column)
- Accessible (keyboard navigable, screen reader compatible)

**Technical Notes**:
- Form submits to: [Specify backend - Formspree, serverless function, etc.]
- Notification email to: [Client email from questionnaire]
- Auto-reply template: [Create thank-you message]
- Spam prevention: Honeypot + rate limiting
- Schema markup: ContactPage

---

#### F5: Portfolio/Gallery/Testimonials Page

**[Include this section if client checked relevant boxes in C2]**

**Purpose**: Showcase work, build credibility through social proof

**Content** [Based on questionnaire C3]:
- Available content: [From C3 - what client has]
- Format: [Infer from industry - before/after, project galleries, text testimonials, video]

**Layout Options**:

*For visual businesses (contractors, designers, photographers)*:
- Grid layout of project photos
- Click to expand gallery
- Each project: Title, brief description, services used
- Optional: Before/after slider

*For service businesses (professional services, healthcare)*:
- Text testimonials with client info
- Star ratings
- Optional: Video testimonials
- Format: Card layout or list

**Content per item**:
- [Specify what to collect: customer name, location, service used, quote, rating, photo]

**Target quantity**: [Recommend 10-20 portfolio items or testimonials]

**Success Criteria**:
- Provides social proof for conversion
- Showcases range of work/services
- Load time <3 seconds (optimized images)

**Technical Notes**:
- Lazy load images
- Schema markup: Review (if testimonials)
- Lightbox/modal for image viewing

---

#### F6: Local SEO Foundation

**Purpose**: Rank in local search results, appear in Google Map Pack

**Components**:

1. **On-Page SEO** (every page):
   - NAP consistency: [Name, Address, Phone from A1 - exact match everywhere]
   - Schema markup: LocalBusiness on all pages
   - Location keywords: [City, State from A1] integrated naturally in content
   - H1: Includes primary keyword
   - Meta tags: Unique per page, includes location

2. **Google Business Profile Integration**:
   - Claim/optimize: [From questionnaire B2]
   - Link profile to website
   - Embed map on contact page
   - Display reviews on site (if API available)

3. **Schema Markup Requirements**:
   ```json
   LocalBusiness:
   - Business name: [From A1]
   - Address: [From A1]
   - Phone: [From A1]
   - Hours: [From E2 or standard]
   - Services: [List from A2]
   - Service area: [From A1]
   - Price range: [$ to $$$$ based on questionnaire]
   - Same As: [Social profiles from B2]
   ```

4. **Content Strategy for Local SEO**:
   - Location pages: [If serving multiple cities]
   - Service + location combinations: [Service 1] in [City]
   - Local content: [Mention local landmarks, neighborhoods, community]

**Success Criteria**:
- Rank in Google Map Pack for "[service] [location]"
- Rank top 10 for 3-5 primary local keywords within 90 days
- Google Business Profile fully optimized and linked

**Technical Notes**:
- Submit sitemap to Google Search Console
- Set up Google Business Profile (if not done from B2)
- Local citations: Ensure NAP consistency across directories

---

#### F7: Mobile Experience Optimization

**Purpose**: Ensure excellent experience for 60-70% of traffic (mobile users)

**Critical Mobile Paths**:

1. **Instant Contact**:
   - Sticky header with tap-to-call button
   - Phone number always visible
   - SMS option if available

2. **Quick Information**:
   - Service area visible without excessive scrolling
   - Hours prominently displayed
   - One-tap directions (Google Maps link)

3. **Simplified Forms**:
   - Fewer fields if possible (name, phone, service - minimum viable)
   - Large input areas (minimum 44x44px touch targets)
   - Proper input types (tel, email for keyboard optimization)
   - Autofill support

4. **Performance**:
   - Load time <3 seconds on 4G
   - Images optimized for mobile (WebP, lazy loading)
   - Minimal JavaScript for faster initial render

**Design Considerations**:
- Single column layouts
- Larger typography (minimum 16px for body)
- Thumb-friendly navigation (bottom placement considerations)
- Reduced hero image size or background only

**Success Criteria**:
- >60% of conversions from mobile devices
- Mobile PageSpeed score >85
- Passes Google Mobile-Friendly Test
- Bounce rate <45% on mobile

**Technical Notes**:
- Viewport meta tag configured
- Touch event optimization
- Test on real devices (iPhone, Android)

---

### 3.2 Enhanced Features (Phase 2 - Automation Upsells)

**[The following features are NOT included in base website. They are upsell opportunities identified from questionnaire pain points.]**

**Automation Opportunity Assessment** [From questionnaire Section E1]:

[For EACH pain point scored 3+ in questionnaire E1, create entry below - MAXIMUM 5 entries. Select the 5 highest-scoring pain points if more exist.]

---

#### AF1: [Automation Feature Name]

**Trigger**: Questionnaire E1 - "[Pain point description]" scored [X/5]

**Business Problem**:
[Describe the pain - current time investment, impact, frequency]

**Solution Overview**:
[High-level description of automation]

**Functionality**:
- [Feature component 1]
- [Feature component 2]
- [Feature component 3]
- [How it integrates with website]

**User Flow**:
1. [Step 1 - trigger]
2. [Step 2 - processing]
3. [Step 3 - action]
4. [Step 4 - result]

**Technical Stack Options**:
- **No-Code**: [Tool recommendation - Zapier, Make.com, etc.]
- **Low-Code**: [Platform recommendation - n8n, Retool, etc.]
- **Custom**: [If complex - tech stack recommendation]

**ROI Calculation**:
- Time currently spent: [Hours/week from E1 or estimate]
- Time saved with automation: [Estimated reduction]
- Additional value: [Lead capture, revenue impact, quality improvement]
- Payback period: [Months to ROI]

**Implementation Details**:
- Estimated setup time: [Hours]
- Dependencies: [CRM, email service, etc.]
- Ongoing maintenance: [Hours/month]
- Monthly cost: [SaaS fees if applicable]

**Pricing**:
- Setup: $[Range]
- Monthly: $[Range] [if applicable]

**Recommendation**: [Phase 2 / Phase 3 - based on priority and complexity]

---

[REPEAT ABOVE STRUCTURE FOR EACH AUTOMATION OPPORTUNITY - MAXIMUM 5 ENTRIES TOTAL]

---

**Common Automation Features by Industry** [Select relevant]:

**For Home Services** (Plumbing, HVAC, Electrical, Landscaping):
- Emergency request triage chatbot
- Estimate/quote calculator
- Review request automation
- Job completion follow-up sequences

**For Professional Services** (Law, Accounting, Consulting):
- Consultation booking with intake forms
- Document upload portal
- FAQ knowledge base with AI search
- Automated meeting reminders

**For Retail/E-commerce**:
- Inventory-aware product recommendations
- Order status chatbot
- Abandoned cart recovery
- Loyalty program automation

**For Healthcare/Wellness**:
- Appointment reminders + intake forms
- Patient education content delivery
- Insurance verification automation
- Post-treatment follow-up

---

## 4. Technical Architecture

### 4.1 Platform Recommendation

**Recommended Platform**: [Choose based on requirements analysis]

**Decision Factors**:
- Budget: [From questionnaire F2]
- Client technical ability: [Infer from questionnaire - will they update content?]
- Content marketing needs: [Blog from C2?]
- E-commerce: [From C2]
- Performance requirements: [Based on service type]
- Long-term scalability: [Automation upsells planned?]

**Platform Choice**: 

[CHOOSE ONE AND JUSTIFY:]

**Option A: WordPress**
- **Why**: [E.g., "Client wants blog (C2), needs occasional content updates, budget allows managed hosting"]
- **Theme**: [Custom child theme / Premium theme: name]
- **Key Plugins**:
  - Elementor / Oxygen Builder (visual editing)
  - Yoast SEO / Rank Math (SEO)
  - WPForms / Gravity Forms (forms)
  - [Additional based on features]
- **Hosting**: [Cloudways / Kinsta / SiteGround] - $[XX]/month
- **Pros**: [SEO-friendly, client can update, extensive plugin ecosystem]
- **Cons**: [Requires ongoing maintenance, security updates]

**Option B: Webflow**
- **Why**: [E.g., "Design-heavy portfolio needs (from C2), client budget $3500+ (F2), modern interactive design preferred (D2)"]
- **Hosting**: Included in Webflow subscription
- **CMS Collections**: [List if needed - Blog, Services, Team, Portfolio]
- **Pros**: [Visual editing, fast performance, no security maintenance]
- **Cons**: [Monthly cost, less flexibility for complex automation]

**Option C: Custom HTML/Tailwind + Vercel**
- **Why**: [E.g., "Simple 5-page site, maximum performance needed, client won't update content, automation upsells planned requiring serverless functions"]
- **Tech Stack**:
  - HTML5 + Tailwind CSS
  - Vanilla JavaScript (no framework - faster load)
  - Vercel (hosting + serverless functions)
- **Hosting**: Vercel free tier / Pro ($20/mo)
- **Pros**: [Maximum performance, version control, easy automation integration, free/cheap hosting]
- **Cons**: [Client can't easily update content, requires developer for changes]

**Option D: Wix / Squarespace**
- **Why**: [E.g., "Client budget <$1500 (F2), wants full DIY control, simple needs, no automation planned"]
- **Platform**: [Wix Business plan / Squarespace Business]
- **Pros**: [All-in-one, easy client updates, no maintenance]
- **Cons**: [Limited automation capabilities, less SEO control, ongoing monthly cost]

---

**Selected Platform**: **[FINAL CHOICE]**

**Rationale**: [Explain why this is best fit based on questionnaire responses]

---

### 4.2 Hosting & Infrastructure

**Domain**:
- Current domain: [From questionnaire B1 if exists]
- Action: [Register new / Transfer / Use existing]
- Registrar: [Recommendation - Cloudflare, Namecheap, etc.]

**Hosting**:
- Provider: [From platform choice above]
- Plan: [Specific plan tier]
- Cost: $[XX]/month
- Included: [SSL, CDN, backups, etc.]

**SSL Certificate**:
- Source: [Let's Encrypt free / Included with hosting]
- Auto-renewal: Yes

**Email Hosting**:
- [If client needs professional email]
- Recommendation: [Google Workspace / Microsoft 365 / Zoho Mail]
- Cost: $[XX]/user/month
- Setup: [Configure MX records, SPF, DKIM]

**CDN**:
- Provider: [Cloudflare free tier / Included with hosting]
- Purpose: Faster global load times, DDoS protection

**Backups**:
- Frequency: Daily
- Retention: 30 days
- Storage: [Included with hosting / Separate service]
- Testing: Monthly restoration test

**Monitoring**:
- Uptime: [UptimeRobot free / Hosting built-in]
- Performance: [Google Analytics, PageSpeed]
- Alerts: Email notification for downtime

---

### 4.3 Integrations Required

**[Based on questionnaire responses, list required integrations:]**

**Google Business Profile**:
- Status: [From B2 - claimed or need to claim]
- Integration: Link website, embed map, [optional: display reviews via API]

**Social Media** [From questionnaire B2]:
- Platforms: [List active profiles]
- Integration: Social share buttons, embedded feeds (optional)
- Links: Footer, contact page

**Email Marketing** [From questionnaire B2]:
- Current tool: [From B2]
- Integration: Newsletter signup form, [API connection if automation]
- Form placement: Footer, [optional: popup, dedicated page]

**Booking/Scheduling** [If checked in C2]:
- Tool: [Calendly / Acuity / Cal.com / Client's existing]
- Integration: Embedded on contact page or service pages
- Sync: Client's calendar (Google Calendar / Outlook)

**CRM** [From questionnaire E2]:
- Current system: [From E2]
- Integration: [If Phase 1: Form submissions via Zapier/webhook / If Phase 2: Direct API]
- Data flow: Form → CRM with fields mapped

**Analytics**:
- Google Analytics 4: [Required - Measurement ID to be created]
- Microsoft Clarity: [Optional - heatmaps and session recordings]
- Call tracking: [If phone leads critical - CallRail / CallTrackingMetrics]

**Payment Processing** [If e-commerce from C2]:
- Gateway: [Stripe / Square / PayPal]
- Integration: [Native or via plugin]

**Other Integrations** [Specific to questionnaire responses]:
- [List any other tools mentioned in questionnaire]

---

### 4.4 Development Environment & Workflow

**Version Control**:
- Repository: GitHub private repo
- Branch structure:
  - `main` → Production
  - `staging` → Client review
  - `development` → Active development

**Environments**:
1. **Local Development**: [Your machine]
2. **Staging**: [staging.clientdomain.com] - Client review and testing
3. **Production**: [www.clientdomain.com] - Live site

**Deployment Workflow**:
```
Development (local) 
  → Push to `development` branch
  → Merge to `staging` branch
  → Deploy to staging URL
  → Client approval
  → Merge to `main` branch
  → Deploy to production
```

**CI/CD** [If using custom platform]:
- GitHub Actions / Vercel auto-deploy
- Automated testing: [Lighthouse CI for performance]
- Build process: [Tailwind compile, minification, image optimization]

---

## 5. Content Strategy

### 5.1 Content Inventory

**Provided by Client** [From questionnaire C3]:

- **Photos**: [Quality: Professional/Amateur/None] | [Quantity: X images]
  - Action: [Use as-is / Optimize / Source additional]
- **Written Content**: [Status: Complete/Partial/None]
  - Action: [Edit existing / Write new / Client to provide]
- **Logo/Branding**: [Status: Vector files available/Needs extraction/Needs design]
  - Action: [Use existing / Recreate / Design new]
- **Testimonials**: [Quantity: X available] | [Format: Text/Video/Both]
  - Action: [Use existing / Collect more / Format for web]

**To Be Created**:

- **Copywriting**: 
  - Pages: [Count from features section]
  - Estimated word count: [Total across all pages]
  - Tone: [From questionnaire D2 - professional/friendly/technical]
  - Writer: [You / Client / Freelancer]

- **Photography**:
  - Need: [Yes/No based on C3]
  - Type: [Team photos, facility, products, action shots]
  - Source: [Professional photographer / Stock images / Client smartphone photos]
  - Budget: $[XX if needed]

- **Video**:
  - Need: [Yes/No based on questionnaire or recommendation]
  - Type: [About us, testimonial, explainer]
  - Budget: $[XX if needed]

- **Graphics/Icons**:
  - Need: [Service icons, infographics, etc.]
  - Source: [Custom design / Icon library (Font Awesome, Heroicons)]

---

### 5.2 Page-by-Page Content Specifications

**[For EACH page, specify content requirements:]**

---

#### Page: Homepage

**Word Count**: ~500 words total

**Sections**:

1. **Hero Headline** (10-15 words):
   - Template: "[Benefit] for [Target Audience] in [Location]"
   - Example: [Craft from questionnaire A2 elevator pitch]

2. **Hero Subheadline** (20-30 words):
   - Expand on unique value proposition from A2

3. **Services Overview** (50 words per service):
   - [Service 1]: [Brief description focusing on client benefits]
   - [Service 2]: [Brief description]
   - [Service 3]: [Brief description]
   - [Continue for all services]

4. **About Snippet** (100-150 words):
   - Who we are
   - Why choose us (differentiators from A2)
   - Years in business, credentials

5. **Social Proof**:
   - 3-5 testimonials (from C3 or to be collected)
   - Format: Quote (30-50 words), Name, Location/Service

**SEO Requirements**:
- Primary keyword: [Service type] in [Location]
- Secondary keywords: [2-3 long-tail variations]
- Keyword density: Natural (2-3% of primary keyword)

**Images Needed**:
- Hero background (1920x1080px minimum)
- Service icons (6 images, 200x200px)
- About photo (team or owner, 800x600px)
- [Optional: Client logos, certifications]

---

#### Page: [Service 1 Name]

**Word Count**: ~600-800 words

**Content Outline**:

1. **Introduction** (100 words):
   - What is this service
   - Who it's for
   - Key benefit

2. **What's Included** (200 words):
   - Detailed list of service components
   - [From questionnaire A2, expand each service]

3. **Our Process** (150 words):
   - Step 1: [Phase 1]
   - Step 2: [Phase 2]
   - Step 3: [Phase 3]
   - [Industry standard or from questionnaire E3 lead journey]

4. **Benefits** (200 words):
   - [Benefit 1]: [Why this matters to customer]
   - [Benefit 2]: [Impact on their life/business]
   - [Benefit 3]: [Differentiator]
   - [Benefit 4]: [Risk mitigation]

5. **FAQ** (150 words - 5-7 Q&As):
   - [Question 1 from common questions in E1]: [Answer]
   - [Question 2]: [Answer]
   - [Continue for 5-7 questions]

**SEO Requirements**:
- Primary keyword: [Service name] [Location]
- Secondary keywords: [Service name] near me, [service variation] [Location]
- H1: [Service Name] in [Location] - [Benefit]
- H2s: Include variations of primary keyword

**Images Needed**:
- Hero image (service-specific, 1920x1080px)
- Process diagram or icon set (3-5 steps)
- [Optional: Before/after, examples]

---

[REPEAT FOR EACH SERVICE PAGE - MAXIMUM 6 SERVICE PAGES. If client has more than 6 distinct services, consolidate related services into broader categories (e.g., "Lawn Care" instead of separate "Mowing", "Edging", "Seeding").]

---

#### Page: About

**Word Count**: ~400-600 words

**Content Outline**:

1. **Introduction** (50 words):
   - [Business name] has been [doing what] in [location] since [year]

2. **Our Story** (150 words):
   - [Why business was started - from questionnaire context or to ask client]
   - [Key milestones or growth]
   - [Mission statement - infer from A2]

3. **What Makes Us Different** (150 words):
   - [Differentiator 1 from questionnaire A2]: [Expand]
   - [Differentiator 2]: [Expand]
   - [Differentiator 3]: [Expand]

4. **Team** (100 words):
   - [If solo]: About owner - experience, credentials, passion
   - [If team]: Brief intro to key team members

5. **Community Involvement** (50 words):
   - [If mentioned in questionnaire - local sponsorships, charity, etc.]
   - [Otherwise: General statement about serving local community]

**SEO Requirements**:
- Primary keyword: [Business name], [Industry] [Location]
- Focus: Brand awareness, local connection

**Images Needed**:
- Team photo or owner portrait (800x600px)
- [Optional: Facility photos, community involvement photos]

---

#### Page: Contact

**Word Count**: ~200 words

**Content**:

1. **Introduction** (50 words):
   - "Get in touch for [primary conversion goal from C1]"
   - Hours, location, service area

2. **Contact Information Display**:
   - Address: [From questionnaire A1]
   - Phone: [From A1]
   - Email: [From E2 or A1]
   - Hours: [Standard or from E2]

3. **Form Instructions** (50 words):
   - "Fill out the form and we'll respond within [X hours/minutes]"
   - [Set expectation based on client response time from E2]

**SEO Requirements**:
- Primary keyword: Contact [Business name], [Service] [Location] contact
- Schema markup: ContactPage

**Images Needed**:
- Map embed (Google Maps)
- [Optional: Office/storefront photo]

---

#### Page: Portfolio/Testimonials [If applicable]

**Word Count**: ~200 words intro + items

**Content**:

1. **Introduction** (100 words):
   - Overview of work showcased
   - [Quantity] projects completed
   - [Range of services demonstrated]

2. **Portfolio Items** [Target: 10-20 items]:
   Each item:
   - Project name/customer name
   - Service(s) provided
   - Brief description (30-50 words)
   - [Optional: Results, timeline]
   - Images: [2-5 per project]

3. **Testimonials** [Target: 10-15]:
   Each testimonial:
   - Quote (30-80 words)
   - Customer name
   - Location/business
   - Service used
   - [Optional: Star rating, date, photo]

**SEO Requirements**:
- Primary keyword: [Service] portfolio [Location], [Business name] reviews
- Schema markup: Review

**Images Needed**:
- Portfolio: [10-20 projects × 2-5 images each]
- Testimonials: [Optional customer photos]

---

### 5.3 SEO Keyword Strategy

**Primary Keywords** (Local intent):

[Generate based on services from A2 and location from A1:]

1. [Service 1] [City, State]
   - Monthly search volume: [Estimate or note to research]
   - Difficulty: [Low/Medium/High - research with tool]
   - Target pages: Homepage, Service 1 page

2. [Service 2] [City, State]
   - Monthly search volume: [Estimate]
   - Difficulty: [Research]
   - Target pages: Homepage, Service 2 page

3. [Service 3] [City, State]
   - Monthly search volume: [Estimate]
   - Difficulty: [Research]
   - Target pages: Homepage, Service 3 page

4. [Industry/Business type] [City, State]
   - Monthly search volume: [Estimate]
   - Difficulty: [Research]
   - Target pages: Homepage, About

**Secondary Keywords** (Long-tail, lower competition):

5. [Service 1] near me
6. Best [Service 1] in [City]
7. [Specific problem] [City] [Service type]
8. [Service variation] [Neighborhood/Area]
9. [Emergency/urgent] [Service] [Location]

**Content Topic Ideas** [For blog if applicable from C2]:
- [Topic 1 addressing common question from E1]
- [Topic 2 based on seasonal trends in industry]
- [Topic 3 targeting long-tail keyword]

**Competitor Analysis** [From questionnaire D1]:

[For EACH competitor URL from questionnaire:]

**Competitor: [Competitor 1 URL]**
- What they rank for: [To research or note to analyze]
- Their strengths: [From questionnaire D1]
- Gaps we can exploit: [Keywords they're missing, content opportunities]

[REPEAT FOR EACH COMPETITOR - MAXIMUM 5 COMPETITORS. If client provides more than 5, select the most relevant/top competitors.]

---

### 5.4 On-Page SEO Checklist

**Per Page Requirements**:

- [ ] Unique title tag (50-60 characters)
  - Format: [Primary Keyword] | [Business Name] | [Location]
- [ ] Unique meta description (150-160 characters)
  - Include primary keyword, location, call-to-action
- [ ] H1 tag with primary keyword (only one H1 per page)
- [ ] H2/H3 tags with secondary keywords and variations
- [ ] Primary keyword in first 100 words
- [ ] Keyword density 2-3% (natural, not stuffed)
- [ ] Internal links to related pages (3-5 per page)
- [ ] External links to authoritative sources (1-2 if relevant)
- [ ] Image alt text with descriptive keywords
- [ ] URL slug: lowercase, hyphens, includes keyword
- [ ] Schema markup appropriate to page type
- [ ] Canonical tag (self-referencing)
- [ ] Word count meets minimum (homepage 500+, service pages 600+)

**Site-Wide SEO**:

- [ ] XML sitemap generated
- [ ] Robots.txt configured
- [ ] Google Search Console setup
- [ ] Google Analytics 4 installed
- [ ] SSL certificate (HTTPS)
- [ ] Mobile responsive (passes Google Mobile-Friendly Test)
- [ ] Page speed >85 on PageSpeed Insights
- [ ] NAP consistency (Name, Address, Phone same everywhere)
- [ ] Social Open Graph tags
- [ ] Structured data (JSON-LD schema)

---

## 6. Design Requirements

### 6.1 Brand Identity

**Style Direction** [From questionnaire D2]:

- **Overall Aesthetic**: [Modern/Traditional, Minimalist/Detailed]
- **Color Mood**: [Colorful/Neutral, Vibrant/Muted]
- **Content Balance**: [Image-heavy/Text-focused]
- **Tone**: [Playful/Serious, Casual/Professional]

**Rationale**: [Explain why this style fits the business from A2 and target audience from A3]

---

### 6.2 Competitor Analysis Summary

**[From questionnaire D1 - analyze patterns:]**

**Competitor Analysis**:

**Competitor 1**: [URL from D1]
- What works: [From questionnaire + your analysis]
- Design elements: [Layout, colors, features to note]
- Our differentiation: [How we'll be different/better]

**Competitor 2**: [URL from D1]
- What works: [Analysis]
- Design elements: [Notes]
- Our differentiation: [How we stand out]

**Competitor 3**: [URL from D1]
- What works: [Analysis]
- Design elements: [Notes]
- Our differentiation: [Unique approach]

**Common Patterns in Industry**:
- [Pattern 1 across competitors]
- [Pattern 2]
- [Overused clichés to avoid]

**Opportunity Gaps**:
- [What competitors aren't doing that we can]
- [Better user experience opportunities]
- [Content or features missing from competitor sites]

---

### 6.3 Inspiration & Style References

**[From questionnaire D2:]**

**Inspiration Site 1**: [URL from D2]
- **Element to borrow**: [Specific component - navigation, hero layout, testimonial design]
- **Why it works**: [Explanation]
- **Adaptation**: [How we'll customize for this client]

**Inspiration Site 2**: [URL from D2]
- **Element to borrow**: [Specific component]
- **Why it works**: [Explanation]
- **Adaptation**: [Customization approach]

**Inspiration Site 3**: [URL from D2]
- **Element to borrow**: [Specific component]
- **Why it works**: [Explanation]
- **Adaptation**: [Customization approach]

---

### 6.4 Design System Specifications

**Color Palette**:

[If client has brand colors from C3, use those. Otherwise, recommend based on psychology and industry:]

- **Primary Color**: [Hex code]
  - Usage: CTA buttons, links, key headings
  - Psychology: [Why this color - trust, energy, calm, etc.]

- **Secondary Color**: [Hex code]
  - Usage: Accents, secondary CTAs, icons
  - Relationship: [Complementary/Analogous to primary]

- **Accent Color**: [Hex code]
  - Usage: Highlights, hover states, badges
  - Purpose: [Draw attention, add visual interest]

- **Neutral Colors**:
  - Background: [Light hex - #FAFAFA or similar]
  - Surface: [White or slightly off-white]
  - Text: [Dark hex - #1A1A1A or similar]
  - Text Secondary: [Medium gray hex]
  - Borders: [Light gray hex]

**Color Rationale**: [Explain choices based on industry, target audience, desired emotion]

---

**Typography**:

[Choose fonts appropriate to style from D2]

- **Headings**:
  - Font: [Google Font or web-safe font]
  - Weights: [Bold, Semibold]
  - Sizes: 
    - H1: 48px (desktop), 32px (mobile)
    - H2: 36px (desktop), 28px (mobile)
    - H3: 28px (desktop), 24px (mobile)
  - Line height: 1.2
  - Character: [Modern/Traditional, Elegant/Bold]

- **Body Text**:
  - Font: [Google Font or web-safe font]
  - Weight: Regular (400)
  - Size: 16px (minimum for readability)
  - Line height: 1.6
  - Character: [Highly readable, professional]

- **Accent/Special** (Optional):
  - Font: [If needed for personality]
  - Usage: [Pull quotes, callouts]

**Typography Rationale**: [Why these fonts match the brand and are readable]

---

**Spacing & Layout**:

- **Container Width**: 1200px maximum (with padding)
- **Grid System**: 12-column grid
- **Spacing Scale**: 8px base unit (8, 16, 24, 32, 48, 64px)
- **Section Padding**: 80px vertical (desktop), 48px (mobile)
- **Card/Element Padding**: 24px internal
- **Gutter**: 24px between columns

---

**UI Components**:

**Buttons**:
- **Primary**: 
  - Background: [Primary color]
  - Text: [White or contrasting]
  - Padding: 12px 32px
  - Border radius: 8px
  - Hover: [Darken 10%]
  
- **Secondary**:
  - Background: [Transparent or secondary color]
  - Border: 2px solid [Primary color]
  - Text: [Primary color]
  - Padding: 12px 32px
  - Border radius: 8px
  - Hover: [Fill with primary color]

- **Text Link**:
  - Color: [Primary color]
  - Underline: On hover
  - Hover: [Darken or accent color]

**Forms**:
- Input fields:
  - Border: 1px solid [Border color]
  - Border radius: 6px
  - Padding: 12px 16px
  - Focus: [Primary color border, subtle glow]
  - Error: [Red border, error message below]

- Labels:
  - Font: [Body font]
  - Weight: Medium
  - Size: 14px
  - Position: Above input
  - Required indicator: Red asterisk

**Cards** (Service cards, testimonial cards, portfolio items):
- Background: White
- Border: 1px solid [Border color] OR subtle shadow
- Border radius: 12px
- Padding: 24px
- Hover: [Lift effect - translateY(-4px) + stronger shadow]

**Navigation**:
- Desktop:
  - Position: Sticky top
  - Background: [White with subtle shadow on scroll]
  - Height: 80px
  - Links: [Text color], hover [Primary color]
  
- Mobile:
  - Hamburger icon: Right side
  - Menu: Slide-in from right or dropdown
  - Background: [White or Primary color]
  - Close button: X icon

**Footer**:
- Background: [Dark - charcoal or primary color dark variant]
- Text: [Light gray or white]
- Links: [Light color], hover [Accent color]
- Layout: [4 columns desktop, stacked mobile]
- Padding: 48px vertical

---

### 6.5 Responsive Breakpoints

- **Mobile**: 320px - 767px (single column, stacked layouts)
- **Tablet**: 768px - 1023px (2 columns where appropriate)
- **Desktop**: 1024px+ (full multi-column layouts)

**Key Responsive Behaviors**:
- Navigation: Hamburger menu <1024px
- Grids: 3 col → 2 col → 1 col
- Hero: Image hidden on mobile, background image instead
- Typography: Reduce heading sizes by 30% on mobile
- Buttons: Full width on mobile
- Forms: Single column, larger touch targets

---

## 7. AI/Automation Opportunity Matrix

**Purpose**: Systematically evaluate and prioritize automation opportunities based on client pain points.

### 7.1 Assessment Methodology

For each process identified in questionnaire Section E1, we calculate a **Priority Score**:

**Formula**: (Repetition × 0.3) + (Time Investment × 0.3) + (Feasibility × 0.2) + (ROI × 0.2)

**Scoring Criteria**:

- **Repetition (0-5)**: How often task occurs
  - 0 = Rarely (monthly or less)
  - 3 = Weekly
  - 5 = Multiple times daily

- **Time Investment (0-5)**: Hours consumed
  - 0 = Minutes per week
  - 3 = Hours per week
  - 5 = Hours per day

- **Feasibility (0-5)**: Ease of automation
  - 0 = Requires complex human judgment
  - 3 = Partial automation possible
  - 5 = Fully automatable with existing tools

- **ROI Potential (0-5)**: Impact of automation
  - 0 = Low impact
  - 3 = Noticeable improvement
  - 5 = Game-changing

**Priority Tiers**:
- **4.0-5.0** = IMMEDIATE (Include in website or Phase 1 within 30 days)
- **3.0-3.9** = HIGH (Phase 2, propose within 30-60 days)
- **2.0-2.9** = MEDIUM (Phase 3, propose within 90 days)
- **<2.0** = LOW (Future consideration)

---

### 7.2 Opportunity Assessment Table

**[For EACH pain point from questionnaire E1, score and prioritize:]**

| Opportunity | Repetition | Time | Feasibility | ROI | Priority Score | Tier | Recommended Phase |
|-------------|-----------|------|-------------|-----|----------------|------|-------------------|
| [E1 Pain 1: e.g., "Answering same questions"] | [Score from E1 or 5] | [Score from E1 or estimate] | [Assess] | [Assess] | [Calculate] | [IMMEDIATE/HIGH/MEDIUM/LOW] | [Phase 1/2/3] |
| [E1 Pain 2: e.g., "Scheduling appointments"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 3: e.g., "Following up with leads"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 4: e.g., "Data entry"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 5: e.g., "Creating quotes"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 6: e.g., "Sending reminders"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 7: e.g., "Managing inventory"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 8: e.g., "Processing orders"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 9: e.g., "Social media posting"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |
| [E1 Pain 10: e.g., "Review management"] | [Score] | [Score] | [Assess] | [Assess] | [Calculate] | [Tier] | [Phase] |

---

### 7.3 Detailed Opportunity Specifications

**[For each opportunity scoring 3.0+, create detailed specification:]**

---

#### Opportunity: [Name - e.g., "AI FAQ Chatbot"]

**Priority Score**: [X.X] - **[Tier]**

**Current State**:
- Pain point: [From E1 - describe current manual process]
- Time spent: [Hours/week from E1 or estimate]
- Frequency: [How often this occurs]
- Business impact: [Cost of current inefficiency]

**Proposed Solution**:
[High-level description of automation]

**Functionality Details**:
1. [Feature component 1]
2. [Feature component 2]
3. [Feature component 3]
4. [Integration with website/systems]

**User Experience**:

*Customer-facing flow*:
1. [User trigger - e.g., "User clicks chat widget"]
2. [System response]
3. [User interaction]
4. [Outcome]

*Business-side flow*:
1. [What happens in background]
2. [Data capture/logging]
3. [Notifications/alerts]
4. [Reporting]

**Technical Implementation**:

*Recommended approach*: [No-code / Low-code / Custom]

*Tech stack*:
- Tool/Platform: [Specific recommendation]
- Integration method: [API / Webhook / Zapier]
- Data storage: [Where leads/data are saved]
- Dependencies: [Required accounts, services]

*Alternative approaches*:
- Option B: [If primary approach too expensive/complex]
- Option C: [Simpler MVP version]

**Implementation Plan**:
- Setup time: [Hours]
- Testing time: [Hours]
- Training time: [Hours for client]
- Total: [Total hours]
- Calendar time: [Days/weeks to completion]

**ROI Analysis**:

*Time savings*:
- Current time spent: [X hours/week]
- Estimated reduction: [Y%]
- Time saved: [Z hours/week]
- Annual value: [Z hours × 52 weeks × $hourly rate]

*Additional value*:
- [E.g., Lead capture after hours: +X leads/month]
- [E.g., Faster response time: +Y% conversion rate]
- [E.g., Improved customer satisfaction]

*Cost*:
- Setup: $[Range]
- Monthly ongoing: $[Range]
- Payback period: [Months]

**Risk Assessment**:
- Technical complexity: [Low/Medium/High]
- Client adoption risk: [Will they use it / Will customers use it]
- Maintenance requirement: [Hours/month]
- Mitigation strategies: [How to reduce risks]

**Recommendation**:
**Phase [1/2/3]** - [Justification for timing]

**Dependencies**:
- [Prerequisite 1 - e.g., "Website must be live first"]
- [Prerequisite 2 - e.g., "Client needs CRM account"]

**Success Metrics**:
- [Metric 1 - e.g., "Chatbot answers 80% of questions without escalation"]
- [Metric 2 - e.g., "Response time reduced from 4 hours to <5 minutes"]
- [Metric 3 - e.g., "30 additional leads captured per month"]

---

[REPEAT FOR EACH HIGH-PRIORITY AUTOMATION OPPORTUNITY - MAXIMUM 5 ENTRIES. Prioritize by Priority Score (highest scores first).]

---

### 7.4 Implementation Roadmap

**Phase 1: Website Launch** (Weeks 1-4)
- Focus: Core website functionality
- Automation: [Only if scored IMMEDIATE tier and low complexity]
  - [Automation 1 if any]
  - [Automation 2 if any]

**Phase 2: Quick Wins** (30-60 days post-launch)
- Focus: Low-hanging fruit automation with high ROI
- Proposed features:
  - [Automation from HIGH tier, Priority Score 3.5-3.9]
  - [Automation from HIGH tier]
- Investment: $[Estimated total]
- Expected ROI: [Combined time savings and value]

**Phase 3: Advanced Automation** (90+ days post-launch)
- Focus: Complex integrations, backend systems
- Proposed features:
  - [Automation from MEDIUM tier or complex HIGH tier]
  - [Automation from MEDIUM tier]
- Investment: $[Estimated total]
- Expected ROI: [Combined impact]

**Ongoing Optimization** (6+ months)
- Monthly retainer: $[Range]
- Included: Monitoring, adjustments, reporting, continuous improvement
- Focus: Data-driven refinements based on usage patterns

---

## 8. Success Criteria & KPIs

### 8.1 Launch Criteria (Definition of Done)

**Website must meet ALL criteria before going live:**

**Functionality**:
- [ ] All pages accessible and loading correctly
- [ ] All links working (no 404 errors)
- [ ] Contact form submitting successfully
- [ ] Form notifications reaching client email
- [ ] Auto-reply emails sending to users
- [ ] Mobile navigation functioning (hamburger menu)
- [ ] All CTAs linked to correct destinations
- [ ] Phone numbers click-to-call on mobile
- [ ] Email addresses linked (mailto:)
- [ ] Booking system integrated (if applicable)

**Content**:
- [ ] No `<<CLIENT_INPUT_REQUIRED>>` markers remaining (all required fields filled)
- [ ] Spelling and grammar checked (all pages)
- [ ] Client-provided content integrated
- [ ] Testimonials added (if available)
- [ ] Photos optimized and uploaded
- [ ] All images have alt text
- [ ] Legal pages (privacy policy, terms) if required

**Design & UX**:
- [ ] Design matches approved mockups/staging
- [ ] Brand colors and fonts consistent throughout
- [ ] Mobile responsive on all pages
- [ ] Tested on iPhone (Safari) and Android (Chrome)
- [ ] Tested on desktop (Chrome, Firefox, Safari)
- [ ] No horizontal scrolling on mobile
- [ ] Touch targets minimum 44x44px (mobile)
- [ ] Readable without zooming (mobile)

**Technical & SEO**:
- [ ] SSL certificate active (HTTPS)
- [ ] Favicon installed (all sizes)
- [ ] Google Analytics 4 installed and tracking
- [ ] Google Search Console set up
- [ ] XML sitemap generated and submitted
- [ ] Robots.txt configured
- [ ] Meta tags unique on each page (title, description)
- [ ] Schema markup on all pages (LocalBusiness, etc.)
- [ ] Open Graph tags for social sharing
- [ ] Canonical tags on all pages
- [ ] Page speed >85 on PageSpeed Insights (mobile & desktop)
- [ ] Mobile-friendly (passes Google test)

**Performance**:
- [ ] Images optimized (WebP format, <200KB each)
- [ ] CSS and JS minified
- [ ] Lazy loading enabled for below-fold images
- [ ] Gzip compression enabled
- [ ] Browser caching configured
- [ ] CDN active (if using)

**Accessibility**:
- [ ] Passes WAVE accessibility checker (0 errors)
- [ ] Color contrast meets WCAG AA (4.5:1)
- [ ] All images have descriptive alt text
- [ ] Form labels properly associated
- [ ] Keyboard navigable (can tab through all elements)
- [ ] Focus indicators visible
- [ ] Heading hierarchy logical (H1 > H2 > H3)
- [ ] ARIA labels where needed

**Business Requirements**:
- [ ] Google Business Profile linked (if applicable)
- [ ] Social media links working
- [ ] NAP (Name, Address, Phone) consistent everywhere
- [ ] Business hours displayed correctly
- [ ] Service area information accurate
- [ ] Pricing information (if displaying) approved by client

**Client Approval**:
- [ ] Client reviewed staging site
- [ ] All client-requested revisions completed
- [ ] Client signed off on go-live
- [ ] Client trained on any CMS/updates (if applicable)
- [ ] Client has access credentials (hosting, domain, email)

**Backup & Security**:
- [ ] Initial backup created
- [ ] Automated backups scheduled
- [ ] Uptime monitoring configured
- [ ] Security headers configured (if custom site)

---

### 8.2 30-Day Metrics (First Month Post-Launch)

**Goal**: Establish baseline performance and identify quick optimization opportunities

**Traffic Metrics**:
- **Total visits**: [Baseline goal - 100-500 for new local business site]
- **Unique visitors**: [80-90% of total visits]
- **Traffic sources**:
  - Direct: [20-30%]
  - Organic search: [30-40%]
  - Referral: [10-20%]
  - Social: [10-20%]
- **Device breakdown**:
  - Mobile: [Target 60-70%]
  - Desktop: [30-35%]
  - Tablet: [5-10%]

**Engagement Metrics**:
- **Bounce rate**: [Target <50% for homepage, <40% for service pages]
- **Average session duration**: [Target >1:30 for service businesses]
- **Pages per session**: [Target 2.5+]
- **Top landing pages**: [Expect homepage, then service pages]
- **Top exit pages**: [Expect contact page - post-conversion]

**Conversion Metrics**:
- **Form submissions**: [Goal based on industry - 10-30 for local service business]
- **Phone calls**: [If tracked - goal based on client's typical volume]
- **Booking completions**: [If applicable]
- **Email signups**: [If newsletter offered]
- **Conversion rate**: [Goal: 2-5% for local service businesses]

**Technical Metrics**:
- **Average page load time**: [Target <3 seconds]
- **PageSpeed score**: [Maintain >85]
- **Uptime**: [Target 99.9%]
- **Form submission success rate**: [100% - monitor for errors]

**Local SEO Metrics**:
- **Google Business Profile views**: [Baseline + growth goal]
- **Direction requests**: [From Google Business Profile]
- **Keyword rankings**: [Track 5-10 primary keywords, expect movement but not top rankings yet]

**Action Items from 30-Day Review**:
- Identify high-traffic, high-bounce pages → Optimize
- Identify low-performing CTAs → Test alternatives
- Analyze form abandonment → Simplify if needed
- Review search queries in Google Search Console → Content opportunities

---

### 8.3 90-Day Metrics (Quarter 1 Performance)

**Goal**: Demonstrate ROI, achieve local SEO rankings, refine for conversions

**Traffic Growth**:
- **Total visits**: [Target: 2-3x month 1 baseline]
- **Organic search growth**: [Target: 50-100% increase from month 1]
- **Returning visitors**: [Target: 20-30% of total]

**SEO Performance**:
- **Keyword rankings**:
  - Primary keywords: [Target: Top 10 for 3-5 keywords]
  - Long-tail keywords: [Target: Top 5 for 10+ variations]
  - "Near me" queries: [Appearing in local pack]
- **Impressions (Search Console)**: [Growth indicator]
- **Click-through rate**: [Target: 3-5% organic average]

**Conversion Optimization**:
- **Conversion rate**: [Target: Improvement of 10-20% from month 1 baseline]
- **Lead quality**: [Track consultation show-up rate, quote acceptance rate]
- **Cost per lead**: [Calculate total investment / leads generated]
- **Revenue attributed to website**: [If client can track - closed deals from website leads]

**Content Performance**:
- **Top-performing pages**: [Which pages drive most conversions]
- **Blog traffic**: [If blog implemented - growth in organic traffic from content]
- **Time on page**: [Improvement indicates better content relevance]

**User Behavior Insights**:
- **Conversion paths**: [Typical journey before conversion]
- **Device preferences**: [Optimize further for highest-converting device]
- **Geographic data**: [Where traffic is coming from - target vs. actual]

**Business Impact**:
- **Leads generated**: [Total from website]
- **Lead-to-customer conversion rate**: [Client's internal metric]
- **Customer acquisition cost**: [Website investment / customers acquired]
- **Competitive position**: [Search visibility vs. competitors from D1]

**Automation Impact** [If Phase 2 implemented]:
- **Time saved**: [Hours per week on automated tasks]
- **Response time improvement**: [Before vs. after automation]
- **Lead capture improvement**: [Leads captured after hours, weekends]
- **Review volume increase**: [If review automation implemented]
- **No-show reduction**: [If appointment reminders implemented]

---

### 8.4 Success Indicators by Business Goal

**[Map to client's top 3 goals from questionnaire A2:]**

**Goal 1**: [Client's top goal from A2]
- **KPI**: [Specific measurable metric]
- **30-day target**: [Realistic milestone]
- **90-day target**: [Bigger milestone]
- **Measurement method**: [How we track this]

**Goal 2**: [Client's second goal from A2]
- **KPI**: [Metric]
- **30-day target**: [Milestone]
- **90-day target**: [Milestone]
- **Measurement method**: [Tracking method]

**Goal 3**: [Client's third goal from A2]
- **KPI**: [Metric]
- **30-day target**: [Milestone]
- **90-day target**: [Milestone]
- **Measurement method**: [Tracking method]

---

### 8.5 Reporting & Review Schedule

**Weekly** (First 4 weeks post-launch):
- Quick check-in: Traffic, form submissions, any issues
- Format: Email update
- Action: Address any technical issues immediately

**30-Day Review** (End of month 1):
- Comprehensive first-month report
- Format: Report document + 30-minute call
- Topics:
  - Traffic and engagement analysis
  - Conversion performance
  - Technical health check
  - Quick optimization opportunities
  - **Introduce Phase 2 automation opportunities** (if appropriate)

**60-Day Check-in** (Month 2):
- Progress update
- Format: Email report
- Focus: Trends, compare to month 1

**90-Day Strategic Review** (End of quarter):
- Comprehensive performance report
- Format: Detailed report + 60-minute strategy call
- Topics:
  - Quarter 1 performance vs. goals
  - ROI analysis
  - SEO progress and rankings
  - User behavior insights
  - Conversion optimization recommendations
  - **Formal Phase 2/3 automation proposal** (with data to support ROI)
  - Content and feature roadmap for next quarter

**Ongoing** (If retainer):
- Monthly reports
- Quarterly strategy sessions
- Continuous optimization

---

## 9. Project Timeline & Milestones

**Total Duration**: [X weeks based on tier from pricing framework]

### Week 1: Discovery & Foundation
- **Days 1-2**:
  - [X] Discovery call completed (questionnaire review)
  - [X] PRD finalized and client approved
  - [X] Contracts signed, deposit received
- **Days 3-5**:
  - [ ] Technical specification completed
  - [ ] Design direction approved (style, colors, inspiration)
  - [ ] Content requirements documented
- **Days 6-7**:
  - [ ] Development environment set up
  - [ ] Repository created
  - [ ] Domain/hosting configured

### Week 2: Design & Development
- **Days 1-3**:
  - [ ] Homepage design/development
  - [ ] Component library built (header, footer, cards)
  - [ ] Design system implemented (colors, typography)
- **Days 4-7**:
  - [ ] Service pages developed
  - [ ] About page developed
  - [ ] Contact page and form built
  - [ ] Portfolio/testimonials page (if applicable)

### Week 3: Integration & Content
- **Days 1-2**:
  - [ ] Backend form handling configured
  - [ ] CRM integration (if applicable)
  - [ ] Analytics and tracking set up
- **Days 3-5**:
  - [ ] Content population (copy, images)
  - [ ] SEO meta tags and schema markup
  - [ ] Performance optimization
- **Days 6-7**:
  - [ ] Cross-browser testing
  - [ ] Mobile responsiveness QA
  - [ ] Accessibility audit and fixes

### Week 4: Launch & Training
- **Days 1-2**:
  - [ ] Client review on staging
  - [ ] Revisions based on feedback
- **Day 3**:
  - [ ] Final approval from client
  - [ ] Pre-launch checklist completed
  - [ ] **LAUNCH** to production
- **Days 4-5**:
  - [ ] Post-launch monitoring (forms, analytics, uptime)
  - [ ] Bug fixes if any issues arise
  - [ ] Client training session (if CMS or tools to manage)
- **Days 6-7**:
  - [ ] Final documentation delivered
  - [ ] Handoff complete
  - [ ] Final payment collected

---

## 10. Risks & Mitigation Strategies

**Potential Risk 1**: Content delays from client
- **Impact**: Timeline extension
- **Mitigation**: Use `<<CLIENT_INPUT_REQUIRED>>` markers where data is missing; provide clear deadlines in kickoff; collect minimal content before development starts

**Potential Risk 2**: Scope creep (client requests additional features)
- **Impact**: Timeline/budget overrun
- **Mitigation**: Clear SOW, change request process, document everything in writing

**Potential Risk 3**: Technical integration issues (CRM, booking system APIs)
- **Impact**: Feature functionality, timeline delays
- **Mitigation**: Test integrations early, have backup options (Zapier vs. direct API), build time buffer

**Potential Risk 4**: Design approval delays (client indecision)
- **Impact**: Timeline extension
- **Mitigation**: Limit revision rounds in contract, provide guided choices (2-3 options max), set approval deadlines

**Potential Risk 5**: Browser/device compatibility issues
- **Impact**: Poor user experience for some visitors
- **Mitigation**: Test early and often, use progressive enhancement, fallbacks for older browsers

---

## 11. Next Steps & Action Items

**Immediate** (This week):
- [ ] Review this PRD with client for accuracy
- [ ] Finalize any missing information from questionnaire
- [ ] Approve design direction and style
- [ ] Client provides brand assets (logo, photos, content)
- [ ] Set up project management (GitHub, Notion, etc.)
- [ ] Schedule weekly check-in calls

**Week 1 Kickoff**:
- [ ] Kickoff call (review timeline, expectations, communication)
- [ ] Domain/hosting access obtained
- [ ] Development environment configured
- [ ] First progress update sent

**Client Responsibilities**:
- [ ] Provide content by [DATE]
- [ ] Provide photos/videos by [DATE]
- [ ] Review staging site by [DATE]
- [ ] Approve for launch by [DATE]
- [ ] Available for feedback (48-hour turnaround)

**Your Responsibilities**:
- [ ] Deliver staging site by [DATE]
- [ ] Weekly progress updates
- [ ] Address feedback within 24-48 hours
- [ ] Launch by [DATE]
- [ ] Post-launch support for [30/60/90 days]

---

## 12. Appendix

### A. Questionnaire Responses (Raw Data)

[Paste complete questionnaire responses here for reference]

### B. Competitor URLs & Analysis Notes

[From questionnaire D1 - full URLs and detailed notes]

### C. Inspiration Sites & Screenshots

[From questionnaire D2 - full URLs and specific elements to reference]

### D. Client-Provided Assets Inventory

- Logo files: [List received files]
- Photos: [List/categorize]
- Brand guidelines: [If provided]
- Existing content: [What's available]

### E. Technical Credentials & Access

[To be filled during project setup]
- Domain registrar: [Login URL]
- Hosting: [Provider, login URL]
- Email: [Provider]
- Analytics: [Google Analytics property ID]
- Other tools: [As needed]

---

**END OF PRD**

---

**Document Information**:
- **Created**: [Date]
- **Last Updated**: [Date]
- **Version**: 1.0
- **Author**: [Your name]
- **Client**: [Business name]
- **Project Code**: [Internal tracking code if you use one]

---

**Approval Signatures**:

**Client**: _________________________ Date: _______

**Project Manager**: _________________________ Date: _______

---

## END OF WORKFLOW SCRIPT

---

## Usage Instructions for IDE Agents

**Note**: For the complete workflow overview and data collection steps, see the "How to Use" section at the top of this document.

### Platform-Specific Instructions:

**For Cursor / Windsurf / Antigravity:**
1. Follow steps 1-3 from "How to Use" section above
2. In Composer/Chat mode, paste the entire workflow script
3. Immediately after the script, paste client questionnaire data in this format:

```
[CLIENT_DATA]

Business Name: [Name]
Industry: [Industry]
Location: [City, State]

[Paste completed questionnaire responses - all sections A through F]

Section E1: Current Pain Points (scored 0-5)
- [Pain point 1]: [Score]
- [Pain point 2]: [Score]
[... continue for all pain points ...]
```

4. Add final instruction: "Generate complete PRD following the framework above. Output as `[BusinessName]_PRD.md` file."

**For GitHub Copilot / Standard Coding Assistants:**
1. Create new file: `[BusinessName]_PRD.md`
2. Add comment block at top:

```markdown
<!--
INSTRUCTIONS FOR AI:
Generate a complete Product Requirements Document following PRD Framework structure below.

CLIENT DATA:
[Paste questionnaire responses - see Pre-Generation Validation Checklist for required fields]

Use the framework sections to create comprehensive, specific PRD with:
- Never invent data - use `<<CLIENT_INPUT_REQUIRED>>` for missing required inputs
- Calculated automation priority scores
- Specific technical recommendations
- Actionable requirements
-->
```

3. Below the comment, paste the PRD Framework structure from this workflow script
4. Use Copilot to fill in each section (tab through, accept suggestions, refine)

### Tips for Best Results:

**Complete data matters**: The more thorough the questionnaire responses, the better the PRD quality

**Review for accuracy**: AI generates comprehensive PRDs, but verify:
- Client-specific language and terminology
- Realistic timelines based on your capacity
- Pricing aligned with your business model
- Technical choices matching your preferred stack

**Iterative generation**: For complex projects, generate sections individually:
- "Generate Section 3: Feature Requirements only"
- "Generate Section 7: Automation Opportunity Matrix only"

**Save customizations**: After first successful PRD, save your framework customizations for future projects

---

## Integration with Main Template

This workflow script works with:
- **Section 1**: Client Discovery Questionnaire (input data source)
- **Section 2**: PRD Generation Framework (structure this script implements)
- **Section 3-8**: All downstream sections reference the PRD as source of truth

**Workflow Position**:
```
Client Discovery Questionnaire (Manual)
    ↓
[THIS SCRIPT] → Generate PRD (AI-Assisted)
    ↓
Technical Specification (Manual/AI-Assisted)
    ↓
Task Breakdown (Manual/AI-Assisted)
    ↓
Development (AI-Assisted)
```

---

## Customization Guide

**To adapt this script for your business:**

1. **Adjust pricing recommendations** in Section 6 to match your rates
2. **Modify tech stack defaults** in Section 4 to your preferred tools
3. **Update automation tools** in Section 7 to platforms you're comfortable with
4. **Change timeline estimates** in Section 9 based on your speed
5. **Add/remove sections** based on your service offerings

**Version Control**: Save customized version as `PRD-Generator-[YourCompany].md`

---

**Version**: 1.0
**Last Updated**: January 30, 2026
**Compatible With**: Main AI Design Consulting Template v1.0
**License**: [Your choice]
