# Bioinformatics Editing Reference / 生信编辑参考

Internal reference used by `academic-editing`.

## Scope / 适用范围
Apply this reference to GWAS, Mendelian randomization, single-cell, and related computational biology manuscripts.

## Mandatory Setup / 必要准备
Collect or confirm:
1. Primary scientific question and manuscript title
2. Study subtype (GWAS / MR / single-cell / mixed)
3. Target journal
4. Code path (default: `/code`)
5. Output/tables path (default: `/output`)
6. Figure path (default: `/figure`)

## Guideline Mapping / 规范映射
- GWAS: STREGA (+ journal and repository submission expectations)
- MR: STROBE-MR
- Single-cell: minSCe + target journal checklist

## Evidence Checks Before Polishing / 润色前证据核查
1. Verify sample sizes and QC attrition across Methods/Results/Figures.
2. Verify model labels and effect measures (beta/OR/HR, SE, CI, P value).
3. Verify multiple-testing threshold statements and replication claims.
4. Verify dataset/build/tool versions are consistent when explicitly stated.
5. Flag internal contradictions (e.g., unmatched counts, swapped direction, unsupported causal wording).

## Writing Rules / 写作规则
- Keep computational detail accurate but concise.
- Separate association, prediction, and causal claims explicitly.
- Maintain one consistent manuscript voice across methods-heavy and biology-heavy paragraphs.
- Prefer transparent language over hype.

## Output Contract / 输出约定
- Polished text only.
- Bold only revised words/sentences.
- If major scientific/logical inconsistency is found, report the issue briefly before the polished text.
