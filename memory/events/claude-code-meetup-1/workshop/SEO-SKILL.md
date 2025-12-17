---
name: SEO
description: Ultimate SEO optimization skill for any website; use when user wants to improve SEO, add meta tags, structured data, or optimize for search engines and AI answer engines
---

# Ultimate SEO Skill

## Overview

This skill provides comprehensive SEO optimization for **any website**, regardless of framework or tech stack. It covers traditional SEO (Google, Bing), Generative Engine Optimization (GEO) for AI search engines (ChatGPT, Perplexity, Claude, Google AI Overviews), and technical SEO best practices.

## When to Use This Skill

Invoke this skill when the user:
- Wants to improve their website's SEO
- Needs to add meta tags, Open Graph, or Twitter Cards
- Wants structured data (JSON-LD schemas)
- Asks about optimizing for search engines
- Mentions improving rankings or visibility
- Wants to optimize for AI search/answer engines
- Needs help with sitemaps, robots.txt, or canonical URLs
- Asks about page speed or Core Web Vitals

---

## 🎨 CUSTOMIZATION GUIDE

### Adapt to Your Framework

This skill works with any framework. Replace examples as needed:

| Framework | Meta Tags Location |
|-----------|-------------------|
| **Next.js** | `layout.tsx` with `Metadata` export |
| **React** | `react-helmet` or `index.html` |
| **Vue/Nuxt** | `nuxt.config.js` or `useHead()` |
| **Astro** | Frontmatter or `<head>` |
| **HTML** | Direct `<head>` tags |
| **WordPress** | Yoast/RankMath or `functions.php` |

### Customize for Your Industry

Replace example content with your industry specifics:
- E-commerce: Product schema, reviews, pricing
- Blog: Article schema, author info, dates
- Local Business: LocalBusiness schema, maps, hours
- SaaS: SoftwareApplication schema, pricing, features
- Portfolio: Person schema, work samples

---

## 📋 SEO IMPLEMENTATION CHECKLIST

### 1. Meta Tags (Required)

```html
<!-- Primary Meta Tags -->
<title>Primary Keyword - Compelling Hook | Brand Name</title>
<meta name="description" content="150-160 char description with primary keyword, benefit, and call-to-action. Include numbers if possible.">
<meta name="keywords" content="primary keyword, secondary keyword, long-tail keyword, semantic keyword, brand term">
<meta name="author" content="Author or Company Name">
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://yoursite.com/page-url">

<!-- Viewport & Encoding -->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### 2. Open Graph Tags (Required for Social)

```html
<!-- Open Graph / Facebook -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://yoursite.com/page-url">
<meta property="og:title" content="Compelling Title for Social Sharing">
<meta property="og:description" content="Engaging description optimized for social feeds (60-90 chars ideal)">
<meta property="og:image" content="https://yoursite.com/images/og-image.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:image:alt" content="Descriptive alt text for the image">
<meta property="og:site_name" content="Your Site Name">
<meta property="og:locale" content="en_US">
```

### 3. Twitter Card Tags (Required for Twitter/X)

```html
<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:url" content="https://yoursite.com/page-url">
<meta name="twitter:title" content="Compelling Title (max 70 chars)">
<meta name="twitter:description" content="Engaging description (max 200 chars)">
<meta name="twitter:image" content="https://yoursite.com/images/twitter-image.png">
<meta name="twitter:image:alt" content="Descriptive alt text">
<meta name="twitter:site" content="@yourtwitterhandle">
<meta name="twitter:creator" content="@authorhandle">
```

### 4. Additional Meta Tags (Recommended)

```html
<!-- Security & Performance -->
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="theme-color" content="#your-brand-color">

<!-- Mobile App Links (if applicable) -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="default">
<meta name="apple-mobile-web-app-title" content="App Name">

<!-- Geo Tags (for local SEO) -->
<meta name="geo.region" content="US-CA">
<meta name="geo.placename" content="San Francisco">
<meta name="geo.position" content="37.7749;-122.4194">
<meta name="ICBM" content="37.7749, -122.4194">

