# Stronghold Crusader KI‑Turnier 2025 – Offizielle Regeln & Setup

## Überblick

Dieses Turnier fordert Modder heraus, überzeugende KI‑Charaktere zu erschaffen, die in verschiedenen Szenarien gegeneinander antreten. Teilnehmende reichen **Teams aus zwei sich ergänzenden KIs** ein, die anschließend in Einzel‑Challenges sowie im Team‑Kampf bewertet werden. Ziel ist es, nicht nur effektive, sondern auch unterhaltsame KIs mit klaren Persönlichkeiten und Strategien zu kreieren, die innerhalb des durch das Turnier‑Plugin vorgegebenen Rahmens agieren.

---

## I. Setup & Startressourcen

* **Pflicht‑Plugin:** Alle Teilnehmenden müssen das offizielle **AI‑Tournament‑2025**‑Plugin installieren und verwenden, um ihre KIs zu erstellen. Dies garantiert identische Startbedingungen und stellt alle benötigten Dateien für KI‑Gegner bereit.
* **Standard‑Match‑Ressourcen (Phase 2 – FFA/2v2):** Sofern nichts anderes angegeben, gelten die im Plugin konfigurierten Bedingungen des **Normal Game**:
  * Gold: 2000  
  * Holz: 100  
  * Stein: 50  
  * Nahrung: 60 Brot
* **Hinweis:** Die Economic‑ und Defensive‑Gauntlets in Phase 1 nutzen **Deathmatch Game** bzw. **Crusader Game**‑Startbedingungen (siehe Abschnitt IV).

---

## II. Einreichungen der Teilnehmenden: KI‑Teams

Jede*r Teilnehmende (oder jedes Zweier‑Team) reicht **ein Team aus zwei KI‑Charakteren** ein. Es wird empfohlen, die Burgen der beiden KIs auf Karten mit sehr nahen Startpositionen gegenseitig abzustimmen.

* **Komplementäres Design:** Die beiden KIs eines Teams sollen sich strategisch ergänzen.
* **Charakter‑Assets:** Jede *einzelne* KI benötigt:
  * **Mindestens drei eigene `.aiv`‑Dateien** (AI Village). Die Auswahl erfolgt automatisch anhand des Kartenlayouts. Alle Dateien müssen in die bereitgestellte AIV‑Vorlage passen.
  * Eine **`.aic`‑Datei** (AI Character)
  * Einzigartige **Porträts, Videos (`.bik`), Sprach‑ und Sounddateien**, die die Persönlichkeit unterstreichen und über die AI Swapper‑Erweiterung im UCP eingebunden werden.

---

## III. Beschränkungen für KI‑Teams

### A. Exklusivität bei Gebäuden & Truppen

* **Exklusive Gebäude:** Abgesehen von Mauern, Zinnen, Treppen, Vorratslagern, Kornspeichern, Waffenkammern und speziellen Rekrutierungsgebäuden (Baumeistergilde, Söldnerposten, Kaserne), dem Marktplatz und Häusern – die beide KIs errichten dürfen – ist **jeder andere Gebäudetyp zwischen den Partnern exklusiv**. Baut eine KI einen bestimmten Gebäudetyp (z. B. einen speziellen Turm oder ein Torhaus), darf die Partner‑KI **denselben Typ nicht** bauen.  
  * *Hinweis:* Diese Exklusivität gilt nur für Gebäude, die über die `.aiv`‑Dateien platziert werden; Gebäude, die durch die `.aic`‑Datei erzeugt werden, sind davon ausgenommen und dürfen von beiden KIs verwendet werden.
* **Haus‑Limit:** Die **Gesamtzahl** der von *beiden* KIs errichteten Häuser darf **23** nicht überschreiten.
* **Exklusive Truppentypen:** Auch Truppentypen sind exklusiv. Rekrutiert eine KI Bogenschützen, Pikeniere usw., darf die andere KI diesen Typ **nicht** ausheben.
 * **Hinweis:** Baumeister sind von dieser Exklusivität ausgenommen

### B. Wall‑Defense‑Limit („WallDef“)

* Die kombinierte Verteidigungsstärke eines Teams auf Mauern und Türmen ist auf **240 WallDef‑Punkte** begrenzt.
* **Truppenkosten:**  
  * Feuerwerfer: **6 Punkte**  
  * Pechkipper: **5 Punkte**  
  * Armbrustschützen: **3 Punkte**  
  * Arabische Bogenschützen: **2 Punkte**  
  * Europäische Bogenschützen: **1 Punkt**  
  * Gepanzerte Nahkämpfer (Arabische Schwertkämpfer, Schwertkämpfer, Pikeniere, Ritter): **1 Punkt**  
  * Schleuderschützen, Streikolbenkämpfer, Assassinen: **0,5 Punkte**  
  * Weitere ungerüstete Nahkämpfer (Speerkämpfer, Sklaven): **0,25 Punkte**
