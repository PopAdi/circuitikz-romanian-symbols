# Mod de utilizare
Downloadati acest proiect, dupa care copiati **folderul _symbols_** in **directorul proiectului vostru** (langa fisierul principal cu extensia .tex). Urmatorul pas este sa scrieti \input{symbols/romanianCircuitSymbols} in preambulul fisierului. La compilare, definitiile simbolurilor vor fi preluate automat. In modul de desenare al circuitului, utilizati to[romanianCurrentSource] pentru generearea simbolului pentru sursa ideala de curent si to[romanianVoltageSource] pentru sursa ideala de tensiune. La fel se procedeaza pentru celelalte elemente. Adaugarea nodurilor personalizate si a etichetelor se poate efectua la fel ca si pentru restul elementelor. Nu uitati sa includeti \usepackage{tikz} si \usepackage{circuitikz} pentru o functionare corecta!

E posibil ca la prima utilizare, sa primiti anumite erori cu privire la lipsa unor pachete. Pentru aceasta, urmati instructiunile de mai jos:
- Daca sunteti pe Linux, scrieti in termnial "sudo apt-get install texlive-full" pentru a vi se instala toate pachetele de care aveti nevoie. Dureaza aproximativ 15-20 de minute instalarea, dar apoi cu siguranta o sa mearga orice o sa mai folositi.
- Daca sunteti pe Windows, va recomand ca mai intai sa instalati Miketex (ultima versiune). De fiecare data cand veti deschide un proiect .tex cu pachete care nu sunt instalate, veti primi un request de instalare si Miketex il va instala singur (folosind editorul Texmaker, asta se intampla mereu).

# Elemente existente
- romanianCurrentSource: sursa ideala de curent
- romanianVoltageSource: sursa ideala de tensiune
- romanianCCS: sursa comandata de curent
- romanianCVS: sursa comandata de tensiune
- zDoZ: dioda Zener
- zDoZZ: dioda Zener inversata
- Ln: bobina neliniara
- Cn: condensator neliniar

# Exemplu cod
    \documentclass{report}

    % Includem pachetele necesare
    \usepackage{circuitikz}
    \usepackage{tikz}

    % Includem pachetul cu simboluri
    \input{symbols/romanianCircuitSymbols}

    \begin{document}
        \begin{center}
        \begin{circuitikz} 
            \draw (0, 0) to[romanianVoltageSource, l=${e_1 = 4V}$, *-*] (4, 0);
            \draw (5, 0) to[romanianCurrentSource, l=${j_1 = 4A}$, *-*] (9, 0);

            \draw (0, -3) to[romanianCVS, l=${e_1 = 4V}$, *-*] (4, -3);
            \draw (5, -3) to[romanianCCS, l=${j_1 = 4A}$, *-*] (9, -3);

            \draw (0, -6) to[zDoZ, l=${D_1}$, *-*] (4, -6);
            \draw (5, -6) to[zDoZZ, l=${D_2}$, *-*] (9, -6);

           \draw (0, -9) to[Cn, l=${i = \dfrac{\mathrm{d} q}{\mathrm{d} t}, F(q, u) = 0}$, *-*] (4, -9);
           \draw (5, -9) to[Ln, l=${u = \dfrac{\mathrm{d} \varphi}{\mathrm{d} t}, F(\varphi, i) = 0}$, *-*] (9, -9);
        \end{circuitikz}
        \end{center}
    \end{document}


# Imagini cu elementele de circuit
![image-1](http://i.imgur.com/KIOllGq.png)


# Probleme de utilizare & erori
Daca intampinati orice probleme in a utiliza acest pachet, ati descoperit erori sau vreti sa ajutati/stiti mai multe, puteti sa ma contactati pe urmatoarea adresa de mail: popadrian1996[at]gmail[dot]com.