<!-- Verification Tags -->
<meta name="google-site-verification" content="your-verification-code">
<meta name="msvalidate.01" content="your-bing-verification">
```

---

## 📊 STRUCTURED DATA (JSON-LD)

### Website Schema (Homepage)

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "Your Website Name",
  "url": "https://yoursite.com",
  "description": "Brief description of your website",
  "publisher": {
    "@type": "Organization",
    "name": "Your Company Name",
    "logo": {
      "@type": "ImageObject",
      "url": "https://yoursite.com/logo.png"
    }
  },
  "potentialAction": {
    "@type": "SearchAction",
    "target": "https://yoursite.com/search?q={search_term_string}",
    "query-input": "required name=search_term_string"
  }
}
```

### Organization Schema

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Your Company Name",
  "url": "https://yoursite.com",
  "logo": "https://yoursite.com/logo.png",
  "description": "What your company does",
  "foundingDate": "2020",
  "founders": [
    {
      "@type": "Person",
      "name": "Founder Name"
    }
  ],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main St",
    "addressLocality": "City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "US"
  },
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+1-555-555-5555",
    "contactType": "customer service",
    "availableLanguage": ["English"]
  },
  "sameAs": [
    "https://twitter.com/yourhandle",
    "https://linkedin.com/company/yourcompany",
    "https://facebook.com/yourpage"
  ]
}
```

### Article Schema (Blog/News)

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Article Title (max 110 characters)",
  "description": "Article summary",
  "image": "https://yoursite.com/article-image.png",
  "datePublished": "2025-01-15T09:00:00+00:00",
  "dateModified": "2025-01-15T12:00:00+00:00",
  "author": {
    "@type": "Person",
    "name": "Author Name",
    "url": "https://yoursite.com/about/author"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Your Site",
    "logo": {
      "@type": "ImageObject",
      "url": "https://yoursite.com/logo.png"
    }
  },
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://yoursite.com/article-url"
  },
  "wordCount": 2500,
  "keywords": "keyword1, keyword2, keyword3"
}
```

### Product Schema (E-commerce)

```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Product Name",
  "image": "https://yoursite.com/product-image.png",
  "description": "Product description",
  "sku": "SKU123",
  "brand": {
    "@type": "Brand",
    "name": "Brand Name"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://yoursite.com/product-url",
    "priceCurrency": "USD",
    "price": "99.99",
    "availability": "https://schema.org/InStock",
    "seller": {
      "@type": "Organization",
      "name": "Your Store"
    }
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.5",
    "reviewCount": "89"
  }
}
```

### LocalBusiness Schema

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Business Name",
  "image": "https://yoursite.com/storefront.png",
  "url": "https://yoursite.com",
  "telephone": "+1-555-555-5555",
  "priceRange": "$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street",
    "addressLocality": "City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 37.7749,
    "longitude": -122.4194
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "09:00",
      "closes": "17:00"
    }
  ]
}
```

### FAQ Schema

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is your product/service?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Comprehensive answer to the question with specific details."
      }
    },
    {
      "@type": "Question",
      "name": "How much does it cost?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Pricing details and any relevant information."
      }
    }
  ]
}
```

### HowTo Schema

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "How to Do Something",
  "description": "Step-by-step guide description",
  "totalTime": "PT30M",
  "estimatedCost": {
    "@type": "MonetaryAmount",
    "currency": "USD",
    "value": "0"
  },
  "tool": ["Tool 1", "Tool 2"],
  "supply": ["Supply 1", "Supply 2"],
  "step": [
    {
      "@type": "HowToStep",
      "name": "Step 1 Title",
      "text": "Step 1 instructions",
      "image": "https://yoursite.com/step1.png",
      "url": "https://yoursite.com/guide#step1"
    },
    {
      "@type": "HowToStep",
      "name": "Step 2 Title",
      "text": "Step 2 instructions",
      "image": "https://yoursite.com/step2.png",
      "url": "https://yoursite.com/guide#step2"
    }
  ]
}
```

### BreadcrumbList Schema

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://yoursite.com"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Category",
      "item": "https://yoursite.com/category"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Current Page",
      "item": "https://yoursite.com/category/page"
    }
  ]
}
```

