# LinkedIn Ads Creative Production — Guide

Production workflow, design specs, templates, and batch creation strategies for ABM campaigns on LinkedIn.

For creative strategy and messaging frameworks, see [linkedin-ads-creative-strategy.md](./linkedin-ads-creative-strategy.md)
For ad formats, budget math, and campaign structure, see [linkedin-ads-abm-guide.md](./linkedin-ads-abm-guide.md)

---

## Creative Production Workflow

### Phase 1: Brief

Before any creative work, document:

| Element | Required Information |
|---------|---------------------|
| **Campaign goal** | Awareness, engagement, conversions |
| **Funnel stage** | TOF/MOF/BOF |
| **Target persona** | Role, JTBD, pain points |
| **Message angle** | Which of the 12 angles (see creative-strategy.md) |
| **Format** | SI, VI, CI, DOC, TLA, VTLA |
| **CTA** | Learn More, Request Demo, etc. |
| **Landing page** | URL and key message match |
| **Deadline** | When creative is needed |

### Creative Brief Template

```
CAMPAIGN: [Name]
DATE: [YYYY-MM-DD]
OWNER: [Name]

OBJECTIVE
- Goal: [Awareness/Engagement/Conversion]
- Stage: [TOF/MOF/BOF]
- Success metric: [CTR/Engagement/Conversions]

AUDIENCE
- Persona: [Title/Role]
- Pain point: [Primary problem]
- JTBD: [What they're trying to accomplish]
- Awareness level: [Problem-aware/Solution-aware/Product-aware]

MESSAGE
- Angle: [From 12 angles]
- Framework: [PAS/BAB/AIDA/PPP/FAB]
- Key value prop: [One sentence]
- Proof point: [Stat, testimonial, or logo]

FORMAT
- Type: [SI/VI/CI/DOC/TLA/VTLA]
- Specs: [Dimensions, length]
- Quantity: [How many variants]

COPY
- Headline: [70 chars max]
- Intro text: [150 chars max]
- CTA: [Learn More/Request Demo/etc.]

VISUAL DIRECTION
- Style: [Minimal/Bold/Corporate/Casual]
- Imagery: [Product screenshot/Photo/Illustration]
- Must-haves: [Logo placement, brand colors]
- Avoid: [Stock photos, specific competitors]

DELIVERY
- Deadline: [Date]
- File format: [PNG/JPG/MP4]
- Naming: [Convention]
```

---

### Phase 2: Design

**Who does what:**

| Role | Responsibility |
|------|---------------|
| **Marketing/PMM** | Brief, copy, messaging approval |
| **Designer** | Visual execution, specs compliance |
| **Paid Media** | Platform requirements, naming, upload |

**Design process:**
1. Designer receives brief
2. First draft within 2-3 business days
3. Internal review (1 round)
4. Revisions (1-2 days)
5. Final approval
6. Export in correct specs
7. Hand off to paid media

### Phase 3: Review

**Quality gates checklist:**

- [ ] Headline under 70 characters
- [ ] Intro text under 150 characters
- [ ] CTA matches landing page CTA
- [ ] No spelling or grammar errors
- [ ] Logo visible and correctly placed
- [ ] Safe area respected (no cropping issues)
- [ ] File size under 5MB
- [ ] Correct dimensions for format
- [ ] Mobile preview looks good
- [ ] Brand guidelines followed
- [ ] Proof point is accurate and verified
- [ ] Naming convention applied

### Phase 4: Launch

**Upload checklist:**

- [ ] Creative uploaded to LinkedIn Campaign Manager
- [ ] Correct campaign selected
- [ ] Naming convention verified
- [ ] Tracking parameters in landing page URL
- [ ] Preview checked (desktop + mobile)
- [ ] Creative status set correctly
- [ ] Documentation updated

---

## Design Specs by Format

### Single Image Ads

