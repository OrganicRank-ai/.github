## OrganicRank

**Most SEO tools hand you a list of problems. This one opens the pull request.**

You give it a domain. Nothing else — no keyword list, no competitor names, no
project setup. It crawls the site, runs deterministic technical checks,
reconstructs what the business sells from its own copy, finds who is outranking
it and why, then scores the whole thing and tells you the three changes worth
making first.

Then it makes them. It maps each URL to the source file that renders it, writes
the change, and opens a pull request you review and merge.

### How the fixes work

**The model never decides what is broken.** Measured crawl facts produce the
instructions; the model only writes the copy. The audit finds a title is 94
characters and truncating in results — the model writes a shorter one. It is
never asked what is wrong.

**URL → source mapping** across Next.js (both routers), Astro, Remix, SvelteKit,
Nuxt, Gatsby, Hugo, Jekyll, Eleventy, plain HTML and WordPress themes. Only ever
to paths that exist in the tree.

**Every edit passes a safety gate** before it can be committed. An edit is
rejected if it truncates the file, balloons it, changes content without
itemising what changed, or silently drops lines. Rejections appear in the pull
request with their reason, so nothing fails quietly.

**We never commit to the default branch and never force-push.** Changes land on
a fresh branch with a PR body showing each change, its before-and-after, and why
it helps.

### What it will not touch

Content and metadata only — titles, meta descriptions, headings, canonicals, alt
text, structured data, internal links, page copy.

Never application logic, dependencies, configuration, build setup, environment,
or routing. **A pull request from us can change how a page describes itself. It
cannot change what it does.**

That boundary is the point. It is what makes granting repository access a
reasonable decision rather than a leap of faith.

### Scoring is code, not model output

The model supplies observations. Every number is computed from a fixed formula,
so two runs on the same inputs produce the same figures and each one can be
explained.

Search volume is deliberately capped in its influence — a 300-search buying term
outranks a 10,000-search curiosity, because the plan is about revenue rather
than traffic.

### Try it

Free audit, no account: **https://organicrank.ai**
