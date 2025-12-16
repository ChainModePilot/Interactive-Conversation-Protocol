# Interactive Conversation Protocol

## 1. Projektdefinition

Interactive Conversation Protocol (ICP) ist ein strukturiertes Protokoll zur Beschreibung von Direktivbedeutungen. Clients können Direktivbedeutungen basierend auf der Struktur dieses Protokolls zu menschenerkennbaren modularen multimodalen Nachrichten kombinieren.

**Kernpositionierung**: Eine Zwischensprachform für die Mensch-Maschine-Interaktion, im Wesentlichen eine strukturierte Textdarstellung eines Konzeptgraphen, die wir "Conception Annotation" nennen.

## 2. Warum dieses Projekt erstellt wurde

### ❓ Zu lösende Probleme

Wir müssen der Realität ins Auge sehen: Für einen beträchtlichen Zeitraum wird bestimmt, wie mit Benutzern interagiert wird, von Endseiten-Entwicklern (oder Unternehmen). Unter den meisten bestehenden Geschäftsmodellen ist die Beteiligung der Benutzer an der Interaktion die Grundlage des Produktwerts und der Rentabilität, wie aktive Benutzerzahlen und Werbeeinnahmen. Niemand kann Endseiten zwingen, ausreichende Berechtigungen zu öffnen und zuzulassen, dass KI Operationen vollständig ohne menschliches Eingreifen ausführt.

Wenn KI intelligent genug ist, müssen Menschen tatsächlich nicht jedes Mal von der Startseite beginnen. Daher können wir sehen, dass der Mensch-Maschine-Dialog zur Hauptschnittstelle der nächsten Generation wird, was fast zu einem Konsens geworden ist.

Die natürlichen Defekte der natürlichen Sprachexpressivität, die ursprünglich hofften, durch gut gestaltete Interaktionen kompensiert zu werden, werden jedoch jetzt durch Dialogfelder ersetzt. Die Einschränkungen von Dialogfeldern werden sofort offengelegt:

#### (1) Verlust der Indikationsfunktion des Cursors

Interaktionsformen verschieben sich vom Modus "Bildschirm + Fokus-Operation" zum natürlichen Sprachmodus. Traditionelle Fokus-Operationen werden über Tastaturen, Mäuse und Touchscreens erreicht und bieten präzise Indikation. Die natürliche Sprachinteraktion bringt folgende Auswirkungen mit sich:

- **Verlust der indikativen Präzision**: Die Schwierigkeit des Ausdrucks und Verstehens nimmt zu, und die Mehrdeutigkeit wächst, was wir den "Cursor-Verlust-Effekt" nennen.
  > Wenn ein Benutzer beispielsweise "lösche dies" sagt, hat das System Schwierigkeiten zu bestimmen, auf welches spezifische Objekt sich "dies" bezieht, während traditionelle Schnittstellen durch Mausklicks präzise lokalisieren können.

- **Begrenzte Effizienz der Informationsausdrücke**: Reine Sprachinformationsausdrücke sind ineffizient, und der Vorteil der Spracheingabe zeigt sich hauptsächlich in Wort-für-Wort-Ausdrucksszenarien.
  > Wenn Sie beispielsweise eine Miniaturansicht vergrößern möchten, müssen Sie möglicherweise "vergrößern" sagen oder "vergrößern" tippen, während die traditionelle Interaktion nur einen einzigen Klick erfordert.

- **Hohe Anforderungen an sprachliche Ausdrucksfähigkeit**: Die natürliche Sprachinteraktion stellt hohe Anforderungen an die sprachliche Ausdrucksfähigkeit der Benutzer und schafft Schwierigkeiten in der Mensch-Maschine-Interaktion.
  > Benutzer, die nicht gut in sprachlichem Ausdruck sind, können möglicherweise ihre Bedürfnisse nicht genau beschreiben, was zu Systemverständnisabweichungen führt, während traditionelle Schnittstellen die Ausdrucksschwelle durch visuelle Elemente wie Schaltflächen und Menüs senken.