| Spec | Horizontal (1.91:1) | Square (1:1) | Vertical (4:5) |
|------|---------------------|--------------|----------------|
| **Dimensions** | 1200 × 628 px | 1200 × 1200 px | 720 × 900 px |
| **Best for** | Desktop feed | Cross-device | Mobile feed |
| **File type** | PNG, JPG, GIF | PNG, JPG, GIF | PNG, JPG, GIF |
| **File size** | Max 5 MB | Max 5 MB | Max 5 MB |

**Copy limits:**
- Headline: 70 characters (200 max, truncates)
- Intro text: 150 characters (600 max, truncates)
- CTA: Select from dropdown

**Safe area:** Keep important content away from edges — feed UI overlays crop differently on mobile vs desktop.

---

### Video Ads

| Spec | Requirement |
|------|-------------|
| **Dimensions** | 1920 × 1080 (horizontal), 1080 × 1080 (square), 1080 × 1920 (vertical) |
| **Aspect ratio** | 16:9, 1:1, or 9:16 |
| **File size** | 75 KB - 200 MB |
| **Duration** | 3 seconds - 30 minutes (recommend 15-30s for TOF, 1-2 min for MOF) |
| **File type** | MP4 |
| **Frame rate** | 30 fps recommended |
| **Audio** | AAC, MP3 (optional but recommended) |

**Best practices:**
- Hook in first 3 seconds
- Add captions/subtitles (80% watch without sound)
- End with clear CTA
- Include logo throughout

---

### Carousel Ads

| Spec | Requirement |
|------|-------------|
| **Cards** | 2-10 per carousel |
| **Image dimensions** | 1080 × 1080 px per card |
| **File type** | PNG, JPG |
| **File size** | Max 10 MB total |
| **Headline** | 45 characters per card |
| **Description** | Optional, 70 characters |

**Best practices:**
- Tell a sequential story
- First card = strongest hook
- Each card should work standalone
- Consistent visual style across cards
- Last card = strongest CTA

---

### Document Ads

| Spec | Requirement |
|------|-------------|
| **File type** | PDF |
| **File size** | Max 100 MB |
| **Pages** | Up to 300 |
| **Recommended** | 3-10 pages for ads |

**Best practices:**
- First page = compelling hook (like a cover)
- Each page should deliver value
- Include CTA on multiple pages
- Optimize for quick scanning
- Brand consistently throughout

---

### Thought Leader Ads (TLA)

| Spec | Requirement |
|------|-------------|
| **Post type** | Organic post from personal profile |
| **Character limit** | 3,000 characters |
| **Recommended** | 1,000-1,500 characters |
| **Images** | Same specs as single image |
| **Video** | Same specs as video ads |

**TLA-specific requirements:**
- Member must be added as Employee or Thought Leader in ad account
- Auto-approval enabled in account settings
- Post must be public
- Cannot sponsor private posts or posts from non-connected members

---

### Text Ads

| Spec | Requirement |
|------|-------------|
| **Image** | 100 × 100 px |
| **Headline** | 25 characters |
| **Description** | 75 characters |

**Best practices:**
- Cheap CPM (~$5.23)
- Good for brand reinforcement
- Don't expect high CTR
- Run alongside other formats

---

## Version Management

### Naming Convention

Format: `[Messaging]_[Format]_[Angle]_[Version]`

| Component | Options | Examples |
|-----------|---------|----------|
| **Messaging** | Product category or value prop | User-Analytics, Session-Replay, Activation |
| **Format** | SI, VI, CI, DOC, TLA, VTLA | SI |
| **Angle** | From 12 angles | Customer-Proof, Pain-Callout, Before-After |
| **Version** | v1, v2, v3 OR date | v1, 15Feb2026 |

**Examples:**
- `User-Analytics_SI_Customer-Proof_v1`
- `Session-Replay_VI_Product-Demo_v2`
- `Activation_CI_Before-After_15Feb2026`
- `Churn_TLA_Thought-Leadership_v1`
- `Growth_VTLA_Customer-Testimonial_v3`

