# Regex

## Was ist Regex?

Regex steht für Regular Expression(Regulärer Ausdruck auf Deutsch). Die Definition auf Wikipedia sagt folgendes:
- Ein regulärer Ausdruck (englisch regular expression, Abkürzung RegExp oder Regex) ist in der theoretischen Informatik eine Zeichenkette, die der Beschreibung von Mengen von Zeichenketten mit Hilfe bestimmter syntaktischer Regeln dient.
- https://de.wikipedia.org/wiki/Regul%C3%A4rer_Ausdruck

Man beschreibt damit also wie eine bestimmte Zeichenkette aussehen soll und wie oft diese vorkommen kann.

Regex ist sehr nützlich, um bestimmte Informationen aus Textinhalten zu extrahieren. Als "Text" ist alles mögliche gemeint, sourcecode, logs, spreadsheet oder mehr
Man kann ASCII, unicode, etc... verwenden

## [Springe zu Advanced Regex](#advancedRegex)

## Regex online tutorial https://regexone.com/ (Basics)

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
Mit Fragezeichen ? kann man gewisse Zeichen als Optional kennzeichnen, also ob sie kein mal oder einmal vorkommen
![image](https://user-images.githubusercontent.com/46607383/162591799-8df9ce54-5186-4fda-8c6a-f75a6c43fb6f.png)

Aufgabe 9 "All this whitespace"
Man kann auch leerzeichen (Spaces matchen) mit \s und mit \s+ beliebig viele whitespaces. Es gibt auch \n für Zeilenumbruch und \t für tab = 4 leerzeichen
![image](https://user-images.githubusercontent.com/46607383/162591896-872b93f7-06f2-44c6-b2a5-148eadd49d40.png)

Aufgabe 10 "Starting and Ending"
Beispiel: man will nach dem Wort success in einem logfile suchen. Es wäre blöd wenn dann im Errorlog sowas steht: "Error unsuccessfull request"
Somit würde das hier auch stimmen, deshalb gibt es eine Möglichkeit um dies zu spezifizieren
Mit ^ vor dem Zeichen kann man sagen, dass die Zeile so anfangen muss und mit $ kann man sagen, dass die Zeile so enden muss
![image](https://user-images.githubusercontent.com/46607383/162592045-6656009c-9d31-4dcb-a0d2-8947860a48ea.png)

Aufgabe 11 "Match Groups"
Man kann zum Beispiel aus .pdf Dateien mit () nur den Dateinamen heraußfiltern wie im Foto unterhalb gezeigt
![image](https://user-images.githubusercontent.com/46607383/162592142-af8f6228-7fb9-4cc1-93e8-c5b9d01cb2d8.png)

Aufgabe 12 "Nested Groups"
Man kann mehrere Daten gleichzeitig herausfiltern
![image](https://user-images.githubusercontent.com/46607383/162592248-df1e089e-0077-49c7-b456-1f21dc20c79b.png)

Aufgabe 13 "More group Work"
![image](https://user-images.githubusercontent.com/46607383/162592293-ae125305-6f48-4948-a8c4-1dfc022194a8.png)

Aufgabe 14 "It's all conditional"
Man kann bei Regex auch logische Verknüpfungen wie ODER (OR) verwenden dafür braucht man das Pipe-Symbol |
![image](https://user-images.githubusercontent.com/46607383/162592364-950edb77-7367-412c-8bf1-193aa50fdcd7.png)

Aufgabe 15 "Other special Characters"
![image](https://user-images.githubusercontent.com/46607383/162592412-4cc70723-59f9-47f0-addb-2a83d4f5f6ab.png)

So Fertig jetzt kann ich Regex EZZZZZZZZZZZZZ (^So.+)

## <a name="advancedRegex">Advanced Regex</a>

Ich habe ein bisschen Laravel programmiert und nach ner Zeit fält es einem schwer if foreach oder die componenten die importiert werden schwer zu erkennen. Daraufhin habe ich nach ner Möglichkeit gesucht diese so zu markieren, dass ich es schneller finde. Der code sah so aus:
![image](https://user-images.githubusercontent.com/46607383/169697877-76933542-f3c9-4ddd-b1c9-c9871256090b.png)
![image](https://user-images.githubusercontent.com/46607383/169697886-1ba26662-3c21-4ea5-b767-d76e74eecfc2.png)

Auf den ersten Blick sieht man nicht sofort wo eine x-componente ein if oder eine for loop ist. Glücklicherweise gibt es ein plugin unter vscode namens Highlight welches mit regex code markieren und stylen kann. Der style ist web css also funktioniert es wie in einer web app. Es sah danach so aus:
![image](https://user-images.githubusercontent.com/46607383/169698076-8be42996-7c09-4909-99a4-f45e4d23b588.png)
![image](https://user-images.githubusercontent.com/46607383/169698109-7a9d8b7d-f002-40da-a938-92cc4369a460.png)
![image](https://user-images.githubusercontent.com/46607383/169698133-1ba34cea-3ba8-4daa-b750-d25e7c3ae8c1.png)

Hier sehe ich nun direkt auf den ersten Blick wo sich was befindet es ist nur eine Frage der Zeit bis ich mir die Farben gemerkt habe!

Das soll demonstrieren wie mächtig regex ist und was man alles damit machen kann. Nun aber zum regex:
```
// @error 
        // @error('body')
        // @enderror
        "(@((end)?(error))(\\(.*\\))?)": [
            {
                "backgroundColor": "#ff4d4d",
                "color": "white",
            }
        ],
        // @foreach($users as $user)
        // @foreach ($users as $user)
        // @endforeach
        "(@(end)?(foreach((\\s+)?\\(.*\\))?))": [
            {
                "backgroundColor": "#68fc51",
                "color": "black",
                "fontWeight": "bold"
            }
        ],
        // @if($user->isAdmin())
        // @if ($user->isAdmin())
        // @endif
        // @else
        // @auth
        // @endauth
        // @guest
        // @endguest
        "(@((end)?(if((\\s+)?\\(.*\\))?|auth|guest|else)))": [
            {
                "backgroundColor": "#51befc",
                "color": "black",
                "fontWeight": "bold"
            }
        ],
        // @include('layouts.app')
        // <x-comment/>
        // </x-comment>
        // <x-picture></x-picture>
        // <x-picture>asdasd</x-picture>
        "((@include\\(.*\\))|(<(/)?x-.+?>))": [
            {
                "backgroundColor": "#8451fc",
                "color": "black",
                "fontWeight": "bold"
            }
        ],
        // jetzt noch eines für label und input tags
        // <input>
        // <input type="test"> asd
        // </input>
        // <input/>
        "(<input|</input>)": [
            {
                "backgroundColor": "#ffcc00",
                "color": "black",
                "fontWeight": "bold"
            }
        ],
        // {{ test }}
        "({{\\s|\\s}})": [
            {
                "backgroundColor": "#a66646",
                "color": "black",
                "fontWeight": "bold",
                
            }
        ],
```