- **Niedrige Effizienz beim Informationslesen**: Textstromlesen und Sprachlesen sind weniger effizient als strukturiertes Informationslesen.
  > Wenn das System beispielsweise eine lange Datenliste per Sprache ausgibt, müssen Benutzer die gesamte Liste anhören, um Zielinformationen zu finden, während traditionelle Schnittstellen es Benutzern ermöglichen, durch strukturierte Formen wie Tabellen und Karten schnell zu scannen und zu lokalisieren.

- **Eingeschränkt durch Dialogrunden**: Interaktionen, die durch Dialogrunden eingeschränkt sind, sind nicht freundlich für schnelle kontinuierliche Operationen.
  > Wenn Benutzer mehrere Operationen kontinuierlich ausführen müssen, müssen sie warten, bis jede Dialogrunde abgeschlossen ist, bevor sie zum nächsten Schritt übergehen können, während traditionelle Schnittstellen mehrere Schaltflächen schnell nacheinander klicken können, um Batch-Operationen abzuschließen.

#### (2) Informationsfragmentierungsüberlauf

Die Streaming-Informationsstruktur von Gesprächen mangelt es an Organisation, anders als traditionelle Software, die Informationsarchitekturen in Seiteneinheiten organisiert und visuell freundliche Informationspräsentationshierarchien durch visuelle grafische Schnittstellen aufbaut. Dies führt zu folgenden abgeleiteten Problemen:

- **Schwierigkeit, verschiedene Informationen zu isolieren**: Kontinuierliche Informationsflüsse innerhalb eines einzelnen Gesprächs machen es schwierig, Grenzen zwischen verschiedenen Themen zu unterscheiden, und sogar mehrere völlig unabhängige Themen können miteinander vermischt werden.
  > Ein Benutzer fragt beispielsweise zuerst "hilf mir, das Wetter von morgen zu überprüfen" in einem Gespräch, fragt dann "wie ist der Projektfortschritt", und fragt dann "empfehle einige gute Bücher". Diese völlig unabhängigen Themen sind miteinander vermischt, was es schwierig macht, schnell zu lokalisieren und zu überprüfen.

- **Zombie-Sitzungs-Explosion**: Wenn Informationen künstlich durch Sitzungen isoliert werden, werden Informationen innerhalb von Sitzungen in Blackboxen mit Sitzungen als Einheiten gefaltet und werden schließlich zu Zombie-Sitzungen aufgrund niedriger Sichtbarkeit.
  > Benutzer erstellen beispielsweise mehrere Sitzungen wie "arbeitsbezogen", "Studiennotizen", "Einkaufsliste", aber jede Sitzung hat nur verstreute Nachrichten. Im Laufe der Zeit werden diese Sitzungen vergessen und werden zu Zombie-Sitzungen, die nicht effektiv genutzt werden können.

- **Nicht in der Lage, mehrdimensional zu verwalten**: Ähnliche Informationen, die über unzählige Sitzungen verstreut sind, können nicht organisiert werden, weil Informationen nicht entlang einer bestimmten Dimension verwaltet werden können.
  > Benutzer haben beispielsweise in verschiedenen Sitzungen nach "Python-Tutorial", "JavaScript-Tutorial", "React-Tutorial" und anderen Lernressourcen gefragt, können sie aber nicht einheitlich entlang der Dimension "Lernressourcen" anzeigen und verwalten und können nur Sitzung für Sitzung suchen.

- **Mangel an indizierbaren Objekten**: Informationen lösen sich in Textinformationen auf, und wenn wir auf etwas verweisen müssen, gibt es kein spezifisches Objekt, auf das verwiesen werden kann.
  > Wenn ein Benutzer beispielsweise sagt "optimieren Sie diesen Vorschlag erneut", ist "dieser Vorschlag" nur ein Absatz im Textstrom ohne unabhängige Identifikation und Struktur, was es dem System erschwert, präzise zu lokalisieren und zu operieren.

#### (3) Erhebliche Unterschiede in Mensch-Maschine-Schnittstellen über verschiedene Terminals

Mehr Terminalgeräte in der Zukunft werden von Agents angetrieben, entsprechen der menschlichen Wahrnehmung durch Bildschirme, Kameras, Mikrofone, Lautsprecher und andere Geräte, um Mensch-Maschine-Interaktionen abzuschließen. Verschiedene Terminals haben jedoch inhärente Unterschiede in ihren physischen Eigenschaften, und es ist unmöglich, denselben Interaktionsmodus zwangsweise zu verwenden. Dies schafft Schwierigkeiten bei der KI-Integration:

- **Medientrennung**: Wenn die von KI zurückgegebene Informationsstruktur terminalsunfreundlich ist, führt dies unweigerlich zu Verlust oder Verwirrung bei der Informationsausdrücke. Umgekehrt ist die von Terminals bereitgestellte Informationsstruktur nicht unbedingt KI-freundlich.
  > Eine komplexe Datenvisualisierung, die ursprünglich für ein Großbildschirm-Dashboard designed wurde, wird beispielsweise direkt "vorgelesen" durch Sprache auf einem intelligenten Lautsprecher, was es Benutzern fast unmöglich macht, ein Gesamtverständnis zu entwickeln; umgekehrt kann eine einzelne Zeile von Prompt-Informationen auf einer Smartwatch kaum die komplexen Semantiken vollständig tragen, die KI auszudrücken erwartet.

- **KI beherrscht Terminaleigenschaften nicht**: Um die Ausdruckskraft zu verbessern, verwenden Menschen oft mehrere Software und Terminals, um in komplexen Kontexten oder beim Ausdrücken komplexer Logik zu demonstrieren. KI scheint nur zu wissen, wie man "spricht".
  > Wenn ein Produktmanager beispielsweise einen Vorschlag präsentiert, zeigen sie Folien, zeichnen Strukturdiagramme auf einem Whiteboard und klicken Operationen auf Demo-Seiten; während aktuelle KI oft nur mit einem langen Text oder einer Sprachfolge erklären kann, was es schwierig macht, Terminalfähigkeiten wie Projektion, Annotation und Animation zu verwenden, um die Ausdruckskraft zu verbessern.

- **Lücke zwischen Virtual und Realität**: Der Kontext (oder Kontext), der derzeit von KI verwendet wird, basiert auf voreingestelltem und auswendig gelerntem Wissen, während der Kontext in realen Szenarien oft dynamisch und mit der realen Umgebung verbunden ist.
  > KI kann beispielsweise "sich erinnern" an persönliche Profile und historische Gespräche der Benutzer, aber es ist schwierig, in Echtzeit wahrzunehmen, dass der Benutzer in einem Konferenzraum sitzt, durch welche Seite eines Papierdokuments blättert oder auf welches physische Display-Board zeigt, und kann daher keine natürlichen Anweisungen und Ergänzungen basierend auf Situationen vor Ort wie ein echter Assistent machen.

### 💡 Verbesserungsideen und Ziele

Zuvor war die Hauptarbeit von Produktmanagern das Design von leicht zu erlernenden und leicht zu verwendenden Schnittstellen und Betriebsabläufen. Mit KI-Unterstützung müssen Benutzer nicht mehr Software-Interaktionsschnittstellen und Betriebslogik lernen. KI hat die Fähigkeit, Benutzern nur notwendige Informationen basierend auf Benutzerfragen und Anweisungen bereitzustellen, und Benutzer benötigen nur minimale Eingriffsoperationen.

Solange Benutzer selbst eingreifen, gibt es jedoch Probleme mit Interaktionsfreundlichkeit, Genauigkeit und Effizienz. Interactive Conversation Protocol spielt genau am Punkt des Mensch-Maschine-Kontakts eine Rolle:

#### Verbesserung der Ausdruckskraft der natürlichen Sprache (Mensch → KI)

Die Verbesserung der Ausdruckskraft bezieht sich hier auf die Verbesserung der natürlichen Sprache. Um die oben erwähnten Probleme zu kompensieren (Verlust der Cursor-Indikation, Informationsfragmentierungsüberlauf und Unterschiede in Mensch-Maschine-Schnittstellen über verschiedene Terminals). Zumindest kann die folgende Verarbeitung an ursprünglicher natürlicher Sprache durchgeführt werden:

