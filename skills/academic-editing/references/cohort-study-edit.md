# Clinical Cohort Editing Reference / 临床队列编辑参考

Internal reference used by `academic-editing`.

## Scope / 适用范围
Apply this reference to prospective or retrospective cohort studies, including population-based cohorts and registry-based cohort analyses.

## Mandatory Setup / 必要准备
Collect or confirm:
1. Primary scientific question and manuscript title
2. Target journal
3. Code path (default: `/code`)
4. Output/tables path (default: `/output`)
5. Figure path (default: `/figure`)

## Guideline Baseline / 规范基线
- Use STROBE as the default reporting standard.
- Enforce participant flow, inclusion/exclusion logic, and analytic sample derivation.

## Evidence Checks Before Polishing / 润色前证据核查
1. Verify all reported N values against outputs.
2. Verify event counts, person-years, follow-up duration, and incidence-rate denominators.
3. Confirm exposure precedes outcome for prospective claims.
4. Check consistency across abstract, main text, tables, and figures.
5. Flag impossible or contradictory numbers before rewriting.

## Writing Rules / 写作规则
- Use exact numbers (`n (%)`, rates, CIs), avoid journalistic approximations.
- Keep Results factual; do not overstate causality.
- Keep tense and terminology consistent across sections.
- Prefer concise, professional medical SCI style.

## Output Contract / 输出约定
- Polished text only.
- Bold only revised words/sentences.
- If major logic/numeric issues exist, output a brief issue block before the polished text.