### File Organization

```
/creative-library
  /[Campaign Name]
    /briefs
      - campaign-brief.md
    /source
      - figma-link.txt
      - assets/
    /exports
      /single-image
        - User-Analytics_SI_Customer-Proof_v1.png
        - User-Analytics_SI_Customer-Proof_v2.png
      /video
        - Session-Replay_VI_Product-Demo_v1.mp4
      /carousel
        - Activation_CI_Before-After_v1_card1.png
        - Activation_CI_Before-After_v1_card2.png
    /archive
      - [retired creatives]
```

### Version Control Rules

| Rule | Why |
|------|-----|
| Never overwrite originals | Need to compare performance |
| Increment version numbers | Track iterations |
| Archive, don't delete | May need to revive later |
| Document changes | Know what was tested |

---

## Creative Library Organization

### Tagging System

Tag every creative with:

| Tag Type | Examples |
|----------|----------|
| **Stage** | TOF, MOF, BOF |
| **Format** | SI, VI, CI, DOC, TLA |
| **Angle** | Customer-Proof, Pain-Callout, Before-After |
| **Persona** | PM, CMO, RevOps, SDR |
| **Status** | Active, Paused, Testing, Retired |
| **Performance** | Winner, Loser, Testing |

### Library Audit (Monthly)

- [ ] All active creatives documented
- [ ] Performance data updated
- [ ] Winners identified for scaling
- [ ] Losers flagged for retirement
- [ ] Gaps identified (missing formats/angles)
- [ ] Next month's creative needs planned

---

## Batch Production Strategies

### How to Create 20 Ads Efficiently

**The 5 × 4 Matrix:**

Create 5 message variations × 4 visual variations = 20 unique ads

| Message Variations | Visual Variations |
|-------------------|-------------------|
| Pain-focused headline | Screenshot-based |
| Benefit-focused headline | Photo-based |
| Question headline | Illustration-based |
| Stat-led headline | Text-heavy/bold |
| Testimonial headline | Logo wall |

**Workflow:**

1. Write all 5 headlines first
2. Get copy approval
3. Designer creates 1 master template
4. Apply each headline to template
5. Create 4 visual variations of each
6. Export all 20 in batch

**Time estimate:**
- Copy: 2 hours
- Design: 4-6 hours
- Review: 1 hour
- Export: 1 hour
- **Total: 1-2 days for 20 ads**

### Template-Based Production

**Master template includes:**
- Brand colors
- Logo placement
- Font styles
- Safe areas marked
- Placeholder text boxes
- Placeholder image areas

**Benefits:**
- Consistent brand look
- Faster iteration
- Easy A/B testing (swap one element)
- Team can use without designer

---

## Tools

### Design Tools

| Tool | Best For | Cost |
|------|----------|------|
| **Figma** | Collaborative design, templates | Free-$15/user/mo |
| **Canva** | Quick iterations, non-designers | Free-$13/user/mo |
| **Adobe Creative Suite** | Professional production | $55/mo |
| **Loom** | Quick video recording | Free-$15/mo |
| **Descript** | Video editing, captions | $15-24/mo |

### Figma Template Libraries

Build templates for:
- Single image (3 aspect ratios)
- Carousel (consistent card style)
- Video thumbnail
- Document cover
- TLA post visual

### Video Production Stack

| Stage | Tools |
|-------|-------|
| **Recording** | Loom, Riverside, Zoom |
| **Editing** | Descript, CapCut, Premiere |
| **Captions** | Descript, Rev, Kapwing |
| **Thumbnails** | Figma, Canva |

---

## Quality Gates

### Pre-Launch Checklist

**Copy:**
- [ ] Headline under character limit
- [ ] Intro text under character limit
- [ ] No spelling/grammar errors
- [ ] CTA clear and matches landing page
- [ ] Proof points verified

