Source: https://zenodo.org/records/1428430
PDF sha256: 80b2fea3fc68f7a31aa0659c4f33ab3eff91cb05269a31557c750d4fca7451c3
License: public domain in the United States (J. Radon, Abh. Math. Sem. Univ. Hamburg 1 (1922) 1-14, published before 1931); public domain worldwide from 2027-01-01
Language: deu
Fidelity: machine-gated

# Transcription of radon_1922_lineare_scharen_orthogonaler_matrizen.pdf

Transcription of `radon_1922_lineare_scharen_orthogonaler_matrizen.pdf` in this directory, 14 pages; each `## PDF page` heading marks a page of the PDF.

Method: pages 1-14 by Surya OCR 0.17.0 at 200 dpi (layout-ordered text, formulas as LaTeX between `<math>` tags), read from the page-image OCR pass of the documents repositories. No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Lineare Scharen orthogonaler Matrizen.
Von J. RADON in Hamburg.
A. HURWITZ hat gelegentlich des Versuches, die Kompositionstheorie
der quadratischen Formen auf beliebig viele Variable auszudehnen<sup>1</sup>), die
Frage aufgeworfen, wann der Gleichung
<math>(x_1^2 + x_2^2 + \ldots + x_n^2) (y_1^2 + y_2^2 + \ldots + y_n^2) = z_1^2 + z_2^2 + \ldots + z_n^2</math>
durch bilineare Funktionen <math>z_i</math> der <math>x_i</math> und <math>y_i</math> genügt werden kann.
Es
ergab sich dabei, daß dies nur für die Werte <math>n=1, 2, 4, 8</math> möglich
ist. Im Anschluß an diese Frage stellt HURWITZ u. a. dasselbe Problem
für die allgemeinere Gleichung
<math>(x_1^2 + x_2^2 + \ldots + x_n^2) (y_1^2 + y_2^2 + \ldots + y_n^2) = z_1^2 + z_2^2 + \ldots + z_n^2</math>
und gibt für den bei gegebenem n unter Voraussetzung der Möglichkeit
einer derartigen Lösung größten zulässigen Wert von <math>p</math> eine Abschätzung.
Faßt man hier in den gesuchten bilinearen Funktionen die <math>x_i</math> als
Parameter auf, so definieren sie eine in <math>x_1 
ldots x_p</math> lineare Schar von ortho-
gonalen Substitutionen.
Demnach kann man mit Hurwitz die gestellte Frage auch so
aussprechen: es sollen quadratische Matrizen <math>A_1, A_2, \dots</math> von je <math>n^2</math> Elementen
in möglichst großer Anzahl (p) so bestimmt werden, daß <math>x_1 A_1 + \ldots + x_p A_p</math>
für alle Werte der Parameter <math>x_1 \dots x_p</math> eine orthogonale Matrix darstellt.
Von ganz anderer Seite her sah ich mich veranlaßt, mich mit diesem
Problem zu beschäftigen. Für den Fall reeller Matrizen ergab sich mir
seine genaue Lösung durch ein eigentümliches Reduktionsverfahren, das
Matrizen heranzieht, deren Elemente komplexe Zahlen sowie Quaternionen
sind. Ich möchte dieses Verfahren im folgenden angeben, zuvor aber
mein Resultat formulieren:
Bezeichnet man für jedes n den gesuchten größtmöglichen Wert
von p durch v (n), hat ferner n die Form:
<math>n = 2^{4a+\beta} n'</math> (<math>\beta = 0, 1, 2, 3; n'</math> ungerade),
so ist:
<math display="block">r(n) = 2^{\beta} + 8\alpha.</math>
1) Göttinger Nachrichten, 1898, S. 309.

## PDF page 2

J. Radon.
2
Dieses Resultat steht im Einklang mit der HURWITZschen Ab-
schätzung.
Den Hinweis auf die Abhandlung von HURWITZ verdanke ich Herrn
A. OSTROWSKI.
I. Vorbereitender Teil.
1. Bezeichnungsweise. Ich bediene mich im folgenden des bekannten
Matrizenkalküls und will die gebrauchten Bezeichnungen in aller Kürze
erläutern.
Mit großen (lateinischen oder griechischen) Lettern bezeichne ich
Matrizen (rechteckige Systeme von m Zeilen und n Spalten) allgemeiner
Natur. Unter <math>E_{\rho}</math> ist die quadratische „Einheitsmatrix“ von <math>\varrho</math> Zeilen und
Spalten vorhanden, deren in der Hauptdiagonale befindliche Elemente
alle eins sind, während die übrigen den Wert 0 besitzen. Mit A bezeichne
ich eine quadratische Matrix, deren Elemente außerhalb der Haupt-
diagonale Null sind; die Elemente der letzteren sollen in der natürlichen
Reihenfolge mit <math>\lambda_1 \lambda_2 \dots</math> bezeichnet sein. O bedeutet eine Matrix, deren
Elemente sämtlich Null sind.
Mit kleinen lateinischen Lettern (z. B. x) bezeichne ich eine einspaltige
Matrix, deren Elemente von oben nach unten gelesen, <math>x_1, x_2, \ldots</math> sind.
Die durch Vertauschung von Zeilen und Spalten aus einer Matrix A
entstehende transponierte Matrix soll mit A' bezeichnet werden.
Aus
einer einspaltigen Matrix <math>x</math> geht dadurch die einzeilige Matrix <math>x'</math> hervor.
Durch einen oberhalb des Symbols einer Matrix angebrachten Quer-
strich ist stets die Ersetzung aller ihrer Elemente durch die konjugiert
komplexen Zahlen (bzw. konjugierten Quaternionen) angedeutet.
Für die Multiplikation der Matrizen dient die übliche Bezeichnung;
es bedeutet also AB die Matrix der Elemente
<math display="block">c_{ik} = \sum_{i}^{p} h \ a_{ih} b_{hk},</math>
wenn A ebensoviel (p) Spalten wie B Zeilen besitzt. Es ist dann z.B.:
<math>Ax = y</math>
die symbolische Schreibung der linearen Gleichungen:
<math display="block">\sum_{i=1}^{n} h \ a_{ih} x_h = y_i,</math>
<math>x'Ay</math> ein kurzer Ausdruck für die Bilinearform <math>\sum a_{ik}x_iy_k</math>.

