# Both.
### A dinner app for couples who don't want to cook two meals.

**Submission · Senior Product Designer challenge · Arrivia**
Tony Dinoff · April 2026

---

## Section A — Design Rationale

**Who and what problem.**

Both is for cohabiting couples, 25–45, where one partner recently adopted a dietary restriction gluten-free, for GLP-1, vegetarianism, etc. — and the other hasn't. They cook together or for each other at least four weeknights. Two patterns have failed them: cooking two meals (time, dishes, resentment), and the unrestricted partner silently giving up favorites (slow mourning of food identity). The break-point is Tuesday at 5:30pm. The problem isn't "find a gluten-free recipe." Every recipe app treats restriction as a filter on the individual; nobody designs for the social unit. This audience needs a tool that ends the nightly negotiation in under two minutes and produces one meal both people feel good about — without making the restricted partner feel like the problem.

**Directions considered.**

I looked at a weekly planner (both diets held in tension), a universal swap engine (any recipe, swap ingredients), and a "couples cookbook" tagged by household. I chose decide-tonight — one screen, one match, one locked-in answer — because the highest-friction moment is the Tuesday 5:30pm standoff, not Sunday planning. Solve the acute moment, earn the right to do planning later.

**Assumptions and the risky one.**

I assumed the decision unit is the couple, not the individual; that four crave-clusters (Fresh, Hearty, Familiar, New) cover weeknight intent; that the swap callout can feel respectful rather than othering. The riskiest one: couples will accept a prescriptive "one recipe, one answer" UX instead of browsing. If that's wrong, the product shape changes, so I'd validate it first — eight diary studies over two weeks.

**Success metrics.**

North star: both-happy meals per couple per week, target 4+ by week 4. Leading: time-to-decide under 90 seconds, activation within 48 hours, weeknight-use rate. Lagging: share of locked-in meals rated "we both liked it" and retention at weeks 8 and 12. I'd deliberately skip recipe saves and session time — those reward the browsing we're replacing.

**MVP cuts and v2.**

Cut: grocery integration, multi-day planning, restaurant mode, households of 3+, nutritional tracking, social sharing, web, and restriction onboarding. V2: a Saturday planning mode that proposes three both-happy dinners for the week; bi-directional pantry awareness (MVP flags a swap from your fridge, v2 picks the recipe from it); a "last week's winners" quick-pick; and a narrow social feature — one couple shares a meal with one other couple, not a public feed.

---

## Section B — Design Decisions & Next Steps

### Decision 1 — One recipe, not a feed.

The match screen shows a single full-bleed recipe card with three actions: Both, Swap it, Show another. I rejected a browseable feed even though users expect one. We give up serendipity and the window-shopping pattern every recipe app leans on. In exchange we get decision speed (the 90-second target) and we rescue the user from the failure mode that drove them to download the app — open a recipe app, browse for twenty minutes, order takeout. With another thirty minutes I'd prototype a browse mode as a sibling tab, not the primary flow, and run a timed task with five couples to see if time-to-decide holds when browsing is one tap away.

### Decision 2 — The swap callout as a small chip, not a banner.

The ingredient swap ("Use tamari instead of soy sauce") sits as a quiet line in a paper-colored card on the match screen, and as a three-letter chip next to the one ingredient it matters for inside cook mode. I considered louder treatments — banner, badge, "swap friendly" label. The trade-off is clarity for first-time users vs. respect for the restricted partner. Loud makes it unambiguous why we picked this recipe, but it frames the restricted partner as the friction every night. I chose integration over announcement because this experience happens 200+ times a year per couple — it has to be livable at that frequency, not just legible on first use. Before shipping I'd validate with six cooks restricted under six months; the newly-restricted cohort is most sensitive to othering.

### Decision 3 — Craving words instead of dietary words.

Both partners tap one of Fresh / Hearty / Familiar / New. I rejected the obvious move — asking for dietary preferences or cuisines — because the restriction is already known to the app, and weeknight intent is emotional, not taxonomic. The risk is real: these four words are a guess, and if users can't find themselves in them the whole flow collapses at screen two. I'd card-sort with fifteen weeknight cooks to validate the clusters before going deeper.

### What changed after the first pass.

The first iteration ran a single recipe — miso salmon — through all six screens, ending on a universal "How was it, really?" rating. Three revisions sharpened it. Adding two more candidates (gnocchi and a Thai coconut curry) forced the "one recipe, one answer" frame to hold three shapes: a standard diet swap, a pantry-memory swap, and a no-swap recipe. Making Cook Mode recipe-specific let the three-letter "Swap" chip land on the one ingredient it matters for, not the whole recipe. And walking the Thai path end-to-end surfaced the revision I'd defend most: "did you both like it?" reads wrong when nothing was adapted — it undersells a naturally-both find and puts the focus on judgment instead of intention. I rewrote After as "Keep this one around?" with "Save to our go-tos" as the primary action and rating demoted to three quiet links. The shift in tone was immediate — relief instead of a quiz — so I rolled the new layout across all three recipes. Copy adapts per meal ("Naturally both" for Thai, "A solid swap-night find" for the others), but the beat is the same: celebrate the meal, save it, move on. The work in a prescriptive product isn't proliferating special cases — it's finding the one beat that carries all of them.

