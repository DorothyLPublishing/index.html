# Dorothy L’s Publishing — Web Ecosystem Build & SOP (v1)

**Author:** Dorothy L. Reddick  
**Owner:** Dorothy L. Reddick  
**Date:** Oct 7, 2025  
**Scope:** DorothyLsPublishing.com (HQ), DorothyLsPublishing.online (Digital Hub), TheBrazenOne.live (Podcast), SchoolTeacher.online (Apparel)

---

## 0) Executive Summary
You own four strategic domains. This document gives you (a) a working homepage layout for **DorothyLsPublishing.com**, (b) a complete step‑by‑step build + deploy plan using free/low‑cost tools, and (c) training material: glossary, checklists, and appendices you can reuse for future clients.

---

## 1) Information Architecture (IA)
**Global nav (same order on every site):** Home • Books & Journals • Services • Academy • Podcast • Shop • About • Press • Contact  
**Footer (identical everywhere):** © Dorothy L’s Publishing • Privacy • Terms • Accessibility • Sitemap • Social links

**HQ (.com) sections:**
1. Hero (value proposition + CTA)  
2. Showcase (Books, Workbooks, Journals)  
3. Services (Editing, Layout, KDP/EPUB, Covers)  
4. Academy teaser (Legacy in Print)  
5. Podcast card (The Brazen One)  
6. Press / Media  
7. Email capture  
8. Footer

---

## 2) Visual Tone (quick board)
- Primary: Deep Bronze Gold `#B88A44`  
- Neutrals: Linen `#F9F4EF`, Charcoal `#222222`  
- Accents: Warm Peach `#F2B8A0`, Burnt Amber `#8C4C28`
- Fonts (no licenses required): *Playfair Display* (headlines), *Inter* (UI/body)

---

