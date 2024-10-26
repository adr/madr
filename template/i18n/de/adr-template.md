---
lang: de_DE
<!-- Die folgenden Felder sind optionale Metadaten. Sie können einfach entfernt werden. -->
status: "{vorgeschlagen | abgelehnt | akzeptiert | überholt | … | ersetzt durch ADR-0123"
datum: {YYYY-MM-DD Datum, an dem die Entscheidung zuletzt verändert wurde}
entscheidende: {Zählt alle an der Entscheidung beteiligten Personen auf}
beratende: {Zählt alle Personen auf, die nach ihrer Meinung gefragt wurden (typischerweise Spezialisten); Feedback gebende Personen sollten hier gelistet werden}
informierte: {Zählt alle Personen auf, die über den Fortschritt informiert werden; Personen, die informiert wurden, aber kein Feedback gaben, sollten hier gelistet werden.}
---

# {Kurzer Titel, der das gelöste Problem und die gefundene Lösung beschreibt}

## Kontext und Problemstellung

{Beschreibt den Kontext und die Problemstellung, z.B. in zwei bis drei Sätzen freiem Text oder in der Form einer Geschichte, die das Problem veranschaulicht. Eine gute Form, das Problem auszudrücken, ist auch eine Frage. Ggf. noch Links zu Boards oder Ticketing System.}

<!-- Dieses Element ist optional. Wenn nicht benötigt, bitte entfernen. -->
## Entscheidungsfaktoren

* {Entscheidungsfaktor 1, z.B. ein Einfluss, ein Bedenken, …}
* {Entscheidungsfaktor 2, z.B. ein Einfluss, ein Bedenken, …}
* <!-- Anzahl der Faktoren kann variieren -->

## Betrachtete Optionen

* {Titel der Optionen 1}
* {Titel der Optionen 2}
* {Titel der Optionen 3}
* … <!-- Anzahl der Optionen kann variieren -->

## Entscheidung

Gewählte Option: "{Titel der Optionen 1}", denn {Begründung, z.B. die einzige Option, die kein Ausschlusskriterium beinhaltet |  … | am besten abschneidet (siehe unten)}.

<!-- Dieses Element ist optional. Wenn nicht benötigt, bitte entfernen. -->
### Konsequenzen

* Gut, weil {positive Konsequenz, z.B. Verbesserung einer oder mehrerer gewünschter Eigenschaften, …}
* Schlecht, weil {negative Konsequenz, z.B. Einschränkung einer oder mehrerer gewünschter Eigenschaften, …}
* … <!-- Anzahl der Konsequenzen kann variieren -->

<!-- Dieses Element ist optional. Wenn nicht benötigt, bitte entfernen. -->
### Prüfung

{Beschreibt, wie die Implementierung/Einhaltung geprüft werden kann/wird.
Entspricht das gewählte Design und seine Implementierung der Entscheidung? Z.B. kann eine Design-/Code-Review oder ein Test mit einer Bibliothek wie ArchUnit dabei helfen, dies zu prüfen. Beachtet, dass wir dieses Element zwar als optional einstufen, es aber in vielen ADRs enthalten ist.}

<!-- Dieses Element ist optional. Wenn nicht benötigt, bitte entfernen. -->
## Vor- und Nachteile der Optionen

### {Titel der Option 1}

<!-- Dieses Element ist optional. Wenn nicht benötigt, bitte entfernen. -->
{Beispiel | Beschreibung | Verweis auf weitere Informationen | …}

* Gut, weil {Argument a}
* Gut, weil {Argument b}
* <!-- Verwendet "Neutral" falls ein Argument weder für noch gegen eine Lösung spricht -->
* Neutral, weil {Argument c}
* Schlecht, weil {Argument d}
* … <!-- Anzahl der Argumente kann variieren.-->

### {Titel einer anderen Option}

{Beispiel | Beschreibung | Verweis auf weitere Informationen | …}

* Gut, weil {Argument a}
* Gut, weil {Argument b}
* Neutral, weil {Argument c}
* Schlecht, weil {Argument d}
* …

<!-- Dieses Element ist optional. Wenn nicht benötigt, bitte entfernen. -->
## Weitere Informationen

{Hier können zusätzliche Hinweise/oder die Zuversichtlichkeit bzgl. des Entscheidungsergebnisses angeführt und/oder die Zustimmung des Teams zur Entscheidung dokumentiert und/oder festlegt werden, wann/wie diese Entscheidung umgesetzt werden soll und ob/wann die Entscheidung erneut überprüft werden sollte. Links zu anderen Entscheidungen und Ressourcen können hier ebenfalls erscheinen.}
