
JavaScript-Frameworks

verfasst von Boris Stöcker und Matthias Mohr
Allgemeines

JavaScript (JS) Frameworks gibt es in großer Zahl und sie haben ganz unterschiedliche Anwendungsgebiete.
Vor- und Nachteile bei der Verwendung von JS-Frameworks sind divers und hängen von den verwendeten Frameworks ab. Folgend sind Gründe genannt, die zutreffen können, aber nicht immer zutreffen, da jedes Framework anders ist. Es handelt sich jedoch um Beispiele, die häufig anzutreffen sind.

Mögliche Vorteile:

    Häufig benutzte Funktionalität ist vorhanden und getestet
    Cross-Browser-Kompatibilität
    Große Anzahl an Erweiterungen / Widgets / ...
    Nutzung eines CDN (s.u.) möglich um Ladezeit zu verkürzen

Mögliche Nachteile:

    Inkompatibilität der Frameworks untereinander
    Hohe Komplexität durch ggf. ungenutzte Funktionalität
    Lange Ladezeit durch ungenutzten Overhead
    Einarbeitung nötig
    Anpassung kompliziert

Eine große Übersicht über JavaScript-Frameworks kann bei Wikipedia gefunden werden:

    Comparison of JavaScript frameworks
    <span>List of JavaScript libraries

Hinweise zu Ladezeiten und CDN

JavaScript-Frameworks tendieren dazu sehr umfangreich zu sein und damit eine hohe Dateigröße zu erreichen. Beispielsweise ist das Framework AngularJS im “normalen” Zustand 766kb groß. Dies ist für die allgemeine Ladezeit einer Seite nicht von Vorteil, insbesondere wenn man z.B. über ein GPRS oder langsame DSL-Verbindungen auf das Internet zugreift. Um die Ladezeiten zu verkürzen werden im allgemeinen drei Techniken verwendet.
1. Minification

Im ersten Schritt wird die JavaScript-Datei im ursprünglichen Zustand um alle Leerzeichen, Kommentare und sonstige Überflüssigen Zeichen reduziert. Häufig werden auch die Namen von Variablen und internen Funktionen gekürzt. Im Falle von AngularJS ist die Dateigröße nach diesem Verfahren bereits von 766kb auf 105kb verkleinert. Die verkleinerte Datei nennt man häufig “minified” und der Dateiname endet auf “.min”.
2. Komprimierung

Zusätzlich kann die Übertragung von Webseiten zwischen Server und Client (Browser), je nach verwendeter Client- und Serversoftware noch komprimiert werden. Häufig wird die GZip-Komprimierung verwendet. Die Kompressionsmethode ist jedoch vom Server abhängig. Im Falle von AngularJS wird die Datei dadurch auf bis zu 40kb verkleinert.
3. Nutzung eines CDN

CDN steht für Content Delivery Network und beschreibt im Grunde einen zentralen Server, der z.B. JavaScript-Dateien der Frameworks zur Verfügung stellt. Als Entwickler von JS-Anwendungen kann man diese JS-Dateien nutzen anstatt sie auf den eigenen Server zu legen. Der Vorteil dabei ist, dass bei häufiger Nutzung eines CDN die Datei nur einmal in den Cache eines Browsers geladen werden muss, da ein Browser JS-Dateien zur Verkürzung der Ladezeit auf dem Client für die spätere erneute Nutzung zwischenspeichert. Im Idealfall liegt die JS-Datei der eigenen Anwendung, also beim Benutzer, bereits im Cache und muss nicht erneut geladen werden, was effektiv Ladezeit spart. CDN wird von verschiedenen Organisationen kostenfrei angeboten, z.B. Google oder cdnjs.
Universal-Frameworks (Kommunikation, DOM, UI, ...)

Universal-Frameworks nennen wir Frameworks, die die allgemeine Arbeit mit JavaScript im Web-Bereich erleichtern, da sie häufig genutzte Funktionen zur Verfügung stellen, z.B. Elementselektion im DOM (Document Object Model), DOM-Manipulation, Event-Handling, AJAX und weitere nützliche Hilfsfunktionen. Zudem wir die Browser-übergreifende Implementierung von Webanwendungen erleichtert.
jQuery (Version 2.1.1 vom 01.05.2014)

Lizenz: MIT- und GPL-Lizenz Dateigröße (minified): 252kb (84kb) Abhängigkeit: Keine
Hinweise

    Inkompatibel mit prototype
    jQuery ist vermutlich das einsteigerfreundlichste Universal-Framework
    Sehr hohe Verbreitung, dadurch viele Erweiterungen und umfangreiche Hilfestellungen
    Version 2.x unterstützt keinen Internet Explorer 8 und ältere Browser, unabhängige Version 1.x unterstützt zusätzlich Internet Explorer 8 und wird noch weiter aktualisiert

mooTools (Version 1.5.1 vom 29.08.2014)