---

## 🤖 AI SEARCH OPTIMIZATION (GEO)

### Quick Answer Box

Add a prominent answer box near the top of content for AI search engines:

```html
<div class="quick-answer">
  <h2>What is [Topic]?</h2>
  <p>
    Direct, comprehensive answer in 60-80 words that AI search engines
    can extract. Include key facts, numbers, and actionable information.
    This should fully answer the question standalone.
  </p>
</div>
```

### TL;DR Section

```html
<div class="tldr">
  <h2>TL;DR - Key Takeaways</h2>
  <ul>
    <li><strong>Point 1</strong> - Specific detail with data</li>
    <li><strong>Point 2</strong> - Quantifiable result (X% improvement)</li>
    <li><strong>Point 3</strong> - Actionable insight</li>
    <li><strong>Point 4</strong> - Technical detail simplified</li>
    <li><strong>Point 5</strong> - Main benefit for user</li>
  </ul>
</div>
```

### FAQ Section

Always include 5-7 FAQs with detailed answers:

```html
<section class="faq">
  <h2>Frequently Asked Questions</h2>

  <details>
    <summary>Question that users actually search for?</summary>
    <p>Comprehensive answer with specific details, examples, and actionable steps.</p>
  </details>

  <!-- Repeat for 5-7 questions -->
</section>
```

### Content Structure for AI

- **One idea per paragraph** - Makes parsing easier
- **Clear headings** - Use descriptive H2/H3 that could be questions
- **Lists and tables** - Well-structured comparison data
- **Citations** - Link to authoritative sources
- **Natural language** - Write conversationally

---

## 📁 TECHNICAL SEO FILES

### robots.txt

```txt
User-agent: *
Allow: /

# Disallow admin/private areas
Disallow: /admin/
Disallow: /api/
Disallow: /private/

# Sitemap location
Sitemap: https://yoursite.com/sitemap.xml
```

### sitemap.xml Structure

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://yoursite.com/</loc>
    <lastmod>2025-01-15</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://yoursite.com/about</loc>
    <lastmod>2025-01-10</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <!-- Add all important pages -->
</urlset>
```

---

## 🖼️ IMAGE SEO

### Image Optimization Checklist

- [ ] **File names**: Descriptive with keywords (`blue-running-shoes.jpg` not `IMG_1234.jpg`)
- [ ] **Alt text**: Descriptive, includes keywords naturally (80-125 chars)
- [ ] **File size**: Compress images (< 200KB for most, < 100KB ideal)
- [ ] **Format**: WebP for web, AVIF for modern browsers, PNG for graphics, JPG for photos
- [ ] **Dimensions**: Serve appropriately sized images (not 4000px for a 400px container)
- [ ] **Lazy loading**: Add `loading="lazy"` for below-fold images
- [ ] **Responsive**: Use `srcset` for different screen sizes

### Image Tag Best Practices

```html
<img
  src="image.webp"
  alt="Descriptive alt text with keyword - what the image shows"
  width="800"
  height="600"
  loading="lazy"
  decoding="async"
>
```

### Open Graph Image Requirements

- **Dimensions**: 1200x630px (optimal for all platforms)
- **Format**: PNG or JPG
- **File size**: < 1MB
- **Text**: Keep important text in center 60% (safe zone)

---

## 🔗 URL & LINK STRUCTURE

### URL Best Practices

```
✅ Good URLs:
https://yoursite.com/blue-running-shoes
https://yoursite.com/blog/how-to-train-for-marathon
https://yoursite.com/products/nike-air-max-2025

