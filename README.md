# DBI 
![Github neueste Downloads](https://img.shields.io/github/downloads/rashevskyv/dbi/total.svg)

Diese Anleitung basiert auf [Brikachu's Arbeit](https://4pda.to/forum/index.php?showtopic=939714&st=1100#Spoil-86288632-5).

[Englische Anleitung](README_ENG.md)

[РУССКИЙ / Russische Anleitung](README_RUS.md)

Die ultimative Lösung zum Installieren von `NSP`, `NSZ`, `XCI` und `XCZ` und zum Arbeiten mit Nintendo Switch. Unterstützt Installation über MTP, USB, http (von Ihrem persönlichen Server), externem USB und mehr. Unterstützung zum Anzeigen von Bildern in den Formaten `jpg`, `png` und `psd`. Unterstützung für die Arbeit mit `zip`- und `rar`-Archiven sowie mit `cbr`/`cbz`-Containern. Unterstützung für Textdateien, einfache Textansicht und Hex-Ansicht. Kann als Dateimanager verwendet werden (Kopieren, Verschieben, Löschen von Dateien und Ordnern, Erstellen von Ordnern). Arbeit mit Saves (einschließlich Backup und Wiederherstellung) und vieles mehr.

## Inhalt: 

1. [Installation](#installation)
1. [Verwendung](#verwendung)
  1. [Benutzeroberfläche](#benutzeroberfläche)
  1. [Tasten](#tasten)
  1. [SD-Karte durchsuchen / USB0-Laufwerk durchsuchen](#sd-karte-durchsuchen--usb0-laufwerk-durchsuchen)
  1. [Titel von DBIbackend installieren](#titel-von-dbibackend-installieren)
  1. [Heimserver](#heimserver)
  1. [Installierte Anwendungen durchsuchen](#installierte-anwendungen-durchsuchen)
     * [Titel-Kontextmenü](#titel-kontextmenü)
     * [Detailliertes Spielmenü](#detailliertes-spielmenü)
      * [Inhaltsdatensätze](#inhaltsdatensätze)
      * [Tickets](#tickets)
      * [Saves](#Saves)
     * [Datensatz-Kontextmenü](#datensatz-kontextmenü)
  1. [Tickets durchsuchen](#tickets-durchsuchen)
     * [Tickets-Kontextmenü](#tickets-kontextmenü)
  1. [Werkzeuge](#werkzeuge)
  1. [Saves durchsuchen](#Saves-durchsuchen)
      * [Kontextmenü Installiert und Deinstalliert](#kontextmenü-installiert-und-deinstalliert)
      * [Backups-Kontextmenü](#backups-kontextmenü)
  1. [MTP-Responder ausführen](#mtp-responder-ausführen)
  1. [Aktivitätsprotokoll](#aktivitätsprotokoll)
    * [Anwendungen](#anwendungen)
    * [Aktivität](#aktivität)
  1. [Konfiguration und dbi.config-Parameter](#konfiguration-und-dbiconfig-parameter)
     * [Allgemein (`[Allgemein]`)](#allgemein-allgemein)
     * [Hauptmenü (`[Hauptmenü]`)](#hauptmenü-hauptmenü)
     * [Anwendungen (`[Anwendungen]`)](#anwendungen-anwendungen)
     * [Installationsoptionen (`[Installation]`)](#installationsoptionen-installation)
     * [MTP-Optionen (`[MTP]`)](#mtp-optionen-mtp)
     * [MTP-Speicher (`[MTP-Speicher]`)](#mtp-speicher-mtp-speicher)
     * [FTP-Optionen (`[FTP]`)](#ftp-optionen-ftp)
     * [Zugangspunkt (`[Zugangspunkt]`)](#zugangspunkt-zugangspunkt)
     * [Existiert in der Konfiguration, aber nicht im Menü](#existiert-in-der-konfiguration-aber-nicht-im-menü)
      * [Netzwerkquellen](#netzwerkquellen)
      * [Lokale Quellen](#lokale-quellen)
      * [Benutzerdefinierte MTP-Speicher](#benutzerdefinierte-mtp-speicher)
      * [Titelname überschreiben](#titelname-überschreiben)
  1. [Beenden](#beenden)
1. [Warnungen und Fehler](#warnungen-und-fehler)
	1. [Warnungen](#warnungen)
	1. [Fehler](#fehler)
   1. [Farbcodes](#farbcodes)
1. [dbi.config](#dbiconfig)
1. [Andere Optionen](#andere-optionen)
      * [Einbinden des Inhalts installierter Titel über MTP](#einbinden-des-inhalts-installierter-titel-über-mtp)
      * [Backup und Wiederherstellung von Saves über MTP](#backup-und-wiederherstellung-von-Saves-über-mtp)
      * [Verwenden von DBI zum Installieren von Mods](#verwenden-von-dbi-zum-installieren-von-mods)
      * [USB 3.0](#usb-30)
      * [Wiederherstellen sauberer BenutzerSaves aus dem Backup](#wiederherstellen-sauberer-benutzerSaves-aus-dem-backup)
      * [Bild als Avatar festlegen](#bild-als-avatar-festlegen)
      * [Dateien bearbeiten und anzeigen](#dateien-bearbeiten-und-anzeigen)
1. [Danksagungen](#danksagungen)

### Installation 

Kopiere `dbi.nro` und `dbi.config` auf deine SD-Karte unter `sdmc:/switch/DBI/`. DBI kann dann entweder im Applet-Modus (über Album) oder im Anwendungsmodus (Titelüberschreibung) gestartet werden, ist jedoch hauptsächlich für den Applet-Modus konzipiert.

*Wenn du DBI erfolgreich im Applet-Modus gestartet hast, siehst du einen blauen Hintergrund. Beim Starten im Anwendungsmodus wird ein schwarzer Hintergrund angezeigt.*

## Verwendung 

### Benutzeroberfläche
![2021041010520200](https://user-images.githubusercontent.com/18294541/114262830-d7643e00-99ea-11eb-8dbb-c8e0996577e5.jpg)
* **SD-Karte durchsuchen** — Installation von `NSP`/`NSZ`/`XCI`/`XCZ`-Dateien von der Speicherkarte.
* **USB0-Laufwerk durchsuchen** — Installation von `NSP`/`NSZ`/`XCI`/`XCZ`-Dateien von einem externen exFAT/FAT32-USB-Laufwerk wie einem USB-Stick, einer Festplatte usw.
* **Titel von DBIbackend installieren** — Installation von NSP/NSZ/XCI/XCZ-Dateien von einem PC über ein USB 2.0- oder 3.0-Kabel mit dem mitgelieferten Programm dbibackend. *Tastenkombination* für diese Option: **(Y)**-Taste.
* **Titel von Gamecard installieren** — Diese Option erscheint, wenn eine Spielkarte in die Switch eingelegt ist, und ermöglicht die Installation eines Spiels von der Spielkarte auf die SD-Karte oder den internen NAND-Speicher der Konsole.
* **Heimserver** — Ab Version v150 ist es möglich, Spiele über das Netzwerk (HTTP) über WLAN ohne Kabel oder einen LAN-USB-Adapter zu installieren. Weitere Details dazu findest du unten.
* **Installierte Anwendungen durchsuchen** — Anzeigen installierter Spiele, Gesamtzahl der installierten Spiele, Anzeige der verbrachten Spielzeit und der Anzahl der Starts, Überprüfung auf Fehler, Übertragung von Spieldaten zwischen internem Speicher, Speicherkarte und zurück, selektives oder kontinuierliches Löschen von Spielen und dazugehörigen LayeredFS-Mods, Anzeige von Updates und DLCs, manuelles Entfernen von DLCs/Updates/LayeredFS-Mods und die Funktion "Reset Required Version", um die Systemupdate-Überprüfung für ein ausgewähltes Spiel zurückzusetzen. *Tastenkombination* für diese Option: **(L)**-Taste.
* **Unnötige Dateien bereinigen** — Automatisches Reinigen von unnötigen gelöschten Spieldateien, falls vorhanden.
* **Tickets durchsuchen** — Anzeigen und manuelles Löschen von Spielsystem-Tickets.
* **Saves durchsuchen** - Anzeigen und Löschen von SpielSaves.
* **MTP-Responder ausführen** — Aktiviert den internen MTP-Server, um die Switch mit einem PC oder Android-Gerät (Handy/Tablet usw., getestet mit Pixel 3, Xiaomi Mi A1, Lenovo Tab 4 7" TB-7304X) zu verbinden, wo du die Speicherkarte (1: SD-Karte) und den internen Konsolenspeicher anzeigen und bearbeiten, installierte Spiele (4: Installierte Spiele) anzeigen, SpielSaves auf einem PC Speichern (7: Saves) und eine Spielkarte (vollständig/geschnitten/Zertifikat) auf einem PC/Android mit einer eingelegten Spielkarte (9: Spielkarte) dumpen kannst. *Tastenkombination* für diese Option: **(X)**-Taste.
* **FTP-Server ausführen** - Aktiviert den DBI-FTP-Server zum Zugriff auf SD-Dateien über Port 5000 oder zum Installieren von Dateien über Port 6000.
* **Beenden** — Beendet das Programm. *Tastenkombination* für diese Option: **(+)**-Taste.

Bottom left corner of DBI zeigt die Gesamtmenge der Daten auf deiner SD-Karte sowie die volle Kapazität an. In der unteren rechten Ecke findest du dieselben Informationen für den nutzbaren Speicherplatz deines NANDs in HOS.

Unten in der Mitte (dbi: XXX) steht die DBI-Version - du solltest immer die neueste Version verwenden.

### Tasten

* **(А)** - auswählen oder bestätigen
* **(B)** - abbrechen, verlässt das Programm **im Hauptmenü**
* **(X)** - Datei auswählen. Auf dem Hauptbildschirm - Schnelltaste zum Einbinden von MTP (Menüpunkt "[Run MTP responder](#run-mtp-responder)")
* **(Y)** - Auswahl umkehren, alles auswählen, wenn nichts ausgewählt ist. Auf dem Hauptbildschirm - Installation über USB mit dbibackend (Menüpunkt "[Install title from DBIbackend](#install-title-from-dbibackend)")
* **(ZL)** und **(ZR)** - Blättern durch Menüseiten, Blättern durch einzelne Spiele im detaillierten Spielmenü
* **(L)** - **im Hauptmenü** die Schnelltaste für die Menüoption "**Browse installed applications**"
* **(R)** - Ändern der angezeigten Sortierreihenfolge von Dateien/Titeln
* **(L3)** - Linken Stick klicken, um Spiele aus der Anwendungsliste oder dem detaillierten Spielmenü zu starten
* **(+)** auf dem rechten Joy-Con - Kontextmenü anzeigen, um Operationen wie Löschen, Zurücksetzen der erforderlichen Firmware-Version, Einbinden über MTP und mehr auszuführen
* **(-)** auf dem linken Joy-Con - Bildschirm ein-/ausschalten, wenn der MTP-Modus aktiviert/Spiele installiert werden

### SD-Karte durchsuchen / USB0-Laufwerk durchsuchen

Wähle diese Optionen aus, wenn du Spiele, Updates und DLCs von Dateien auf deiner SD-Karte oder von einem externen USB-Laufwerk installieren möchtest.
Drücke **(A)**, um den Ordner zu öffnen, und **(B)**, um zurückzukehren. Nach dem Öffnen des Ordners mit deinen Installationsdateien verwende die **(X)**-Taste, um einzelne oder mehrere Dateien für die Installation auszuwählen. Die **(Y)**-Taste kehrt deine Auswahl um, und die Farbe des Namens der ausgewählten Dateien ändert sich von weiß zu hellblau.

Drücke die **(A)**-Taste, um zu bestätigen. Ein Fenster mit Installationsoptionen wird angezeigt:

![2021041011441100](https://user-images.githubusercontent.com/18294541/114264183-18138580-99f2-11eb-8c7b-536b4b831195.jpg)

* **Gesamtübertragungsgröße** - die Gesamtmenge der ausgewählten Daten (NSP/NSZ/XCI/XCZ-Dateien) für die Installation
* **Gesamtinstallationsgröße** - die Menge an freiem Speicherplatz, die zum Installieren der ausgewählten Dateien erforderlich ist
* **Installationsziel** - wähle den Installationsort aus: **NAND** - interner Speicher der Nintendo Switch-Konsole, **SD** - SD-Karte, **AUTO** - standardmäßig wird dies auf deiner SD-Karte installiert, aber wenn nicht genügend Platz vorhanden ist, wird die Installation auf NAND (interner Speicher) zurückfallen
* **Nach der Installation löschen** - löscht Installationsdateien (NSP/NSZ/XCI/XCZ-Dateien) von der Quelle, nachdem sie erfolgreich installiert wurden; dafür muss das Attribut "Schreibgeschützt" von Dateien entfernt werden, falls vorhanden. Standardmäßig werden Dateien nicht gelöscht. Diese Option ist nur sichtbar, wenn von einer SD-Karte/externen USB-Laufwerk installiert wird
* **Bildschirm ausschalten** - schaltet den Bildschirm während der Installation zum Stromsparen aus. Nach erfolgreicher Installation wird der Bildschirm automatisch wieder eingeschaltet. Diese Option funktioniert nur im Handheld-Modus
* Wähle **Start installieren**, um mit der Installation zu beginnen. Nach erfolgreicher Installation erscheint "**Installation abgeschlossen. Drücke B, um zurückzukehren**"

*DBI entfernt automatisch und sofort alte Updates, wenn ein neues Update für ein Spiel installiert wird, sodass du dir keine Sorgen um den zusätzlichen Speicherplatz machen musst, den sie beanspruchen.*

Du kannst auch zu deinen Homebrew-Dateien navigieren und .nro-Dateien direkt starten, indem du sie markierst und **(A)** drückst.

### Titel von DBIbackend installieren

Wenn du den MTP-Responder von DBI nicht verwenden kannst, ist dies eine weitere bequeme Methode, um Titel über USB zu installieren. Die Installation über USB ermöglicht es dir, Dateien direkt von deinem PC zum Beispiel zu übertragen, was den Umstand vermeidet, zuerst die Datei auf deine SD-Karte verschieben zu müssen und sie dann zu installieren.

*Hauptmenü-Schnelltaste für diese Option*: **(Y)**-Taste

Um diese Option zu nutzen, benötigst du zunächst dbibackend (`dbibackend.exe` für Windows oder das `dbibackend`-Skript für alle Betriebssysteme). Starte dbibackend, wähle die zu installierenden Dateien aus, wähle "Server starten", verbinde ein USB-C-Kabel von deinem PC zu deiner Switch und wähle dann **Install title from DBIbackend** in DBI.

Für den ordnungsgemäßen Betrieb von dbibackend unter Windows müssen die Treiber "**libusbK (v3.1.0.0)**" installiert sein. Sie können über das [Zadig-Programm](https://zadig.akeo.ie/) installiert werden, indem du DBI in den "**Install title from DBIbackend**"-Modus versetzt und das Gerät auswählst, das im Programm erscheint.

Von hier aus kannst du deine Dateien auf der Switch genauso auswählen und installieren wie beim Durchsuchen der SD-Karte/des USB0-Laufwerks.

Um Dateien oder Ordner mit Spielen schnell zur Installation zu senden, klicke mit der rechten Maustaste darauf, wähle `Send from dbibackend` und die Installationsdateien werden sofort in die Warteschlange von dbibackend verschoben. Um dies in Windows zu konfigurieren, drücke `Win + R`, gib `shell: sendto` ein und erstelle eine Verknüpfung für `dbibackend.exe` im Ordner.

Es gibt alternative Clients für die Arbeit mit DBIbackend, zum Beispiel die [kopflose Implementierung](https://github.com/cyb3rwarden/dbibackend/blob/0885ef67edf28cbca30fb2c193ad7ab9a62786f7/dbibackend/dbibackend.py), [NSW-DBI 2.0.0 auf NodeGUI](https://4pda.to/forum/index.php?showtopic=939714&st=6080#entry100701109) (erfordert die Installation des libusb-Treibers für Linux oder WinUSB (libusb) für Windows über Zadig).

Du kannst Befehle an das Skript übergeben, indem du es von der Befehlszeile ausführst und dann den Pfad zum Spiel oder den Spielen angibst, die du installieren möchtest. Zum Beispiel:

```
python ~/dbi/dbibackend ~/Switch/File1.nsp ~/Switch/File2.nsp ~/Switch/File3.nsp
```

```
dbibackend.exe "e:\Switch\Games\File1.nsp" "e:\Switch\Games\File2.nsp" "e:\Switch\Games\File3.nsp"
```

#### Abhängigkeiten, die möglicherweise erforderlich sind, um unter MacOS oder Linux auszuführen

```bash
brew install python-tk
pip3 install pyusb
```

#### Installationsanweisungen für Ubuntu 22.04.3

Dies installiert die DBI-Abhängigkeiten und erstellt eine udev-Regel, um einem nicht-root-Benutzer den Zugriff auf eine über USB verbundene Switch zu ermöglichen.

```bash
pip3 install pyusb
sudo apt install python-tk
echo 'SUBSYSTEM=="usb", ATTRS{idVendor}=="057e", ATTRS{idProduct}=="3000", MODE="0666"' | sudo tee /etc/udev/rules.d/nintendo-switch.rules
sudo udevadm control --reload-rules
```

### Home-Server

Die Option **"Home-Server"** wird angezeigt, wenn der Abschnitt **Network install sources** in der Datei **[dbi.config](#dbiconfig)** konfiguriert wurde. Du kannst den Namen der Option wie erforderlich in der Konfigurationsdatei angeben.

Um Spiele über dein Netzwerk zu installieren, bearbeite die dbi.config-Datei, die sich im Ordner `sdmc:/switch/DBI/` befindet, wie benötigt. Zum Beispiel:

```
; Netzwerkinstallationsquellen
[Network sources]
; <Anzeigename>=<Typ>|<URL>
Home server=ApacheHTTP|http://192.168.1.47/Nintendo/Switch/
```

Installiere einen beliebigen HTTP-Server mit aktivierter Directory-Listing-Funktion auf deinem PC: Apache, Mongoose, Python SimpleHTTP, sheret, rclone usw.

Beispiel für nginx unter Windows:
Bearbeite die Datei `/nginx/conf/nginx.conf`, indem du die Adresse deiner Switch in `location` registrierst, anstelle der im Beispiel angegebenen `127.0.0.1` (oder dein gesamtes Subnetz wie 192.168.1.1/24 oder 192.168.0.0/16); diese finden Sie auf der Switch unter **Systemeinstellungen** > **Internet**:

```
location / {
root html;
index index.html index.htm;
}
location /Nintendo/Switch/ {
allow 127.0.0.1;
deny all;
autoindex on;
}
```

Speichere die Konfiguration, starte `nginx.exe`, erlaube dem Programm den Zugriff auf das Netzwerk, kopiere dann das gewünschte Spiel in den lokalen `/nginx/html/Nintendo/Switch/`-Ordner auf deinem PC, und auf der Switch wähle "Home-Server".
Du erhältst nun die gewohnte Benutzeroberfläche zur Installation von Dateien, und du kannst mit der Installation von Dateien über das Netzwerk beginnen. Du kannst den Webserver über `nginx -s stop` stoppen.

Für die Serveradresse in `dbi.config` kannst du auch einen Domainnamen verwenden, zum Beispiel deinen Remote-VPS - es wird empfohlen, dies mit HTTP-Basisauthentifizierung zu verwenden, z.B.: `http://user:password@host:port/Nintendo/Switch/`

Zum Beispiel:
```
ApacheHTTP|Netzwerk-Repo|http://127.0.0.1/Nintendo/Switch/
ApacheHTTP|WWW VPS-Repo|http://www.meineeigenevpsdomain.su/Nintendo/Switch/
```

Generiere die htpasswd-Datei, lege sie in /nginx/conf/ ab, und passe dann die nginx.conf-Datei wie folgt an:

```
        location /Nintendo/Switch/ {
			   satisfy all;
			   allow 127.0.0.1;
			   deny all;
			   auth_basic "Passwortgeschützter Bereich";
			   auth_basic_user_file htpasswd; 
               autoindex on;
        }
```

Login "switch", Passwort "pwd":

htpasswd-Datei:
```
switch:{SHA}N/omUzCtg+qoee+x4ttjgIls9jk=
```

### Installierte Anwendungen durchsuchen

In **Installierte Anwendungen durchsuchen** siehst du eine Liste der installierten Programme, Updates und DLCs mit ihrem belegten Speicherplatz, der Version (Anzeigeversion und Hex-Version), ihrer Titel-ID, der Gesamtspielzeit und der Anzahl der Starts sowie der vorhandenen LayeredFS-Mods für das Spiel (für Atmosphére).

*Hauptmenü-Hotkey für diese Option*: **(L)**-Taste

Oben in der Mitte wird die Gesamtzahl der installierten Spiele und der Sortierungstyp angezeigt.

![2021062719353200](https://user-images.githubusercontent.com/18294541/123554546-32efcd80-d789-11eb-8d3f-3124448624e0.jpg)

Auf der linken Seite in eckigen Klammern wird die Information zum Installationsort des Spiels, zum installierten Dateityp und zum Vorhandensein von LayeredFS-Mods oder Cheats angegeben:

* **N/S/M/G** - NAND/SD/Gemischt/Spielmodul - Ort der installierten Dateien, Gemischt zeigt an, dass installierte Dateien sowohl im NAND als auch auf der SD-Karte erkannt wurden
* **b** - BASE - das Basis-Spiel
* **u** - Update - installiertes Update
* **d** - DLC - installiertes DLC
* **l** - LayeredFS-Mod - LayeredFS-Mods oder Cheats für das Spiel wurden unter `sdmc:/atmosphere/contents/%Titel-ID%/` erkannt

Du kannst ein Spiel direkt aus der Liste starten, indem du es markierst und **(L3)** drückst.

**Bitte beachten!** Wenn das Spiel **rot markiert ist**, ist nur ein Update und/oder DLC installiert, das eigentliche Spiel ist NICHT installiert.

#### Titel-Kontextmenü

![2021062719354100](https://user-images.githubusercontent.com/18294541/123554557-3b480880-d789-11eb-9235-d547f2c588bd.jpg)

Angezeigt durch Klicken auf **(+)** auf dem ausgewählten Titel.

* **Titel löschen** - ausgewählte Titel löschen
* **Titel auf SD/NAND verschieben** - die ausgewählten Titel auf die SD-Karte oder den NAND verschieben, abhängig davon, wo sich der Titel derzeit befindet. Wenn Inhalte an beiden Orten installiert sind, werden beide Optionen angezeigt
* **Erforderliche Version zurücksetzen** - setzt die Versionsprüfung des Systems zurück, die erforderlich ist, um den Titel auszuführen (Debug muss in Atmosphere aktiviert sein)
* **Integrität überprüfen** - überprüft die Datenintegrität der ausgewählten Titel
* **Inhalte über MTP freigeben** - die Inhalte der ausgewählten Titel über MTP bereitstellen
* **Auf SD Speichern** - alle verfügbaren Inhalte (Spiel, DLC, Update) auf eine SD-Karte dumpen, wobei der im Config-File angegebene Pfad verwendet wird (Standard ist `switch/DBI/dumps`)
* **Inhaltsinfo** - zusätzliche Informationen zum Inhalt anzeigen (SDK-Version, erforderliche Schlüsselerstellung, ID, Patch-Informationen und mehr)

Wenn du die **(A)**-Taste auf dem Titel drückst, wird das **detaillierte Spielmenü** geöffnet.

### Detailliertes Spielmenü

Das **detaillierte Spielmenü** wird geöffnet, wenn du die **(A)**-Taste auf einem Titel drückst, während du dich im Menü zum Durchsuchen installierter Spiele befindest (**Installierte Anwendungen durchsuchen**)

![2021062719353600](https://user-images.githubusercontent.com/18294541/123554561-400cbc80-d789-11eb-8d81-e3403f33b365.jpg)

Im detaillierten Spielmenü werden das Symbol des Spiels, die Titel-ID, der Name, der Autor, die Version, unterstützte Sprachen und die Anwesenheit eines LFS-Mods angezeigt. Dieses Menü kann aufgerufen werden, indem du die **(A)**-Taste auf dem Kachel des Spiels drückst, während du dich im Menü zum Durchsuchen installierter Anwendungen befindest.

Darüber hinaus zeigt das Menü die Gesamtspielzeit, die Gesamtanzahl der Starts, den gesamten belegten Speicherplatz, den Speicherplatz im NAND und auf der SD-Karte, die Gesamtgröße der Saves und die erzwungene Sprache des Spiels an.

Darunter befinden sich drei Registerkarten, zwischen denen du mit den **(L)**- und **(R)**-Tasten wechseln kannst:

* **Inhaltsprotokolle**
* **Tickets**
* **Saves**

#### Inhaltsprotokolle

Die Informationen werden im folgenden Format angezeigt:

[Ort] Typ | Version [Versionsnummer] | Größe

**Ort** - **NAND** oder **SD**, abhängig davon, wo der Inhalt installiert ist
**Typ** - **Anwendung** für das Grundspiel, **Update** für Updates, **Addon** für DLC, und die Nummer des DLC wird daneben angezeigt
**Version [Versionsnummer]** - die Inhaltsversion in Dezimal- und [Hexadezimal] (zum Beispiel ist 786432 0.12.0.0)
**Größe** - belegter Speicherplatz

Durch Drücken der **(A)**-Taste auf dem Inhalt kannst du dessen Inhalt anzeigen. Der Inhalt kann kopiert werden, indem du das entsprechende Element im Kontextmenü auswählst (das sich durch Drücken der **(+)**-Taste öffnet). Der Inhalt wird im "read-only"-Modus geöffnet.

Wenn du die (+)-Taste auf dem ausgewählten Inhalt drückst, kannst du auf das Kontextmenü zugreifen, das Folgendes enthält:

* **Protokolle löschen** - löscht den ausgewählten Eintrag
* **Einträge auf SD/NAND verschieben** - verschiebt den ausgewählten Eintrag in den NAND oder die Speicherkarte, abhängig davon, wo er sich derzeit befindet. Wenn Teile des Titels an beiden Orten vorhanden sind, werden beide Optionen angezeigt.
* **Erforderliche Version zurücksetzen** - setzt die erforderliche Systemversionsüberprüfung für das Starten des Titels zurück (Debug muss in Atmosphère aktiviert sein). Dies hilft nicht, wenn das Spiel auf einer neuen SDK-Version erstellt wurde.
* **Sprache erzwingen** - ermöglicht das erzwungene Starten des Spiels mit einer ausgewählten Sprache. Standardmäßig wird das Spiel mit derselben im System ausgewählten Sprache ausgeführt, falls diese im Spiel nicht verfügbar ist, abhängig von der Konsolenregion. Die ausgewählte Sprache wird neben dem Spielsymbol im Feld **Erzwungene Sprache** angezeigt.
* **Integrität überprüfen** - überprüft die Integrität der ausgewählten Titeldaten.
* **Inhalte über MTP freigeben** - bindet den Inhalt der ausgewählten Titel über MTP ein.
* **Auf SD dumpen** - dumpen Sie alle verfügbaren Inhalte (Spiel, DLC, Update) auf die SD-Karte gemäß dem im Konfigurationsbereich festgelegten Pfad (Standard: switch/DBI/dumps).
* **Info zum Inhalt** - zeigt zusätzliche Informationen zum Inhalt an, einschließlich der SDK-Version, erforderlicher Schlüsselgeneration, ID, Patch-Informationen und vielem mehr.

#### Tickets

Ein **Ticket (oder verschlüsselter Titelschlüssel)** ist eine einzigartige verschlüsselte Information über die Rechte zur Ausführung von Spielinhalten, die während der Installation jedes Spiels (endend mit **000** in der Titel-ID)/Updates (endend mit **800** in der Titel-ID)/DLC im System installiert wird.

Installierte Tickets für Inhalte werden angezeigt, einschließlich:

- **Personalisiertes Ticket** - ein Ticket, das bei der Installation eines Spiels aus dem eShop vergeben wird und das für jeden Account personalisiert und einzigartig ist.
- **Allgemeines Ticket** - ein allgemeines Ticket, das für Updates vorhanden ist und auch als Workaround bei Raubkopien verwendet wird.

Die Spieldatenbanken auf den Nintendo-Servern sind mit demselben Schlüssel verschlüsselt, aber dieser Schlüssel ist mit seinem eigenen eindeutigen Schlüssel für jeden Spiellizenzinhaber (auf der Konsole generiert) verschlüsselt. Daher kann der Schlüssel zur Entschlüsselung des Spiels nur aus dem personalisierten Ticket auf der Konsole, für die es erstellt wurde, erhalten werden. Somit enthalten zwar personalisierte Tickets unterschiedliche Tickets für jeden Käufer, aber alle enthalten denselben Entschlüsselungsschlüssel. Allgemeine Tickets haben keine Verschlüsselung, sondern nur eine Signatur.

Durch Klicken auf die **(+)**-Taste auf dem ausgewählten Inhalt kannst du auf ein Kontextmenü zugreifen, in dem du ausgewählte Tickets löschen kannst.

In einigen Fällen, wenn ein bestimmter Fehler auftritt und du sicher bist, was du tust, kannst du es für ein bestimmtes Spiel und dessen Updates/DLC löschen. Es ist jedoch im Allgemeinen besser, die Tickets in Ruhe zu lassen, um Fehler beim Starten von Spielen zu vermeiden.

#### Saves (Spielstände)

Anzeigen und Löschen von Saves. Falls kein Save (Spielstand) vorhanden ist, kann es über das Kontextmenü (Taste (+)) für das ausgewählte Konto erstellt werden.

Falls ein Save vorhanden ist:

* **Backup** - Erstelle ein Backup des Saves. Standardmäßig wird das Backup im Ordner ~~switch/DBI/saves~~ gespeichert.Für Save Backups `DBI/saves` in die confin.ini einzutragen
* **Wiederherstellen** - Stelle das Backup des Saves wieder her.
* **Save info...** - Detaillierte Informationen über den Save wie Typ, Größe, Kontoname usw.
* **Speicherplatz für Save erhöhen** - Erhöhe den für den Save zugewiesenen Speicherplatz um einen bestimmten Wert.
* **Löschen** - Lösche den Save.

### Tickets durchsuchen

Hier kannst du Spiel-Tickets anzeigen und löschen. Ein **Ticket (oder verschlüsselter Titelschlüssel)** ist eine spezielle verschlüsselte eindeutige Information über die Rechte zur Ausführung des Inhalts des Spiels, die während der Installation jedes Spiels (**000** am Ende der Titel-ID) / Updates (**800** am Ende der Titel-ID) / jedes DLC im System installiert wird.

- **+** bedeutet, dass ein Spiel installiert ist.
- **[c]** (**Personalisiertes Ticket**) - ein Ticket, das beim Installieren eines Spiels aus dem eShop vergeben wird. Es ist personalisiert, was bedeutet, dass es mit einem einzigartigen Schlüssel von deiner Konsole verschlüsselt ist.
- **[p]** (**Allgemeines Ticket**) - eine gängige Art von Ticket, die für Updates verwendet wird und auch als Workaround für Raubkopien verwendet wird.

Die Spieldatenbanken auf Nintendo-Servern sind mit demselben Schlüssel verschlüsselt, aber dieser Schlüssel ist mit einem einzigartigen Schlüssel für jedes gekaufte Spiel verschlüsselt (dieser Schlüssel wird auf der Konsole selbst generiert). Daher ist es nur möglich, den Entschlüsselungsschlüssel für ein Spiel von einem personalisierten Ticket auf der Konsole zu erhalten, für die es erstellt wurde.
Dies bedeutet, dass alle gekauften personalisierten Tickets unterschiedlich sind, aber sie enthalten denselben Entschlüsselungsschlüssel für das Spiel.
Allgemeine Tickets hingegen haben keine Verschlüsselung, nur eine Signatur.

Manchmal kann es, wenn ein bestimmter Fehler auftritt und du genau weißt, was du tust, von einem bestimmten Spiel und seinem Update/DLC entfernt werden.

In den meisten Fällen ist es jedoch besser, hier nichts zu berühren, um Fehler beim Starten von Spielen zu vermeiden.

#### Kontextmenü für Tickets

Das Kontextmenü wird angezeigt, wenn du auf **(+)** auf ausgewählten Tickets klickst.

Oben im Kontextfenster wird die Anzahl der ausgewählten Tickets angezeigt.

- **Tickets löschen** - Lösche ausgewählte Tickets.
- **Gleiches Spiel auswählen** - Markiere alle Tickets, die mit dem ausgewählten Spiel zusammenhängen.

### Werkzeuge

- **Verwaiste Dateien bereinigen** - Bereinigt verlorene Dateien. Reinigt automatisch unnötige Spieldateien, Dateien von unterbrochenen/fehlgeschlagenen Spielinstallationen, offiziell heruntergeladene Firmware-Updates und alle unbenutzten Spieltickets, sofern vorhanden.
- **Elterliche Kontrollen löschen** - Entfernt vollständig elterliche Kontrollen. Kein Neustart erforderlich.
- **Benutzer löschen...** - Entfernt den ausgewählten Benutzer vollständig aus dem System (die entfernten BenutzerSaves bleiben im System erhalten).
- **Zufälliges Spiel starten** - Startet ein zufälliges Spiel aus den installierten Spielen.
- **NTP-Zeitsynchronisierung** - Synchronisiert die Zeit der Konsole mit einem entfernten Zeit-Synchronisationsserver. Eine Internetverbindung und korrekt eingestellte Zeitzone in den Konsoleneinstellungen sind für den Betrieb erforderlich.
- **Nach Titelupdates suchen** - Überprüft auf Updates und neue DLCs für installierte Spiele. Die Datenbank für die Überprüfung ist in den Einstellungen festgelegt.

### Saves durchsuchen

Anzeigen, speichern und Löschen von Saves.

Im Allgemeinen werden Saves im folgenden Format angezeigt:

`[Konto] Spielname Save Datum Größe`

- **Konto** - zeigt den Namen des Kontos an, für das der Save erstellt wurde. Wenn der Savetyp "Konto" ist, zeigt er den Namen des Kontos an, andernfalls zeigt er den Typ an.
- **Spielname** - zeigt den Namen des Spiels an, für das der Save erstellt wurde.
- **Save Datum** - zeigt das Datum an, an dem die Save erstellt wurde. Nur im Backup-Tab angezeigt.
- **Größe** - die Größe des Saves oder der Save.

Darunter befinden sich drei Registerkarten, die mit den **(L)** und **(R)** Tasten gewechselt werden können:

- **Installiert** - zeigt Saves für alle installierten Spiele an.
- **Deinstalliert** - zeigt Saves für alle deinstallierten Spiele an.
- **Saves** - zeigt erstellte Saves an.

#### Kontextmenü "Installiert" und "Deinstalliert"

Wird angezeigt, wenn **(+)** auf ausgewählte Saves gedrückt wird.

- **Speichern** - erstellt Saves der ausgewählten Saves.
- **Öffnen** - öffnet den Save.
- **Save-Info...** - zeigt Informationen zum Save an (ID, Typ, Größe, Erstellungszeit usw.).
- **Löschen** - löscht die ausgewählten Saves.
- **Gleiches Spiel auswählen** - wählt alle Saves aus, die mit dem ausgewählten Spiel zusammenhängen.
- **Apps durchsuchen** - geht zur [Datensatzkarte](#content-records) des ausgewählten Spiels. Sie können zwischen den Karten mit den **(ZL)**/**(ZR)**-Tasten wechseln. Nur im Tab "Installiert" verfügbar.

#### Kontextmenü "Saves"

Wird angezeigt, wenn auf **(+)** für ausgewählte Saves geklickt wird.

- **Saves überprüfen** - überprüft die Integrität der Saves.
- **Wiederherstellen** - stellt ausgewählte Saves wieder her.
- **Öffnen** - öffnet den ausgewählten Save.
- **Löschen** - löscht die ausgewählten Saves.
- **Apps durchsuchen** - geht zur [Datensatzkarte](#content-records) des ausgewählten Spiels. Sie können zwischen den Karten mit den **(ZL)**/**(ZR)**-Tasten wechseln. Nur im Tab "Installiert" verfügbar.
- **Gleiches Konto auswählen** - wählt alle Saves aus, die zu einem bestimmten Benutzer gehören.

Wenn mehrere Saves für ein Spiel und einen Benutzer in der Liste ausgewählt sind, wird nur die neueste Save wiederhergestellt.

**Run MTP responder** aktiviert den integrierten MTP-Server in DBI, um Daten mit einem PC oder einem Android-Gerät über USB-C OTG (Telefon/Tablet/andere Geräte) auszutauschen. *Hotkey, um diese Option aus dem Hauptmenü aufzurufen*: die **(X)**-Taste (auch zum Beenden von MTP verwendet). Nach dem Anschließen des USB-Kabels an den PC und dem Starten des MTP-Servers in DBI erscheint folgendes Fenster auf dem PC:

1: **SD-Karte** - zum Anzeigen, Kopieren und Löschen von Dateien und Ordnern von/nach einem PC und von/nach Ihrer SD-Karte. Ziehen Sie eine Datei größer als 4 GB auf die SD-Karte, und DBI teilt die Datei automatisch in einen archivierten Ordner auf, sodass die Switch sie als eine einzige Datei sieht. Auf diese Weise können Sie beispielsweise ganz einfach eine >4GB .XCI für die Verwendung in SX OS hinzufügen oder einen >4GB-Film für das Ansehen in NXMP oder pPlay hinzufügen.

2: **NAND-Benutzer** - Anzeigen und Kopieren von Dateien und Ordnern von der internen Speicherpartition des Switch zum PC (diese Partition ist schreibgeschützt).

3: **NAND-System** - Anzeigen und Kopieren von Dateien und Ordnern von der internen Speicherpartition des Switch zum PC (diese Partition ist schreibgeschützt).

4: **Installierte Spiele** - Alle installierten Spiele werden sowohl aus NAND (internem Speicher des Switch) als auch von der SD-Karte angezeigt. Um installierte Spiele im NSP-Format auf Ihren PC zu dumpen, kopieren Sie einfach den Ordner mit dem Namen des Spiels von "Installierte Spiele" auf Ihren PC. Ein gemeinsamer Ticket mit vollständig gelöschten persönlichen Informationen wird basierend auf Ihrem personalisierten Ticket generiert. Ihr Dump wird in separaten Dateien - dem Spiel selbst, dem Update und allen DLC-Dateien - vorliegen. Wenn Cheats oder Mods für das Spiel installiert wurden, befinden sie sich im Ordner `Mods & Cheats`. Sie können auch eine einzige kombinierte Multicontent-Datei dumpen, die das Spiel selbst, das Update und alle DLC enthält. Diese Dateien befinden sich im Stammverzeichnis des Ordners **Installierte Spiele**.

5: **SD install** - Lasse deine **NSP**/**NSZ**/**XCI** oder **XCZ**-Dateien in diesem Ordner fallen oder kopiere sie. Wenn der Transfer abgeschlossen ist, wird das Spiel auf der **SD-Karte** deiner Konsole installiert. Beachte, dass sich die tatsächliche Größe von NSZ- oder XCZ-Dateien nach der Installation erheblich von ihrer Originalgröße unterscheiden kann: Wenn du also beispielsweise mit 2 GB freiem Speicher auf deiner SD-Karte beginnst und nicht genügend Platz hast, um eine NSZ von 1 GB zu installieren, liegt das daran, dass NSZ- und XCZ-Dateien komprimiert sind und vor der Installation dekomprimiert werden müssen.

6: **NAND install** - Lasse deine **NSP**/**NSZ**/**XCI** oder **XCZ**-Dateien in diesem Ordner fallen oder kopiere sie. Wenn der Transfer abgeschlossen ist, wird das Spiel auf dem **internen Speicher** deiner Konsole installiert.

7: **Saves** - Zugriff auf alle Speichertypen, die im internen Speicher des Switch gespeichert sind: Konten **(Account)**, Systemprogramme **(System)**, Asymmetrische synchronisierte Hintergrundinhaltsübertragung (**BCAT**, zum Beispiel: Ereignisse in ACNH), temporäre **(Temporary)**, Cache (**Cache**, zum Beispiel: Add-Ons in DOOM), System-BCAT **(SystemBCAT)** und Gerätespeicher **(Device)**.

Sichere, wiederherstelle und verwalte Speicherdetails für installierte und deinstallierte Spiele. Du kannst Backups erstellen, indem du sie auf einen PC kopierst, und auch Speicher löschen, den du nicht mehr benötigst - öffne dazu den Ordner mit dem Namen des benötigten Spiels und lösche den entsprechenden Speicherordner.
Um Speicher wiederherzustellen, kopiere sie aus deinem PC in den entsprechenden Ordner. DBI erfordert kein Vorausstarten des Spiels vor der Wiederherstellung eines Speichers.

8: **Album** - Direkter Zugriff auf offizielle Album-Screenshots und Videos pro Spiel/Titel, ähnlich wie das offizielle Feature, das in OFW 11.0.0 hinzugefügt wurde.

9: **Gamecard** - Wenn eine Gamecard in den Switch eingelegt ist, kannst du diese auf dem PC als .XCI oder getrimmtes .XCI dumpen, zusammen mit dem darin enthaltenen Update, sofern vorhanden. Das persönliche RSA-Zertifikat wird automatisch entfernt und separat gedumpt.

Nach Aktivierung des MTP-Servers auf dem Switch erscheint ein Fenster mit deinem Kontonamen und deiner UID sowie der Anzahl der Saves:

![2021041013152900](https://user-images.githubusercontent.com/18294541/114266673-27013480-9a00-11eb-81ba-f1ff1c3c5abb.jpg)

#: **Benutzerdefinierter Speicher** - Wenn du ein benutzerdefiniertes virtuelles MTP-Laufwerk in der **[dbi.config](#dbiconfig)**-Datei definiert hast, wird es hier angezeigt.

Um den MTP-Server auszuschalten und zum Hauptmenü zurückzukehren, drücke entweder die **(X)**- oder **(B)**-Taste.

### Aktivitätsprotokoll

Zeigt Aktivitätsdiagramme in Spielen nach Datum für alle vorhandenen Benutzer für jedes spezifische Spiel an.

Beim Start werden zwei Registerkarten angezeigt, die mit den (L)- und (R)-Tasten gewechselt werden können:

Tasten-Kombi's:
* (L)/(R) - Zwischen den Tabs wechseln
* (ZL)/(ZR) - Ändern des Datums
* (Y) - Ändern des Anzeigezeitraums: Gesamtzeit, Tag, Monat, Jahr
* (X) - Sortierung: nach Spieletitel, nach Anzahl der Starts, nach verbrachter Zeit im Spiel
* (+) - Benutzer für die Anzeige auswählen

#### Anwendungen

Es wird eine Liste der Spiele angezeigt, für die Startstatistiken vorhanden sind. Oben im Fenster befindet sich eine Statuszeile vom folgenden Typ:

`[Spieler] Zeitraum. Insgesamt: Anzahl der Stunden (Sortiermethode)`. Zum Beispiel bedeutet die Zeile `[Alle Spieler] Januar 2023. Insgesamt: 72 Stunden (nach Spielzeit)`, dass die Statistiken **für alle Spieler für Januar 2023 angezeigt werden, sortiert nach Spielzeit, wobei 72 Stunden gespielt wurden**.

Das Fenster ist in drei Spalten unterteilt. Von links nach rechts:
  * Spieltitel
  * Anzahl der Starts
  * Zeit, die im Spiel verbracht wurde

Wenn du (A) auf ein Spiel drückst, gelangst du zur **Aktivität** für das aktuelle Spiel, wo Statistiken für das ausgewählte Spiel angezeigt werden. Wenn du (A) auf einen Eintrag drückst, gehst du tiefer (Jahr -> Monat -> Tag -> Stunde)

#### Aktivität

Die Aktivität wird als Diagramm für alle Spiele gleichzeitig angezeigt. Um zum Diagramm für ein bestimmtes Spiel zu gelangen, gehe zum Tab **Anwendungen** und wähle ein Spiel aus, um es anzuzeigen.

### Konfiguration und dbi.config-Parameter

Der Programm-Konfigurationsmanager ermöglicht eine einfache Konfiguration des Programms, ohne die Datei `dbi.config` manuell bearbeiten zu müssen.

Nachfolgend sind die Konfigurationspunkte über die GUI aufgeführt. Die entsprechenden Einträge in `dbi.config` werden in Klammern angegeben.

**true** in der Konfiguration entspricht **Ja** in den Einstellungen, **false** - **Nein**

#### Allgemein (`[General]`)

* **Externe USB-Laufwerke verwenden** (`UseLibUsbHsFS`) - true aktiviert die [libusbhsfs](https://github.com/DarkMatterCore/libusbhsfs)-Bibliothek für die Arbeit mit externen USB-Laufwerken über USB-OTG auf der Switch, false deaktiviert sie.
* **Direkter Ausgang zum Homescreen** (`ExitToHomeScreen`) - Wenn **false**, führt das Verlassen von DBI zum hbmenu, wenn **true**, zum Homescreen der Switch.
* **Ereignisse und Operationen protokollieren** (`LogEvents`) - ob Ereignisprotokolle für "*Install*", "*Integrität prüfen*" und "*Aufräumen*" gespeichert werden sollen oder nicht.
* **Update-Dateien hervorheben** (`HighlightUpdates`) - ob Updates für installierte Spiele im Dateimanager hervorgehoben werden sollen oder nicht.
* **Bildschirm umdrehen (180 Grad)** (`RotateScreen`) - dreht den Bildschirm um 180 Grad.
* **Joy-Con-Steuerung umdrehen** (`RotateJoycon`) - dreht die Steuerung um, um zum umgedrehten Bildschirm zu passen.
* **Unter- / Übertaktung verwenden** (`OptimizeClockSpeed`) - deaktiviert die Optimierung der SoC-Frequenz während der Leerlaufzeit. Standardmäßig deaktiviert, da dies **Lags auf dem Startbildschirm verursachen kann, wenn DBI nicht korrekt beendet wird**! Die korrekte Beendigung erfolgt über den Menüpunkt **Beenden**.
* **Save von Saves im read-only-Modus durchsuchen** (`ROSaveFS`) - Saves im read-only-Modus anzeigen.
* **'Von hier aktualisieren' anzeigen** (`ShowUpdateFromHere`) - zeigt die Schaltfläche "Alle Titel aktualisieren" im Kontextmenü zum automatischen Aktualisieren installierter Spiele aus allen verfügbaren Quellen (SD/USB/HTTP/FTP) an.
* **Ordner für Saves** (`SavesFolder`) - Ordner zum Speichern von Saves.
* **Protokollordner** (`LogsFolder`) - Ordner zum Speichern von Protokollen.
* **Ordner für Spiele-Dumps** (`DumpsFolder`) - Ordner auf der Speicherkarte, in dem Spiele gedumpt werden.
* **Versionsinformations-URL** (`VersionsURL`) - kann einen direkten Link zu einer Datei auf einem entfernten Server oder einer Datei auf der Speicherkarte akzeptieren. Beispiele: `https://raw.githubusercontent.com/blawar/titledb/master/versions.txt` oder `sdmc:/versions.txt`.
* **Cache-Wärmeindikator anzeigen** (`ShowCacheWarmingIndicator`) - zeigt eine Benachrichtigung an, wenn Informationen über installierte Programme gecacht werden.
* **Cursor nach Auswahl nach unten setzen** (`MoveDownAfterX`) - ob der Cursor nach Markierung eines Spiels mit der **(X)**-Taste nach unten bewegt werden soll oder nicht.
* **Bildschirm-Leerlaufzeit in Sekunden** (`ScreenIdleTimeout`) - Zeit bis zur Bildschirmabschaltung.
* **Tastenautomatik beim Halten** / **Autorepeat** (`Autorepeat`) - durch Halten der Taste im Menü navigieren
* **Cursor auf beiden Panels** / **Secondcursor** (`Secondcursor`) - ob der Cursor auf dem inaktiven Panel angezeigt werden soll oder nicht

**Existiert in der Konfiguration, aber nicht im Menü:**

* **AppSorting** - Optionen zum Sortieren der Liste der Anwendungen
* **SaveSorting** - Optionen zum Sortieren von Saves

#### Hauptmenü (`[MainMenu]`)

Einstellungen für die Menüpunkte, die im Hauptmenü von DBI angezeigt werden sollen. **Ja** in den Einstellungen entspricht **true** in der Konfiguration, **Nein** entspricht **false**.

* **SD-Karte durchsuchen** (`BrowseSD`) - Menüpunkt "[SD-Karte durchsuchen und USB0-Laufwerk durchsuchen](#browse-sd-card--browse-usb0-drive)", um Spiele von einer SD-Karte zu installieren
* **System durchsuchen** (`BrowseSystem`) - ermöglicht das Durchsuchen und Kopieren von Dateien aus der SYSTEM-Partition
* **Benutzer durchsuchen** (`BrowseUser`) - ermöglicht das Durchsuchen und Kopieren von Dateien aus der USER-Partition
* **USB durchsuchen** (`USBHost`) - Menüpunkt "**USB0-Laufwerk durchsuchen**", um Spiele von einem externen USB-Laufwerk zu installieren
* **Von USB installieren** (`BackendInstall`) - Menüpunkt "[Titel von DBI-Backend installieren](#install-title-from-dbibackend)", um Titel vom DBI-Backend zu installieren
* **Von Gamecard installieren** (`GameCard`) - Menüpunkt "**Titel von Gamecard installieren**", um Inhalte von Spielkarten auf den Systemspeicher zu installieren
* **Netzwerk durchsuchen** (`Network`) - Menüpunkt "**Heimserver**", um Spiele von einem Heim-Webserver zu installieren
* **SD-Verknüpfungen durchsuchen** (`Local`) - ob Links zu Ordnern im Abschnitt [Lokale Quellen](#local-sources) angezeigt werden sollen oder nicht
* **Anwendungen durchsuchen** (`BrowseApps`) - Menüpunkt "[Installierte Anwendungen durchsuchen](#browse-installed-applications)", um installierte Anwendungen zu verwalten
* **Verwaiste Dateien bereinigen** (`Cleanup`) - Menüpunkt "[Verwaiste Dateien bereinigen](#cleanup-orphaned-files)", um verwaiste Dateien von der Speicherkarte zu entfernen
* **Titelaktualisierungen überprüfen** (`UpdateCheck`) - Menüpunkt "**Nach Titelaktualisierungen suchen**", um nach Updates und DLC für installierte Spiele zu suchen
* **Tickets durchsuchen** (`Tickets`) - Menüpunkt "[Tickets durchsuchen](#browse-tickets)", um Tickets zu verwalten
* **Saves durchsuchen** (`Saves`) - [Saves durchsuchen](#browse-saves)
* **MTP-Server starten** (`MTP`) - Menüpunkt "[MTP-Server starten](#run-mtp-responder)", um MTP zu starten
* **FTP-Server starten** (`FTP`) - Menüpunkt "**FTP-Server starten**", um FTP zu starten

#### Anwendungen / Installierte Spiele (`[Applications]`)

* **LFS-Ordnergröße anzeigen (langsam)** (`CalculateLFSSize`) - Aktiviert oder deaktiviert die Berechnung der Größe installierter LFS-Mods. Wenn aktiviert, kann dies die Geschwindigkeit beim Öffnen des Menüs "*Installierte Anwendungen durchsuchen*" beeinträchtigen.

##### Installationsoptionen (`[Install]`)

* **Prüfen des Hash während der Installation** (`CheckHash`) - Wenn auf **true** gesetzt, wird der Hash von `.nca`-Dateien während der Spielinstallation auf der Switch überprüft. Wenn auf **false** gesetzt, wird er nicht überprüft.
* **Chunked HTTP/FTP-Übertragung** (`ChunkedTransfer`) - Aktiviert oder deaktiviert die segmentierte Übertragung von Daten über HTTP.

#### MTP-Optionen (`[MTP]`)

* **Kombinierte NSP anzeigen** (`ShowCombinedNSPInInstalledGames`) - Wenn auf **false** gesetzt, werden Mehrfachtitel-NSP-Dateien nicht im Menü "Installierte Spiele" im MTP-Modus angezeigt.
* **'Mods & Cheats'-Ordner anzeigen** (`ShowMACInInstalledGames`) - Wenn auf false gesetzt, wird das virtuelle Verzeichnis **Mods & Cheats** im Menü "Installierte Spiele" im MTP-Modus nicht angezeigt, das auf `sdmc:/atmosphere/contents/TITLEID/` auf der Speicherkarte verweist.
* **TitleID für 'Mods & Cheats' verwenden** (`MACasTID`) - Zeigt den Ordner "Mods & Cheats" im MTP-Modus als TitleID an.
* **Bildschirm ausschalten** (`TurnOffScreen`) - Aktiviert oder deaktiviert das Ausschalten des Konsolenbildschirms beim Anschließen im MTP-Modus.
* **Android-Erweiterungen** (`ReportAndroidExtension`) - Ob der entsprechende Befehlssatz bei der Arbeit mit MTP verwendet werden soll. Manchmal erkennen PC-Clients auf der Grundlage von libmtp (Mac oder Linux) das Gerät möglicherweise nicht korrekt, was zu einer Verringerung der Datenübertragungsgeschwindigkeit führen kann. In solchen Fällen wird empfohlen, diese Einstellung zu ändern.

**In der Konfiguration, aber nicht im Menü:**

* **LogAllFiles** - Wenn auf **false** gesetzt, werden Dateien kleiner als 4 MB beim Arbeiten mit MTP nicht protokolliert. Wenn auf **true** gesetzt, werden alle Dateien protokolliert.

#### MTP-Speicher (`[MTP Storages]`)

Zeigt die entsprechenden Elemente an, wenn [MTP Responder](#run-mtp-responder) mit einem PC/Android verwendet wird. Standardmäßig sind alle Elemente für die Anzeige aktiviert.

**true** - Anzeige im Hauptmenü, **false** - nicht anzeigen.

Die Namen der Elemente entsprechen den Abschnittsnamen.

* **SD-Karte** (`1: SD-Karte`)
* **Nand USER** (`2: Nand USER`)
* **Nand SYSTEM** (`3: Nand SYSTEM`)
* **Installierte Spiele** (`4: Installierte Spiele`)
* **SD-Installation** (`5: SD-Installation`)
* **NAND-Installation** (`6: NAND-Installation`)
* **Saves** (`7: Saves`)
* **Album** (`8: Album`)
* **Spielkarte** (`9: Spielkarte`)
* **Benutzerdefinierte Speicher anzeigen** (`CustomStorages`) - Anzeigen oder Ausblenden benutzerdefinierter Menüelemente, die im Abschnitt "MTP-Benutzerdefinierte Speicher" angegeben sind.

#### FTP-Optionen (`[FTP]`)

* **Bildschirm ausschalten** (`TurnOffScreen`) - Bildschirm ausschalten beim Betreten des FTP-Modus.
* **Lokalen Access Point starten** (`UseAP`) - Schaltet den Switch ein, damit er als Zugriffspunkt arbeiten kann, zu dem FTP-Clients direkt eine Verbindung herstellen können. Unten befinden sich Einstellungen für diesen Zugriffspunkt.
* **Dateidatum lesen** (`ReadMT`) - Ob das Änderungsdatum der Datei gelesen werden soll oder nicht.

#### Zugriffspunkt (`[Access point]`)

* **SSID** (`SSID`) - der Name des Zugriffspunkts.
* **Passwort** (`Password`) - das Passwort.
* **5 GHz verwenden** (`Use5GHz`) - ob 5 GHz verwendet werden soll. Wenn es deaktiviert ist, wird es im 2,4 GHz-Modus arbeiten.
* **Versteckte SSID verwenden** (`Hidden`) - die SSID für die Suche verstecken. Dies bedeutet, dass sie nur verbunden werden kann, indem die angegebene SSID eingegeben wird.

#### Existiert in der Konfiguration, aber nicht im Menü

##### [Netzwerkquellen](#network-sources)
Namen und Adressen zur Einrichtung von Netzwerkinstallationen (über WLAN/LAN-Adapter)

**NSP-Indexer** - Adresse für das Indexieren von NSP ([Details](https://github.com/rashevskyv/dbi/issues/44))

##### **Lokale Quellen**

Erstellen Sie Menüelemente mit schnellem Zugriff auf ausgewählte Ordner auf der Speicherkarte, die in der Konfiguration konfiguriert sind (ähnlich wie "Verknüpfungen"), zum Beispiel:

`Homebrew Shortcut=sdmc:/switch` erstellt ein Menüelement "**Homebrew Shortcut**", das den Ordner `sdmc:/switch` öffnet.

##### **MTP-Benutzerdefinierte Speicher**

Benutzerdefinierte Elemente für den MTP-Modus für schnellen Zugriff auf Ordner auf Ihrer Speicherkarte. Format: `<angezeigter_Ordnername>=<Pfad>`, zum Beispiel: `Homebrew=sdmc:/switch`.
Im MTP-Modus wird ein `Homebrew`-Ordner angezeigt, der auf den `switch`-Ordner auf Ihrer Speicherkarte verweist.

##### **Titelnamenüberschreibung**

Ermöglicht es, den angezeigten Titelnamen zu ändern. Wenn du zum Beispiel `10023901191C000=Naheulbeuk` angibst, wird in der Anwendung anstelle von `The Dungeon of Naheulbeuk: The Amulet of Chaos` einfach `Naheulbeuk` angezeigt.

### Beenden

**Beenden** - beendet das Programm und kehrt zum HOS zurück, umgeht hbmenu oder kehrt zu hbmenu zurück (konfigurierbar in dbi.config); wenn DBI von einem Titel/Forwarder aus gestartet wurde, wird das Programm neu gestartet oder bleibt auf einem schwarzen Bildschirm.

## Warnungen und Fehler
### Warnungen

In Orange dargestellt. Dies sind KEINE Fehler!

* **[SIGNATURE: Ungültig]**, **[SIGNATURE: XCI->NSP]**, **[HASH NICHT MIT META ÜBEREINSTIMMEND]**, **[HASH IN META BEHOBEN]** — dies sind KEINE Fehler, sondern Benachrichtigungen über eine Signaturenungleichheit in den Headern, zum Beispiel bei der Verwendung von Konvertierung oder Bearbeitung, benutzerdefiniertem NSP, Forwarder.
* **HASH-UNSTIMMIGKEIT** — meistens KEIN Fehler, das Spiel wurde von einer Cartridge konvertiert (dann ist alles in Ordnung), manchmal gibt es Probleme mit der Dateiintegrität, lade sie erneut herunter/hash sie erneut, übertrage Daten über das USB-Kabel/USB-Port/beim Installieren zwischen PC und Switch.
Wenn das Spiel nicht startet oder mit einem Fehler startet, versuche es erneut zu installieren, überprüfe oder ersetze das USB-Kabel/SD-Ändere den USB-Port.
* **[DELTA ÜBERSPRUNGEN]** — dies ist KEIN Fehler, sondern eine Benachrichtigung, dass unnötige Fragmente in der Update-Datei übersprungen wurden, wenn sie vorhanden waren, wie es sein sollte.
* **Keine Tickets gefunden** — dies ist KEIN Fehler, es beeinträchtigt nicht die Funktionalität des Spiels, informiert aber darüber, dass das Spiel ohne Tickets ist. Es kann sich um einen Dump aus einer .XCI-Cartridge handeln oder um eine Konvertierung in Standard Crypto.
* **Anwendung verwendet AddonContent-Titel-ID**, **Anwendung verwendet Update-Titel-ID** — dies ist KEIN Fehler und zeigt in der Regel ein Homebrew-Spiel in .NSP an, das nicht nach Standard erstellt wurde, zum Beispiel wenn das AddonContent-Flag (DLC) dem Anwendungstitel (Hauptspiel, v0) hinzugefügt wurde.
Wenn ein solches Spiel startet und funktioniert, ist alles in Ordnung.
* **Diese Anwendungsgrundlage ist nicht eigenständig. Stelle sicher, dass du das Update installiert hast** - beim Installieren neuer Sparse Storage-Spiele — dies ist KEIN Fehler, vergiss nicht, zusätzlich zur Basisspieldatei auch ein Update dafür zu installieren, bevor du es startest.

### FEHLER

* **USB-Kommunikation fehlgeschlagen** - Überprüfe/ersetze das USB-Kabel und den USB-Port am PC.
* **Metadateninhalt kann nicht analysiert werden**:
  * **Alte Firmware** - deine Firmware ist zu veraltet, um die Metadatendatei zu analysieren. Aktualisiere die CFW und die Systemsoftware auf die neuesten Versionen.
  * **Unerwarteter Fehler** - die Datei ist beschädigt. Überprüfe und lade die Datei erneut herunter.
* **Ungültige PFS0-Magie!** - Lade die Installationsdatei des Spiels erneut herunter und überprüfe ihre Integrität, da diese Datei beschädigt ist.
* **[UNGÜLTIGE NCA-MAGIE]** - Aktualisiere auf die neueste Version von OFW und CFW, und überprüfe bei fortbestehendem Fehler die Integrität der Installationsdatei des Spiels erneut.
* **Installation abgebrochen** - Datenübertragungsfehler, überprüfe und falls erforderlich, ersetze das USB-Kabel/USB-Port zwischen der Switch und dem PC. Stelle außerdem sicher, dass du die neueste Version der Software installiert hast, wie in diesem Beitrag.
* **Nichts zu installieren** - Im Dateiauswahlmenü benenne die Datei ohne Sonderzeichen, Hieroglyphen oder kyrillische Buchstaben im Namen und Pfad um.
* **Transferfehler**, **[ÜBERTRAGUNGS CRC FEHLER]**, **[ÜBERTRAGUNG ABGEBROCHEN]** - Überprüfe die USB-C-Kabelverbindung und den USB-Port, überprüfe mit anderen USB-C-Kabeln, überprüfe die Integrität der Spieledatei und der Speicherkarte auf Fehler. Beim Installieren über MTP starte dbi durch ein beliebiges Spiel (Titel), während du die (R)-Taste gedrückt hältst, anstatt im Applet-Modus über Alben.
* **Fehler aufgetreten: Ungültiges Argument** - Aktualisiere deine dbi auf die neueste Version.
* **EINIGE INHALTE FEHLEN. DIE ANWENDUNG WIRD UNBENUTZBAR SEIN** - ein beschädigtes Dateisystem auf der Speicherkarte oder ein nicht funktionierendes/schlecht verarbeitetes Flash-Laufwerk. Überprüfe es mit chkdsk und h2testw; wenn keine Fehler gefunden werden, formatiere es neu mit FAT32.
* **[NICHT GENÜGEND SPEICHERPLATZ]**, **[PLATZHALTER KANN NICHT ERSTELLT WERDEN]** - Es gibt nicht genügend Speicherplatz auf der Speicherkarte/NAND, schaffe mehr Platz oder überprüfe die Speicherkarte. Überprüfe es mit chkdsk und h2testw; wenn keine Fehler gefunden werden, formatiere es neu mit FAT32.
* **Zusätzliche Puffer überschritten. Die Schreibgeschwindigkeit des Mediums ist zu niedrig** - Beim Installieren über MTP starte dbi durch ein beliebiges Spiel (Titel), während du die **(R)-Taste** gedrückt hältst. Alternativ verwende einen NSP-Forwarder und eine schnellere SD-Karte mit einem anderen USB-Kabel/Port.
* **Keine Tickets gefunden, aber sie sind erforderlich** - Ein falscher (unvollständiger, ohne Ticket, aber mit Titelrechten) Spieledump, finde einen anderen.
* **Ungültiges personalisiertes Ticket** - Dieser Fehler tritt am Ende der Spielinstallation auf, wenn ein .tik-Ticket installiert wird, und deutet darauf hin, dass ein falscher Spieledump verwendet wurde, bei dem ein personalisiertes Ticket von der Konsole, auf der das Spiel gekauft wurde, anstelle eines gemeinsamen Tickets verbleiben wurde. Bitte lade einen anderen korrekten Dump herunter.
* **Keine ES-Sigpatches vorhanden!** - Diese Fehlermeldung bedeutet, dass die ES-Sigpatches veraltet, falsch oder nicht auf der Konsole installiert sind. Bitte installiere die neueste Version der ES-Sigpatches.

  ### Farbcodes:

* In allen Menüs
  * <span style="color:#ffffff; background-color: black;">WEISS auf SCHWARZEM HG</span> - fokussiert
  * <span style="color:#008578; background-color: #000084;">BLAU</span> - ausgewählt (mit **(X)**-Taste)
* In "**SD-Karte durchsuchen**"
  * <span style="color:#c7c6d6; background-color: #000084;">WEISS</span> - Ordner
  * <span style="color:#80878f; background-color: #000084;">HELLGRAU</span> - Datei
  * <span style="color:#414e54; background-color: #000084;">DUNKELGRAU</span> - installiertes Spiel
  * <span style="color:#3bce28; background-color: #000084;">GRÜN</span> - Update oder DLC für installiertes Spiel
* In "**Installierte Anwendungen durchsuchen**"
  * <span style="color:#cebfde; background-color: #000084;">WEISS</span> - installiertes Spiel
  * <span style="color:#8e0000; background-color: #000084;">ROT</span> - installiertes Update oder DLC ohne Spiel
* **In Protokollen** bei der Installation:
  * <span style="color:#00ff02; background-color: #000084;">GRÜN</span> - keine Fehler
  * <span style="color:#fa7f08; background-color: #000084;">ORANGE</span> - keine Fehler, aber Warnungen (zum Beispiel, installierte NSP ist XCI-Konvertierung oder Hash wurde in Meta repariert)
  * <span style="color:#f80100; background-color: #000084;">ROT</span> - [Fehler](#fehler). Datei wurde nicht installiert
* **In Protokollen** nach der Installation:
  * <span style="color:#00ff02; background-color: #000084;">GRÜN</span> - endete ohne Fehler
  * <span style="color:#f6ff05; background-color: #000084;">GELB</span> - endete ohne Fehler, aber mit Warnungen
  * <span style="color:#f80100; background-color: #000084;">ROT</span> - endete mit Fehlern
  
Die `dbi.config`-Datei ist für die Speicherung der Programm-Einstellungen verantwortlich. Sie befindet sich neben `DBI.nro`. 
Hier ist ihr Inhalt:
```
; Allgemeine Einstellungen
[General]
; Verwenden von libusbhsfs für den Zugriff auf USB-Massenspeicherlaufwerke, die an Switch oder Dock angeschlossen sind
UseLibUsbHsFS=true
; Direkter Startbildschirm
ExitToHomeScreen=false
; Ordner, in dem Backups von Saves gespeichert werden
SavesFoldDBI/
; Protokollierung von "Installieren", "Integrität prüfen" und "Aufräumen" Prozessen
LogEvents=false
; Ordner, in dem Protokolle gespeichert werden
LogsFolder=sdmc:/DBI/logs/
; Ordner, in dem Spiele-Dumps gespeichert werden
DumpsFolder=sdmc:/DBI/dumps/
; Sortierungsoptionen für die Anwendungsliste
AppSorting=LastPlayed,InstallLocation,Size,Name
; Sortierungsoptionen für die Speicherliste
SaveSorting=AppLastPlayed,AppName,UserUid,Size,SaveId
; Hervorhebung von Dateien mit Updates für aktuell installierte Titel im Dateibrowser
HighlightUpdates=true
; Bildschirm umdrehen
RotateScreen=false
; Joy-Cons umdrehen
RotateJoycon=false
; CPU in Menüs untertakten, um den Batterieverbrauch zu reduzieren
OptimizeClockSpeed=false
; URL mit Titelversionen im Format <id>|<rightsId>|[version]
VersionsURL=https://raw.githubusercontent.com/blawar/titledb/master/versions.txt
;VersionsURL=sdmc:/versions.txt
; Durchsuchen von Speichern im read-only-Modus
ROSaveFS=true
; "Alle Elemente von hier aktualisieren..." im Kontextmenü der Dateibrowser anzeigen
ShowUpdateFromHere=false
; Anzeigen des Cache-Wärmezeichens
ShowCacheWarmingIndicator=true
; Cursor nach Auswahl nach unten bewegen
MoveDownAfterX=true
; Bildschirm-Leerlaufzeit in Sekunden
ScreenIdleTimeout=0
; Auto-Wiederholung von Navigationsbuttons beim Halten
Autorepeat=true
; Cursor auf beiden Panels in Zwei-Panel-Browsermodus anzeigen
Secondcursor=false
; Backup von Saves erstellen vor dem Löschen
FoolproofSaveDelete=true

; Sichtbarkeit der Hauptmenüpunkte
[MainMenu]
; Durchsuchen und Installieren von Dateien von der SD-Karte
BrowseSD=true
; Durchsuchen und Kopieren von Dateien von der SYSTEM-Partition
BrowseSystem=false
; Durchsuchen und Kopieren von Dateien von der USER-Partition
BrowseUser=false
; Durchsuchen und Installieren von Dateien von USB-Flash-Laufwerken und HDD
USBHost=true
; Durchsuchen und Installieren von Dateien vom PC über dbibackend
BackendInstall=true
; Spiel von eingelegter Spielkassette installieren
GameCard=true
; Durchsuchen und Installieren von Dateien von konfigurierten Netzwerkquellen
Network=true
; Durchsuchen und Installieren von Dateien von konfigurierten SD-Kartenordnern
Local=true
; Installierte Anwendungen durchsuchen
BrowseApps=true
; Aufräumen von Dateien von schlechten Installationen/alten Updates/unbenutzten Tickets usw.
Cleanup=true
; Nach App-Updates suchen
UpdateCheck=true
; Anzeigen, wo installierte Tickets angezeigt oder gelöscht werden können
Tickets=false
; Anzeigen, wo Saves angezeigt oder gelöscht werden können
Saves=true
; MTP-Responder
MTP=true
; FTP-Server
FTP=true

[Applications]
; Ob LFS-Mod-Größe überprüft wird oder nicht
CalculateLFSSize=false

; Installationsoptionen
[Install]
; Überprüfen des NCA-Hash während der Installation
CheckHash=true
; Chunked HTTP-Übertragung verwenden (gut in schlechten Umgebungen)
ChunkedTransfer=true

; MTP-Optionen
[MTP]
; Alle Dateien protokollieren, wenn deaktiviert, wird nur für Dateien >= 2 MB übertragen
LogAllFiles=false
; NSP anzeigen, das Basisspiel, neuestes Update und alle DLCs in einer einzigen Multi-Titel-Datei enthält
ShowCombinedNSP=true
; Virtuellen "Mods & Cheats"-Ordner anzeigen, der auf sdmc:/atmosphere/contents/TITLEID umleitet
ShowMAC=true
; TitleID für "Mods & Cheats"-Ordner verwenden
MACasTID=true
; Benutzerdefinierte Verknüpfungen zu MircoSD-Ordnern als separate Speicher anzeigen
CustomStorages=true
; Bildschirm beim Starten des MTP-Modus ausschalten
TurnOffScreen=false
; Android-Erweiterungen melden (einige Initiator denken, dass Android Fehler hat)
ReportAndroidExtension=true

; FTP-Optionen
[FTP]
; Bildschirm beim Starten des FTP-Modus ausschalten
TurnOffScreen=false
; Lokalen Zugriffspunkt für FTP-Server starten
UseAP=false
; Dateiänderungszeit lesen (kann bei großen Verzeichnissen verlangsamt

 werden)
ReadMT=false

; Access-Point-Optionen
[Access point]
SSID=
Password=
Use5GHz=true
Hidden=false

;De- und Aktivieren diverser MTP-Speicher
[MTP Storages]
1: SD-Karte=true
2: Nand USER=false
3: Nand SYSTEM=false
4: Installierte Spiele=true
5: SD-Karte installieren=true
6: NAND installieren=false
7: Saves=true
8: Album=true
9: Spielkassette=true

; Netzwerk-Installationsquellen
[Network sources]
; <Anzeigename>=<Typ>|<URL>
; NSP-Indexer=URLList|http://192.168.1.47/nspindexer/index.php?DBI
; Heimserver=ApacheHTTP|http://192.168.1.47/Nintendo/Switch/
; Test-FTP=FTP|ftp://anonymous:password@192.168.1.24:2121/

; Hauptmenüverknüpfungen zu SD-Kartenstandorten
[Local sources]
; <Anzeigename>=<Pfad>
Homebrew=sdmc:/switch
; Inhalte=sdmc:/atmosphere/contents
; DBI-Protokolle=sdmc:/switch/DBI/logs

[MTP custom storages]
; <Anzeigename>=<Pfad>
Homebrew=sdmc:/switch/
Screenshots=sdmc:/Nintendo/Album/

; Überschreiben des Anzeigenamens
; <GROSSGESCHRIEBENE TID>=<Gewünschter Name>
[Title name override]
; 010023901191C000=Naheulbeuk
```

Die Beschreibung jedes Elements findest du im Abschnitt [DBI Einstellungen](#configuration-and-dbiconfig-parameters).

### Montage des Inhalts installierter Titel über MTP

1. Gehe zu "**Installierte Anwendungen durchsuchen**" -> Wähle die Apps aus, die du mit **(X)** montieren möchtest -> Drücke **(+)** -> "**Inhalte über MTP freigeben**"

### Save und Wiederherstellung von Saves über MTP

1. Verbinde deine Konsole im MTP-Modus über DBI.
2. Navigiere zum **Saves**-Ordner auf deinem PC.
3. Du kannst entweder deine Saves auf deinem PC kopieren oder sie einfach durch Ziehen in diesen Ordner wiederherstellen.

### Verwendung von DBI zur Installation von Mods

1. Verbinde dich im MTP-Modus über DBI mit deinem Computer.
2. Gehe zu **Installierte Spiele**, in den Ordner mit dem Namen deines Spiels.
3. Gehe zum Ordner **Mods & Cheats**.
4. Platziere deinen Mod im **Mods & Cheats**-Ordner.
   * **Hier aufpassen!**, du musst sicherstellen, dass du den Inhalt des Ordners mit der titleID kopierst und nicht den titleID Ordner selbst! Zum Beispiel hast du eine Übersetzung für das Spiel Cadence of Hyrule heruntergeladen, in Form des Archivs `Cadence of Hyrule.rar`. In diesem Archiv siehst du einen Ordner mit der titleID `01000B900D8B0000`des Spiels. Extrahiere das Archiv, öffne den Ordner `01000B900D8B0000` und den kopiere den gesamten Inhalt des Ordners **in** den **Mods & Cheats**-Ordner! Nicht den Ordner `01000B900D8B0000` selbst, sondern alles darin! In diesem Beispiel (und in den meisten Fällen) wäre darin der `romfs`-Ordner. 
   
   ### USB 3.0 
   
   DBI unterstützt USB 3.0. Wenn du Kefir verwendest, ist USB 3.0 standardmäßig aktiviert. Andernfalls musst du diese Funktion aktivieren, indem du die Atmosphere Systemeinstellungen in der Konfigurationsdatei unter `sdmc:/atmosphere/config/system_settings.ini` wie folgt mit einem Texteditor bearbeitest:

```
[usb]
usb30_force_enabled = u8!0x1
```

**Wichtig** - Die Aktivierung von USB 3.0 kann die Bluetooth- und 2,4-GHz-WLAN-Verbindungen stören. Wenn du Probleme mit drahtlosen Controllern oder 2,4-GHz-WLAN-Netzwerken hast, solltest du USB 3.0 nicht aktivieren. 5-GHz-WLAN-Verbindungen sollten in der Regel nicht betroffen sein.

### Wiederherstellen von reinen SaveBackups, extrahiert mit TegraExplorer etc.

Es sind entschlüsselte Saves, die sich im `USER:/saves` Verzeichnis des emuMMC/sysMMC befinden. Falls die emuMMC beschädigt ist, können diese Saves über einen PC oder TegraExplorer extrahiert und mit DBI wiederhergestellt werden.

Du kannst die Saves im Backup-Saves-Ordner von DBI ablegen ( `sdmc:/dbi/saves`) und über das Wiederherstellungsmenü wiederherstellen (der Nutzername wird dabei in geschweifte Klammern `{}` gesetzt), oder über das Kontextmenü, das auf einer solchen Save-Datei aufgerufen wird.

### Bild als Avatar festlegen

Fahre mit dem Cursor über das gewünschte Bild und rufe das Kontextmenü mit der (+)-Taste auf. Wähle "**Als Avatar festlegen...**" aus. Das ausgewählte Bild wird als dein Avatar festgelegt. Das Bild wird automatisch auf quadratische Proportionen skaliert und auf die erforderliche Größe verkleinert. Wenn du möchtest, dass das Bild sein ursprüngliches Seitenverhältnis beibehält, bereite es im Voraus vor.

### Bearbeiten und Anzeigen von Dateien

Jede Datei kann als Text oder HEX geöffnet werden. Nicht leere Dateien werden im Anzeigemodus geöffnet, jedoch schaltet die (L3)-Taste in den Bearbeitungsmodus um. Betrachten wir beide Modi separat.

Du kannst auch eine leere Textdatei aus dem Kontextmenü erstellen (aufgerufen durch die (+)-Taste > **Neue Datei erstellen...**). Beim Öffnen einer leeren Textdatei wird der Editor automatisch gestartet.

#### Datei-Anzeigemodus

**Tasten-Kombi's:**
- **DPAD / Linker Stick / Rechter Stick** - Textscrollen
- **(L) / (R) / (ZL) / (ZR)** - Nächste / Vorherige Seite (Bildschirm)
- **(R3)** - Umschalten zwischen Text- oder HEX-Anzeigemodi
- **(L3)** - Wechsel in den Bearbeitungsmodus
- **(+)** - Kontextmenü

**Kontextmenü:**
- **Bearbeiten** - Wechsel in den Bearbeitungsmodus
- **Kodierung** - Ändern der Textkodierung. Beachte, dass beim Ändern der Kodierung im Anzeigemodus, nachdem die Datei geschlossen und erneut geöffnet wurde, die Kodierung nicht geändert wird.
- **Zeilenumbruch** - ob der Text bei Erreichen des Bildschirmrands in eine neue Zeile umbrochen werden soll oder nichtchung

#### Datei-Bearbeitungsmodus

Du kannst Text bearbeiten, indem du mit dem rechten Stick auf der Tastatur navigierst und einen Buchstaben mit der (A)-Taste auswählst.

**Tasten-Kombi's:**
- **Rechter Stick** - Bewegen auf der Tastatur
- **DPAD / Linker Stick** - Bewegen im Text
- **(A)** - Auswahl des markierten Zeichens auf der Tastatur
- **(X)** - Löschen des Zeichens (Rücktaste)
- **(B)** - Menü zum Speichern der Datei
- **(Y)** - Leertaste
- **(L)+(LINKS)** - Springe zum Anfang der Zeile (HOME)
- **(L)+(RECHTS)** - Springe zum Ende der Zeile (END)
- **(R)+(LINKS)** - Gehe zum nächsten Wort
- **(R)+(RECHTS)** - Gehe zum vorherigen Wort
- **(ZL)** - Groß-/Kleinschreibung ändern
- **(ZR)** - Gehe zur nächsten Zeile (Enter)
- **(R3)** - Sprache wechseln
- **(L3)** - Wechsel in den Anzeigemodus

Beim Schließen einer Datei oder Wechseln in den Anzeigemodus kannst du wählen, ob Änderungen gespeichert werden sollen, wenn Änderungen an der Datei vorgenommen wurden.

## Danksagungen
Vielen Dank an [SciresM](https://github.com/SciresM) für [hactool](https://github.com/SciresM/hactool) (lizenziert unter [ISC](https://de.wikipedia.org/wiki/ISC-Lizenz)) - DBI verwendet einige Datenstrukturdefinitionen von dort.
