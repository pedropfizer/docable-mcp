# PublicationByte & ContentByte Email: Self-Contained Generation Bundle (MCP/Cowork)

A standalone, **fully self-contained** process for turning a **journal-article PDF** (or publication
details) into a **Pfizer-branded internal awareness email** — either a **PublicationByte**
(new publication alert) or a **ContentByte** (M2M deck / resource announcement) — delivered as a
**production-ready HTML file** suitable for email clients and/or PDF export.

The Pfizer brand colors, font guidance, and HTML template skeleton are embedded in this file, so the
only thing you need to supply is the source content (publication PDF, or publication details plus
optional supporting text).

---

## For the assistant: format selection (run this FIRST)

Before generating any content, identify which format applies:

| Signal in the user's input | Format to produce |
|---|---|
| A journal article PDF or DOI is provided | **PublicationByte** |
| An M2M slide deck, training resource, or toolkit is the subject | **ContentByte** |
| Conference abstract disposition / abstract acceptance notifications | **ConferenceByte** (see section below) |

If the signal is ambiguous, **ask the user** before proceeding.

---

## Role & audience

- **Role:** Senior Medical Affairs scientific communications specialist producing internal
  publication awareness communications.
- **Audience:** Internal Medical Affairs / Vaccines Medical colleagues globally — highly scientific,
  evidence-oriented.
- **Tone:** Objective, factual, awareness-focused, non-promotional.
- **Purpose:** Make colleagues aware of new data; the email is not a full training document — it is
  a curated, high-signal alert.

---

## Hard requirements (non-negotiable, all formats)

1. **No fabrication.** Report only what is stated in the source; never invent data, quotes, or
   conclusions. Mark gaps with `[PLACEHOLDER — verify]`.
2. **AMA citation format** for every publication reference (see footnote scheme below).
3. **Subject line format:** `PublicationByte: [Article Title]` / `ContentByte: [Deck/Topic Title]`.
4. **P-values:** capital italic *P*, no leading zero (`P < .001`, `P = .04`). All other statistics
   keep their leading zeros (e.g., `HR 0.85`, `95% CI 0.72–0.99`).
5. **Never use the em dash (—)** in authored text. Use a colon, comma, or parentheses instead.
   The en dash (–) is retained in numeric ranges and verbatim reproduced text.
6. **Compliance note** must be included in ContentByte (see blueprint). For PublicationByte it is
   optional unless local adaptation is expected.
7. **One publication per email.** Do not combine multiple papers into a single PublicationByte.
8. **Key Findings bullets:** strictly sourced from the paper's reported data; ≤ 5 bullets.
9. **Pfizer Notes bullets:** internal Pfizer scientific/strategic perspective; ≤ 5 bullets;
   clearly differentiated from objective findings.
10. **HTML output must use inline CSS** (no `<style>` blocks, no external stylesheets) for maximum
    email-client compatibility.
11. **No PHI/PII.** Do not include patient-identifiable information from the source.

---

## Format 1: PublicationByte — blueprint

Used when sharing a new Pfizer-authored or Pfizer-affiliated journal publication.

### Email structure (in order)

```
[Pfizer Header Banner]

[Introduction paragraph]
  "Dear Colleagues,
   We wanted to bring your attention to the manuscript titled "[BOLD TITLE]" published in
   [JOURNAL] [status: online ahead of print | in press | Volume X Issue Y, Pages A–B].
   PublicationBytes are intended to make [Franchise, e.g., Vaccines] Medical colleagues
   around the globe aware of new Pfizer Global/US publications."

[Em-dash separator + Sender first name]

[Publication Highlights section header]

[AMA citation block]
[Article availability line: "The publication [and supplement] [is/are] attached and can also be
 found here [ARTICLE_URL]."]

[Key Findings table/section]
  • [Background & Methods bullet — 1 bullet]
  • [Key result bullet 1]
  • [Key result bullet 2 — additional results as needed, max 2–3 more]

[Pfizer Notes table/section]
  • [Internal framing bullet 1 — what this means for the portfolio/narrative]
  • [Alignment with prior evidence bullet]
  • [Limitations / ongoing work bullet — if applicable]

[Copyright line: © YEAR Pfizer Inc. All rights reserved]

[Sender signature block]
```

### Section-by-section writing rules (PublicationByte)

**Introduction paragraph**
- Name the article title in **bold**.
- Italicize the journal name.
- State the publication status exactly: "online ahead of print", "in press", or give
  Volume/Issue/Pages if known.
- Do not editorialize — this is a factual announcement.