## 3) CODE — HQ Landing Page (static HTML, Netlify‑ready)
> **How to use:** Create `/site` folder, save as `index.html`, drag‑drop the folder into Netlify. Swap copy & links as needed.

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Dorothy L’s Publishing — Stories That Build Legacy</title>
  <meta name="description" content="Independent Black publishing house based in Tulsa. Books, journals, workbooks, and the Legacy in Print Academy." />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    :root { --gold:#B88A44; --peach:#F2B8A0; --linen:#F9F4EF; --char:#222; }
    body{font-family:Inter,system-ui,Arial,sans-serif;}
    .h1{font-family:"Playfair Display",serif}
  </style>
</head>
<body class="bg-[var(--linen)] text-[var(--char)]">
  <!-- Top utility bar (gold hairline) -->
  <div class="h-1 bg-[var(--gold)]"></div>

  <!-- Header / Nav -->
  <header class="max-w-6xl mx-auto px-4 py-5 flex items-center justify-between">
    <a href="#" class="flex items-center gap-3">
      <div class="w-8 h-8 rounded-full border border-[var(--gold)]"></div>
      <span class="font-semibold">Dorothy L’s Publishing</span>
    </a>
    <nav class="hidden md:flex items-center gap-6 text-sm">
      <a href="#books" class="hover:text-[var(--gold)]">Books & Journals</a>
      <a href="#services" class="hover:text-[var(--gold)]">Services</a>
      <a href="#academy" class="hover:text-[var(--gold)]">Academy</a>
      <a href="#podcast" class="hover:text-[var(--gold)]">Podcast</a>
      <a href="#shop" class="hover:text-[var(--gold)]">Shop</a>
      <a href="#about" class="hover:text-[var(--gold)]">About</a>
      <a href="#press" class="hover:text-[var(--gold)]">Press</a>
      <a href="#contact" class="hover:text-[var(--gold)]">Contact</a>
    </nav>
  </header>

  <!-- Hero -->
  <section class="max-w-6xl mx-auto px-4 py-16 grid md:grid-cols-2 gap-10 items-center">
    <div>
      <h1 class="h1 text-4xl md:text-5xl leading-tight">Stories That Build Legacy.</h1>
      <p class="mt-5 text-lg text-neutral-700">An independent Black publishing house in Tulsa—crafting books, journals, and workbooks that honor heritage, heal communities, and teach the art of authorship.</p>
      <div class="mt-8 flex gap-4">
        <a href="#services" class="px-5 py-3 bg-[var(--gold)] text-white rounded-lg shadow">Start a Project</a>
        <a href="#books" class="px-5 py-3 border border-[var(--gold)] rounded-lg">Browse Our Books</a>
      </div>
      <div class="mt-6 text-sm">Listen to the podcast → <a href="https://thebrazenone.live" class="underline hover:text-[var(--gold)]">TheBrazenOne.live</a></div>
    </div>
    <div class="bg-white rounded-2xl p-6 shadow">
      <div class="aspect-[4/3] bg-[var(--peach)]/30 rounded-xl flex items-center justify-center">
        <span class="text-sm">(Hero image / butterfly watermark)</span>
      </div>
    </div>
  </section>

  <!-- Books Showcase -->
  <section id="books" class="bg-white border-t">
    <div class="max-w-6xl mx-auto px-4 py-14">
      <h2 class="h1 text-3xl">Featured Books & Workbooks</h2>
      <p class="mt-2 text-neutral-600">From The Velvet Peach to Miss Ola’s Teas & Elixirs and the She Who Rises series.</p>
      <div class="mt-8 grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <article class="p-5 rounded-xl border">
          <div class="aspect-[3/4] bg-[var(--linen)] rounded-lg"></div>
          <h3 class="mt-4 font-semibold">The Velvet Peach</h3>
          <p class="text-sm text-neutral-600">Novel • Print & eBook</p>
        </article>
        <article class="p-5 rounded-xl border">
          <div class="aspect-[3/4] bg-[var(--linen)] rounded-lg"></div>
          <h3 class="mt-4 font-semibold">Breathe, Sis (Expanded)</h3>
          <p class="text-sm text-neutral-600">Workbook • Print & PDF</p>
        </article>
        <article class="p-5 rounded-xl border">
          <div class="aspect-[3/4] bg-[var(--linen)] rounded-lg"></div>
          <h3 class="mt-4 font-semibold">Miss Ola’s Teas & Elixirs</h3>
          <p class="text-sm text-neutral-600">Recipe Book • Print & eBook</p>
        </article>
      </div>
    </div>
  </section>

  <!-- Services -->
  <section id="services" class="max-w-6xl mx-auto px-4 py-14">
    <h2 class="h1 text-3xl">Publishing Services</h2>
    <p class="mt-2 text-neutral-600">Editing • Layout • Cover Design • KDP/EPUB • Audiobook Teasers • Launch Kits</p>
    <div class="mt-8 grid md:grid-cols-3 gap-6">
      <div class="p-6 bg-white border rounded-xl">
        <h3 class="font-semibold">Manuscript to Market</h3>
        <p class="text-sm text-neutral-600 mt-2">Developmental edit → Proof → Formatting → KDP/EPUB delivery.</p>
      </div>
      <div class="p-6 bg-white border rounded-xl">
        <h3 class="font-semibold">Design & Covers</h3>
        <p class="text-sm text-neutral-600 mt-2">Wraparounds, spines, mockups, brand‑aligned visuals.</p>
      </div>
      <div class="p-6 bg-white border rounded-xl">
        <h3 class="font-semibold">Launch & PR</h3>
        <p class="text-sm text-neutral-600 mt-2">Press kits, one‑pagers, social packs, podcast features.</p>
      </div>
    </div>
    <a href="#contact" class="inline-block mt-8 px-5 py-3 bg-[var(--gold)] text-white rounded-lg shadow">Request a Quote</a>
  </section>

  <!-- Academy Teaser -->
  <section id="academy" class="bg-white border-t">
    <div class="max-w-6xl mx-auto px-4 py-14 grid md:grid-cols-2 gap-8 items-center">
      <div>
        <h2 class="h1 text-3xl">Legacy in Print Academy</h2>
        <p class="mt-2 text-neutral-700">Courses, templates, and live workshops guiding authors from idea to ISBN—especially for Black women building legacy through print.</p>
        <a href="https://dorothylspublishing.online" class="inline-block mt-6 px-5 py-3 border border-[var(--gold)] rounded-lg">Preview the Hub</a>
      </div>
      <div class="aspect-video bg-[var(--peach)]/30 rounded-xl"></div>
    </div>
  </section>

  <!-- Podcast Card -->
  <section id="podcast" class="max-w-6xl mx-auto px-4 py-14">
    <div class="p-8 bg-white border rounded-2xl grid md:grid-cols-3 gap-8 items-center">
      <div class="md:col-span-2">
        <h2 class="h1 text-3xl">The Brazen One — Podcast</h2>
        <p class="mt-2 text-neutral-700">Somatic healing, culture, and community conversations with Dirty Red – The Brazen.</p>
        <div class="mt-4 flex gap-3 text-sm">
          <a class="underline hover:text-[var(--gold)]" href="https://thebrazenone.live">Listen Now</a>
          <span>•</span>
          <a class="underline hover:text-[var(--gold)]" href="#">Apple Podcasts</a>
          <span>•</span>
          <a class="underline hover:text-[var(--gold)]" href="#">Spotify</a>
        </div>
      </div>
      <div class="aspect-square bg-[var(--linen)] rounded-xl"></div>
    </div>
  </section>

  <!-- Press -->
  <section id="press" class="bg-white border-t">
    <div class="max-w-6xl mx-auto px-4 py-14">
      <h2 class="h1 text-3xl">Press & Media</h2>
      <ul class="mt-6 grid md:grid-cols-3 gap-6 text-sm">
        <li class="p-5 border rounded-xl bg-[var(--linen)]">Press Kit (PDF) — One‑pager, bio, book list, contact</li>
        <li class="p-5 border rounded-xl bg-[var(--linen)]">Media Inquiries — <a class="underline" href="mailto:press@dorothylspublishing.com">press@dorothylspublishing.com</a></li>
        <li class="p-5 border rounded-xl bg-[var(--linen)]">Speaking & Workshops — Request a booking</li>
      </ul>
    </div>
  </section>

  <!-- Email Capture -->
  <section id="contact" class="max-w-6xl mx-auto px-4 py-14">
    <div class="p-8 bg-white border rounded-2xl">
      <h2 class="h1 text-3xl">Stay in the Loop</h2>
      <p class="mt-2 text-neutral-700">Get new releases, workshops, and live events.</p>
      <form class="mt-6 grid sm:grid-cols-[1fr_auto] gap-3">
        <input class="border rounded-lg px-4 py-3" placeholder="Your email address" type="email" required>
        <button class="px-5 py-3 bg-[var(--gold)] text-white rounded-lg">Subscribe</button>
      </form>
      <p class="mt-3 text-xs text-neutral-500">We respect your privacy. Unsubscribe anytime.</p>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-[#111] text-white">
    <div class="max-w-6xl mx-auto px-4 py-10 grid md:grid-cols-4 gap-8 text-sm">
      <div>
        <div class="font-semibold">Dorothy L’s Publishing</div>
        <p class="mt-2 text-neutral-400">Stories that build legacy.</p>
      </div>
      <div>
        <div class="font-semibold">Explore</div>
        <ul class="mt-2 space-y-1 text-neutral-300">
          <li><a href="#books" class="hover:text-white">Books & Journals</a></li>
          <li><a href="#services" class="hover:text-white">Services</a></li>
          <li><a href="#academy" class="hover:text-white">Academy</a></li>
          <li><a href="#podcast" class="hover:text-white">Podcast</a></li>
        </ul>
      </div>
      <div>
        <div class="font-semibold">Company</div>
        <ul class="mt-2 space-y-1 text-neutral-300">
          <li><a href="#about" class="hover:text-white">About</a></li>
          <li><a href="#press" class="hover:text-white">Press</a></li>
          <li><a href="#contact" class="hover:text-white">Contact</a></li>
        </ul>
      </div>
      <div>
        <div class="font-semibold">Legal</div>
        <ul class="mt-2 space-y-1 text-neutral-300">
          <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
          <li><a href="#" class="hover:text-white">Terms of Use</a></li>
          <li><a href="#" class="hover:text-white">Accessibility</a></li>
        </ul>
      </div>
    </div>
    <div class="border-t border-white/10">
      <div class="max-w-6xl mx-auto px-4 py-4 text-xs text-neutral-400">© Dorothy L. Reddick — All rights reserved.</div>
    </div>
  </footer>
</body>
</html>
```

**Why this approach?** One‑file static site = fastest path to live. We can refactor into React/Next later for blogs, CMS, or e‑commerce.

---

## 4) Folder Structure (simple)
```
/site
  ├── index.html      # above file
  ├── /assets         # images, logos, PDFs
  │    ├── press-kit.pdf
  │    └── butterfly.png
  └── /legal
       ├── privacy.html
       └── terms.html
```

---

## 5) Deployment (Netlify) — Step‑by‑Step
1) Go to **netlify.com** → Sign up (free).  
2) Click **Add new site** → **Deploy manually** → Drag your `/site` folder.  
3) After deploy, copy the temp URL `example.netlify.app`.  
4) In **Namecheap → Domain → Advanced DNS**:
   - Add **CNAME** record: **Host** = `@` (or `www`), **Value** = your `example.netlify.app`, **TTL** = Automatic.  
   - If you set `www` as CNAME, add a URL redirect from root `@` → `www` (Namecheap “URL Redirect Record”).
5) In **Netlify → Site settings → Domain management** add your custom domain.  
6) Enable **Automatic HTTPS** (Let’s Encrypt) in Netlify.  
7) Test: visit `https://dorothylspublishing.com` (padlock should show).

> **Alternative:** Use a Netlify DNS integration (simpler) — but the above works fine and keeps DNS at Namecheap.

---

## 6) Branded Email (choose one)
**Option A — Zoho Mail (free):**  
- Create account → Add domain `dorothylspublishing.com`.  
- Follow wizard to add **MX** records at Namecheap (Zoho provides values).  
- Create addresses: `info@`, `press@`.

**Option B — Google Workspace:**  
- Start Workspace → Verify domain → Add **MX** records for Google.  
- Create users/aliases.  

> **Tip:** Add SPF + DKIM (from provider) to DNS to keep emails out of spam.

---

## 7) Analytics + SEO Setup
- **Google Analytics 4:** Create property → get Measurement ID → add GA snippet before `</head>` in `index.html`.  
- **Search Console:** Add property for each domain → verify by DNS TXT record → submit sitemap later.  
- **Meta:** Unique `<title>` & `<meta description>` per page.  
- **Performance:** Use compressed images in `/assets`.

---

## 8) Accessibility & Quality Checklist
- Keyboard navigable (Tab through links).  
- Sufficient color contrast (gold on linen tested).  
- Images have `alt` text.  
- Form fields have labels.  
- Headings are semantic (`h1` → `h2` → `h3`).  

---

## 9) Ongoing Ops (SOP)
- **Content updates:** Edit `index.html` and redeploy (drag‑drop).  
- **Backups:** Keep a local `/DL-Publishing-Sites` folder; copy to cloud (Drive/Dropbox).  
- **Versioning:** Optional GitHub repo → connect Netlify for auto‑deploys on push.  
- **Security:** Turn on 2FA on Namecheap, Netlify, email provider.  
- **Renewals:** Auto‑renew domains yearly; calendar reminder 30 days prior.

---

## 10) Cross‑Site Linking Plan
- **.com → .online:** “Explore the Digital Hub” (store, downloads).  
- **.com → .live:** “Listen to the Podcast”.  
- **.online → .com:** “Work with the Publishing House.”  
- **.live → .com/.online:** “Read the books • Join the Academy.”  
- **SchoolTeacher.online:** links to Podcast and HQ in header/footer.

---

## 11) Future Enhancements
- Convert to Next.js for blog/news & Press section.  
- Add Netlify Forms for email capture, or integrate ConvertKit/Beehiiv.  
- Add a `/press` page with downloadable photos, bios, and one‑pagers.  
- Migrate store to Shopify/Printful on **SchoolTeacher.online**.  

---

## 12) Glossary (Plain‑English)
- **Domain:** Your website’s street address (e.g., dorothylspublishing.com).  
- **DNS:** The phonebook that connects your domain to your website host.  
- **A Record / CNAME / MX / TXT:** DNS record types — A = address (IP), CNAME = nickname/alias, MX = mail routing, TXT = notes/verification.  
- **Hosting:** The house where your website files live (Netlify).  
- **SSL/HTTPS:** Security padlock; encrypts traffic.  
- **Deploy:** Publish website changes to the internet.  
- **CDN:** Network that delivers your site fast (Netlify includes this).  
- **GA4:** Google Analytics 4 — traffic + behavior analytics.  
- **Search Console:** Google’s tool for indexing and SEO health.  
- **Meta Tags:** Hidden page info used by search engines and social shares.  
- **Accessibility (a11y):** Making the site usable by everyone.  
- **Responsive:** Works on phone, tablet, desktop.  
- **CTA:** Call‑to‑action button (“Start a Project”).

---

## 13) Checklists (printable)
**Go‑Live Checklist:**
- [ ] Domain purchased + auto‑renew + privacy enabled  
- [ ] Netlify site deployed with `index.html`  
- [ ] Custom domain connected + HTTPS active  
- [ ] Email provider set + MX/SPF/DKIM  
- [ ] GA4 + Search Console installed  
- [ ] Accessibility pass  
- [ ] Footer legal pages linked

**Content Refresh (Monthly):**
- [ ] New releases added to Books grid  
- [ ] Update Services offers  
- [ ] Swap hero image/quote  
- [ ] Check broken links  
- [ ] Export GA4 report

---

## 14) Appendices

### A) Sample DNS Records (Namecheap → Advanced DNS)
- **CNAME**: `www` → `your-site-name.netlify.app`  
- **URL Redirect**: `@` → `https://www.dorothylspublishing.com` (Permanent 301)  
- **MX (Zoho example)**: `mx.zoho.com` priority 10 (plus the two backups Zoho provides)  
- **TXT (SPF)**: `v=spf1 include:zoho.com ~all`  
- **TXT (DKIM)**: Provided by email provider  
- **TXT (Google Site Verification)**: Provided by Search Console

### B) Press Kit Contents (template)
- 1‑page PDF: Founder bio, mission, flagship titles, contact, headshot, logo.  
- Downloadable images (web + print).  
- 3 talking points + 3 sample interview questions.  

### C) Legal Pages (starter)
- **Privacy:** What you collect (email), how you use it, unsubscribe policy.  
- **Terms:** Acceptable use, IP ownership, no unlawful use.  
- **Accessibility:** Commitment + contact for assistance.

### D) Content Inventory Sheet (columns)
- Page • Owner • Status • Last Updated • URL • Notes • Asset links

### E) Branding Tokens (copy‑paste)
```
:root{
  --gold:#B88A44; --peach:#F2B8A0; --linen:#F9F4EF; --char:#222;
  --radius:14px; --shadow:0 10px 20px rgba(0,0,0,.06);
}
```

### F) Next.js Upgrade (when ready)
- Create Next app → Port sections into components → Add `/press`, `/books/[slug]` → Add CMS (Notion, Contentful, or local MDX) → Connect to Netlify.

---

## 15) Training Notes (for Protégés / Clients)
1. Own the domain first.  
2. Keep DNS changes minimal and documented.  
3. Start with a single static page; scale later.  
4. Reuse this SOP, IA, and checklists for any client.  
5. Measure results monthly; iterate.

---

**End of v1** — Ready for deployment. Next, we can clone this for **TheBrazenOne.live** and **DorothyLsPublishing.online**, adjusting copy and modules (podcast feed, store blocks, etc.).

