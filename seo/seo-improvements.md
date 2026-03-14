# MyClawAgent.io — SEO Improvements
**Specific changes to make to index.html (and site structure)**

Audit based on: http://myclawagent.io (GitHub Pages deployment, March 2026)

---

## 1. Title Tag — CRITICAL FIX

**Current:**
```html
<title>MyClawAgent — Your AI Agent, Deployed & Done</title>
```

**Problem:** The primary keyword "OpenClaw" is completely absent. This is the #1 search term for your service. Anyone Googling "OpenClaw setup service" won't see your brand.

**Recommended:**
```html
<title>MyClawAgent — OpenClaw Setup & Deployment Service for Founders</title>
```

**Alt variant (A/B test):**
```html
<title>MyClawAgent | Managed OpenClaw Agent for CEOs & Exec Teams</title>
```

---

## 2. Meta Description — CRITICAL FIX

**Current:** None detected (Google will auto-generate from page text — uncontrolled)

**Recommended:**
```html
<meta name="description" content="We deploy and manage your OpenClaw AI agent — fully secured, same-day setup. Handles email, calendar, and CRM 24/7 via Telegram, Discord, or WhatsApp. No tech skills required. Built for founders, CEOs, and exec teams.">
```

Keep under 160 characters for display. Include: OpenClaw, founders, 24/7, setup, managed.

---

## 3. H1 Tag — FIX

**Current H1 (inferred):** "Your Personal AI Agent. Deployed. Secured. Always On."

**Problem:** Keyword-free. No mention of OpenClaw, setup, deployment.

**Recommended H1:**
```html
<h1>OpenClaw Setup & Management Service for Founders and Exec Teams</h1>
```

Then use the current tagline as a styled subheadline/paragraph (not H1).

---

## 4. H2 Structure — IMPROVE

Current H2s: "Built For People Who Move Fast", "Always On. Always Working.", "How It Works", "Simple Pricing", "What People Are Saying", "Ready to Get Your Agent?"

**Problems:** No keywords in H2s. Google uses H2s for understanding page topic.

**Recommended H2 rewrites:**

| Current H2 | Recommended H2 |
|------------|----------------|
| "Built For People Who Move Fast" | "Who Gets the Most from a Managed OpenClaw Agent?" |
| "Always On. Always Working." | "Your OpenClaw Agent Works 24/7 — Even While You Sleep" |
| "How It Works" | "How Our OpenClaw Deployment Process Works" |
| "Simple Pricing" | "OpenClaw Setup & Managed Care Pricing" |
| "What People Are Saying" | "What Founders Say About Their OpenClaw Agent" |
| "Ready to Get Your Agent?" | "Ready to Deploy Your OpenClaw AI Agent?" |

---

## 5. Add Missing Meta Tags

Add to `<head>`:

```html
<!-- Canonical (especially important since GitHub Pages may create duplicate) -->
<link rel="canonical" href="https://myclawagent.io/" />

<!-- Robots -->
<meta name="robots" content="index, follow" />

<!-- Keywords (secondary, but still used by some engines) -->
<meta name="keywords" content="OpenClaw setup, OpenClaw deployment, AI agent for founders, managed AI assistant, personal AI agent, OpenClaw service, executive AI agent" />

<!-- Author -->
<meta name="author" content="MyClawAgent" />
```

---

## 6. Schema Markup — ADD (Currently Missing Entirely)

Add these JSON-LD schema blocks inside `<head>` or before `</body>`:

### Organization Schema
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "MyClawAgent",
  "url": "https://myclawagent.io",
  "logo": "https://myclawagent.io/logo.png",
  "description": "Managed OpenClaw AI agent deployment and support service for founders and executive teams.",
  "sameAs": [
    "https://twitter.com/myclawagent",
    "https://linkedin.com/company/myclawagent"
  ]
}
</script>
```

### Service Schema
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "OpenClaw AI Agent Deployment",
  "provider": {
    "@type": "Organization",
    "name": "MyClawAgent"
  },
  "description": "White-glove OpenClaw AI agent setup, security hardening, and ongoing managed support for founders and exec teams.",
  "serviceType": "AI Agent Deployment & Management",
  "audience": {
    "@type": "Audience",
    "audienceType": "Founders, CEOs, Executive Teams, Agencies"
  }
}
</script>
```

