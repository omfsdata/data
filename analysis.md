---
layout: default
title: SDN Match Analysis
nav: analysis
permalink: /analysis/
container: page
---

<p class="eyebrow">Exploratory data analysis</p>

# What seven years of SDN match posts say about the OMFS match
{: .title}

An exploratory look at self-reported Oral & Maxillofacial Surgery residency match results, 2020–2026 · 111 matched applicants
{: .byline}

Every January, oral surgery applicants post their stats to the Student Doctor Network (SDN) "Official OMS Match Results" threads once results are released. Those threads are the closest thing the specialty has to a public dataset. This page pulls together seven cycles of them and asks a simple question: among people who matched, how do objective metrics — CBSE score, class rank, research, externships — relate to the *kind* of program they landed?
{: .lede}

<div class="callout warn" markdown="1">
### Read this first: what this data can and can't tell you
Every number below comes from people who **chose to post after matching**. There is no comparison group of applicants who didn't match, and the posts skew toward "if I could do it, so can you" success stories. So nothing here describes *whether* someone matches — only how metrics relate to *where* matchers ended up. Treat all of it as hypothesis-generating, not predictive. Self-reported, self-selected, and small.
</div>

## How the data was collected

The seven "Official OMS Match Results" threads (2020 through 2026) were read in full — every page — and each self-reported result post was coded into a structured row: program length (4-year single-degree vs 6-year dual-degree/MD), CBSE score, class-rank percentile, number of externships, research intensity, and the application funnel (programs applied to → interview invites → interviews attended → programs ranked). Purely conversational posts were skipped.

Program length was recorded only when a poster stated it explicitly ("4-year", "6yr", "dual-degree") or where it was unambiguous; otherwise it was left blank. Research was coded on a four-level ordinal scale (none / light / moderate / heavy) from the described publications, posters, and projects. The final dataset is **111 matched applicants** plus one applicant who explicitly reported *not* matching.

<div class="callout" markdown="1">
### The CBSE scoring wrinkle
The CBSE has been reported on several scales over the years: an older 2-digit scaled score, a 3-digit USMLE-aligned score, and the current **Equated Percent Correct (EPC)**. To make seven years comparable, every score was converted to **EPC** using the official NBME equivalency tables — the old-2-digit → EPC table and the 3-digit → EPC table.

One trap worth naming: when a 2021–2023 poster wrote something like "`218 (77)`," the number in parentheses is the *old 2-digit scaled* score, not EPC. The 3-digit value was used and converted (218 → EPC 73). The conversion was validated against posters who volunteered multiple formats for the same performance — e.g. a "72 EPC" that the poster also called "217," which the table maps back to 72 exactly.
</div>

<div class="stats">
  <div class="stat"><div class="num">111</div><div class="lab">matched applicants coded</div></div>
  <div class="stat"><div class="num">7</div><div class="lab">match cycles (2020–2026)</div></div>
  <div class="stat"><div class="num">ρ = 0.50</div><div class="lab">CBSE vs interview conversion</div></div>
  <div class="stat"><div class="num">p = 0.006</div><div class="lab">CBSE gap, 4-yr vs 6-yr</div></div>
</div>

## 1. CBSE and program length

The recurring belief in the threads is that 6-year (dual-degree/MD) programs demand a higher CBSE than 4-year programs, because the affiliated medical school screens on it. Pooled across all seven cycles, the data supports this — modestly. Six-year matchers have a higher median CBSE (**75** EPC) than 4-year matchers (**71** EPC), and the difference is statistically reliable (Mann–Whitney *p* = 0.006).

But notice the overlap in the figure below. The 6-year distribution reaches higher at the top, yet its *floor* is essentially the same as the 4-year floor. A high CBSE is disproportionately a 6-year thing; a low one doesn't rule out either track.

{% include figure.html num="1" src="f1_cbse_length.png" caption="CBSE (EPC) by program length, all matchers 2020–2026. Each dot is one applicant; boxes show median and interquartile range. Six-year programs skew higher, but both tracks span nearly the full range." %}

## 2. The one robust relationship: CBSE → interview invites

If the score does one thing clearly, it's convert applications into interview invites. Plotting CBSE against interview conversion (invites ÷ applications) gives a Spearman correlation of **ρ = 0.50** (*p* < 0.001) — the strongest and most reliable relationship in the whole dataset. This is the quantified version of the advice repeated in every thread: the score gets your foot in the door, and everything after the interview is about fit.