## PDF page 3

Lineare Scharen orthogonaler Matrizen.
3
Tritt zu einer Matrix eine Zahl als Faktor, der sämtliche Elemente
multipliziert, so soll diese Zahl stets mit einem kleinen griechischen
Buchstaben bezeichnet werden.
Durch Anschreiben der Symbole für <math>m \cdot n</math> Matrizen <math>A^{(i,k)}</math> <math>(i = 1, 2, ...m,</math>
<math>k = 1, 2, ... n</math>) mit <math>r_i</math> Zeilen und <math>s_k</math> Spalten in der Form:
<math>\|A^{(i,k)}\| = \left\| A^{(1,1)} \dots A^{(1,n)} \right\|_{A^{(m,1)} \dots A^{(m,n)}}</math>
soll jene Matrix von <math>r_1 + r_2 + \ldots + r_m</math> Zeilen und <math>s_1 + s_2 + \ldots + s_n</math> Spalten
bezeichnet werden, die aus diesem Symbol entsteht, wenn man die <math>A^{(i,k)}</math>
durch die ausgeschriebenen rechteckigen Systeme ersetzt.
Jede Matrix mit ebensoviel Zeilen und Spalten kann dann durch
„homologe“ Zerlegung in Teilsysteme in analoger Form geschrieben werden.
Die Multiplikation zweier solcher Matrizen mit den „Elementen“
<math>A^{(i,h)}</math> bzw. <math>B^{(h,h)}</math> läßt sich, sobald die Spaltenanzahl von <math>A^{(i,h)}</math> mit der
Zeilenanzahl von <math>B^{(h,k)}</math> für alle i und k übereinstimmt und die Anzahl der
Spaltengruppen von <math>\|A^{(i,h)}\|</math> mit jener der Zeilengruppen von <math>\|B^{(h,k)}\|</math>
identisch ist, formal wie ein gewöhnliches Matrizenprodukt aus den
Teilsystemen ausführen.
2. Quaternionen. Die vier Grundeinheiten der Quaternionen bezeichne
ich mit <math>(1, \epsilon_1, \epsilon_2, \epsilon_3)</math> und setze jede Quaternion in die Form
<math display="block">q = q_0 + \epsilon_1 q_1 + \epsilon_2 q_2 + \epsilon_8 q_8,</math>
so daß ihre reellen „Komponenten“ durch Indizes in der angegebenen
Weise gekennzeichnet werden. Die Multiplikationsregel der Matrizen-
rechnung überträgt sich unverändert auf Matrizen, deren Elemente
Quaternionen sind. Dagegen verliert die Regel <math>(AB)' = B'A'</math> wegen
der nicht kommutativen Multiplikation der Quaternionen ihre Gültigkeit.
Hingegen gilt stets:
<math>(\overline{A}\overline{B})' = \overline{B}'\overline{A}'.</math>
Ein System linearer Quaternionengleichungen der Form:
<math>Ax = y</math>
(A bedeutet eine quadratische Matrix) liefert durch Auflösung in die
reellen Komponenten gewöhnliche lineare Gleichungen für die x-Kom-
ponenten. Daraus geht hervor, daß auch hier die bekannte „Alternative“
gilt: entweder lassen sich die vorgelegten Gleichungen für beliebige
Werte der y — und dann eindeutig — lösen, oder das zugehörige
homogene System
<math>Ax = 0</math>
besitzt eine Auflösung, die nicht die triviale <math>x_i = 0</math> ist.

## PDF page 4

