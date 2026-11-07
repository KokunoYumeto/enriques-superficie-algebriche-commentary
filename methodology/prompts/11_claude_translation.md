TRANSLATE INTO ENGLISH: Federigo Enriques, Le superficie algebriche (Bologna: Zanichelli, 1949), printed pages
@@PAGES@@ (part @@PART@@ of @@PARTS@@).

ATTACHED. The Italian text of these pages, in LaTeX, between BEGIN ITALIAN and END ITALIAN. It is a careful edition of
the print and the authority.

TASK. Translate the LaTeX into English LaTeX, completely and faithfully, sentence by sentence.
- Keep every formula, symbol, index, label, equation tag, footnote marker, page marker and macro exactly as in the
  Italian. Translate only words, including words inside \text{...}, in headings and in footnotes. Keep the lines
  "% scan: ..." and "% !PRINTED ..." and every \weberpage{...}, \weberblank{...} and \editiongap exactly where they
  stand, so that each printed page can be found in the English.
- Macros with text arguments: \edchapter{n}{title}{bookmark}{running head}: translate the last three arguments; keep n.
  \edsection{heading}{bookmark}{label}: translate the first two, keep the label. \origfootnote{n}{id}{text}:
  translate the text only. \gesperrt{...}, \textit{...}, \textbf{...}: keep the macro, translate the words.
  \sourcewarning{...}: translate the note.
- Use the classical English terminology of the subject (as in Zariski's Algebraic Surfaces), with these renderings:
  superficie: surface | curva: curve | sistema lineare: linear system | sistema continuo: continuous system | sistema completo: complete system | fascio: pencil | rete: net | serie lineare: linear series | gruppo di punti: group of points | punto base: base point | punto multiplo, doppio, triplo: multiple, double, triple point | curva eccezionale: exceptional curve | curva fondamentale: fundamental curve | trasformazione birazionale (cremoniana): birational (Cremona) transformation | trasformata: transform | curva aggiunta, sistema aggiunto: adjoint curve, adjoint system | aggiunzione: adjunction | curva canonica, sistema canonico: canonical curve, canonical system | sistema bicanonico, pluricanonico: bicanonical, pluricanonical system | genere geometrico: geometric genus | genere numerico: arithmetic genus | genere lineare: linear genus | bigenere: bigenus | plurigeneri: plurigenera | irregolarità: irregularity | superficie regolare, irregolare: regular, irregular surface | superficie rigata: ruled surface | superficie razionale: rational surface | superficie ellittica, iperellittica: elliptic, hyperelliptic surface | piano doppio: double plane | curva di diramazione: branch curve | involuzione: involution | serie caratteristica: characteristic series | curve equivalenti, disequivalenti: equivalent, non-equivalent curves | virtuale, effettivo: virtual, effective | dimensione: dimension | grado (di un sistema): degree | ordine (di una curva o superficie): order | classe: class | invariante di Zeuthen-Segre: Zeuthen-Segre invariant | sezione iperpiana: hyperplane section | curva doppia: double curve | integrale (semplice, doppio) di prima, seconda specie: (simple, double) integral of the first, second kind | varietà di Picard: Picard variety | modello: model | si vede facilmente: one easily sees | c. d. d.: Q.E.D. | cfr.: cf. | n. (numero): no. | Capitolo: Chapter | Introduzione: Introduction | Prefazione: Preface | INDICE: CONTENTS
- Keep Enriques's notation, his numbering, his emphases and his references ("cfr. Cap. II, § 8" becomes "cf. Chap. II,
  § 8"). Do not modernize his mathematics, correct him, add notes or omit anything. Where he is wrong, translate what he
  wrote. A word broken at the end of a page stays broken in the same place in English as far as English allows.
- Write natural, precise English; long Italian sentences may become two English sentences only where English needs it.

DELIVER exactly one fenced block ```latex containing the English LaTeX of all these pages, and nothing else.

BEGIN ITALIAN
@@TEX@@
END ITALIAN