### FAQ Schema (Add this — big CTR boost in SERPs)
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is OpenClaw?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "OpenClaw is an open-source AI assistant that runs 24/7 on dedicated infrastructure. It handles email triage, calendar management, CRM updates, and more — proactively, without you asking."
      }
    },
    {
      "@type": "Question",
      "name": "Do I need technical knowledge to use your service?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. We handle everything — from installation and security hardening to integration with your email, calendar, and messaging apps. You just tell us what to automate."
      }
    },
    {
      "@type": "Question",
      "name": "How long does OpenClaw setup take?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Most agents go live same day. After your kickoff call, we deploy and configure your OpenClaw agent within hours."
      }
    },
    {
      "@type": "Question",
      "name": "What messaging apps does my OpenClaw agent work with?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Your agent works through Telegram, Discord, or WhatsApp — whatever you already use."
      }
    }
  ]
}
</script>
```

---

## 7. Add an FAQ Section to the Page (HTML)

SetupClaw has 12 FAQ items. myclawagent.io has zero. **Add a FAQ section** before the final CTA block. Minimum 6–8 questions targeting long-tail keywords like:
- "What is OpenClaw?"
- "Do I need to be technical?"
- "How long does setup take?"
- "Is my data secure?"
- "What's the difference between Starter and Full Agent?"
- "What happens after 14-day hypercare?"

---

## 8. Add Investors/VCs as a Fourth ICP

SetupClaw specifically calls out investors and VCs. myclawagent.io is missing this segment entirely. Add:

```html
<div class="icp-card">
  <span>📊</span>
  <h3>Investors & VCs</h3>
  <p>Deal flow tracking, portfolio company updates, LP comms — your agent keeps you informed and responsive without inbox overload.</p>
</div>
```

---

## 9. Internal Linking Structure

Currently there are no blog posts or additional pages to link to. As soon as you publish blog posts (see content-plan.md), add:
- Footer link to blog index
- Contextual links in copy (e.g., "Learn more about OpenClaw security →")
- Breadcrumbs if you add subpages

---

## 10. Page Speed & Core Web Vitals

Since this is a GitHub Pages static site:

1. **Images:** Ensure any images (logo, illustrations) are served in WebP format with explicit `width` and `height` attributes to prevent Cumulative Layout Shift (CLS)
2. **Fonts:** If using Google Fonts, add `<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>` to reduce font load time
3. **Remove unused CSS/JS:** Audit for any unused CSS (likely minimal on a simple landing page)
4. **Add `loading="lazy"`** to any below-the-fold images
5. **Compress assets** using GitHub Actions with image compression workflow
6. **Add `<link rel="preload">`** for the hero section image/font

---

## 11. Redirect myclawagent.net and myclawagent.cloud

Once those domains are live, set up 301 redirects to myclawagent.io. This consolidates link equity to the primary domain.

---

## 12. Fix "As Seen In" Section

Currently lists MacStories, Fast Company, IBM Think, Cisco Blogs — but these are references to OpenClaw coverage, not myclawagent.io coverage specifically. This could be misleading. Two options:
- Label it: "OpenClaw — as featured in" (honest)
- Replace with actual customer testimonials from named sources
- Pursue actual coverage and earn those logos properly (see backlink-strategy.md)

---

## Priority Order

1. ✅ Fix title tag (TODAY)
2. ✅ Add meta description (TODAY)
3. ✅ Fix H1 to include "OpenClaw" (TODAY)
4. ✅ Add canonical tag (TODAY)
5. ✅ Add JSON-LD schema (this week)
6. ✅ Add FAQ section with 6–8 Q&As (this week)
7. ✅ Fix H2s to include keywords (this week)
8. ✅ Add Investors/VCs ICP card (this week)
9. ✅ Page speed audit and fixes (month 1)
10. ✅ Internal linking as content grows (ongoing)