J. Radon.
4
Hat <math>A</math> eine „hintere Reziproke“ <math>B</math>, so daß <math>AB = E</math>, so sind die
vorgelegten linearen Gleichungen durch <math>x = By</math> gelöst; also liegt der
erste Fall der Alternative vor. Wird jetzt BA mit U bezeichnet, so gilt:
<math>AU = A \text{ oder } A(U-E) = 0.</math>
Wenn wir nun <math>U-E</math> in Spaltenmatrizen zerlegen:
<math display="block">U-E = \| x^{(1)} x^{(2)} \cdots x^{(n)} \|,</math>
so muß
<math>A x^{(i)} = 0</math>
بغز
Daraus folgt nach der obigen Alternative <math>x^{(i)} = 0</math>, d. h.
sein.
<math>BA = E</math>
so daß B auch „vordere Reziproke“ ist.
Es seien <math>\nu < n</math> Spaltenmatrizen von je n Elementen gegeben:
<math>x^{(1)}, x^{(2)}, \ldots x^{(\nu)}.</math>
welche die Relationen erfüllen:
<math>\overline{x^{(i)}}' x^{(i)} = 1</math>, <math>\overline{x^{(i)}}' x^{(k)} = 0</math> <math>(i \neq k)</math>.
Fügt man zu den <math>x^{(i)}</math> noch <math>n-\nu</math> weitere aus Nullen bestehende Spalten
und bezeichnet die entstehende quadratische Matrix <math>\parallel x^{(1)} \cdots x^{(\nu)} \ 0 \cdots 0 \parallel</math>
mit <math>U</math>, so ist das Gleichungssystem <math>Uz = 0</math> in nichttrivialer Weise lös-
bar; man kann folglich das System <math>Uz = y</math> nicht für beliebige <math>y</math> erfüllen.
Wählen wir jetzt eine Spaltenmatrix <math>y</math> so, daß <math>Uz=y</math> nicht lösbar
ist, und setzen:
<math display="block">x^{(\nu+1)} = y - x^{(1)} (\overline{x^{(1)}}' y) - x^{(2)} (\overline{x^{(2)}}' y) \dots - x^{(\nu)} (\overline{x^{(\nu)}}' y),</math>
so ist sicher <math>x^{(\nu+1)} \neq 0</math>, und es gilt:
<math>\overline{x^{(i)'}} x^{(\nu+1)} = 0, \ \overline{x^{(\nu+1)'}} x^{(i)} = 0 \ (i = 1, 2, \ldots \nu).</math>
Normieren wir <math>x^{(\nu+1)}</math> durch Hinzufügen eines skalaren Faktors so, daß
<math>\overline{x^{(\nu+1)}}</math>, <math>x^{(\nu+1)} = 1</math>, so haben wir zu den <math>x^{(1)} \dots x^{(\nu)}</math> noch eine Spalte <math>x^{(\nu+1)}</math>
unter Erhaltung der gestellten „Orthogonalitätsbedingungen“ hinzugefügt.
Durch Fortsetzung dieses Verfahrens erhalten wir eine Matrix
<math>X = ||x^{(1)}x^{(2)}\dots x^{(n)}||</math>
mit der Eigenschaft:
<math>\overline{X}'X = E</math>

## PDF page 5

Lineare Scharen orthogonaler Matrizen.
5
woraus nach dem früher Bewiesenen auch
<math>X\overline{X}' = E</math>
folgt.
3. Normalformen. Es wird mehrfach das Problem auftreten, eine
Matrix spezieller Natur in bestimmter Weise in eine Normalform über-
zuführen. Ich stelle hier die benötigten Sätze zusammen unter Hinzu-
fügung der Beweise, soweit letztere nicht bekannt sind.
a) Eine reelle symmetrische Matrix <math>S(S' = S)</math> läßt sich mit Hilfe
einer reellen orthogonalen Matrix <math>O(OO' = E)</math> in die Gestalt setzen:
<math>S = 0 A O'</math>
wo <math>\lambda_1 \lambda_2</math>.. (vgl. 1) reelle Zahlen sind.
Ist insbesondere <math>S^2 = E_n</math>, so kann <math>\mathcal{A}</math> in der Form:
<math display="block">A = \left\| \begin{smallmatrix} E_{\rho} & 0 \\ 0 & -E_{n-1} \end{smallmatrix} \right\|</math>
angenommen werden (Satz und Beweis bekannt).
b) Eine reelle schiefe Matrix <math>T(T'=-T)</math> von gerader Zeilen-
anzahl <math>n</math> läßt sich mit Hilfe einer reellen orthogonalen Matrix <math>O</math> in die
Gestalt setzen:
<math display="block">T = O \left\| \begin{array}{c} 0 & A \\ -A & 0 \end{array} \right\| O',</math>
wo <math>\lambda_1 \cdot \lambda_n</math> reelle Zahlen <math>\geqslant 0</math> sind. Ist insbesondere <math>T^2 = -E</math>, so kann
<math>A=E_{\frac{n}{2}}</math> angenommen werden. (Satz und Beweis bekannt.)
c) Eine komplexe symmetrische Matrix läßt sich mit Hilfe einer
komplexen Matrix O, für die <math>OO' = E</math>, in die Gestalt setzen:
<math>S = 0 A O'</math>
wo <math>\lambda_1, \lambda_2, \ldots</math> reelle Zahlen <math>\geqslant 0</math> sind. Ist insbesondere <math>S\overline{S} = E</math>, so ist
<math>A = E</math> zu setzen.
Zum Beweise suchen wir ein reelles <math>\lambda</math> und eine Spaltenmatrix <math>x^{(1)}</math>,
für welche:
<math>S\overline{x^{(1)}} = \lambda x^{(1)}, \quad \overline{x^{(1)}}'x^{(1)} = 1.</math>
Setzen wir <math>S = A + iB</math>, <math>x^{(1)} = u + iv</math>, so haben wir das Gleichungssystem:
<math>Au + Bv = \lambda u</math>
<math>Bu - Av = \lambda v</math>

## PDF page 6

J. Radon.
6
dessen Determinante
<math display="block">\begin{vmatrix} A - \lambda E, & B \\ B - A - \lambda E \end{vmatrix} = 0</math>
Wegen der Symmetrie von <math>S</math> ist dies eine gewöhnliche
sein muß.
Säkulargleichung mit lauter reellen Wurzeln, die paarweise nur durch
das Vorzeichen unterschieden sind. Wir denken für <math>\lambda</math> eine Wurzel <math>\geq 0</math>
gewählt und die zugehörige Lösung <math>x^{(1)}</math> so normiert, daß <math>\overline{x^{(1)}}'x^{(1)} = 1</math>.
Wir ergänzen jetzt die Spalte <math>x^{(1)}</math> durch Hinzufügen von <math>n-1</math>
weiteren Spalten <math>x^{(1)} \cdot x^{(n)}</math> zu einer Matrix <math>O'</math> mit <math>O'O = E</math>. Da dann
<math>\overline{O}'S\overline{O} = \|\overline{x^{(i)}}'S\overline{x^{(k)}}\|.</math>
so folgt, wie man leicht einsieht,
<math display="block">S = O \left\| \frac{\lambda 0}{0.8^*} \right\| O',</math>
wo <math>S^*</math> wieder symmetrisch ist. Es ist klar, wie man durch Fortsetzung
dieses Verfahrens das ausgesprochene Ergebnis erhält.
d) Eine komplexe schiefe Matrix <math>T</math> mit gerader Zeilenanzahl läßt sich
mittels einer komplexen Matrix O, für welche <math>O\overline{O}'=E</math>, in die Gestalt
bringen:
<math display="block">T = 0 \left\| \begin{array}{cc} -A & 0 \\ 0 & A \end{array} \right\| O',</math>
wo <math>\lambda_1 \lambda_2 ... \lambda_{\underline{n}}</math> reell und <math>\geqslant 0</math> sind. Ist insbesondere <math>T\overline{T} = -E</math>, so ist
<math>A = E_{\underline{n}}</math> zu setzen.
Der Beweis verläuft analog wie unter c); wir setzen hier die
Gleichungen an:
<math>T\overline{x^{(1)}} = -\lambda x^{(2)}</math>
<math display="block">T\overline{x^{(2)}} = \lambda x^{(1)}.</math>
Trennt man wieder Reelles und Imaginäres, so erkennt man, daß
für <math>\lambda</math> eine gewöhnliche Säkulargleichung herauskommt, deren Wurzeln
paarweise entgegengesetzt gleich sind. Nehmen wir eine solche Wurzel <math>\ge 0</math>,
und normieren das zugehörige <math>x^{(1)}</math> durch
<math>\overline{x^{(1)}}' x^{(1)} = 1</math>,
so folgt:
<math>\overline{x^{(2)'}}T\overline{x^{(1)}} = -\lambda \overline{x^{(2)'}}x^{(2)} = -\overline{x^{(1)'}}T\overline{x^{(2)}} = -\lambda \overline{x^{(1)'}}x^{(1)}.</math>
Für <math>\lambda \neq 0</math> folgt daraus auch
<math>\overline{x^{(2)}}'x^{(2)} = 1,</math>
für <math>\lambda = 0</math> kann <math>x^{(2)}</math> unabhängig von <math>x^{(1)}</math> so normiert werden.

