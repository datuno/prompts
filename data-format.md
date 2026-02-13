Reading Survey AI Markdown Exports

- Top-Level Survey Header
  The document begins with # <Survey Name> followed by _Generated on YYYY-MM-DD HH:MM_. Treat this as the report
  title and timestamp.
- Page Breaks Between Sections
  --- marks the boundary between top-level FancyTree folders (or standalone questions). Everything after a divider
  belongs to the next major section until the following divider or the end of the file.
- Folder Headings
  Tree folders appear as nested headings (e.g., ## Demographics, ### Employment Status). These are organizational
  only—no statistics live directly under a folder unless it contains questions at that level.
- Question Blocks
  Each analyzable question starts with a heading (##, ###, etc.) followed immediately by a scope callout:
  > Scope: all following results refer to **Question Title**.
  Everything until the next heading of equal or higher level applies to this question.
- Question Metadata
    - If present, the next line is the type badge (e.g., *Type: SINGLE*).
    - Use this to anticipate whether multiple answers, matrices, or open text may follow.
- Target Group Section (### Target Group)
    - Lists the access filter in effect, user-defined filters with their questions and selected answers, or a note
      indicating full target group coverage.
    - Use this to understand the universe each metric reflects.
- Total Results Section (### Total Results)
  Bullet list format:
    - Answer Label — 42.1% (n=1 234; +- 2.5%: 39.6-44.6%)
        - Percent: share of the target group.
        - n=: weighted count (rounded).
        - Margin: total sampling error band. If missing, the cell lacked enough data.
- Subgroup Results Section (### Subgroup Results)
  Begins with > Breakdown: subgroup metrics for **Question Title**.
  Nested headings map to crossings (e.g., #### Education Level), followed by segment headings (##### Secondary
  Education) and lists in the same bullet format.
    - Read the headings like a hierarchy: crossing → segment → bullet metrics.
    - Missing segments indicate insufficient data for that slice.
- Interpreting Empty Notes
  Bullets reading - No data available. mean the question had no usable counts under that section; ignore for
  insights but note potential data sparsity.
- Language and Labels
  All labels are pulled from translations active in the analysis session, so text matches what end users see on
  the platform.
- Troubleshooting
    - If a section seems out of place, check the preceding scope callout and heading level.
    - Repeated subgroup names under different questions are expected; rely on the question heading to keep context
      straight.
    - Missing scope or breakdown notes indicate the export predates the latest format; request regeneration.

Use these cues to navigate quickly: scan dividers for major folders, read question scope callouts, then consume
totals before diving into subgroup breakouts.