- **Markieren ausgedrückter Informationen**: Markieren Sie Informationen, die eine spezielle Verarbeitung benötigen. Die hier erwähnte spezielle Verarbeitung umfasst die Verwendung strukturierter Informationen, das Zusammenstellen von Schnittstellen, das Ausführen von Hilfsprogrammen usw. Sie können sich das vorstellen, als würden Sie Notizen machen, indem Sie Punkte auf einem Textstück umkreisen. In Bezug auf die Markierungsform beziehen wir uns auf Markdown, verwenden spezielle Zeichen, um spezifische Bedeutungen darzustellen, während die Erklärung und Auslösung von Hilfsfunktionen sich auf das Annotationsprinzip in der Java-Entwicklung bezieht. Durch diese Methode können wir den Ton der Sprache ergänzen, darauf hinweisen, was wichtig ist, was spezielle Präsentationsformen benötigt und was Voroperationen benötigt (wie Authentifizierung, die nur für sich selbst sichtbar ist) im ursprünglichen expository Inhalt.
  > Wenn ein Benutzer beispielsweise sagt "hilf mir, die To-dos dieser Woche zu organisieren", markieren Sie Daten, Prioritäten und verantwortliche Personen leicht im Satz, kann KI direkt eine überprüfbare To-do-Liste generieren, anstatt nur einen beschreibenden Text zurückzugeben.

- **Hinzufügen von Kontextinformationen**: Ergänzen Sie notwendige virtuelle Informationen und reale Umgebung in die narrative Information, um die reale Situation des Sprechers zu reproduzieren. Traditionelle Interaktionsschnittstellen stellen oft optionale Kontextinformationen in der Schnittstelle bereit, um genaue Absichten der Benutzer aus einfachen Klicks zu erfassen, während natürliche Sprache umfangreiche Texte organisieren muss, um den Kontext vollständig zu beschreiben. Durch Ergänzen von Kontextinformationen wie Zeit, Ort, Gerätestatus und Teilnehmeridentität im Protokoll kann KI die echten Semantiken von "hier und jetzt" genauer verstehen.
  > Wenn ein Benutzer beispielsweise nur sagt "buchen Sie ein Restaurant, das Marry in der Nähe mag", ergänzen Sie Standort, Budgetpräferenzen und historische Bestellungen als Kontextinformationen. Die Anwendung von Kontextinformationen ist sehr breit, und wir werden Szenarien später speziell diskutieren.

- **Übersetzen in Standard-Zwischensprache**: Nach der Verarbeitung ursprünglicher Informationen (Hinzufügen von Anmerkungen und Kontextinformationen), um eine vollständige und genaue Interpretation zu ermöglichen, ist ein vereinbartes Datenidentifikationssystem erforderlich. Um sich an die Ausdruckskraft aller Terminals anzupassen, kann dieses Identifikationssystem auf JSON-Spezifikationen aufgebaut werden und vereinbarte Parametertabellen und Strukturen bereitstellen. Auf diese Weise können KIs an verschiedenen Empfangsenden alle verfügbaren Terminals mobilisieren, um maximale Ausdruckskraft zu zeigen und die vollständige Bedeutung des Ausdrückers zu reproduzieren.
  > Ein Satz "senden Sie diesen Absatz an die Projektgruppe und lassen Sie alle vor Arbeitsende heute bestätigen" wird beispielsweise letztendlich in eine Standard-JSON-Struktur übersetzt, die Nachrichtenkörper, Empfängerliste, Frist und Bestätigungstastenkonfiguration enthält. Chat-Tools, Web-Backends oder mobile Apps können alle ihre jeweiligen angepassten Schnittstellen entsprechend rendern.

#### On-Demand-Angepasste Schnittstelle (KI → Mensch)

Unsere Prämisse ist, dass Menschen es vorziehen werden, mit KI durch "Sprechen" zu interagieren, was der menschlichen Kommunikation am nächsten kommt. Daher werden Menschen es zunehmend zu lästig finden, die benötigten Funktionsschnittstellen durch Klicken zu finden. Die Informationen und Schnittstellen, die Menschen benötigen, sollten direkt zu den "Augen" der Benutzer gepusht werden. Um diesen Effekt zu erzielen, sollten Empfangsenden bestimmte Interpretationsfähigkeiten haben:

- **Interpretieren der Zwischensprache**: Da die Zwischensprache im JSON-Format ist, können alle Empfangsenden vollständige Semantiken lesen und zumindest eine Trennung bei der Informationsempfang vermeiden.
  > Die gleichen Zwischensprachdaten einer "Spesenabrechnungsprüfanfrage" können beispielsweise als Großbildschirmschnittstelle mit Tabellen und Anhangsvorschau auf dem Desktop gerendert werden, zeigen nur wichtige Informationen und zwei Tasten (genehmigen/ablehnen) auf dem Mobilgerät, während intelligente Lautsprecher Zusammenfassungen vorlesen und auf Sprachbestätigung warten können.

- **Dynamisches Konstruieren von Nachrichtenschnittstellen**: Basierend auf vollständigem Kontext und Anmerkungen wählen Sie die interaktionsfreundlichste Lösung und setzen dynamisch eine interaktive Schnittstelle mit Informationshierarchie zusammen (natürlich können auch mit Terminals inkompatible Anmerkungen ignoriert werden). Diese Schnittstelle ist nicht unbedingt schreibgeschützte multimodale Information, kann aber auch ein interaktiver Mini-Programmkörper sein.
  > Wenn KI beispielsweise versteht "dies ist eine Informationssammlung", kann es automatisch eine ausfüllbare kleine Formularkarte in der Chat-Schnittstelle einfügen, anstatt Benutzer zu haben, die Fragen nacheinander in Klartext beantworten.

- **Reproduzieren des Kontexts**: Haben Sie die Fähigkeit, einige Elemente im Kontext anzuzeigen oder zu steuern. Dies erfordert normalerweise die Mobilisierung mehrerer Anwendungen oder Terminalgeräte. Wir haben gesehen, dass die Perspektive der ersten Person durch Kameras auf Brillen reproduziert werden kann, die Perspektive der dritten Person von Begleitdrohnen bedient werden kann und Projektion oder VR-Symbole auf eine bestimmte Position an physischen Objekten zeigen können... und so weiter.
  > In einem Szenario der Fernwartung von Geräten kann KI beispielsweise die Position von Schrauben, die demontiert werden müssen, im AR-Sichtfeld des Ingenieurs hervorheben, während gleichzeitig Schaltkreisdiagramme und Schrittanweisungen auf einem Großbildschirm angezeigt werden, wodurch "Kontext" gemeinsam über mehrere Terminals reproduziert werden kann.

#### ❗️❗️ Besonderer Hinweis: Ist Zwischensprache wirklich notwendig?

Viele Menschen denken, dass Zwischensprache tatsächlich nicht benötigt wird, im Allgemeinen aus zwei Gründen:

(1) Langfristig hat AGI die Fähigkeit, "zwischen den Zeilen zu lesen" und die impliziten Absichten der Benutzer zu verstehen. Es ist nicht notwendig, natürliche Sprache künstlich unnötig zu verarbeiten, nur um KI zu helfen, besser zu verstehen.

(2) Das Design menschfreundlicher Interaktionsschnittstellen ist auch AGIs Pflicht in der Zukunft, und KI kann sogar eine lauffähige Interaktionsschnittstelle speziell für jede Interaktion entwerfen. Daher ist es noch unnötiger, KIs Worte in eine Zwischensprache zu übersetzen.

Wir haben letztendlich immer noch das ICP-Protokoll im iFay-System entworfen. Wir haben die folgenden 3 Bedenken und glauben, dass sie kurzfristig schwer zu lösen sind, daher haben wir uns entschieden, eine Annotationsstil-Zwischensprache zu entwerfen:

(1) KIs Kontrolle über die Umgebung ist nicht so groß

Im Allgemeinen vergleichen Menschen Mensch-KI-Interaktionen mit der Kommunikation zwischen einer Person und einem Assistenten. Sie denken, dass ein intelligenter Assistent aktiv Umgebungsbedingungen anpassen wird, um gute Kommunikationseffekte zu erzielen, wie z. B. Lichter einschalten, wenn nicht genug Licht vorhanden ist; Markierungen an wichtigen Stellen von Dokumenten machen. Aber die Berechtigungen und Fähigkeiten von Assistenten erlauben es ihnen nicht immer, alles zu tun, wie z. B. wenn ein Gebäude plötzlich Strom verliert und Präsentationsfolien nicht abgespielt werden können.