## PDF page 7

Lineare Scharen orthogonaler Matrizen.
7
Außerdem ist wegen der schiefen Symmetrie:
<math>\overline{x^{(1)}}' \ T \overline{x^{(1)}} = -\lambda \overline{x^{(1)}}' \ x^{(2)} = 0.</math>
also folgt für <math>\lambda \neq 0</math>: <math>\overline{x^{(1)}} x^{(2)} = 0</math>; dies kann aber auch für <math>\lambda = 0</math>
erreicht werden. Denn die Matrix <math>T</math> hat geraden Rang, und <math>T\overline{x}=0</math>
besitzt dann sicher zwei linear unabhängige Lösungen.
Ergänzt man die beiden Spalten <math>x^{(1)}x^{(2)}</math> zu einer Matrix O' mit
<math>O'\overline{O} = E</math>, so wird, ähnlich wie unter c):
<math display="block">T = O \left\| \begin{array}{cc} R & 0 \\ 0 & T^* \end{array} \right\| O',</math>
wo <math>R = \begin{pmatrix} 0 & \lambda \\ -\lambda & 0 \end{pmatrix}</math> und <math>T^*</math> wieder schief ist. Fortsetzung dieses Pro-
zesses und eine schließliche Umstellung der Zeilen und Kolonnen führt
zu dem ausgesprochenen Ergebnis.
e) Eine Quaternionenmatrix <math>S</math> mit <math>\overline{S}' = S</math> läßt sich mit Hilfe einer
Quaternionenmatrix <math>O</math>, für welche <math>O\overline{O}' = E</math>, in die Form bringen:
<math>S = 0 A \bar{0}'</math>
wo <math>\lambda_1 \lambda_2 ... \lambda_n</math> skalar sind. Ist insbesondere <math>S^2 = E</math>, so kann
<math>A = \begin{bmatrix} E_{\rho} & 0 \\ 0 & -E_{n-\rho} \end{bmatrix}</math>
gesetzt werden.
Beweis: Wir setzen mit einem reellen <math>\lambda</math> die Gleichungen an:
<math>Sx^{(1)} = \lambda x^{(2)}</math>
und zerspalten in die vier reellen Komponenten. Für λ ergibt sich wieder
eine gewöhnliche Säkulargleichung.
Nehmen wir eine Wurzel derselben und normieren das zugehörige
Lösungssystem <math>x^{(1)}</math> durch <math>\overline{x^{(1)}}'x^{(1)} = 1</math>, bestimmen ferner nach 2. <math>n-1</math>
weitere Spalten <math>x^{(2)} 	cdots x^{(n)}</math>, so daß die Matrix <math>X = \|x^{(1)} 	cdots x^{(2)}\|</math> der
Bedingung <math>\overline{X}'X = E</math> genügt, so wird:
<math>\overline{X}'SX = \|\overline{x^{(i)}}'Sx^{(k)}\| = \|\frac{\lambda}{0} - \frac{0}{S^*}\|,</math>
wo wieder <math>\overline{S^*}'=S^*</math>. Fortsetzung des Verfahrens führt zu der zu
beweisenden Aussage.
f) Eine Quaternionenmatrix <math>T</math>, für welche <math>T+\overline{T}'=0</math>, läßt sich
mit Hilfe einer Matrix <math>O(O\overline{O}' = E)</math> in die Gestalt setzen:
<math>T = 0 \Lambda \overline{0}'</math>

## PDF page 8

J. Radon.
8
wo <math>\lambda_1, \lambda_2, \ldots</math> vektorielle Quaternionen sind, deren Richtungen im übrigen
beliebig vorgeschrieben werden können. Ist insbesondere <math>T^2 = -E</math>,
so kann man <math>A = \epsilon_1 E</math> annehmen.
Beweis: Es werden die Gleichungen angesetzt (mit reellem <math>\lambda</math>):
<math>Tx^{(1)} = x^{(1)} \cdot \lambda_1 \epsilon_1</math>
Zerspaltung in die vier Komponenten gibt eine Säkulargleichung
für <math>\lambda</math>, also kann man durch ein reelles <math>\lambda</math> und eine Quaternionenspalte <math>x^{(1)}</math>
diese Gleichungen erfüllen. Setzt man <math>x^{(1)} = z^{(1)}\alpha</math>, wo <math>\alpha</math> eine beliebige
Quaternion, so wird:
<math>Tz^{(1)} = z^{(1)} \lambda \alpha \varepsilon_1 \alpha^{-1}</math>.
Man kann also nach einer bekannten Darstellung der Rotationen
statt der vektoriellen Quaternion <math>\lambda \epsilon_1</math> eine andere von demselben Betrage
und beliebig vorgeschriebener Richtung wählen.
Ergänzt man die Spalte <math>x^{(1)}</math> nach Normierung durch <math>\overline{x^{(1)}}'x^{(1)}=1</math>
wieder zu einer Matrix X mit <math>\overline{X}'X = E</math>, so folgt:
<math>\overline{X}'TX = \begin{vmatrix} \lambda \epsilon_1 & 0 \\ 0 & T^* \end{vmatrix}</math>, wo <math>\overline{T}^{*\prime} + T^* = 0</math>.
Durch Fortsetzung dieses Verfahrens erhält man das zu beweisende
Ergebnis.
II. Lösung des Problems.
1. Formulierung. Es sind reelle quadratische linear unabhängige
Matrizen von je <math>n^2</math> Elementen in möglichst großer Anzahl <math>\nu</math> zu bestimmen,
so daß
<math display="block">(\lambda_1 T_1 + \lambda_2 T_2 + \ldots + \lambda_\nu T_\nu) (\lambda_1 T_1' + \lambda_2 T_2' + \ldots + \lambda_\nu T_\nu') = \varrho (\lambda_1 \ldots \lambda_\nu) E.</math>
Offenbar ist <math>\varrho(\lambda_1 ... \lambda_{\nu})</math> eine quadratische Form der <math>\lambda</math> und stets <math>\geq 0</math>. Durch
Vornahme einer linearen Transformation der <math>\lambda</math> kann man also <math>\varrho(\lambda_1...\lambda_{\nu})</math>
<math>=\lambda_1^2+\ldots+\lambda_\mu^2, \, \mu \leq \nu</math> annehmen. Da für <math>\mu < \nu</math> dann sofort <math>T_{\mu+1}=\ldots=</math>
<math>=T_{\nu}=0</math> folgt, was der vorausgesetzten linearen Unabhängigkeit der <math>T</math>
widerspricht, so können wir die Frage (der HURWITZschen Problem-
stellung entsprechend) so formulieren:
Es sollen reelle Matrizen Ti von je nº Elementen in möglichst
großer Anzahl v so bestimmt werden, daß:
<math>T_i T'_i = E_n, T_i T'_k + T_k T'_i = 0 (i \neq k)</math>
<b>(1)</b>
<math>(i, k = 1, 2, ... \nu).</math>

## PDF page 9

Lineare Scharen orthogonaler Matrizen.
9
2. Erste Reduktion. Das gesuchte System läßt sich in sofort ver-
ständlicher Weise so schreiben:
<math>(T_1, T_2, \ldots T_{\nu}) = T_{\nu} (A_1 A_2 \ldots A_{\nu-1} E_n),</math>
und für die Matrizen <math>A_i (= T'_i T_i)</math>, <math>E_n</math> bleiben die Relationen (1) aufrecht.
Sie lauten nun:
<math>A_i + A'_i = 0</math>, <math>A_i^2 = -E_n</math>, <math>A_i A_k + A_k A_i = 0</math>
(2)
<math>(i, k = 1, 2 \dots \nu - 1).</math>
Offenbar erhält man zu jedem System <math>(A_1 
ldots A_{i-1})</math>, das den Relationen (2)
genügt, unter Hinzuziehung einer beliebigen Orthogonalmatrix <math>T_{\nu}</math> wieder
ein T-System der gewünschten Art. Es ist also nunmehr ein System
<math>(A_1 ... A_{\nu-1})</math> mit möglichst vielen Elementen zu finden, welche die
Relationen (2) erfüllen.
Ist n ungerade, so gibt es keine <math>A_i</math>; denn nach (2) müßte <math>|A_i|^2 = 1</math>
sein, während <math>A_i</math> schief ist, was einen Widerspruch bedeutet.
Ist also n ungerade, so ist <math>\nu(n) = 1^{1}</math>.
3. Zweite Reduktion. Wenn n gerade ist, so können wir nach I, 3b)
<math>A_{\nu-1} = 0 A_{\nu-1}^{\bullet} 0'</math>
setzen, wo O eine reelle Orthogonalmatrix und
<math display="block">A_{\nu-1}^{\bullet} = \left\| \begin{array}{c} 0 & E_n \\ -E_n, & 0 \end{array} \right\|</math>
Es kann also das A-System geschrieben werden:
ist.
<math>(A_1 ... A_{\nu-1}) = O(A_1^* ... A_{\nu-1}^*)O'.</math>
Für die <math>A^*</math> gelten die Beziehungen (2) unverändert weiter.
Spaltet man die ersten <math>(\nu-2)A^*</math> homolog zu <math>A_{\nu-1}^*</math> in Teilsysteme:
<math>A_{i}^{*} = \left\| \begin{array}{c} R_{i} & S_{i} \\ -S_{i}' & W_{i} \end{array} \right\| (i = 1, 2, ... - 2, R_{i}, W_{i} \text{ schief}),</math>
so ergeben die Beziehungen (2) zunächst aus <math>A_i^* A_{\nu-1}^* + A_{\nu-1}^* A_i^* = 0</math>,
daß <math>W_i = -R_i</math> und <math>S_i</math> schief ist. Also wird:
<math>A_{i}^{\bullet} = \begin{pmatrix} R_{i} & S_{i} \\ S_{i} - R_{i} \end{pmatrix} (R_{i}, S_{i} \text{ schief, } i = 1, 2, ... \nu - 2).</math>
1) Dieser erste Schritt der Reduktion findet sich ebenso bei HURWITZ.

## PDF page 10

J. Radon.
10
Fassen wir <math>R_i</math> und <math>S_i</math> zu einer schiefen komplexen Matrix zusammen:
<math>R_i + iS_i = B_i \ (i = 1, 2, ..., \nu - 2)</math>
so berechnet man leicht:
<math display="block">A_i^* A_k^* = \left\| \frac{\Re(B_i B_k) - \Im(B_i B_k)}{\Im(B_i \overline{B_k})} \right\|</math>
und die Relationen (2) gehen über in:
<math>B_i + B_i' = 0</math>, <math>B_i \overline{B_i} = -E_{\underline{n}}</math>, <math>B_i \overline{B_k} + B_k \overline{B_i} = 0</math>
(3)
<math>(i, k = 1, 2, \dots \nu - 2).</math>
Ist nun <math>\frac{n}{2}</math> ungerade, so gibt es wieder keine <math>B</math>, da diese zugleich
schief sein und eine von Null verschiedene Determinante haben müssen.
Also folgt:
Ist <math>\frac{n}{2}</math> ungerade, so ist <math>v(n) = 2</math>.
4. Dritte Reduktion. Ist <math>\frac{n}{2}</math> gerade, so kann nach I, 3d)
<math>B_{u-2} = OB_{u-2}^{\bullet}O'</math>
gesetzt werden, wo
<math>O\overline{O}' = E, \ B_{\nu-2}^* = \begin{bmatrix} 0 & E_n \\ -E_n & 0 \end{bmatrix}</math>
Man erhält so das System <math>(B_1 
ldots B_{\nu+2})</math> in der Form:
<math>(B_1 ... B_{\nu-2}) = O(B_1^* ... B_{\nu-2}^*) O'</math>
und die B* genügen wieder den Relationen (3).
Die <math>B_i^*</math> <math>(i = 1, 2, \dots \nu - 3)</math> zerspalten wir homolog zu <math>B_{\nu-2}^*</math> und
erhalten dann aus <math>B_i^* \overline{B_{\nu-2}^*} + B_{\nu-2}^* \overline{B_i^*} = 0</math>:
<math display="block">B_{i}^{*} = \left\| \frac{P_{i}}{\bar{Q}_{i}} - \frac{Q_{i}}{\bar{P}_{i}} \right\| \quad (P_{i} + P'_{i} = 0, \ Q_{i} + Q'_{i} = 0).</math>
Zerlegen wir noch <math>P_i</math>, <math>Q_i</math> in Real- und Imaginärteil, indem wir
<math>P_{i} = -T_{i}^{(1)} - i T_{i}^{(2)}, \ Q_{i} = -T_{i}^{(8)} + i S_{i}</math>
setzen (<math>S_i</math> symmetrisch, die <math>T_i</math> schief), so ergibt sich:
<math display="block">B_i^{\bullet} \, \overline{B_k^{\bullet}} = \left\| \frac{A}{-\overline{C}} \, \frac{C}{A} \, \right\|,</math>

