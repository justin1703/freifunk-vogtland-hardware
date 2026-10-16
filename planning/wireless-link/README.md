# Planung einer Richtfunkverbindung zum Garagenkomplex

## 1. Zielsetzung

Ziel des Vorhabens ist es, einen bestehenden Freifunk-Vogtland-Uplink über eine drahtlose Punkt-zu-Punkt-Verbindung zu einem Garagenkomplex zu erweitern und dort einen zusätzlichen Freifunk-Zugang bereitzustellen.

Die Internet- und Freifunk-Anbindung erfolgt über den vorhandenen Anschluss am Ausgangspunkt. Der Netzwerkverkehr wird über eine Richtfunkstrecke zum Garagenkomplex übertragen. Dort stellt zum Beispiel ein TP-Link EAP225 Outdoor den WLAN-Zugang bereit.

Aktuell werden zwei mögliche Betriebskonzepte geprüft: Entweder übernimmt ein separater Offloader die Freifunk-Funktionalität und die Richtfunkgeräte übertragen den vorgesehenen Netzwerkverkehr einschließlich VLAN 30 transparent, oder die Richtfunkgeräte selbst werden – sofern die exakte Hardware unterstützt wird – mit einer geeigneten Freifunk-Firmware betrieben. Eine Entscheidung für eine der beiden Varianten ist noch nicht getroffen.

## 2. Ausgangssituation

- **Entfernung:** ca. 300 m
- **Ausgangspunkt:** bestehender Freifunk-Vogtland-Uplink
- **Zielstandort:** Garagenkomplex
- **Hindernisse:** Bäume, Äste und möglicherweise eine Gebäudeecke
- **WLAN-Access-Point am Ziel:** TP-Link EAP225 Outdoor V3.20
- **Netzwerktransport:** VLAN 30 muss transparent bis zum vorgesehenen Offloader transportiert werden
- **Montage am Ausgangspunkt:** ca. 82 cm lange Stange an einer Fenster- beziehungsweise Fassadenklemme

Die größte technische Unsicherheit ist die Funkstrecke selbst. Entfernung und Antennengewinn allein reichen nicht aus, um eine stabile Verbindung vorherzusagen. Insbesondere die Sichtverbindung, die Fresnelzone und der jahreszeitlich veränderliche Bewuchs müssen berücksichtigt werden.

## 3. Anforderungen an die Richtfunklösung

- Transparenter Transport von VLAN 30 über beide Funkendpunkte
- Ausreichende Nutzdatenrate und stabile Verbindung
- Möglichst geringe Windangriffsfläche und mechanische Belastung der vorhandenen Halterung
- Outdoor-Eignung für den vorgesehenen Montageort
- Möglichst langfristige und nachvollziehbare Firmwarepflege
- Wirtschaftlicher Betrieb und geringer Wartungsaufwand

## 4. Vergleich der Richtfunkgeräte

Die folgende Tabelle vergleicht fünf mögliche Lösungen für die geplante Verbindung. Die technischen Daten, Preise und Supportangaben sind vor dem Kauf anhand der konkreten Hardwareversion und der aktuellen Herstellerdokumentation zu überprüfen.