Daher ist ein vorsichtigerer Ansatz, alle notwendigen Materialien vorzubereiten und die Präsentation anzupassen (oder sie dem Hausmeister zu überlassen). Dies ist, als würde man alle Materialien mitbringen, um einen Kunden zu treffen. Ob der Kunde einen Konferenzraum hat, ob Präsentationsfolien abgespielt werden können oder ob Papierberichte angesehen werden müssen, wird von der anderen Partei entschieden.

(2) KI und Menschen sind möglicherweise nicht so nah

Da KIs Kontrolle über die Umgebung begrenzt ist, versteht KI tatsächlich in vielen Fällen die menschliche Bedeutung nicht wirklich. Es ist, als würde man auf einen Datensatz auf einer Folie zeigen und KI fragen: "Was bedeutet diese Daten?" Tatsächlich weiß KI nicht, wo Sie zeigen. Idealerweise wären Bewegungsaufzeichnungsgeräte erforderlich, um KI diese Information mitzuteilen. Sie können sich auch ein anderes Szenario vorstellen: Ein Boss hält eine geschlossene Sitzung ab und sagt dem Assistenten danach: "Folgen Sie den Sitzungsbeschlüssen nach." Zu diesem Zeitpunkt hat der Assistent tatsächlich keine Informationen aus erster Hand erhalten, sondern Sitzungsprotokolle, die von einem Sitzungsprotokollführer organisiert wurden. Sitzungsprotokolle ähneln Informationen, die von Zwischensprache verarbeitet wurden.

Daher reichen in vielen Fällen die von Menschen explizit bereitgestellten Informationen nicht aus, um zu urteilen. Zu diesem Zeitpunkt müssen Kontextinformationen ergänzt werden, aber dies ist nicht die Autorität einer bestimmten KI.

(3) Es gibt möglicherweise überhaupt keine universelle AGI

Zukünftige KI wird definitiv auf die gleichen Arbeitsteilungsprobleme stoßen wie die menschliche Gesellschaft. Es wird individuelle KIs (ähnlich wie iFay) und KIs mit sozialen öffentlichen Funktionen (ähnlich wie coFay) geben. Zwischen ihnen wird es zwangsläufig Berechtigungsgrenzen geben.

Es ist schwierig für uns vorherzusagen, ob in der zukünftigen KI-Ökosystem die Verantwortung von KI nur darin besteht, bereitgestellte (Systemeingabe-)Informationen zu verarbeiten, oder ob KI auch dafür verantwortlich sein sollte, aktiv mehr "Implikationen" zu sammeln.

Daher wählen wir einen vorsichtigen Ansatz. Wir nehmen an, dass KI nur bekannte Informationen verarbeitet. Es ist nur so, dass diese Informationen jedes Mal durch einen Verarbeitungsfluss gehen, und diese Verarbeitungsaktion kann von einer Software, einem Terminalgerät oder einer KI abgeschlossen werden. Dies ist auch eine sehr reife Praxis in aktuellen technischen Lösungen, wie z. B. die Verwendung eines Browsers zum Zugriff auf eine Website, bei der der Server einen Teil der Kontextinformationen des Benutzers erfahren kann.

### 🌟 Vision

ICP (Interactive Conversation Protocol) zielt darauf ab, eine Zwischensprachform zwischen Menschen und Maschinen aufzubauen und eine effiziente, genaue und reichhaltige bidirektionale Kommunikation zwischen Menschen und Maschinen zu erreichen:

#### Mensch → Maschine: Umfassende Replikation von ausgedrückter Bedeutung und Kontext

- Die Bedeutung und den Kontext, die von Menschen ausgedrückt werden, so umfassend wie möglich erfassen
- Natürliche Sprache und Interaktionsabsichten in strukturierte Elemente umwandeln, die Maschinen genau verstehen können
- Interaktionspräzision und Kontextinformationen bewahren

#### Maschine → Mensch: Dynamische Zusammenstellung von Interaktionsmethoden

- Konzeptanmerkungen mit dem aktuellen Kontext integrieren
- Basierend auf Gerätefähigkeiten und Benutzerpräferenzen die am besten geeigneten Interaktionsmethoden dynamisch zusammenstellen
- Multi-perzeptive Informationspräsentation unterstützen (Text, Stimme, Vision, Berührung, Geruch usw.)