The bubble sizes are telling, too: several low scorers still matched by applying to 40–50 programs, using sheer volume to compensate for a lower per-application hit rate.

{% include figure.html num="2" src="f3_cbse_conv.png" caption="CBSE vs interview conversion. Bubble size is the number of programs applied to. Higher scores convert a larger share of applications into invites; low scorers compensate with volume." %}

## 3. Research is a separate lever

Research intensity tracks with interview conversion (**ρ = 0.29**, *p* = 0.002): median conversion climbs steadily from **46%** (no research) to **71%** (heavy research). Six-year matchers also carry more research than 4-year matchers — the "heavy" band is visibly larger for 6-year programs — consistent with academic medical centers valuing it.

The most interesting part: research and CBSE are essentially **uncorrelated** (ρ = 0.12, not significant). They aren't the same strong applicants doing both — research looks like a genuinely independent path to invites rather than a proxy for test-taking ability.

{% include figure.html num="3" src="f4_research.png" wide="true" caption="Left: research intensity by program length — 6-year matchers report more heavy research. Right: interview conversion rises monotonically with research intensity." %}

## 4. Externships

More externships track with better conversion (**ρ = 0.38**, *p* < 0.001), though the median count is identical for both tracks (4 each). Read the causation carefully: externing where you apply is itself a targeting strategy, so some of this is "people extern at the places most likely to interview them." It remains the single most-emphasized *qualitative* theme across all seven years — nearly every write-up credits externship relationships and letter-writers over raw numbers.

{% include figure.html num="4" src="f5_ext.png" wide="true" caption="Left: externship counts don't separate the two tracks. Right: more externships track with higher conversion." %}

## 5. A myth-check: are scores really rising every year?

The perennial forum refrain is that matched CBSE scores climb every cycle. Once every score is placed on the same EPC scale, that march mostly disappears — matched-applicant medians bounce around the low-70s (6-year) and high-60s/low-70s (4-year) without a strong upward trend. The perceived rise appears to be largely an artifact of the old→new scale change inflating the raw numbers people saw, not a real jump in matched performance.

{% include figure.html num="5" src="f2_cbse_trend.png" caption="Matched-applicant CBSE by cycle. Six-year sits at or above 4-year every year, but neither marches steadily upward once scores are on a common scale. (Early years have small per-track samples — interpret the endpoints loosely.)" %}

## 6. Class rank doesn't separate the tracks

Class-rank percentile has essentially no relationship with program length (ρ = 0.01). Matchers span from top-of-class to near-bottom in both 4- and 6-year programs. The low-rank cases almost always pair a mediocre rank with *something else* carrying the application — a strong CBSE, heavy research, an extra degree, or externship-driven relationships.

{% include figure.html num="6" src="f6_rank.png" caption="Rank vs CBSE among matchers. Both tracks span the full rank range; rank alone doesn't distinguish where people matched." %}

## 7. The application funnel

The attrition is overwhelmingly at the first step — applications to invites. Once applicants reach the interview, they rank almost everything they attend. In other words, for these matchers the binding constraint was *getting invited*, not converting interviews into a rank slot.

{% include figure.html num="7" src="f7_funnel.png" caption="Median application funnel by cycle. The steep drop is applications → invites; the interview → ranked step barely narrows." %}

## Qualitative patterns worth keeping

- **"Score for the interview, personality for the spot."** The most repeated sentiment across all seven years: the CBSE screens you in, then fit and social skills decide.
- **Letters and externships are the hidden currency.** Multiple matchers were told their letters were decisive; many matched where they externed.
- **The low end matches too — usually the long way.** A recurring cast of applicants matched with CBSEs in the low 60s or near-bottom class ranks, almost always into 4-year programs and almost always after one or two non-categorical years.
- **Rank where you want to go.** The standard warning against ranking strategically "to match" rather than by genuine preference shows up every cycle.

## Limitations

Beyond the survivorship and self-selection issues flagged at the top: program length is imputed for a handful of entries and blank where a poster didn't state it; research and extracurricular coding involve judgment; and the 2020–2021 scores are the messiest, since some applicants took the CBSE before the scale change and self-converted. There is essentially no matched-vs-unmatched comparison here — the "Official Results" threads contain almost only matchers. The parallel "PASS / Interviews / Non-Match" threads would be the right source to actually model *whether* someone matches.

[↓ Download the coded dataset (CSV)]({{ '/assets/omfs_all.csv' | relative_url }}) · every row includes a note recording the raw score and its conversion path.