| Eigenschaft | TP-Link CPE210 | MikroTik SXTsq Lite2 | Ubiquiti NanoStation loco M2 | TP-Link CPE510 | TP-Link Omada EAP211-Bridge KIT |
|---|---|---|---|---|---|
| Geräteart | Einzelnes Richtfunkgerät | Einzelnes Richtfunkgerät | Einzelnes Richtfunkgerät | Einzelnes Richtfunkgerät | Komplettset mit zwei Bridge-Geräten |
| Frequenzband | 2,4 GHz | 2,4 GHz | 2,4 GHz | 5 GHz | 5 GHz |
| WLAN-Standard | 802.11b/g/n | 802.11b/g/n | 802.11b/g/n | 802.11a/n | 802.11ac |
| Beworbene maximale PHY-Datenrate | 300 Mbit/s | 300 Mbit/s | 300 Mbit/s | 300 Mbit/s | 867 Mbit/s |
| Antennengewinn | 9 dBi | 10 dBi | 8,5 dBi | 13 dBi | 7 dBi |
| Antennencharakteristik | Gerichtete integrierte Antenne | Gerichtete integrierte Antenne | Gerichtete integrierte Antenne | Gerichtete integrierte Antenne | Gerichtete integrierte Antenne |
| Öffnungswinkel horizontal | ca. 65° | Herstellerangabe prüfen | Herstellerangabe prüfen | ca. 45° | Herstellerangabe prüfen |
| Öffnungswinkel vertikal | ca. 35° | Herstellerangabe prüfen | Herstellerangabe prüfen | ca. 30° | Herstellerangabe prüfen |
| Ethernet-Anschluss | 1 × 100 Mbit/s bei v2/v3; v1 mit abweichender Anschlussausstattung | 1 × 100 Mbit/s | 1 × 100 Mbit/s | 1 × 100 Mbit/s | 3 × Gigabit-Ethernet je Gerät laut Produktangabe prüfen |
| Gigabit-Ethernet | Nein | Nein | Nein | Nein | Ja |
| Maximale Leistungsaufnahme | ca. 10,5 W | ca. 5 W | ca. 5,5 W | ca. 10,5 W | Versionabhängig |
| Stromversorgung | Passives PoE, typischerweise 24 V | Passives PoE, 10–30 V | Passives 24-V-PoE | Passives PoE, typischerweise 24 V | Versionabhängig |
| Schutzart | IPX5 | IP54 | ? | IPX5 | IP65 laut Produktversion prüfen |
| Abmessungen | ca. 224 × 79 × 60 mm | ca. 129 × 129 × 34 mm | ca. 161 × 31 × 80 mm | ca. 224 × 79 × 60 mm | ca. 224 × 79 × 60 mm je Gerät, Versionabhängig |
| Gewicht | Versionabhängig | Versionabhängig | ca. 180 g | Versionabhängig | Versionabhängig |
| Montage | Mast- beziehungsweise Stangenmontage | Kompakte Stangenmontage | Mastmontage, Halterung je nach Lieferumfang | Mast- beziehungsweise Stangenmontage | Mastmontage |
| Hersteller-Management | TP-Link Pharos Weboberfläche | RouterOS, WinBox und WebFig | airOS | TP-Link Pharos Weboberfläche | Omada-Management beziehungsweise Bridge-Modus, versionsabhängig |
| VLAN-Unterstützung | VLAN-Funktionen vorhanden; transparente Trunk-Übertragung im gewählten Bridge-Modus testen | Bridge und VLAN mit RouterOS konfigurierbar | Bridge- und VLAN-Funktionen versionsabhängig prüfen | VLAN-Funktionen vorhanden; transparente Trunk-Übertragung testen | VLAN- und Bridge-Verhalten für die konkrete Version prüfen |
| VLAN 30 für Freifunk | ? | Grundsätzlich flexibel konfigurierbar; Bridge-Konfiguration erforderlich | Konfiguration und Firmware vorab prüfen | ? | Für den konkreten VLAN-Trunk-Einsatz anhand der aktuellen Dokumentation prüfen |
| Verhalten bei Bewuchs | 2,4 GHz kann gegenüber 5 GHz Vorteile bieten; Äste und feuchte Blätter dämpfen dennoch stark | Wie andere 2,4-GHz-Lösungen | Wie andere 2,4-GHz-Lösungen | 5 GHz kann durch Bewuchs stärker beeinträchtigt werden | 5 GHz kann durch Bewuchs stärker beeinträchtigt werden |
| 300 m bei freier Sicht | Grundsätzlich gut möglich | Grundsätzlich gut möglich | Grundsätzlich gut möglich | Grundsätzlich gut möglich | Grundsätzlich gut möglich |
| 300 m mit Bäumen im Funkweg | Abhängig von Bewuchs und Sichtverbindung | Abhängig von Bewuchs und Sichtverbindung | Abhängig von Bewuchs und Sichtverbindung | Bei ausgeprägtem Bewuchs problematisch möglich | Bei ausgeprägtem Bewuchs problematisch möglich |
| Grobe Preisorientierung | ca. 40 € je Gerät | ca. 40 € je Gerät | ca. 50 € je Gerät | ca. 55 € je Gerät | ca. 65–70 € pro Gerät |
| Kosten für beide Funkendpunkte | ca. 80 € | ca. 80 € | ca. 90 € | ca. 110 € | ca. 130–140 € pro Set |
| Offizielle Firmwarepflege | Hardwareversion und Region beachten | RouterOS-Updates; modellbezogenen Produktstatus prüfen | Aktuelle Supportlage und Firmwarestatus prüfen | Hardwareversion und End-of-Life-Status beachten | Exakte Version und End-of-Life-Status prüfen |
| Größter Vorteil | Preiswert und 2,4 GHz | Kompakte Bauform, niedriger Verbrauch, flexible Konfiguration | Schmal und leicht | Höherer Antennengewinn im 5-GHz-Band | Komplettset und Gigabit-Ethernet |
| Größter Nachteil | 100-Mbit-Ethernet; Supportperspektive versionsabhängig | 100-Mbit-Ethernet; RouterOS erfordert Einarbeitung | 100-Mbit-Ethernet; Supportperspektive prüfen | 100-Mbit-Ethernet; 5 GHz bei Bewuchs nachteilig | 5 GHz bei Bewuchs nachteilig; Versionsstatus prüfen |
| Vorläufige Einschätzung | Preiswerte Option bei passender Version | Interessant bei kompaktem Aufbau und flexibler Konfiguration | Mechanisch attraktiv | Bei ausreichend freier Sicht interessant | Komfortable Komplettlösung bei geeigneter Funkstrecke |

