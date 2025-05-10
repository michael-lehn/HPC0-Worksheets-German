# HPC0 Arbeitsblätter – Deutsche Version

Dies ist die deutsche Version der Arbeitsblätter zur Veranstaltung
**Introduction to High Performance Computing** – so heißt die Veranstaltung
ganz offiziell.  
Ehrlicher wäre: **HPC 0 – Programmieren ohne Schnickschnack**.  
Denn hier lernt ihr, wie man seinen eigenen Computer baut – und einen
Compiler dafür schreibt.


## Organisation der Vorlesung

Die Vorlesung folgt dem **Flipped-Classroom-Konzept**:  
Zu Hause schaut ihr **Lernvideos** an – und zwar vollständig und **mit
Nachmachen aller gezeigten Beispiele**, egal wie trivial sie wirken. In den
Präsenzphasen bearbeiten wir dann gemeinsam die Arbeitsblätter und vertiefen
das Verständnis.

Die Struktur ist in drei Phasen gegliedert:

1. **Sessions 1–10:** Es wechseln sich **Top-Down**- und
   **Bottom-Up**-Einheiten ab:
   - In **Top-Down-Sessions** arbeiten wir mit einem existierenden Computer und
     Compiler und entdecken durch gezielte Experimente immer mehr Details.
   - In **Bottom-Up-Sessions** bauen wir ausgehend von Logikgattern Stück für
     Stück unsere eigene Hardware – Addierer, Register, Flipflops – bis hin zum
     eigenen Rechner.

2. **Ab Session 11:**  
   In dieser Phase habt ihr eine klare Vorstellung davon, wie ein Computer
   aufgebaut ist und wie ein Compiler funktioniert. Wir entwickeln nun **unsere
   eigene Hardware und unseren eigenen Compiler weiter**.  
   Die Trennung zwischen Top-Down und Bottom-Up wird weniger strikt – je nach
   Thema gibt es eher **High-Level-Sessions** (z. B. zu Datenstrukturen) oder
   **Low-Level-Sessions** (z. B. zu Funktionsaufrufen auf Hard- und
   Softwareebene).

👉 Vorlesungskonzept und Inhalte im Überblick:  
- [Video auf Deutsch](https://youtu.be/9TEyFQLgfUw)  
- [Video auf Englisch](https://youtu.be/JOkwqfFm4GY)



## Sessions

1. [Erste Schritte mit der Programmiersprache ABC (Top-Down)](session01/README.md)  
   Einführung in Variablen, Kontrollstrukturen und erste Experimente mit Assemblercode.

   👉 Am Ende des Arbeitsblatts schreibt ihr einen einfachen **Lexer** – und im
   Ausblick einen kleinen **Parser**,  der arithmetische Ausdrücke wie
   `2*(4+5)` in Assembler übersetzt. Das ist bereits ein funktionierender
   **Compiler**,  auch wenn man anfangs kaum glauben würde, wie einfach das
   geht.

2. [Erste Schritte mit Logik-Gattern (Bottom-Up)](session02/README.md)  
   Grundbegriffe der digitalen Logik, Darstellung von Ganzzahlen und einfache Schaltungen mit Gattern.

3. [Funktionsaufrufe verstehen (Top-Down)](session03/README.md)  
   Wir bleiben in ABC, führen aber gezielt Experimente durch, um zu verstehen,
   was bei einem **Funktionsaufruf im Hintergrund passieren muss**.  
   Dabei gewinnen wir erste Einsichten in das Konzept des **Stacks** – ein
   zentrales Bauelement für spätere eigene Rechner und Compiler.

4. [Subtraktion und Zweierkomplement (Bottom-Up)](session04/README.md)  
   Aufbau komplexerer Schaltungen: Subtraktion, Multiplexer und Darstellung negativer Zahlen.

5. [Kontrollstrukturen und Arrays in ABC (Top-Down)](session05/README.md)  
   Programmierung mit Gotos, bedingten Sprüngen, Arrays und einfachem Stack.

6. [Speichernde Logik: D-Latches und Flipflops (Bottom-Up)](session06/README.md)  
   Einführung in speichernde Schaltungen und sequenzielle Logik.

---

Die zugehörigen Webseiten mit Videos und Aufgaben findest du hier:  
👉 https://www.mathematik.uni-ulm.de/numerik/hpc/ss25/hpc0/

## Verwendete Werkzeuge

In der Vorlesung kommen verschiedene Werkzeuge zum Einsatz, mit denen ihr
sowohl **Software als auch Hardware selbst entwickelt**:

- [**abc-llvm** – Compiler für die Sprache ABC](https://github.com/michael-lehn/abc-llvm)  
  Mit der Programmiersprache **ABC** schreiben wir alle Beispiele und
  Arbeitsblattlösungen – und später sogar unseren **eigenen Compiler**.  
  Die Sprache wurde speziell für diese Veranstaltung von mir entwickelt, um
  typische Einstiegshürden beim Lernen von C zu vermeiden,  ohne auf Nähe zur
  realen Hardware zu verzichten.

- [**CircuitVerse** – digitale Schaltungen im Browser](https://circuitverse.org)  
  Damit entwerfen wir Logikschaltungen direkt im Webbrowser: von einfachen
  Gattern über Addierer bis hin zu einer eigenen ALU mit Registern.  
  Ideal für den visuellen Einstieg in die digitale Logik.

- [**ulm-generator** – Komponenten-Layout für den Gesamtcomputer](https://github.com/michael-lehn/ulm-generator)  
  Sobald einzelne Bausteine klar sind, wird es in CircuitVerse schnell
  unübersichtlich.  
  Mit dem ULM-Generator beschreiben wir unsere Rechnerarchitektur **textuell**
  –  damit lassen sich auch größere Systeme strukturiert und wiederverwendbar
  zusammenbauen.

- [**ulm-on-ice** – Umsetzung der ULM in SystemVerilog](https://github.com/michael-lehn/ulm-on-ice)  
  Für alle, die tiefer einsteigen wollen: Hier wird die **ULM (Ulm Lecture
  Machine)** in  
  [SystemVerilog](https://en.wikipedia.org/wiki/SystemVerilog) beschrieben –  
  eine Hardwarebeschreibungssprache, mit der sich reale digitale Schaltungen
  definieren lassen.  Diese Version lässt sich auf einem **iCE40-FPGA** real
  ausführen – euer selbst gebauter Rechner in echter Hardware.