❌ Bad URLs:
https://yoursite.com/p?id=12345
https://yoursite.com/blog/post/2025/01/15/this-is-a-really-long-url-that-goes-on-forever
https://yoursite.com/PRODUCTS/Nike_Air_MAX
```

### Internal Linking Strategy

- Link to 3-5 relevant internal pages per content piece
- Use descriptive anchor text (not "click here")
- Link to high-value pages (services, products, key content)
- Create topic clusters with pillar content

### External Linking

- Link to 2-3 authoritative external sources
- Use `rel="noopener noreferrer"` for external links
- Open external links in new tabs (`target="_blank"`)

---

## ⚡ PERFORMANCE SEO (Core Web Vitals)

### Key Metrics

| Metric | Good | Needs Improvement | Poor |
|--------|------|-------------------|------|
| **LCP** (Largest Contentful Paint) | ≤ 2.5s | 2.5-4s | > 4s |
| **INP** (Interaction to Next Paint) | ≤ 200ms | 200-500ms | > 500ms |
| **CLS** (Cumulative Layout Shift) | ≤ 0.1 | 0.1-0.25 | > 0.25 |

### Quick Performance Wins

1. **Compress images** - Use WebP, proper sizing
2. **Minimize CSS/JS** - Remove unused code
3. **Enable caching** - Set cache headers
4. **Use CDN** - Serve assets from edge locations
5. **Lazy load** - Images, videos, iframes below fold
6. **Preload critical assets** - Fonts, hero images
7. **Reduce redirects** - Direct links only
8. **Enable compression** - Gzip/Brotli

---

## 📝 CONTENT SEO GUIDELINES

### Keyword Optimization

| Location | Primary Keyword | Notes |
|----------|-----------------|-------|
| Title tag | ✅ Required | Front-load if possible |
| Meta description | ✅ Required | Natural inclusion |
| H1 heading | ✅ Required | Only one H1 per page |
| First 100 words | ✅ Required | Within first paragraph |
| URL slug | ✅ Required | Hyphenated, lowercase |
| H2 headings | Secondary keywords | 2-4 variations |
| Image alt text | Natural inclusion | Don't force |
| Body content | 1-2% density | Natural, not stuffed |

### Content Length Guidelines

| Content Type | Minimum | Optimal | Notes |
|--------------|---------|---------|-------|
| Landing page | 500 words | 1000-1500 | Focus on conversion |
| Blog post | 1000 words | 2000-3000 | Comprehensive coverage |
| Product page | 300 words | 500-800 | Include specs, reviews |
| Service page | 800 words | 1500-2000 | Benefits, process, FAQ |

### Heading Hierarchy

```
H1 - Main Page Title (ONE per page)
  H2 - Major Section
    H3 - Subsection
      H4 - Detail
    H3 - Another Subsection
  H2 - Another Major Section
```

---

## 🔧 FRAMEWORK-SPECIFIC IMPLEMENTATION

### Next.js (App Router)

```typescript
// app/page/layout.tsx
import { Metadata } from 'next'

export const metadata: Metadata = {
  title: 'Page Title | Site Name',
  description: 'Page description',
  keywords: ['keyword1', 'keyword2'],
  openGraph: {
    title: 'OG Title',
    description: 'OG Description',
    url: 'https://yoursite.com/page',
    images: [{ url: '/og-image.png', width: 1200, height: 630 }],
  },
  twitter: {
    card: 'summary_large_image',
    title: 'Twitter Title',
    description: 'Twitter Description',
  },
  robots: { index: true, follow: true },
  alternates: { canonical: 'https://yoursite.com/page' },
}
```

### React (react-helmet)

```jsx
import { Helmet } from 'react-helmet'