## PDF page 11

Lineare Scharen orthogonaler Matrizen.
11
wo:
<math display="block">A = -S_i S_i + T_i^{(1)} T_i^{(1)} + T_i^{(2)} T_i^{(2)} + T_i^{(3)} T_i^{(3)} +</math>
<math>+i(-S_i T_k^{(8)} - T_i^{(8)} S_k - T_i^{(1)} T_k^{(2)} + T_i^{(2)} T_k^{(1)})</math>
<math display="block">C = -S_i T_k^{(2)} - T_i^{(2)} S_k - T_i^{(8)} T_k^{(1)} + T_i^{(1)} T_k^{(8)} +</math>
<math>+i(S_iT_k^{(1)}+T_i^{(1)}S_k+T_i^{(2)}T_k^{(3)}-T_i^{(8)}T_k^{(2)}).</math>
Führen wir nun die Quaternionenmatrizen ein:
<math>C_i = S_i + \epsilon_1 T_i^{(1)} + \epsilon_2 T_i^{(2)} + \epsilon_2 T_i^{(3)} \quad (C_i = C_i), \quad i = 1, 2, \dots \nu - 3),</math>
so schreibt sich dies einfach so:
<math display="block">B_{i}^{\bullet} B_{k}^{\bullet} = \left\| \frac{-(C_{i}C_{k})_{0} - i(C_{i}C_{k})_{3}, \quad -(C_{i}C_{k})_{2} + i(C_{i}C_{k})_{1}}{(C_{i}C_{k})_{2} + i(C_{i}C_{k})_{1}, \quad -(C_{i}C_{k})_{0} + i(C_{i}C_{k})_{3}} \right\|,</math>
und die Beziehungen (3) gehen in die gleichwertigen über:
<math>C_{i} = \overline{C}'_{i}, C_{i}^{2} = E_{\underline{n}}, C_{i}C_{k} + C_{k}C_{i} = 0</math>
(4)
<math>(i, k = 1, 2, \dots \nu - 3)</math>
5. Vierte Reduktion. Nach I, 3c) läßt sich <math>C_{\nu-3}</math> in die Form bringen:
<math>C_{u-2} = OC_{u-2}^*O'</math>
<math>\mathbf{w}</math>o
<math display="block">O\overline{O}' = E_{\underline{n}}, C_{\nu-3}^* = \left\| \begin{array}{c} E_{\rho} & 0 \\ 0 & -E_{\underline{n}-\rho} \end{array} \right\|</math>
Setzen wir also das System der <math>C</math> so an:
<math>(C_1, C_2, \ldots C_{\nu-3}) = O(C_1^* C_2^* \ldots C_{\nu-3}^*) O',</math>
so erfüllen die <math>C_i^*</math> ebenfalls die Relationen (4). Zerlegen wir die ersten
<math>(\nu-4)</math> <math>C_i^*</math> homolog zu <math>C_{\nu-8}^*</math>, so ergibt sich aus <math>C_i^*=\overline{C_i^{\bullet}}'</math> und <math>C_i^*</math> <math>C_{\nu-8}^*+</math>
<math>+ C_{\nu-3}^* C_i^* = 0</math>:
<math>C_i^* = \left\| \begin{array}{cc} 0 & B_i \\ \overline{B}_i' & 0 \end{array} \right\| (i = 1, 2, ... \nu - 4).</math>
<math>C_i^{\bullet 2} = E</math> liefert dann: <math>B_i \overline{B}_i' = E_\rho, \ \overline{B}_i' B_i = E_{n-\rho}.</math>
Daraus folgt, daß die linearen Gleichungen
<math>B_i x = y</math>
für beliebige Wahl der <math>y</math> durch <math>x = B'_i y</math> lösbar sind. Nach Zerspaltung
in reelle Komponenten hat man <math>4 \varrho</math> lineare Gleichungen für <math>n-4 \varrho</math>