* **Defensive Belagerungsgeräte (Basis):**  
  * Turm‑Balliste/Mangen: **5 Punkte**  
  * Boden‑Feuer Balliste: **5 Punkte**  
  * Boden‑Triböcke: **3 Punkte**
* **Steigende Kosten:** Das *n‑te* defensive Belagerungsgerät eines Teams kostet **Basis + (n‑1)** Punkte.  
  * *Beispiel:* 5 vorhandene Geräte → nächstes Boden‑Trebuchet (Basis 3) = 3 + 5 = **8 Punkte**.
* **Harassing Siege Engines:** Eine KI darf höchstens *so viele* angreifende Belagerungsgeräte bauen wie sie defensive besitzt, **+ 1**.

* **WallDef‑Berechnung:** Rekrutierungs‑Timing kann das reale Verhältnis verzerren. Überschreitet ein Team durch Praxis‑Tests deutlich das Budget, dürfen Schiedsrichter die effektive Berechnung anpassen oder Strafen verhängen.

### C. Starttruppen‑Limit

* Jedes **Team** hat ein Budget von **30 Punkten** (WallDef‑Kosten) für Starttruppen *beider* KIs.
* **Ausnahme Defensive Challenge:** Im **Defensive Challenge**‑Setup (Phase 1) steht dem Team ein gemeinsames Starttruppen‑Budget von **150 Punkten** zur Verfügung.
* **Steigende Kosten für Fernkämpfer:** Jeder *Fernkampf*‑Einheit erhöht die Kosten aller folgenden Fernkämpfer um die **Summen der bisherigen Basis‑Kosten**.  
  * *Beispiel 1:* 2 Europäische Bogenschützen (1 P), 1 Armbrustschütze (3 P) → Gesamtkosten **8 Punkte**  
  * *Beispiel 2:* 2 Armbrustschützen → **9 Punkte**  
  * *Beispiel 3:* 2 Arabische Schwertkämpfer, 2 Schleuderschützen, 1 Feuerwerfer → 1 + 1 + 0.5 + (0.5 + 0.5) + (1 + 6) → **10,5 Punkte**


### D. Exploit‑Vermeidung

* Kein Platzieren von Truppen an unangreifbaren Stellen.  
* Keine extrem langen oder missbräuchlichen Pitch‑Teppiche.  
* Allgemeines Fairplay: Keine Pathfinding‑Labyrinthe, nahezu geschlossene Gatehouses an unzugänglichen Orten, etc.

---

## IV. Turnieraufbau

Das Turnier verläuft in zwei Hauptphasen, gefolgt von einer subjektiven Bewertungsphase.

### Phase 1: Individuelle KI‑Gauntlets

**Hier wird jede KI einzeln getestet; der Partner ist nicht anwesend.** Pro Challenge erfolgt eine Normalisierung auf 0 – 10 Punkte.  

* *Normalisierungsbeispiel:* Schlechteste Überlebenszeit 15 J, beste 50 J → 40 J ergeben  
`round(((40‑15)/(50‑15))*10) = 7 Punkte`.

#### Challenge 1: Economic Gauntlet – „The Barren Boom“

* **Ziel:** Höchsten Wirtschafts‑Score innerhalb des Zeitlimits erreichen.  
* **Karte:** `ChallengeMap_Eco_v1.map`  
* **Gegner:** Reiche, stark befestigte „Economy Challenge Lords“, die kleine Brandstifter‑Überfälle starten.  
* **Zeitlimit:** **30 Jahre** (In‑Game).  
* **Startbedingungen (Deathmatch Game):** 400 Gold, 50 Holz, 0 Stein, 30 Nahrung (15 Brot, 15 Obst), Starttruppen‑Budget 20 P.  
* **Wertung:** `(Gebäudewert) + (Gold / 5) – (Verlorene Gebäude × 10)`.

#### Challenge 2: Defensive Gauntlet – „Rampart Resilience“