Lizenz: MIT-Lizenz Dateigröße (minified): 152kb (89kb) Abhängigkeit: keine
Hinweise

    Starke Nutzung der Objektorientierung, sodass hohe Erweiterbarkeit und Flexibilität durch hohe Modularität gewährleistet sind.
    Browserübergreifend kompatibler Code
    I.d.R. relativ wenig eigener Code benötigt
    Erweiterung der nativen JS-Objekte um neue Funktionalität

Alternativen

    prototype & script.aculo.us
    Dojo Toolkit
    YUI Library
    ExtJS

Frameworks zur Visualisierung von Daten
D3.js (Version 3.4.11 vom 2014-07-18)

Lizenz: BSD-Lizenz Dateigröße (minified): 319kb (144kb) Abhängigkeit: Keine
Hinweise

    D3 = Data Driven Documents
    Ermöglicht mit relativ wenig Aufwand teils aufwändige Visualisierungen
    Interaktive Visualisierungen möglich
    Neben Visualisierungen sind verschiedenste Funktionalitäten um Daten zu selektieren, zu verändern, abzufragen, darzustellen, etc. vorhanden

Alternativen

    Raphaël
    ExtJS
    Dojo GFX

MVC-Frameworks für Single-Page-Webanwendungen, Routing, ...

Single-Page-Webanwendungen (SPA) brechen mit der üblichen Art von Internetseiten, die aus mehreren verlinkten Seiten bestehen und wo bei jeder Interaktion eine neue Seite geladen werden muss. SPA bestehen nur aus einer einzigen Seite, die die benötigten Inhalte dynamisch nachlädt.
Das übliche MVC-Entwurfsmuster (Model View Controller) wird in der Webentwicklung häufig aufgeweicht. Die hier genannten Frameworks sind nicht zwingend alle MVC-Frameworks, sondern können auch anderen Entwurfsmustern folgen, z.B. MVVM (Mode View ViewModel). Eine interessante Hilfe zur MVC-Framework-Wahl ist TodoMVC, die es sich zum Ziel gesetzt hat, eine ToDo-Listen-Anwendung in vielen verschiedenen Frameworks umzusetzen. Der interessierte Entwickler kann sich anhand dieser Beispiele für ein entsprechendes Framework entscheiden.
AngularJS (Version 1.2.26 vom 01.10.2014)

Lizenz: MIT-Lizenz Dateigröße (minified): 766kb (105kb) Abhängigkeit: jQuery Light
Hinweise

    Template-Engine fest integriert
    Two-way data binding (automatische Benachrichtigung von Model und View gegenseitig bei Änderungen) möglich
    Teilweise komplizierte API / Konzepte

Backbone.js (Version 1.1.2 vom 20.02.2014)

Lizenz: MIT-Lizenz Dateigröße (minified): 60kb (20kb) Abhängigkeit: Underscore.js, jQuery (empfohlen)
Hinweise

    Template-Engine frei wählbar, Standard: Underscore.js
    Nur grundlegende Funktionen vorhanden, daher sind darauf aufbauende Frameworks mit erweiterter Funktionalität entstanden, z.B. Aura, Backbone UI, LayoutManager, und zusätzlich sind viele Erweiterungen vorhanden.

Alternativen

    enber.js
    ExtJS
    Cappuccino

Frameworks für JSON/XML-Umwandlung
JSONIX (Version 2.0.0 vom 24.02.2014)

Lizenz: BSD-artige Lizenz Dateigröße (minified): 163kb (104kb) Abhängigkeit: keine
Hinweise

    Umwandlung XML => JSON (“Unmarshalling”)
    Umwandlung JSON => XML (“Marshalling”)
    Optionale Benutzung eines XML-Schemas
    Fest strukturiert und typsicher

Frameworks zum Templating (Vorlagen)

Templating erlaubt die Trennung von Programmlogik und Oberfläche. Zudem können häufig genutzte Oberflächenelemente wiederverwendet werden.
Mustache (Version 0.8.2 vom 17.03.2014)

Lizenz: MIT-Lizenz Dateigröße (minified): 17kb (-) Abhängigkeit: Keine
Hinweise
Alternativen

    Underscore.js
    Handlebars.js

Frameworks zur Oberflächengestaltung (GUI/Widgets)

Basierend auf bereits vorgestellten Frameworks gibt es Frameworks, die sich mit der Oberflächengestaltung von (Web-)Anwendungen beschäftigen. Je nach bereits gewählten Frameworks bietet es sich an, das dazu passende GUI-Framework zu nutzen.
jQuery UI (Version 1.11.1 vom 01.05.2014)

Lizenz: MIT- und GPL-Lizenz Dateigröße (minified): 454kb (233kb) Abhängigkeit: jQuery
Hinweise

Unterstützt:

    Interaktionen (Drag & Drop, Skalierung, Sortierung, ...)
    Widgets (Autovervollständigung, Dialog, Menü, Fortschrittsbalken, Tabs, ...)
    Effekte (Farbanimation, Toggle, Zeigen/Verstecken, ...)

Alternativen

    Dojo >Widgets
    Ext JS
    script.aculo.us
    YUI Library