## PDF page 12

J. Radon.
12
Unbekannte, die für beliebige Wahl der rechten Seiten lösbar sind. Das
ist nur für <math>n = 8 \rho</math> möglich. Wir schließen daraus:
Ist <math>\frac{n}{4}</math> ungerade, so ist <math>\nu(n) = 4</math>.
Ist dagegen <math>\frac{n}{4}</math> gerade, so können wir <math>\varrho = \frac{n}{8}</math> annehmen und die
<math>C_i^{\bullet}</math> zu bilden suchen. Wir schreiben sie jetzt so:
<math>C_i^* = \left\| \begin{array}{cc} 0 & D_i \\ \overline{D}_i' & 0 \end{array} \right\| (i = 1, 2, ... \nu - 4),</math>
und die (quadratischen) <math>D_i</math> erfüllen nunmehr die Beziehungen:
<math display="block">D_i \overline{D}_i' = E_{\underline{n}}, \ D_i \overline{D}_k' + D_k \overline{D}_i' = 0,</math>
(5)
(Die ebenfalls geltenden Relationen
<math display="block">\bar{D}_i'D_i = E_n, \ \bar{D}_i'D_k + \bar{D}_k'D_i = 0</math>
folgen aus (5), wie man mit Hilfe des unter I, 2 über die Reziproke
einer Quaternionenmatrix hergeleiteten Ergebnisses leicht einsieht.)
Die Bestimmung der <math>D_i</math> ist, wie man bemerkt, eine Verallgemeinerung
des in 1. für die <math>T_i</math> formulierten „Grundproblemes“. Auch sie läßt sich
vollständig aus dem hier gegebenen Reduktionsverfahren herleiten.
6. Fünfte Reduktion. Wir schreiben das System der <math>D_i</math> so:
<math>(D_1 ... D_{\nu-4}) = D_{\nu-4} (F_1 ... F_{\nu-5}, E)</math>
und erhalten für die <math>F_i</math> die Relationen:
<math>F_i + \overline{F}_i' = 0, \ F_i^a = -E_n, \ F_i F_k + F_k F_i = 0 \ (i, k = 1, 2, ... \nu - 5).</math>
<b>(6)</b>
7. Sechste Reduktion. Nach I, 3 f) können wir setzen:
<math display="block">F_{\nu-5} = OF_{\nu-5}^* \bar{O}',</math>
W0
<math>O\overline{O}' = E, F_{\nu-5}^{\bullet} = \epsilon_1 E_{\underline{n}},</math>
und schreiben dann das F-System so:
<math display="block">(F_1F_2..F_{\nu-5}) = O(F_1^*F_2^*..F_{\nu-5}^*)\overline{O}'.</math>
Zwischen den <math>F_i^{\bullet}</math> bestehen dann die Relationen (6) fort.

