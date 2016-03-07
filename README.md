# circuitikz-romanian-symbols
O mica prezentare asupra definirii simbolurilor in circuitikz si LaTeX + pachetul cu definitii.

# Mod de utilizare
Downloadati acest proiect, dupa care copiati folderul *symbols* in directorul proiectului vostru. Urmatorul pas este sa scrieti \input{symbols/romanianCircuitSymbols} in preambulul fisierului *.tex*. La compilare, definitiile simbolurilor vor fi preluate automat. In modul de desenare al circuitului, utilizati to[romanianCurrentSource] pentru generearea simbolului pentru sursa ideala de curent si to[romanianVoltageSource] pentru sursa ideala de tensiune. Adaugarea nodurilor personalizate si a etichetelor se poate efectua la fel ca si pentru restul elementelor. Nu uitati sa includeti \usepackage{tikz} si \usepackage{circuitikz} pentru o functionare corecta!

![image-1](http://i.imgur.com/QRY37lX.png?1)
![image-2](http://i.imgur.com/EcdQGua.png?1)