**Hinweis:** Die Tabelle ist eine Vorauswahl, keine abschließende technische Freigabe. Einzelne Daten und Preisangaben sind abhängig von Hardwareversion, Region und Lieferumfang. Herstellerangaben sollten vor einer Beschaffung anhand aktueller Datenblätter überprüft werden.

## 5. Zusätzliche Komponenten und Netzwerkaufbau

| Komponente | Aufgabe | Wichtige Hinweise |
|---|---|---|
| Richtfunkgerät am Ausgangspunkt | Überträgt den Netzwerkverkehr zur Garage | VLAN 30 muss transparent transportiert werden |
| Richtfunkgerät an der Garage | Empfängt die Verbindung | Kompatibler Bridge-Modus und VLAN-Transport erforderlich |
| TP-Link EAP225 Outdoor V3.20 | Stellt WLAN für Nutzer bereit | Arbeitet als Access Point, nicht als Ersatz für die Richtfunkstrecke |
| VLAN 30 | Transportiert den vorgesehenen Freifunk-Verkehr | Portkonfiguration am Offloader und an den Bridge-Endpunkten abstimmen |
| PoE-Injektoren und Netzteile | Versorgen die Richtfunkgeräte | Spannung, Polarität und PoE-Verfahren exakt prüfen |
| Außenkabel und Überspannungsschutz | Verbindet die Komponenten und schützt die Installation | Außenkabel, Erdung und Schutzmaßnahmen fachgerecht planen |

## 6. Einschätzung der Firmwarepflege

Die langfristige Verfügbarkeit von Sicherheitsupdates ist ein wichtiges Auswahlkriterium. Eine allgemeine Update-Zusage eines Herstellers ist jedoch nicht automatisch eine Garantie für den gesamten Lebenszyklus eines bestimmten älteren Modells.

Vor der Auswahl sollten deshalb folgende Punkte geprüft werden:

- Ist die konkrete Hardwareversion noch offiziell unterstützt?
- Gibt es aktuelle Firmware für die vorgesehene Region?
- Ist ein End-of-Life- oder End-of-Support-Status veröffentlicht?
- Werden Sicherheitsupdates weiterhin bereitgestellt?
- Ist die Gerätekonfiguration langfristig dokumentierbar und wartbar?

Ein pauschales Ranking zur langfristigen Unterstützung sollte erst nach Prüfung der aktuellen, modellbezogenen Herstellerangaben festgelegt werden.

## 7. Montage und mechanische Randbedingungen

Die Befestigung am Ausgangspunkt erfolgt über eine ungefähr 82 cm lange Stange an einer Fenster- beziehungsweise Fassadenklemme.

Bei dieser Konstruktion sind nicht nur Gewicht und Abmessungen des Richtfunkgeräts entscheidend. Die Windangriffsfläche, die Hebelwirkung der Stange, die Belastbarkeit der Klemme und die Eignung für eine dauerhafte Außenmontage müssen ebenfalls berücksichtigt werden.

Eine kompakte Bauform kann Vorteile bieten, ersetzt aber keine Prüfung der Tragfähigkeit und der Befestigung.

## 8. Offene Prüfungen vor der Beschaffung

- Sichtverbindung zwischen Ausgangspunkt und Garagenkomplex prüfen
- Fresnelzone und mögliche Hindernisse bewerten
- Bewuchs bei unterschiedlichen Jahreszeiten berücksichtigen
- VLAN 30 mit den vorgesehenen Geräten praktisch testen
- Nutzdatenrate und Verbindungsstabilität messen
- Hardwareversionen und regionale Varianten festlegen
- Firmware- und Supportstatus überprüfen
- PoE-Versorgung und Lieferumfang beider Endpunkte prüfen
- Montage und mechanische Belastung beurteilen

## 9. Ergebnis und weitere Dokumentation

Die endgültige Geräteauswahl erfolgt nach Prüfung der Funkstrecke, des VLAN-Transports, der mechanischen Randbedingungen und der Firmwarepflege.

Nach der Inbetriebnahme wird diese Dokumentation um die tatsächlich verwendeten Geräte, die Konfiguration, Messergebnisse und Erfahrungen aus dem Betrieb ergänzt.