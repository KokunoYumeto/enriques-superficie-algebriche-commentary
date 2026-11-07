FINISH A TRANSLATION: Federigo Enriques, Le superficie algebriche (Bologna: Zanichelli, 1949), printed pages @@PAGES@@.

ATTACHED
1. The Italian text of these pages (LaTeX), between BEGIN ITALIAN and END ITALIAN: the authority.
2. The English translation of the same pages (LaTeX), between BEGIN ENGLISH and END ENGLISH.
3. Problems that an independent reader found in the English, between BEGIN PROBLEMS and END PROBLEMS, one per line:
   id | page | Italian passage | English passage | problem | suggested English.
4. Corrections made in a second, corrected Italian version, between BEGIN CORRECTIONS and END CORRECTIONS, one per line:
   item | page | printed Italian | corrected Italian | kind | justification. Each corrects a misprint of the print or a
   slip of the author.

TASK 1. THE TRANSLATION. For each problem, read the Italian and decide: accept (the English does not say what the
Italian says) or reject (the English is right, or an acceptable rendering; or the "problem" asks to correct Enriques,
whose own errors are translated as he wrote them). For an accepted problem, give the fix: en_snippet copied exactly
from the English (at least 20 characters, occurring exactly once) and replacement. Keep every formula and macro.
The independent reader found the following kinds of problem in several parts. Check the whole English of these pages
for them too, and fix every occurrence, as further rows with problem ids NEW-1, NEW-2, ...:
- "linea" in Enriques usually means a curve, not a straight line ("linea doppia": double curve; "linee base": base
  curves); "retta" is a straight line. Translate "linea" as "curve" unless the context makes it straight.
- "irriducibili" said of surfaces or types that cannot be transformed into one another ("superficie ... irriducibili
  per trasformazioni birazionali", "due tipi irriducibili") means birationally inequivalent (not transformable into
  one another), not "irreducible". Said of a single curve, surface or system, "irriducibile" is "irreducible".
- "composto con un'involuzione" (of a series, system or pencil): "composed with an involution".
- points "vicini e fronteggianti" a point: infinitely near points "proximate" to it.
- "rappresentare in modo semplice" (a surface on a plane): "represent one-to-one".
- "gruppi di curve equivalenti", where the groups are equivalent to one another: "equivalent groups of curves".
Deliver a fenced block ```csv with the header
problem,decision,en_snippet,replacement,reason
decision: accept | reject. reason: one sentence.

TASK 2. THE CORRECTED TRANSLATION. For each correction, make the same correction in the English: en_snippet copied
exactly from the English as it reads after your task 1 fixes (at least 20 characters, occurring exactly once) and
replacement with only that error corrected. If the correction has no counterpart in the English (for example an
Italian spelling slip the translation already reads correctly), decision "no change" and say why.
Deliver a second fenced block ```csv with the header
item,decision,en_snippet,replacement,note
decision: apply | no change.

Quote every field that contains a comma, a quote or a line break (a quote inside is doubled). One row per problem or
correction, in the order given. If a list is empty, deliver its block with the header only.

BEGIN PROBLEMS
@@PROBLEMS@@
END PROBLEMS

BEGIN CORRECTIONS
@@CORRECTIONS@@
END CORRECTIONS

BEGIN ITALIAN
@@IT@@
END ITALIAN

BEGIN ENGLISH
@@EN@@
END ENGLISH