### If I had another thirty minutes.

I'd add a real error state for cravings that can't be reconciled (Fresh + Hearty is fine; Familiar + New is harder). I'd prototype second-phone pairing so one partner can tap from their own device. I'd polish cook-mode — the weakest screen, and where there's a real question about when the swap should surface during cooking. And I'd write more microcopy variants for After, because "Save to our go-tos" is carrying a lot of weight now and I'd want alternatives across different meal temperatures.

### How I'd validate the core assumption.

The core assumption is that couples will use a prescriptive, decide-tonight tool instead of browsing. I'd run eight diary studies over two weeks — give eight couples the prototype (live-coded against a recipe API), have them use it every weeknight, and collect a sixty-second voice note after. I'd measure: fraction of weeknights they open the app, fraction of opens that end in a locked-in meal, and qualitatively — relief, or bossy? If open-rate is under 50% by week two, the prescriptive model is wrong and I'd pivot to a lighter planning tool.

---

## Section C — AI Usage Log

I used Claude (via Anthropic's Cowork desktop mode) as a design partner throughout. I also leaned on a Claude Code plugin I'd built for my own design practice — it bundles design skills (critique, UX copy, handoff, design system, accessibility) and validation skills (user research, research synthesis). The UX-copy skill shaped the swap-callout voice in Interaction 3; the user-research skill shaped the diary-study plan in Section B. Three representative moments:

### Interaction 1 — Audience sharpening.

**What I asked:** I handed Claude the brief and asked for five activity options that'd make a specific enough audience story. I told it to stand on craft, not pander to the hiring company with a travel-adjacent pick.

**What it gave me:** Cruise port-day planning, gym-to-crag climbing, spring migration birding, weekend bikepacking, and home cooks. Inside home cooks: mixed-diet couples, CSA subscribers, ADHD home cooks, GLP-1 home cooks. It recommended ADHD for distinctiveness.

**What I kept, changed, or rejected:** I kept home cooks and overrode ADHD for mixed-diet couples. The emotional texture — restricted partner's guilt, unrestricted partner's mourning — gives a sharper story for the video than attention-management would. ADHD is the more original design problem; mixed-diet is the more resonant product story. The interview hinges on storytelling more than design novelty, so I went against Claude's pick.

### Interaction 2 — The initial journey sketch.

**What I asked:** Given the mixed-diet audience, propose a single end-to-end core journey I can prototype in one sitting.

**What it gave me:** Six screens — Home → Check-in → Match → Decide → Cook mode → After — anchored by a shared "craving" check-in (Fresh / Hearty / Familiar / New) and a single-recipe decision screen with three actions.

**What I kept, changed, or rejected:** I kept the skeleton. I pushed back on the check-in — Claude first put both partners' chips side by side on one screen with a shared tap. I changed it to a stacked, sequential layout so whose turn it is stays unambiguous whether the couple's sharing one phone or not. I also cut Claude's confetti moment on the "we both liked it" rating — it pushed toward gamified reward imagery. This audience is adult, the feeling we're rewarding is relief not achievement, and gamification would break the editorial tone.

### Interaction 3 — The swap callout wording.

**What I asked:** Draft three microcopy variants for the ingredient-swap callout, keeping the tone respectful to the restricted partner.

**What it gave me:** (a) "This recipe works great for gluten-free households!" (b) "Smart swap: tamari for soy sauce — you've got it." (c) "Use tamari instead of soy sauce. You have it in the door of the fridge — $0 today."

**What I kept, changed, or rejected:** I kept (c). I rejected (a) outright because "gluten-free households" names the restriction in product copy every single night — the exact othering pattern the design is trying to avoid. I rejected (b) because "smart swap" is marketing voice; it flatters the app, not the user. (c) keeps the restricted partner invisible in the copy, flatters the couple's existing pantry knowledge, and the "$0 today" line quietly signals the app knows their fridge — a demonstration of value rather than an announcement of intelligence. It's the single edit that most shaped the product's voice.

---

## Appendix

- **Prototype file:** `both-prototype.html` — open in any modern browser; scale to mobile viewport if desired. Single self-contained file, but an internet connection is required for the full experience (calls to Google Fonts for typography and Unsplash for photos). 
- **Video walkthrough:** See separate file.
- **Design tools used:** Claude (Cowork mode) for ideation, copy drafting, and single-file HTML prototype implementation, plus my design-practice plugin.
- **Known gaps:** Figma frames were deprioritized in favor of a working interactive prototype. A Figma file mirroring the six screens could be reconstructed in about 30 minutes using the HTML as reference.
