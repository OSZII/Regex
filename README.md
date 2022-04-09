# Regex

## Was ist Regex?

Regex steht für Regular Expression(Regulärer Ausdruck auf Deutsch). Die Definition auf Wikipedia sagt folgendes:
- Ein regulärer Ausdruck (englisch regular expression, Abkürzung RegExp oder Regex) ist in der theoretischen Informatik eine Zeichenkette, die der Beschreibung von Mengen von Zeichenketten mit Hilfe bestimmter syntaktischer Regeln dient.
- https://de.wikipedia.org/wiki/Regul%C3%A4rer_Ausdruck

Man beschreibt damit also wie eine bestimmte Zeichenkette aussehen soll und wie oft diese vorkommen kann.

Regex ist sehr nützlich, um bestimmte Informationen aus Textinhalten zu extrahieren. Als "Text" ist alles mögliche gemeint, sourcecode, logs, spreadsheet oder mehr
Man kann ASCII, unicode, etc... verwenden

## Regex online tutorial https://regexone.com/

### Aufgabe 1
Hier musste man alle Zeilen komplett matchen man kann unterschiedliche Sachen verwenden hier habe ich [a-z]+ verwendet
[a-z] sagt alle Buchstaben und das plus sagt alles dahinter was der Bedingung matched.
Es geht aber auch mit \w+ habe das auf ner anderen Website gesehen. \w steht hierbei für Word
![image](https://user-images.githubusercontent.com/46607383/162590438-859ffaac-15eb-4772-a9c2-6f033354441b.png)

### Aufgabe 1 1/2
Hier war es die Aufgabe alle Digits zu matchen hier habe ich \d+ verwendet. \d steht für digits und das plus für alle digits die danach folgen
Es wäre aber auch [0-9]+ gegangen
![image](https://user-images.githubusercontent.com/46607383/162590512-80e6d5a8-016e-44d2-857e-c374a818da44.png)

### Aufgabe 2 "The Dot"
Man kann . escapen indem man einen backslash davor einfügt .\, dass bedeutet alles also alle Zeichen stimmen überein weil .\ eine wildcard ist.
![image](https://user-images.githubusercontent.com/46607383/162590677-0e7bbf05-0cb1-4c50-8fd9-dda966b8ec47.png)

### Aufgabe 3 "Matching Specific characters"
Ok anscheinend war das mit dem plus oben schon zu weit es reicht einfach bei aufgabe 1 a einzugeben für den buchstaben a der in jeder Reihe vorkommt.
bei 1 1/2 reicht auch nur \d
hier habe ich die ersten 3 strings matchen müssen und dafür die eckigen Klammern gebraucht [], weil ich nur c, m und f matchen musste.
![image](https://user-images.githubusercontent.com/46607383/162590764-faea3fe4-7a4f-4f21-b68e-0293c97e2954.png)

### Aufgabe 4 "Excluding specific characters"
Mit ^ excludiert man spezielle zeichen
![image](https://user-images.githubusercontent.com/46607383/162590908-e0491a7b-e48e-4e5d-9bb4-d4795748c00c.png)

### Aufgabe 5 "Character Ranges"
Man kann character ranges verwenden um zum beispiel eine reihe von buchstaben oder Zahlen zu definieren bzw. einzugrenzen
[A-Z] sagt zum beispiel alle Großbuchstaben von A bis Z [0-9] alle Zahlen von 0 bis 9.
[^A-G] Alle Zeichen außer A bis G. [^0-7] alle Zeichen außer 0-7 also 8 und 9 und alle anderen.
\w wird hier auch erklärt und zwar matched \w  [A-Za-z0-9_] also alle Zeichen von A bis Z (groß), a bis z (klein) 0 bis 9 und underscore _

Hier musste ich alle Characters matchen wo match stand und alle skippen wo skip daneben stand
![image](https://user-images.githubusercontent.com/46607383/162591153-91c0a899-f496-4277-92ed-c52a2899134c.png)

### Aufgabe 6 "Catching some ZZZ'S"
Bei dieser Aufgabe geht es um die Anzahl an Wiederholungen
man könnte zum Beispiel für 3 Zahle \d\d\d machen
aber es geht besser a{3} wird 3 a's matchen, und manche Regexsysteme unterstützen sogar diesen Syntax: a{1,3} also 1 bis 3 a's
ich hätte es mit z{2,100} gemacht, was aber falsch wäre, weil dann würde es nicht nach wa und up überprüfen.
![image](https://user-images.githubusercontent.com/46607383/162591443-d50d83af-972f-4a70-a03b-1bfd91a34e7f.png)

### Aufgabe 7 
+ bzw * operator für mehrere vorkommnisse oder alles danach
![image](https://user-images.githubusercontent.com/46607383/162591686-ad0cae53-3efa-40d8-84b8-d8758fd1c00f.png)

Aufgabe 8 "Optional Characters"