## PDF page 13

Lineare Scharen orthogonaler Matrizen.
13
Aus <math>F_i^* F_{\nu-5}^* + F_{\nu-5}^* F_i^* = 0</math> und <math>F_i^* + \overline{F_i^*}' = 0</math> folgt nun zunächst:
<math display="block">F_i^* = \epsilon_2 S_i^{(1)} + \epsilon_2 S_i^{(2)},</math>
wo <math>S_i^{(1)}, S_i^{(2)}</math> reell symmetrisch sind.
Setzen wir nun:
<math>S_i^{(1)} + iS_i^{(2)} = G_i \quad (i = 1, 2, ... \nu - b),</math>
so sind die <math>G_i</math> symmetrische komplexe Matrizen und es wird:
<math>F_i^* F_k^* = -S_i^{(1)} S_k^{(1)} - S_i^{(2)} S_k^{(2)} + \epsilon_1 (S_i^{(1)} S_k^{(2)} - S_i^{(2)} S_k^{(1)})</math>
<math>=-\Re(G_iG_k)-\epsilon_1\Im(G_i\overline{G}_k)</math>
Für die <math>G_i</math> folgen daraus die zu (6) äquivalenten Beziehungen:
<math>G_i' = G_i</math>, <math>G_iG_i = E_{\underline{n}}</math>, <math>G_iG_k + G_k\overline{G}_i = 0</math>
<b>(7)</b>
<math>(i, k = 1, 2, \dots \nu - 6).</math>
8. Siebente Reduktion. Nach I, 3c) setzen wir:
<math>G_{\nu-6} = OG_{\nu-6}^{\bullet}O'</math>
<math>\mathbf{w}_0</math>:
<math>OO' = E_{\underline{n}}, \ G_{\nu-6}^* = E_{\underline{n}}.</math>
Schreiben wir entsprechend das G-System so:
<math>(G_1 G_2, \ldots G_{n-6}) = O(G_1^* G_2^* \ldots G_{n-6}^*) O',</math>
so bestehen für die <math>G_i^*</math> die Relationen (7) fort. Aus <math>G_i^* \overline{G_{\nu-6}^*} + G_{\nu-6}^* \overline{G_i^*} = 0</math>
und <math>G'_i = G_i</math> folgt nun:
<math>G_i^* = i H_i</math>
Die Relationen (7) lassen sich
wo <math>H_1 
ldots H_{\nu-7}</math> reell symmetrisch sind.
dann in die gleichwertigen umsetzen:
<math>H'_{i} = H_{i}, \ H^{2}_{i} = E_{\frac{n}{8}}, \ H_{i}H_{k} + H_{k}H_{i} = 0</math>
(8)
<math>(i, k = 1, 2, \dots \nu - 7).</math>
Nach I, 3a) kann man setzen:
9. Achte Reduktion.
<math>H_{\nu-7} = OH_{\nu-7}^*O'</math>
mit
<math>OO' = E, H_{\nu-7}^* = \begin{bmatrix} E_{\rho} & 0 \\ 0 - E_{\frac{n}{\rho} - \rho} \end{bmatrix}.</math>

