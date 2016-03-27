# Mod de utilizare
Downloadati acest proiect, dupa care copiati **folderul _symbols_** in **directorul proiectului vostru** (langa fisierul principal cu extensia .tex). Urmatorul pas este sa scrieti \input{symbols/romanianCircuitSymbols} in preambulul fisierului. La compilare, definitiile simbolurilor vor fi preluate automat. In modul de desenare al circuitului, utilizati to[romanianCurrentSource] pentru generearea simbolului pentru sursa ideala de curent si to[romanianVoltageSource] pentru sursa ideala de tensiune. Adaugarea nodurilor personalizate si a etichetelor se poate efectua la fel ca si pentru restul elementelor. Nu uitati sa includeti \usepackage{tikz} si \usepackage{circuitikz} pentru o functionare corecta!

# Elemente existente
- romanianCurrentSource: sursa ideala de curent
- romanianVoltageSource: sursa ideala de tensiune
- romanianCCS: sursa comandata de curent
- romanianCVS: sursa comandata de tensiune

# Exemplu cod
    \begin{center}
        \begin{circuitikz} 
            \draw (0, 0) to[romanianVoltageSource, l=${e_1 = 4V}$, *-*] (4, 0);
            \draw (5, 0) to[romanianCurrentSource, l=${j_1 = 4A}$, *-*] (9, 0);
        
            \draw (0, -3) to[romanianCVS, l=${e_1 = 4V}$, *-*] (4, -3);
            \draw (5, -3) to[romanianCCS, l=${j_1 = 4A}$, *-*] (9, -3);
        \end{circuitikz}
    \end{center}

# Imagini cu elementele de circuit
![image-1](http://i.imgur.com/Gpsw3x4.png)


# Probleme de utilizare & erori
Daca intampinati orice probleme in a utiliza acest pachet, ati descoperit erori sau vreti sa ajutati/stiti mai multe, puteti sa ma contactati pe urmatoarea adresa de mail: popadrian1996[at]gmail[dot]com.
