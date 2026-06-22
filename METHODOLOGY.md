# Methodology & Quality Assurance

**Maintained by:** Anzee Hassanali

This document explains how FfD Country Scorecards are built, scored, sourced, and updated — and
is the place to look for the full set of caveats before citing or reusing any figure or score.

---

## 1. What this is, and what it isn't

The FfD Country Scorecard is a **diagnostic conversation-starter**, designed to help quickly orient on a country's financing-for-development position and
identify priority areas for dialogue.

It is:
- A structured synthesis of publicly available development-finance indicators
- A way to surface trends, gaps, and red flags at a glance
- A prompt for further discussion — each indicator card includes a suggested conversation
  question, not a conclusion

It is **not**:
- An official assessment by any government, donor, or institution
- A predictive or econometric model
- A ranking instrument — scores are not designed to be compared *across* countries, only used to
  track a single country's position and trajectory over time
- A replacement for primary-source data. Always verify against the cited source before using a
  figure in a formal document.

---

## 2. Framework structure

- **25 indicators**, grouped into **5 pillars**:
  1. Flows
  2. Expenditure
  3. Spending Effectiveness
  4. Enabling Environment
  5. Financial Market Diagnostics
- Each indicator is scored on a **1–5 scale** against a fixed, pre-defined benchmark threshold
  (e.g., tax revenue ≥15% of GDP = adequate). Thresholds are sourced from the relevant
  international standard-setter (IMF, WHO, UNESCO, PEFA, etc.) and documented on each card.
- Score bands used throughout:

  | Score | Label |
  |---|---|
  | 1 | Critical |
  | 2 | Weak |
  | 3 | Moderate |
  | 4 | Good |
  | 5 | Strong / Excellent |

---

## 3. Scoring & aggregation rules

- **Pillar scores** are the **unweighted average** of the indicator scores within that pillar.
- **Overall score** is the unweighted average of the five pillar scores.
- **Blank-aware averaging is non-negotiable.** Where an indicator has no available data, it is
  **excluded from the average** — never imputed and never treated as zero. A scorecard that
  shows "22 of 25 indicators scored" means the remaining 3 were left out of every average they
  would have affected, and this is stated explicitly on the scorecard.
- **Numeric vs. letter-grade inputs:** for indicators that can be reported either as a composite
  numeric score (e.g., a PEFA score of 2.42) or a letter grade (e.g., "B-"), the numeric value is
  always used preferentially in scoring logic, with letter-grade matching as a fallback only when
  no numeric figure is available.

---

## 4. Data sources

Indicators are drawn from publicly available international databases, including:

- World Bank World Development Indicators (WDI) and V2 API
- IMF World Economic Outlook (WEO), Financial Soundness Indicators (FSI), Data Mapper API, and
  **Article IV Consultation Staff Reports**
- OECD DAC Statistics
- WHO Global Health Expenditure Database
- UNESCO Institute for Statistics
- Transparency International (Corruption Perceptions Index)
- PEFA Secretariat (Public Financial Management assessments)
- Basel Institute on Governance (Basel AML Index)
- World Bank Enterprise Surveys
- World Bank B-READY (Business Ready) Programme
- FATF Mutual Evaluation Reports
- UN INFF Knowledge Platform

Each indicator card on a scorecard links directly to its source. Of the 25 indicators, roughly
half are available through automated API pulls (World Bank, IMF); the remainder are manually
sourced and refreshed, with the source link documented on the card itself.

**Preferred update source:** when an indicator needs a gap-fill or refresh, an **IMF Article IV
Consultation Staff Report** is the preferred authoritative source where available, given its
depth, consistency, and recency relative to other cross-country databases.

---

## 5. Update cadence & visible versioning

Scorecards are updated **opportunistically** — typically when a new IMF Article IV Consultation
or equivalent authoritative report is published for a given country — rather than on a fixed
schedule.

Every update is:
- **Visibly marked on the scorecard itself** (e.g., an "Updated [date] · [source]" badge),
  never silently applied
- **Logged in [CHANGELOG.md](./CHANGELOG.md)** with the date, source document, and a summary of
  which indicators/scores changed and why
- Applied without altering the historical record of *why* a score moved — score changes are
  explained, not just shown

---

## 6. Known limitations

- **Estimates stand in for missing official data** in some cases (e.g., where an indicator's
  most recent official release pre-dates the scorecard's reference period). These are marked as
  estimates on the card itself.
- **Cross-source substitution:** where a primary source is unavailable, a comparable secondary
  source may be substituted (e.g., IMF estimate used in place of a delayed national statistics
  release). This is noted on the relevant card.
- **Indicator selection involves judgment calls.** The framework targets a fixed set of 25
  indicators across 5 pillars; in a small number of cases a candidate indicator was dropped to
  stay within that count (for example, "% Firms Citing Unfavourable Loan Conditions" was dropped
  from the Financial Market Diagnostics pillar in the current version). These substitution
  decisions are recorded in the CHANGELOG when they occur.
- **Not comparable across countries.** Differences in data availability, statistical capacity,
  and context mean a score of "3" in one country's scorecard is not equivalent to a "3" in
  another's. Each scorecard should be read as a standalone diagnostic.
- **Pilot scope.** The current toolchain has been applied to few countries. It has not yet been validated at scale across a broader country set.
- **Not a verdict.** Scores compress complex, multi-causal realities into single numbers for the
  sake of structuring conversation. The qualitative framing on each card (trend, benchmark
  context, conversation prompt) is intended to carry equal weight to the numeric score — readers
  should not anchor on the number alone.

---

## 7. Intended audience and use

Built primarily for:
- Donor agency staff preparing for country dialogue
- Government counterparts seeking a structured external view of financing priorities
- Analysts needing a fast diagnostic starting point before deeper country-specific research

Not intended for:
- Automated decision-making or country risk scoring in financial products
- Formal compliance, audit, or legal documentation without independent verification
- Direct cross-country comparison or league-table style rankings

---

## 8. Authorship & feedback

This framework and scorecard series were designed and are maintained by **Anzee Hassanali**. Corrections,
data-quality concerns, or methodology questions can be raised via the repository's
[Issues](../../issues) page.
