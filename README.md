# The Exchange Rate

**How much CAT does your marksheet buy?**

An interactive, single-page breakdown of IIM Ahmedabad's new shortlisting formula for the PGP 2027–29 batch (CAT 2026). You enter your marks, and it shows what every Application Rating (AR) point is worth in CAT percentile, compared side by side with last year's rules.

**Live:** https://devanshgohil07.github.io/iima-new-admission-policy-impact/

---

## Why it exists

IIMA kept the 35 / 65 split between marksheet and CAT, but changed two things:

1. **The CAT half now counts as a percentile out of 100, not a raw score out of 204.** You can always score more marks, but no one scores above the 100th percentile. Once you clear your category's cut-off there is very little CAT left to win, while AR still separates candidates by many points. So the marksheet ends up deciding much more than it did.
2. **Five degree tables and three Class 12 tables became one common table.** For almost every background, the same marksheet now earns fewer points. This was never announced as a cut.

IIMA published the weights but never said what they add up to for an applicant. This page works that out.

## What it shows

| Chapter | The question it answers |
|---|---|
| 1 · The exchange rate | What is one AR point worth in CAT terms? (1.417 percentile points now; 2.891 raw marks last year) |
| 2 · The two profiles | How far ahead is a rival with a better marksheet, and does that head start fade as you score higher? |
| 3 · Closing the gap | Which of your own AR bands can you still change, and what is each worth? What CAT score ties you with a rival? |
| 4 · Where the line fell | What would last year's real category cut-offs have asked of you under each table? |
| 5 · Hidden effects | Why AR can outweigh CAT above the cut-off, who lost most from the common table, and why the unpublished top-50 AR average matters |
| 6 · Method & notes | Formulas, sources, assumptions and limits |

### Three findings that hold for every profile

- **A marksheet head start no longer fades.** A rival with 3 more AR points (a non-male twin, for example) is **4.25 percentile** ahead of you under the new rules at any score. Last year the same gap was worth 3.25 at the 95th percentile and only 0.38 at the 99.5th.
- **The common table is a loss or a wash for nearly everyone.** CA/CS/CMA candidates lose up to 7 points, medicine and arts degrees up to 5, commerce and management up to 3, and engineering 3 at 75–80 %. The only gain anywhere is one point for an engineering, science or other degree between 55 and 65 %.
- **The change is regressive if the top-50 average falls.** A candidate already at AR 38 loses nothing to the new table and gains from any drop in the divisor. A mid-table candidate loses to the table first and only wins part of it back.

## The formulas

**New rules: PGP 2027–29, CAT 2026**

```
Raw CS         = 0.35 × (AR ÷ top-50 AR average) + 0.65 × (CAT percentile ÷ 100)
Normalised CS  = Raw CS ÷ (average of top 1 % raw CS in the applicant's UG discipline)
1 AR point     = 0.35 ÷ 38 ÷ 0.0065 = 1.417 percentile points   (divisor 38)
```

**Old rules: PGP 2026–28, CAT 2025**

```
CS          = AR × 0.35 ÷ 38 + overall CAT score × 0.65 ÷ 204
1 AR point  = 2.891 raw marks
```

**Rating table under the new rules** (one table for Class 10, Class 12 and bachelor's): ≤ 55 → 1, > 55 → 2, > 60 → 3, > 70 → 5, > 80 → 8, > 90 → 10. Work experience: under 12 months → 0; 12–36 months → 0.20 × (months − 11); over 36 → 5. Non-male → 3. Maximum 38.

Comparisons between two candidates assume they studied the same discipline, so the discipline normalisation cancels out. The top-50 AR average for 2027–29 is unpublished (it was 35, 37 and 38 in the last three cycles). The page defaults to 38 and lets you test 34–38 under *Advanced assumptions*.

## Data and sources

- **IIMA Admission Procedure, PGP 2027–29:** new formula, common table, CAT percentile floors (Table 4)
- **IIMA Shortlisting Criteria, PGP 2024–26, 2025–27 and 2026–28:** old tables, published top-50 AR averages, Stage-2 minimum composite scores
- **CAT 2022–24 score-vs-percentile curves:** inverted from slot-wise score-calculator data, with outliers filtered and the curves made monotone. They check out against published benchmarks (2024: 99th percentile at 94.75 marks).
- **CAT 2025 curve:** no public scorecard dataset exists. The default averages the published IMS and Cracku estimates, and the gap between the two is shown as the uncertainty.

Where this page and an official IIMA document disagree, the official document is right.

## What it does not do

- **It does not predict who gets shortlisted.** It compares two sets of rules, using the same candidates. CAT 2025 and CAT 2026 are different papers sat by different applicants, and the new rules are already changing who applies.
- **It stops at the shortlist.** The written test (AWT) and personal interview decide 60 % of the final score, and none of that is modelled.
- **Sectional cut-offs are not modelled.** They are pass/fail gates rather than scores.

## Privacy

Nothing you type leaves your browser. There are no analytics, no cookies, no storage and no network requests after the fonts load. The **Copy permalink** button saves your scenario in the URL fragment (the part after `#`), which browsers never send to a server.

## Technical

- One self-contained `index.html`: vanilla JavaScript, inline CSS, and the curve data embedded as JSON. No build step and no dependencies apart from Google Fonts.
- Hosted on GitHub Pages from `main` / root.
- Before each release it is checked by a private Playwright test suite (141 checks): exchange rates, rating tables, curve values, cut-off maths, decimal input handling, permalinks, and layout at 400 px on phones.

To run it locally, open `index.html` in any modern browser.

## Licence and credit

© 2026 **Devansh Gohil**. Released under [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/). The full text is in [`LICENSE`](LICENSE).

- **You may** share and adapt this work, privately or publicly, as long as you credit Devansh Gohil and link back to this repository or the live page.
- **You may not** use it commercially. That includes coaching institutes, test-prep companies and admissions consultancies.

Suggested credit: *"The Exchange Rate" by Devansh Gohil — https://devanshgohil07.github.io/iima-new-admission-policy-impact/ — CC BY-NC 4.0*

## Not affiliated

This is an independent analysis of published criteria. It is not affiliated with, endorsed by, or connected to IIM Ahmedabad or the CAT conducting body, and it is not admissions advice.
