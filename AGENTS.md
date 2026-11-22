# AGENTS.md — jonathanmccallum-tr (Turkish mirror of jonathanmccallum.com)

Turkish mirror site. Same theme and design as the main site (Paper Light),
content translated into Turkish, meaning-first. Repo: streamjonathan/jonathanmccallum-tr.
Live (when approved): tr.jonathanmccallum.com. Proof: jonathanmccallum-tr.pages.dev.

## Mission

Mirror jonathanmccallum.com in Turkish — every article translated for meaning,
not word for word, in Jonathan's voice: plain short sentences, friendly, positive,
never preachy. An average person interested in Jesus, not an expert or theologian.

## Roles

- **Bobby (Muse) is the lead builder.** He coordinates, builds, pushes to GitHub
  and deploys to Cloudflare. He is the ONLY one who pushes or deploys.
- **Claude advises and reviews** translation quality. He does not push or deploy.
- **Helper Muses translate** one article at a time, drafts only.

## The one rule above all

**Never publish or alter live production assets without Jonathan's clear
permission.** The Turkish site goes live on tr.jonathanmccallum.com only when
he says so, after reading the pilot article(s). Drafts stay drafts until he
approves them. Work on a branch, never straight on main. Give Bobby a preview URL.

## Translation rules

- English repo (streamjonathan.github.io) is the source of truth. Articles are
  translated from the English Markdown, keeping the same date, slug, source_video
  and shareImage. Only the title and body are translated.
- Register: warm informal "sen" throughout (matches the French proof's "tu").
  Short plain sentences, scene → reflection → closing question, no preaching.
- Names (never vary): İsa, Tanrı, Mesih, Petrus, Âdem ve Havva, Aslan, Narnia,
  Lucy, Digory, Tirian (Kral Tirian). Book titles use the published Turkish
  editions (Doğan Egmont, tr. Müfit Balabanlılar): Narnia Günlükleri,
  Büyücünün Yeğeni, Son Savaş, Kozmik Üçleme. The Great Divorce has NO published
  Turkish edition — glossed in-text as "Büyük Boşanma — bu site için çevrildi".
- Bible verses: none of the 5 articles contains a direct Bible quotation, so no
  verse text was reproduced. The bread/water of life lines are Jonathan's
  paraphrase (echoing Yuhanna 6:35 / 4:14) — yaşam ekmeği / yaşam suyu — never
  presented as quoted Scripture. No direct Lewis quotations appear either.
- No emojis, no newsletter form, no links the English article does not have.
- Never invent facts, dates, links or details.

## Site facts

- Eleventy 3, Cloudflare Pages, Paper Light theme (Fraunces + Newsreader).
- No Ask chat and no note Worker on this site yet — search (Pagefind) works,
  Ask and notes come later. The Ask floating button and ask.js are removed.
- CSS is preloaded, not inlined (CSP blocks inline style). Bump the `?v=` query
  on any CSS/JS file you change.