function Page() {
  return (
    <>
      <Helmet>
        <title>Page Title | Site Name</title>
        <meta name="description" content="Description" />
        <meta property="og:title" content="OG Title" />
        <link rel="canonical" href="https://yoursite.com/page" />
      </Helmet>
      {/* Page content */}
    </>
  )
}
```

### Vue/Nuxt

```javascript
// nuxt.config.js or useHead()
export default {
  head: {
    title: 'Page Title',
    meta: [
      { name: 'description', content: 'Description' },
      { property: 'og:title', content: 'OG Title' }
    ],
    link: [
      { rel: 'canonical', href: 'https://yoursite.com/page' }
    ]
  }
}
```

### Plain HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title | Site Name</title>
  <meta name="description" content="Description">
  <meta property="og:title" content="OG Title">
  <link rel="canonical" href="https://yoursite.com/page">
  <script type="application/ld+json">
    { "@context": "https://schema.org", ... }
  </script>
</head>
<body>
  <!-- Content -->
</body>
</html>
```

---

## ✅ SEO AUDIT CHECKLIST

### Technical SEO
- [ ] robots.txt exists and is correct
- [ ] sitemap.xml exists and is submitted to Google Search Console
- [ ] All pages have canonical URLs
- [ ] No broken links (404s)
- [ ] HTTPS enabled (SSL certificate)
- [ ] Mobile-friendly (responsive design)
- [ ] Page speed < 3 seconds
- [ ] No duplicate content
- [ ] Proper redirects (301 for permanent)

### On-Page SEO
- [ ] Unique title tag per page (50-60 chars)
- [ ] Unique meta description per page (150-160 chars)
- [ ] One H1 per page with primary keyword
- [ ] Logical heading hierarchy (H1 > H2 > H3)
- [ ] Keyword in first 100 words
- [ ] Internal links to relevant pages
- [ ] External links to authoritative sources
- [ ] Images have alt text
- [ ] URLs are clean and descriptive

### Structured Data
- [ ] Organization schema on homepage
- [ ] Appropriate schema for page type (Article, Product, LocalBusiness, etc.)
- [ ] BreadcrumbList schema
- [ ] FAQ schema (if applicable)
- [ ] Schemas validate without errors

### AI Search Optimization
- [ ] Quick Answer box near top
- [ ] TL;DR section with key points
- [ ] FAQ section with 5-7 questions
- [ ] Clear, conversational content
- [ ] One idea per paragraph
- [ ] Tables/lists for comparisons

---

## 🛠️ SEO TOOLS & VALIDATION

### Free Tools
- **Google Search Console** - Monitor indexing, errors
- **Google PageSpeed Insights** - Performance testing
- **Schema Markup Validator** - schema.markup.io/test
- **Rich Results Test** - search.google.com/test/rich-results
- **Mobile-Friendly Test** - search.google.com/test/mobile-friendly
- **Ahrefs Webmaster Tools** - Free backlink checker

### Validation Commands
```bash
# Test structured data
curl -s "https://yoursite.com" | grep -o '<script type="application/ld+json">.*</script>'

# Check robots.txt
curl https://yoursite.com/robots.txt

# Check sitemap
curl https://yoursite.com/sitemap.xml
```

---

## 📈 SUCCESS METRICS

Track these KPIs after implementing SEO:

1. **Organic traffic** - Google Analytics
2. **Keyword rankings** - Search Console, Ahrefs
3. **Click-through rate (CTR)** - Search Console
4. **Core Web Vitals** - PageSpeed Insights
5. **Indexed pages** - Search Console
6. **Backlinks** - Ahrefs, Moz
7. **AI citations** - Check Perplexity, ChatGPT mentions

---

## 🚀 QUICK START

For any new page, implement these minimum requirements:

1. **Title tag** with primary keyword
2. **Meta description** with benefit + CTA
3. **Canonical URL**
4. **Open Graph tags** (title, description, image)
5. **One H1** with primary keyword
6. **Structured data** (appropriate schema)
7. **Alt text** for all images

Then enhance with:
- FAQ section + schema
- Quick Answer box
- Internal/external links
- Performance optimization
