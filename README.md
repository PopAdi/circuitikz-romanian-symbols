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
    \draw (0, 0) 
          to[romanianVoltageSource, shape=circle, l=${e_1 = 4A}$, *-*] (4, 0)
          to[romanianVoltageSource, l=${e_3}$, *-*] (4, -4)
          (0, 0)
          to[european resistor] (4, -4)
          (4, 0)
          to[european resistor] (8, 0)
          to[romanianVoltageSource, l=${e_2 = 7V}$, *-*] (4, -4)
          ;
    \end{circuitikz}
    \end{center}

# Imagini cu elementele (in pozitie verticala, orizontala, diagonala)
![image-1](http://i.imgur.com/QRY37lX.png?1)
![image-2](http://i.imgur.com/EcdQGua.png?1)
![image-3](http://i.imgur.com/MUocjbG.png?1)
![image-4](http://i.imgur.com/vZ6DzWo.png?1)

# Probleme de utilizare & erori
Daca intampinati orice probleme in a utiliza acest pachet, ati descoperit erori sau vreti sa ajutati/stiti mai multe, puteti sa ma contactati pe urmatoarea adresa de mail: popadrian1996[at]gmail[dot]com.