* **Ziel:** Möglichst lange gegen permanente Angriffe überleben.  
* **Karte:** `ChallengeMap_Def_v1.map`  
* **Gegner:** Aggressive Wolf (von Krarilotus), Lord Stauten (von Monsterfish), Alexios IV (von Nevikov), Apex Marshal (von Xander10alpha), Emira (von Crusader Pilaw).  
* **Zeitlimit:** Max **50 Jahre** oder Tod des Lords.  
* **Startbedingungen (Crusader Game):** 1500 Gold, 100 Holz, 100 Stein, 125 Nahrung (50 Brot, 25 Obst, 25 Käse, 25 Fleisch), Starttruppen‑Budget 150 P (team‑geteilt).  
* **Wertung:** Überlebenszeit. 50 Jahre = hoher Score.

#### Challenge 3: Offensive Gauntlet – „Shatter the Alliance“

* **Ziel:** Alle feindlichen Lords so schnell wie möglich besiegen.  
* **Karte:** `ChallengeMap_Off_v1.map`  
* **Gegner:** Lord Stauten (von Monsterfish), LotO Pig (von Crusader Pilaw), Alexios IV (von Nevikov), Aggressive Sultan (von Krarilotus), Menschenhändler (von Tobbi), Apex Caliph (von Xander10alpha).  
* **Zeitlimit:** Max **50 Jahre** oder bis alle 6 Lords gefallen sind.  
* **Startbedingungen (Normal Game):** 2000 Gold, 100 Holz, 50 Stein, 60 Brot, Starttruppen‑Budget 20 P.  
* **Wertung:** `Kills × Σ(10 / Time_to_Kill_N)` (Jahre).

#### Team‑Wertung Phase 1

Gesamtscore = **Produkt** der normalisierten Summen beider KIs (0–30).  
*Beispiel:* 17 × 18 = **306 Punkte**.

---

### Phase 2: Team‑Gefechte

Teams treten mit Standard‑Einstellungen (Abschnitt I) gegeneinander an (8 Teams angenommen).

#### Format 1: Free‑For‑All (FFA)

* **Struktur:** Zwei 8‑Spieler‑FFAs → Top 4 in Winners’ Final, Bottom 4 in Consolation Final.  
* **Wertung:** Platzierung (1.=100, …, 8.=30) **+ 10 Punkte** je Kill in *allen* vier FFAs.

#### Format 2: 2v2 Swiss‑Turnier

* **Struktur:** Best‑of‑3, 3 Runden Swiss. Erstes Seeding per FFA‑Ergebnis.  
* **Wertung:** **40 Punkte** pro Match‑Sieg. **+10 P** pro Match für meist verdientes Gold. **+20 P** pro Runde für Team mit meisten zerstörten Gebäuden *innerhalb* seines Matches.

#### Format 3: Sudden Death Gauntlet – „The Tri‑Force Trial“

* **Struktur:** Ein einmaliger, mehrstufiger Szenario‑Run pro Team auf `ChallengeMap_SuddenDeath_v1.map`.  
* **Trophäen (je 0–50 P):**  
  * **Aggressive Trophy:** Kill des Sultans – schnellster = 50 P, langsamster = 25 P, kein Kill = 0 P.  
  * **Defensive Trophy:** Verteidiger überlebt 50 J → 25 P Basis + bis zu 25 Bonus nach Kill‑Differenz.  
  * **Economic Trophy:** Gold pro Kopf nach 50 J im Vergleich zu beiden Nicht‑Sultan‑Fraktionen (min. 25 P, max. 50 P).  
* **Wahl der Gegner‑Prioritäten:** Teams stimmen vorab über die taktischen Prioritäten der vorplatzierten Feind‑Fraktionen ab; niedriger Gesamt‑Score wählt zuerst.

---

## V. Subjektive Bewertung: Immersion & Storytelling

* **Gesamt:** **1000 Punkte** nach Caster‑ und Zuschauer‑Votes.  
* **Kriterien:** Persönlichkeit, Burgen‑Design, Voice‑Lines, Strategie & Narrativ.  
* **Verteilung:** Punkte proportional zur Stimmenzahl.

---

## VI. Endscore

Rangliste = Summe aller Punkte.

### VI.A Beispielrechnung (Team „Alpha“)

| Phase | Punkte |
|-------|--------|
| Individuelle Gauntlets | 12 × 17 = **204** |
| FFA | 70 + (4 Kills × 10) = **110** |
| Swiss | (2 Siege × 40) + 10 Gold + 20 Buildings = **110** |
| Sudden Death | 35 + 0 + 40 = **75** |
| Subjektiv | **161** |
| **Gesamt** | **660 Punkte** |

*(Maximal theoretisch erreichbar: 2480 Punkte – praktisch unerreichbar.)*

---

Viel Erfolg! Vergewissert euch, dass das AI‑Tournament‑Plugin korrekt installiert und nach den Anleitungen konfiguriert ist.