**Key Findings**
- First bullet always starts with "Background and Methods:" followed by a concise summary of
  the study design, population, and the key safety/efficacy outcomes evaluated.
- Subsequent bullets start with "Results:" or with a topic label (e.g., "Primary endpoint:").
- Include effect sizes, confidence intervals, and P-values where reported.
- Match the study's own language for outcomes (do not rephrase clinical endpoint definitions).
- If the paper is an interim analysis, state "This publication provides interim results…"

**Pfizer Notes**
- These represent Pfizer's internal scientific interpretation — clearly authored, not "results."
- First bullet: summarize the overarching implication ("In this [study design], there were no
  statistically significant increases in…").
- Second bullet: align with prior Pfizer data or external evidence; cite study names if known.
- Third bullet: acknowledge limitations or ongoing work, where relevant ("Continuous monitoring
  remains essential…").
- Do **not** use promotional language. Do not claim superiority or make comparative claims not
  supported by the data.

---

## Format 2: ContentByte — blueprint

Used when sharing a new Medical-to-Medical (M2M) deck, toolkit, or training resource.

### Email structure (in order)

```
[Pfizer Header Banner]

[Introduction paragraph]
  "Dear Colleagues,
   We are happy to share the M2M deck about [TOPIC / STUDY / ASSET NAME]."

[Relevance to Medical Narrative]
  [1–3 sentences: why this asset matters to the medical narrative / portfolio]

[Key Highlights]
  • [Highlight 1]
  • [Highlight 2]
  [Up to 4 bullet highlights from the deck]

[Compliance Note — REQUIRED]
  "Local use of this global resource requires review and approval according to Local Pfizer
   policies and procedures, and any local rules and regulations prior to any external use."

[Additional Support Materials]
  Resource Name | Link | Additional Information
  (table listing any Q&A doc, training recording, or supporting material)

[Special thanks line: "Special thanks to [NAME(S)] for their contributions."]

[Contact line: "If you have questions/comments, please reach out to [NAME/EMAIL]."]

[Medical Resources section]
  Resource Name | Link | Additional Information
  (repository or mGCMA links)

[mGCMA instruction line if needed]
  "To utilize locally, the content will require submission and approval through local
   processes and local country regulations. For directions on how to correctly create a
   linked copy in mGCMA, click here."

[Copyright line: © YEAR Pfizer Inc. All rights reserved]

[Sender signature block]
```

### Section-by-section writing rules (ContentByte)

**Introduction paragraph**
- Name the deck/resource in **bold**.
- Keep to 1–2 sentences.

**Relevance to Medical Narrative**
- Connect the resource to the current medical affairs narrative, unmet need, or data gap it
  addresses.
- Do not exceed 3 sentences.

**Key Highlights**
- Extract the 3–4 highest-value claims or features of the deck/resource.
- Each bullet should be standalone and actionable.

**Compliance Note**
- Use the verbatim compliance language above; do not modify it.

---

## Format 3: ConferenceByte — blueprint

Used when sharing conference abstract acceptance/disposition updates for a franchise.

### Email structure (in order)

```
[Pfizer Header Banner]

[Introduction paragraph]
  "Dear Colleagues,
   We are happy to share the disposition decisions across the [FRANCHISE] franchise for
   [late-breaker / regular] abstracts submitted to [CONFERENCE NAME + YEAR]
   ([DATES + CITY]). A total of [N] abstracts have been accepted [...]"

[Presence by the Numbers — summary stats block]
  [TOTAL ACCEPTED] — Accepted Abstracts
  [N ORAL] — Oral Presentations
  [N POSTER] — Poster Presentations

[Late-breaker Highlights — or main highlights — section]
  For each abstract:
    [DISEASE AREA / PROGRAM LABEL] — [Abstract short title]
    [First Author et al.] (Abstract #[NUMBER]) [Date, Time, Timezone] ([presentation type])

[Link to disposition report if applicable]

[Copyright line]

[Sender signature block]
```

### Section-by-section writing rules (ConferenceByte)

**Introduction paragraph**
- State the exact number of accepted abstracts.
- Distinguish oral presentations from posters.
- Note embargoed status if applicable ("all abstracts are embargoed").

**Highlights section**
- Group by disease area or program label using a consistent label format (e.g., "RSV Maternal",
  "PCV Adult", "RNA Flu").
- For each abstract: Author last name + first initial et al., abstract number, date, time
  (with timezone), and presentation type.
- Use en dash (–) in time ranges (e.g., `16:50–17:35 CET`).

---

## Step-by-step process

1. **Identify the format** (PublicationByte / ContentByte / ConferenceByte) as described above.
2. **Validate the source.** If a PDF is missing or unreadable → ask before proceeding. If
   multiple files are provided → confirm the primary source.
3. **Extract content:**
   - *PublicationByte:* citation fields (authors, title, journal, year, volume, pages, DOI);
     study design and population; primary and key secondary endpoints and their results; safety
     summary; author-stated limitations.
   - *ContentByte:* deck/resource title; key messages; compliance and access details.
   - *ConferenceByte:* conference name, dates, city; abstract titles, numbers, authors,
     presentation types and times.
4. **Draft the email sections** following the relevant blueprint above. Stay within bullet limits.
   Check every number against the source before including it.
5. **Write the AMA citation** (see citation rules below).
6. **Render the HTML** using the template skeleton and brand standards below. Apply inline CSS
   only. Validate that the structure matches the blueprint exactly.
7. **Verify:**
   - No fabricated data or conclusions.
   - All statistics trace back to source text.
   - Bullet limits respected (≤ 5 Key Findings; ≤ 5 Pfizer Notes; ≤ 4 Key Highlights).
   - AMA citation complete and accurate.
   - Compliance note present (ContentByte).
   - Inline CSS only; no orphaned `<style>` blocks.
   - P-value formatting: capital *P*, no leading zero.
   - No em dashes in authored text.
8. **Deliver** the HTML file and a brief verification note (what source, any gaps flagged).

---

## AMA citation rules

Format: `AuthorLastName AI, AuthorLastName BB, AuthorLastName CC, et al. Article title. *Journal Abbr*. Year;Volume(Issue):Pages. doi:XX.XXXXX/XXXXX.`

- Up to 6 authors; 7 or more → list first 3, then "et al."
- Journal name italicized in HTML (`<i>Journal Abbr</i>`).
- Build only from fields present in the source — never invent volume, pages, or DOI.
- For online-ahead-of-print: `Year Mon Day. doi:XX.` (omit volume/pages).
- Abbreviated in body text (body of email prose): `First-Author et al. *Journal*. Year.`

---

## HTML template skeleton

Use this skeleton for all formats. Fill in `[PLACEHOLDERS]`. Apply **inline CSS only** throughout
(email clients strip `<style>` blocks). Preserve the table-based layout for Outlook/Exchange
compatibility.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>[SUBJECT_LINE]</title>
</head>
<body style="margin:0;padding:0;background-color:#f4f4f4;font-family:Arial,Helvetica,sans-serif;">
<div align="center">
<table width="600" cellpadding="0" cellspacing="0" border="0"
       style="width:600px;background-color:#FFFFFE;border-collapse:collapse;">

  <!-- ═══════ PFIZER HEADER BANNER ═══════ -->
  <!-- If brand asset is available (see Appendix), reference working/assets/pfizer_email_header.png -->
  <!-- Fallback: solid Deep Blue bar with white wordmark text -->
  <tr>
    <td style="background-color:#000067;padding:18px 40px 14px 40px;text-align:left;">
      <span style="font-family:Arial,sans-serif;font-size:22px;font-weight:bold;
                   color:#FFFFFF;letter-spacing:1px;">Pfizer</span>
    </td>
  </tr>

  <!-- ═══════ CONTENT AREA ═══════ -->
  <tr>
    <td style="padding:27px 41px 54px 40px;">

      <!-- INTRODUCTION -->
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;
                line-height:15pt;margin:0 0 4.5pt 0;">
        <b>Dear Colleagues,</b>
      </p>
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;
                line-height:15pt;margin:0 0 18.75pt 0;">
        [INTRODUCTION_PARAGRAPH]
      </p>
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;
                line-height:15pt;margin:0 0 12pt 0;">
        [PUBLICATION_BYTE_PURPOSE_LINE or omit for ContentByte]
      </p>

      <!-- SEPARATOR + SENDER -->
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;margin:0 0 4pt 0;">
        &#8212;
      </p>
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;margin:0 0 20pt 0;">
        [SENDER_FIRST_NAME]
      </p>

      <!-- ── SECTION HEADER: Publication Highlights / Key Highlights ── -->
      <p style="font-family:Arial,sans-serif;font-size:13pt;font-weight:bold;
                color:#0000C9;margin:0 0 8pt 0;">
        [SECTION_HEADER_TITLE]
      </p>

      <!-- CITATION (PublicationByte only) -->
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;
                line-height:15pt;font-weight:bold;margin:0 0 4pt 0;">
        [AMA_CITATION_FULL]
      </p>
      <p style="font-family:Arial,sans-serif;font-size:10pt;color:#353B3E;
                line-height:15pt;margin:0 0 18pt 0;">
        The publication [and supplement] [is/are] attached and can also be found
        <a href="[ARTICLE_URL]" style="color:#467886;">here</a>.
      </p>

      <!-- ── KEY FINDINGS table ── -->
      <table width="100%" cellpadding="0" cellspacing="0" border="0"
             style="width:100%;border-collapse:collapse;margin-bottom:16pt;">
        <tr>
          <td style="background-color:#0000C9;padding:7px 12px;
                     font-family:Arial,sans-serif;font-size:10.5pt;font-weight:bold;
                     color:#FFFFFF;">
            Key Findings
          </td>
        </tr>
        <tr>
          <td style="padding:10px 0 0 0;">
            <ul style="margin:0;padding-left:18px;
                       font-family:Arial,sans-serif;font-size:10pt;
                       color:#353B3E;line-height:15pt;">
              <li style="margin-bottom:8pt;">[KEY_FINDING_1_BACKGROUND_METHODS]</li>
              <li style="margin-bottom:8pt;">[KEY_FINDING_2_PRIMARY_RESULTS]</li>
              <!-- add <li> elements up to 5 total -->
            </ul>
          </td>
        </tr>
      </table>

      <!-- ── PFIZER NOTES table (PublicationByte) / COMPLIANCE NOTE (ContentByte) ── -->
      <table width="100%" cellpadding="0" cellspacing="0" border="0"
             style="width:100%;border-collapse:collapse;margin-bottom:16pt;">
        <tr>
          <td style="background-color:#0000C9;padding:7px 12px;
                     font-family:Arial,sans-serif;font-size:10.5pt;font-weight:bold;
                     color:#FFFFFF;">
            Pfizer Notes
          </td>
        </tr>
        <tr>
          <td style="padding:10px 0 0 0;">
            <ul style="margin:0;padding-left:18px;
                       font-family:Arial,sans-serif;font-size:10pt;
                       color:#353B3E;line-height:15pt;">
              <li style="margin-bottom:8pt;">[PFIZER_NOTE_1]</li>
              <li style="margin-bottom:8pt;">[PFIZER_NOTE_2]</li>
              <!-- add <li> elements up to 5 total -->
            </ul>
          </td>
        </tr>
      </table>

      <!-- COMPLIANCE NOTE (ContentByte only — include verbatim) -->
      <!--
      <p style="font-family:Arial,sans-serif;font-size:9pt;color:#666666;
                line-height:13pt;margin:0 0 12pt 0;">
        <b>Compliance Note:</b> Local use of this global resource requires review and approval
        according to Local Pfizer policies and procedures, and any local rules and regulations
        prior to any external use.
      </p>
      -->

    </td>
  </tr>

  <!-- ═══════ FOOTER ═══════ -->
  <tr>
    <td style="padding:0 41px 20px 40px;font-family:Arial,sans-serif;
               font-size:10pt;color:#353B3E;line-height:15pt;">
      <p style="margin:0 0 4pt 0;">
        <a href="[PFIZER_LINK]" style="color:#467886;">[LINK_LABEL_IF_ANY]</a>
      </p>
      <p style="margin:0 0 12pt 0;">
        &copy; [YEAR] Pfizer Inc. All rights reserved
      </p>
      <p style="margin:0 0 4pt 0;font-size:9pt;color:#666666;">
        [SENDER_FULL_NAME], [CREDENTIALS]<br>
        [SENDER_TITLE]<br>
        M: [PHONE]
      </p>
      <p style="margin:0;font-size:9pt;color:#666666;">
        Pfizer Research &amp; Development
      </p>
    </td>
  </tr>

</table>
</div>
</body>
</html>
```

---

## PDF export command

To convert the HTML output to a PDF for attachment or archiving, run either of the following after
the HTML file is written to `output/`:

```bash
# Option A — Google Chrome headless (preferred, best email fidelity)
google-chrome --headless --disable-gpu --no-sandbox \
  --print-to-pdf="output/publication_byte.pdf" \
  --print-to-pdf-no-header \
  "output/publication_byte.html"

# Option B — wkhtmltopdf (widely available on Linux/CI)
wkhtmltopdf --page-size A4 --margin-top 10 --margin-bottom 10 \
  --margin-left 15 --margin-right 15 \
  output/publication_byte.html output/publication_byte.pdf

# Option C — Python (requires weasyprint)
python3 -c "
from weasyprint import HTML
HTML('output/publication_byte.html').write_pdf('output/publication_byte.pdf')
"
```

---

## Pfizer brand standards (email)

**Colors:**

| Role | Name | Hex |
|------|------|-----|
| Primary brand / headers, section titles | Pfizer Blue | `#0000C9` |
| Dark header bar | Deep Blue | `#000067` |
| Section header blocks | Pfizer Blue | `#0000C9` with white text |
| Body text | Dark Gray | `#353B3E` |
| Secondary / captions / compliance | Medium Gray | `#666666` |
| Email canvas | Near-white | `#FFFFFE` |
| Links | Teal link | `#467886` |
| Visited links | Mauve | `#96607D` |

**Typography:**
- Fonts: `"Pfizer Diatype", Arial, Helvetica, sans-serif` — always include Arial fallback.
- Email clients will render Arial; Pfizer Diatype renders only if installed on recipient's system.
- Body text: 10pt (13.3px), line-height 15pt.
- Section headers: 13pt, bold, Pfizer Blue.
- Copyright/footnote: 9pt, Gray 60 (`#666666`).

**Layout:**
- Email width: **600px** fixed, table-based.
- Content padding: `27px top, 41px right, 54px bottom, 40px left` (mirrors Pfizer Outlook template).
- Bullet list padding-left: 18px.
- Inter-bullet spacing: 8pt margin-bottom on each `<li>`.
- Section header blocks (Key Findings / Pfizer Notes): solid `#0000C9` background, white bold text,
  7px/12px padding, immediately above the bullet list with no gap.

---

## Compliance & safety

- No PHI/PII in any field.
- No off-label language; do not use findings to promote unapproved uses.
- Pfizer Notes must not contain promotional claims or comparative efficacy assertions not supported
  by the cited study.
- ContentByte: the compliance note is **mandatory** and must use the verbatim text provided in the
  blueprint above.
- For local country adaptation, add: "Local use of this global resource requires review and
  approval according to Local Pfizer policies and procedures…" (see ContentByte blueprint).
- Cite only the source study; do not merge findings from multiple papers without explicit flagging.
- Mark any item that cannot be verified from the source with `[PLACEHOLDER — verify]` rather than
  fabricating.

---

## Quick-reference checklist (run before delivering)

- [ ] Correct format selected (PublicationByte / ContentByte / ConferenceByte)
- [ ] Subject line matches format (`PublicationByte: ...` / `ContentByte: ...`)
- [ ] All data traces to source — no fabricated numbers
- [ ] AMA citation complete (no invented volume/pages/DOI)
- [ ] Key Findings ≤ 5 bullets; Pfizer Notes ≤ 5 bullets
- [ ] P-values: capital *P*, no leading zero
- [ ] No em dash in authored text
- [ ] Inline CSS only — no `<style>` blocks
- [ ] Compliance note present (ContentByte)
- [ ] No PHI/PII
- [ ] Placeholders for sender name, URL, year, and contact info clearly marked for human fill-in

---

## Example output summary (PublicationByte)

**Subject:** `PublicationByte: Interim Safety of RSVpreF Vaccination During Pregnancy`

**Introduction:** Announces the manuscript in *JAMA*, online ahead of print.

**Key Findings (5 bullets):**
1. Background and Methods: interim retrospective cohort study across 5 US health plans; 54,011
   pregnancies; 10,273 (19%) received RSVpreF at 32w0d–36w6d during first RSV season post-approval.
2. Results: After 1:1 matching (n = 6,857/group), no statistically significant increases in
   preterm birth, PROM, preterm PROM, or incident HDP versus unvaccinated pregnancies.
3. Results: Subcomponents of HDP showed similar prevalence between groups; no hypothesis testing
   conducted for subcomponents.
4. Results: Final report expected 2029; will include Medicaid, minority populations, and subgroup
   analyses (immunocompromised, prior HDP).

**Pfizer Notes (3 bullets):**
1. In this interim report, no statistically significant increases were seen in prespecified safety
   outcomes (preterm birth, incident HDP, PROM, preterm PROM) vs. unvaccinated pregnancies.
2. These results align with prior Pfizer sequential safety surveillance and VSD data, which also
   found no increased risk of preterm birth.
3. Prior Pfizer and VSD work showed an increased HDP risk; this more confounding-controlled study
   did not replicate a statistically significant HDP signal — continuous monitoring remains essential.