**Visual:**
- [ ] Correct dimensions
- [ ] File size under limit
- [ ] Brand colors correct
- [ ] Logo visible
- [ ] Safe areas respected
- [ ] Mobile preview looks good

**Compliance:**
- [ ] No competitor trademarks
- [ ] Claims are substantiated
- [ ] Testimonials have permission
- [ ] LinkedIn ad policies followed

**Technical:**
- [ ] File format correct
- [ ] Naming convention applied
- [ ] Tracking parameters in URL
- [ ] UTM tags configured

### Post-Launch Checklist (Day 1)

- [ ] Ads serving impressions
- [ ] No disapprovals
- [ ] Landing page loading
- [ ] Tracking firing correctly
- [ ] Mobile rendering properly

---

## Refresh Playbooks

### Visual Refresh (Same Message)

When: CTR dropping, same angle still works

**What to change:**
- Color scheme
- Image/illustration style
- Layout arrangement
- Typography treatment
- Background texture

**What stays the same:**
- Headline
- Value proposition
- CTA
- Core message

**Time: 2-4 hours per creative**

### Message Refresh (Same Visual Style)

When: Visual works, message fatigue

**What to change:**
- Headline angle
- Proof point
- Problem framing
- CTA text

**What stays the same:**
- Visual style
- Brand elements
- Layout structure

**Time: 1-2 hours per creative**

### Complete Refresh

When: New campaign, major pivot, or full fatigue

**What to change:**
- Everything

**Process:**
- Start from new brief
- New angle selection
- Fresh visual direction
- Full production cycle

**Time: 1-2 weeks for full suite**

---

## Production Calendar Template

### Monthly Cadence

| Week | Activity |
|------|----------|
| **Week 1** | Review performance, identify refresh needs |
| **Week 2** | Briefs for new creatives, copy development |
| **Week 3** | Design production |
| **Week 4** | Review, approval, staging for next month |

### Quarterly Planning

| Quarter Start | Deliverable |
|--------------|-------------|
| **Q planning** | Full creative audit |
| **Week 1** | Campaign briefs finalized |
| **Week 2-3** | Hero creative production |
| **Week 4-6** | Variation production |
| **Week 7-12** | Testing and optimization |

---

## Common Production Mistakes

| Mistake | Impact | Fix |
|---------|--------|-----|
| Designing for one size only | Bad mobile experience | Design mobile-first or create all sizes |
| Ignoring safe areas | Cropped text/logos | Use LinkedIn's safe zone guidelines |
| Text too small | Illegible on mobile | Minimum 24px for body, 36px for headlines |
| No version control | Can't track what's working | Strict naming convention |
| Skipping review | Errors go live | Use quality gates checklist |
| Over-designing | Message gets lost | Simplicity wins in feed |
| No templates | Slow production | Build reusable templates |
| Designer bottleneck | Delays | Empower team with Canva/simple tools |

---

## Quick Reference: Specs Summary

| Format | Dimensions | Max File Size | Key Limit |
|--------|-----------|---------------|-----------|
| **SI (horizontal)** | 1200 × 628 | 5 MB | 70 char headline |
| **SI (square)** | 1200 × 1200 | 5 MB | 70 char headline |
| **SI (vertical)** | 720 × 900 | 5 MB | 70 char headline |
| **Video** | 1920 × 1080 | 200 MB | 30 min max |
| **Carousel** | 1080 × 1080/card | 10 MB total | 2-10 cards |
| **Document** | PDF | 100 MB | 300 pages |
| **Text Ad** | 100 × 100 | — | 25 char headline |

---

> **Built by [ColdIQ](https://www.coldiq.com) & [Ivan Falco](https://www.linkedin.com/in/ivanfalco/en/).** For questions on implementation or anything not covered here, reach out to Ivan directly on [LinkedIn](https://www.linkedin.com/in/ivanfalco/en/).
