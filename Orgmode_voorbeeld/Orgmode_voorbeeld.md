- [Toetsaanslagen](#orgf30c8df)
- [Te doen <code>[1/3]</code>](#org81778ae)
  - [MarColumn december schrijven <code>[6/6]</code>](#orgeac9505)
  - [File met eenvoudige voorbeelden toevoegen <code>[5/6]</code>](#org4551e3a)
    - [Tekststijl](#orgdda7a18)
    - [Takenlijst en kopjes <code>[33%]</code>](#org4aa4629)
    - [Links](#orgc28d6de)
    - [Tabel/spreadsheet](#orga55cc76)
  - [Meer geavanceerde voorbeelden](#orgdde8a0c)
    - [Formule](#org65c5323)
    - [Code](#org8e33ed3)



<a id="orgf30c8df"></a>

# Toetsaanslagen

1.  Ik gebruik kleine letter `a` voor de `A`-toets.
2.  Ik gebruik hoofdletters `C-` voor de `Ctrl`-toets, `M-` voor de Alt (meta)-toets en `S-` voor de `Shift`-toets.
    -   `C-c` is dus `Ctrl-C`, `C-c C-c` is dat tweemaal en `C-M-a` is gelijktijdig `Ctrl`, `Alt` en `A` indrukken.
3.  `ENTER`, `TAB` en `ESC` zijn de toetsen die je verwacht.
4.  Raak je verstrikt? Druk `ESC ESC ESC ESC` en je kunt weer typen.
5.  Zie ook <http://pub.vandersluys.nl/download/GettingStartedWithEmacs.pdf> (met name sectie 1.2 en het begin van 1.3)


<a id="org81778ae"></a>

# TODO Te doen <code>[1/3]</code>


<a id="orgeac9505"></a>

## DONE MarColumn december schrijven <code>[6/6]</code>

1.  [X] klokken taken, projecten
2.  [X] agenda, plannen, takenlijsten (TODO/DONE, OPEN/CLOSED), ideeenlijsten
3.  [X] (interne) links
4.  [X] tabellen, simpele spreadsheets
5.  [X] export, publish: plain text, html, md, LaTeX/PDF, odt, rST, &#x2026;
6.  [X] code, formules


<a id="org4551e3a"></a>

## PROGRESS File met eenvoudige voorbeelden toevoegen <code>[5/6]</code>


<a id="orgdda7a18"></a>

### DONE Tekststijl

-   **vet**
-   *cursief*
-   <span class="underline">onderlijnd</span>
-   ~~doorgehaald~~
-   `code` of `vebatim`


<a id="org4aa4629"></a>

### DONE Takenlijst en kopjes <code>[33%]</code>

-   [X] Zie [2](#org81778ae)
-   [X] inspringen:
    -   zet de cursor op een item (b.v. in deze lijst) en typ `Alt-pijl rechts/links`
    -   hetzelfde voor kopjes
-   [ ] slepen:
    -   zet de cursor op een item en typ `Alt-pijl op/neer`
    -   op/neer wisselt voor een item (met dezelfde indentatie en indien mogelijk)
    -   hetzelfde voor kopjes (van hetzelfde level)
-   [ ] lijstsymbool veranderen:
    -   zet de cursor op een item en typ `Shift rechts/links`
    -   symbolen springen van tussen `+/-/*/1./1)` (`*` indien mogelijk)
-   [X] item aan/uitvinken:
    -   zet de cursor op het item en typ `C-c C-c`
    -   het aantal of percentage in het kopje erboven (gemaakt door `[/]` of `[%]` te typen) verandert mee
-   [ ] TODO veranderen:
    -   zet de cursor op een kopje en typ `Shift rechts/links`
    -   als alle subkopjes DONE zijn, wordt het hogere kopje dat ook (mits er TODO staat)
-   [ ] Nieuw item:
    -   `Alt-ENTER`
-   [ ] Nieuw kopje:
    -   `Ctrl-ENTER`
-   [ ] Nieuwe lijst maken
    1.  Genummerd:
        1.  typ een `1.` of `1)` gevolgd door een spatie en de omschrijving
        2.  typ `Alt-ENTER` voor het volgende item (telt automatisch door)
    2.  Ongenummerd:
        1.  typ een `+`, `-` of (indien subitem) `*` gevolgd door een spatie en de omschrijving
        2.  typ `Alt-ENTER` voor het volgende item met hetzelfde symbool
    3.  Definitie:
        -   **Definitie:** een definitie is een **ongenummerd** item met een keyword, gevolgd door een dubbele dubbele punt (`::`) en de definitie.
        -   `Alt-ENTER` vraagt om de volgende definitie met hetzelfde symbool
    4.  Vink (*radio button*):
        1.  typ een item symbool of nummer, gevolgd door een spatie, `[ ]`, weer een spatie en de omschrijving
        2.  de `[ ]` licht op ten teken dat de *radio button* actief is
        3.  `Alt-ENTER` geeft een nieuw item, maar **geen** lege radio button (bug?)
        4.  `C-c C-c` op de regel switcht tussen `[ ]` en `[X]`


<a id="orgc28d6de"></a>

### DONE Links

-   Interne link: zie [2](#org81778ae)
-   Externe link: <https://github.com/MarcvdSluys/NLLGG-docs>
-   Externe link met onschrijving: [NLLGG docs](https://github.com/MarcvdSluys/NLLGG-docs)


<a id="orga55cc76"></a>

### DONE Tabel/spreadsheet

1.  typ `|- TAB` voor een horizontale lijn
2.  typ `x|x^2|x^3 TAB` in de nieuwe regel voor de header
3.  typ `-` rechts tegen de `|` voor nog een lijn
4.  in de linker kolom, typ `1 ENTER 2 ENTER` etc.
5.  onder x<sup>2</sup>, typ `=$1**2 TAB`. `$1` staat voor kolom 1.
6.  onder x<sup>3</sup>, typ `=$1**3 TAB`
7.  ga naar de regel met `TBLFM` (tabelformule) onder de tabel en typ `C-c C-c`

| x | x<sup>2</sup> | x<sup>3</sup> |
| 1 | 1             | 1             |
| 2 | 4             | 8             |
| 3 | 9             | 27            |
| 4 | 16            | 64            |
| 5 | 25            | 125           |


<a id="orgdde8a0c"></a>

## PROGRESS Meer geavanceerde voorbeelden


<a id="org65c5323"></a>

### DONE Formule

LaTeX moet geinstalleerd zijn&#x2026;

1.  inline: typ `$\int_0^\infty \frac{\sin x}{x} dx$` en druk `C-c C-x C-l` Dit is een mooie formule $\int_0^\infty \frac{\sin x}{x} dx$, maar wel ingewikkeld.

2.  tussen de tekst: typ `\[\int_0^\infty \frac{\sin x}{x} dx\]` en druk `C-c C-x C-l` $$\int_0^\infty \frac{\sin x}{x} dx$$


<a id="org8e33ed3"></a>

### ACTIVE Code

-   Elisp werkt altijd?

1.  Elisp (emacs lisp script)

    1.  Typ `C-c C-, s` voor een `#+begin/end_src`-block en voeg zelf `elisp` toe
    2.  Typ wat code in en return een waarde (zie voorbeeld hieronder)
    3.  In het codeblok, typ `C-c C-c` en beantwoord de vraag onderin met `yes ENTER`
    4.  Het resultaat verschijnt in een `RESULTS`-blok onder de code.
    
    ```elisp
    (concat  (emacs-version)
    	 "\nOrgmode " (org-version))  
    ```
    
        GNU Emacs 27.2 (build 1, x86_64-pc-linux-gnu, GTK+ Version 3.24.29, cairo version 1.16.0)
         of 2021-10-01
        Orgmode N/A

2.  Bash

    Bash moet geinstalleerd zijn en Babel moet geactiveerd zijn voor Bash&#x2026;
    
    ```bash
    echo "Mijn homedirectory is $HOME"
    ```
    
        Mijn homedirectory is /home/sluys

3.  Python

    Python moet geinstalleerd zijn en Babel moet geactiveerd zijn voor Python&#x2026;
    
    1.  Typ `C-c C-, s` voor een `#+begin/end_src`-block en voeg zelf `python` toe
    2.  Typ wat code en return een waarde
    3.  In het codeblok, typ `C-c C-c` en beantwoord de vraag onderin met `yes ENTER`
    4.  De returnwaarde verschijnt onder de code in
    
    ```python
    x=3
    y=4
    z=x*y
    return z
    ```
    
        12
    
    ```python
    import numpy as np
    import matplotlib.pyplot as plt
    x = np.linspace(-15,15)
    plt.plot(x, np.sin(x)/x)
    plt.savefig('Orgmode_voorbeeld.png')
    return 'Orgmode_voorbeeld.png'  # Return filename to orgmode
    ```
    
    ![img](Orgmode_voorbeeld.png)

4.  Python + Bash

    -   Hier gejat: <https://jherrlin.github.io/posts/emacs-orgmode-source-code-blocks/>
    
    Print een lijst met een selectie van files in deze directory in bash. Ik wil zowel (`both`) de code als het resultaat exporteren (naar bijvoorbeeld .md of .pdf). En ik geef de code een naam (`ls`) zodat de output hieronder gebruikt kan worden:
    
    ```bash
    ls -lb Orgmode_voorbeeld[._]*
    ```
    
        -rw-r--r-- 1 sluys sluys   9184 Dec 12 12:01 Orgmode_voorbeeld_ascii.txt
        -rw-r--r-- 1 sluys sluys  26861 Dec 12 12:10 Orgmode_voorbeeld.html
        -rw-r--r-- 1 sluys sluys   9414 Dec 12 11:59 Orgmode_voorbeeld.md
        -rw-r--r-- 1 sluys sluys  37244 Dec 12 12:00 Orgmode_voorbeeld.odt
        -rw-r--r-- 1 sluys sluys   8509 Dec 12 12:15 Orgmode_voorbeeld.org
        -rw-r--r-- 1 sluys sluys 308254 Dec 12 12:00 Orgmode_voorbeeld.pdf
        -rw-r--r-- 1 sluys sluys  23293 Dec 12 12:30 Orgmode_voorbeeld.png
        -rw-r--r-- 1 sluys sluys  10210 Dec 12 12:01 Orgmode_voorbeeld.rst
        -rw-r--r-- 1 sluys sluys  12052 Dec 12 12:00 Orgmode_voorbeeld.tex
        -rw-r--r-- 1 sluys sluys  10605 Dec 12 12:02 Orgmode_voorbeeld_utf8.txt
    
    Gebruik awk om de filename en grootte te nemen van de files uit `ls` en maak een tabel:
    
    ```awk
    BEGIN { OFS="|" }; { print $5, $9}
    ```
    
    | 9184   | Orgmode<sub>voorbeeld</sub><sub>ascii.txt</sub> |
    | 26861  | Orgmode<sub>voorbeeld.html</sub>                |
    | 9414   | Orgmode<sub>voorbeeld.md</sub>                  |
    | 37244  | Orgmode<sub>voorbeeld.odt</sub>                 |
    | 8509   | Orgmode<sub>voorbeeld.org</sub>                 |
    | 308254 | Orgmode<sub>voorbeeld.pdf</sub>                 |
    | 23293  | Orgmode<sub>voorbeeld.png</sub>                 |
    | 10210  | Orgmode<sub>voorbeeld.rst</sub>                 |
    | 12052  | Orgmode<sub>voorbeeld.tex</sub>                 |
    | 10605  | Orgmode<sub>voorbeeld</sub><sub>utf8.txt</sub>  |
    
    Gebruik Python om o.a. de kleinste en grootste file te vinden in de tabel van `awk`:
    
    ```python
    print(table[0])                      # Eerste rij van de tabel zoals ingelezen
    print("Aantal bestanden: %i"         % len(table))
    print("Kleinste bestand: (%i b) %s"  % tuple(min(table)))
    print("Grootste bestand: (%i b) %s"  % tuple(max(table)))
    print("Totale grootte: %0.3f kb"     % (sum([x for x,y in table]) / 1000))
    ```
    
        [9184, 'Orgmode_voorbeeld_ascii.txt']
        Aantal bestanden: 10
        Kleinste bestand: (8509 b) Orgmode_voorbeeld.org
        Grootste bestand: (308254 b) Orgmode_voorbeeld.pdf
        Totale grootte: 455.626 kb