## PDF page 14

J. Radon.
14
Schreiben wir dementsprechend:
<math>(H_1 H_2 ... H_{\nu-\tau}) = O(H_1^* H_2^* ... H_{\nu-\tau}^*) O',</math>
so gelten für die H* die Relationen (8) unverändert weiter. Zerspalten
wir die ersten <math>(\nu - 8)H^*</math> homolog zu <math>H_{\nu-7}^*</math>, so ergibt <math>H_i^*H_{\nu-7}^* +</math>
<math>+H_{\nu-7}^{\bullet}H_i^{\bullet}=0</math> und <math>H_i^{\bullet\prime}=H_i^{\bullet}</math> zunächst:
<math>H_i^{\bullet} = \left\| \begin{array}{cc} 0 & T_i \\ T_i^{\prime} & 0 \end{array} \right\| \quad (i = 1, 2, \ldots \nu - 8).</math>
Wegen <math>H_{i}^{*2}=E_{\underline{n}\atop \underline{n}}</math> darf die Determinante <math>|H_{i}^{*}|</math> nicht verschwinden;
dies ist offenbar nur für <math>\varrho = \frac{n}{8} - \varrho</math> möglich. Also erhalten wir zuerst:
Ist <math>\frac{n}{Q}</math> ungerade, so ist <math>\nu(n) = 8</math>.
Ist aber <math>\frac{n}{8}</math> gerade, so können wir <math>\varrho = \frac{n}{16}</math> annehmen und nach
geeigneten <math>T_i</math> fragen. Für diese ergeben sich aber nach (8) die
Bedingungen:
<math display="block">T_i T_i' = E_{\underline{n}}, \ T_i T_k' + T_k T_i' = 0</math>
(9)
<math>(i, k = 1, 2, \dots \nu - 8),</math>
Diese Bedingungen sind aber mit den Bedingungen (1), von denen
wir ausgingen, völlig identisch.
Daher folgt:
<math display="block">\nu(n) = \nu\left(\frac{n}{16}\right) + 8.</math>
Dies ergibt aber in Verbindung mit den im Verlaufe der Reduktion
erhaltenen Aussagen über die Fälle, wo <math>\frac{n}{2^a}</math> (<math>\alpha = 0, 1, 2, 3</math>) ungerade
ist, das am Schlusse der Einleitung formulierte Ergebnis.
Offenbar
gestattet unser Verfahren für jedes n jede mögliche lineare Schar ortho-
gonaler Matrizen zu gewinnen, doch ist eine Übersicht über die Gesamtheit
der möglichen Scharen so kaum zu erhalten.
Hamburg, 29. Mai 1921.
