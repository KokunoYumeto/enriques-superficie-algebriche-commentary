CHECK A TRANSLATION: Federigo Enriques, Le superficie algebriche (Bologna: Zanichelli, 1949), printed pages @@PAGES@@.

ATTACHED
1. The Italian text of these pages in LaTeX, between BEGIN ITALIAN and END ITALIAN. It is the authority.
2. An English translation of the same pages in LaTeX, between BEGIN ENGLISH and END ENGLISH.

TASK. Read both, page by page (the lines "% !PRINTED n" mark the printed pages). List every place where the English
does not say what the Italian says: a mistranslation, an omission, an addition, a wrong technical term, a changed or
dropped formula, index or reference, a negation lost or added, a sentence whose mathematical meaning shifted. Do not
list matters of style, or renderings that are acceptable alternatives. Enriques's own errors are translated as he wrote
them on purpose; they are not translation errors.

DELIVER exactly one fenced block ```csv with the header
page,italian,english,problem,suggestion
italian and english: the passage, quoted exactly and briefly (enough to find it); problem: one sentence; suggestion: the
corrected English for that passage. Quote every field. If a page has no problem, it has no row. After the block, one
line with the number of rows.

BEGIN ITALIAN
@@IT@@
END ITALIAN

BEGIN ENGLISH
@@EN@@
END ENGLISH
