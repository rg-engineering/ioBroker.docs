---
translatedFrom: en
translatedWarning: Wenn Sie dieses Dokument bearbeiten möchten, löschen Sie bitte das Feld "translationsFrom". Andernfalls wird dieses Dokument automatisch erneut übersetzt
editLink: https://github.com/ioBroker/ioBroker.docs/edit/master/docs/de/adapterref/iobroker.vis-materialdesign/README.md
title: ioBroker.vis-materialdesign
hash: tkqQ0iCvAMMQR8Bb8iaue0JYwNErVGBKaPsLgKcKJb4=
---
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/admin/vis-materialdesign.png)

![stabile Version](http://iobroker.live/badges/vis-materialdesign.svg)
![NPM-Version](http://img.shields.io/npm/v/iobroker.vis-materialdesign.svg)
![Anzahl der Installationen](http://iobroker.live/badges/vis-materialdesign-installed.svg)
![Downloads](https://img.shields.io/npm/dm/iobroker.vis-materialdesign.svg)
![Abhängigkeitsstatus](https://img.shields.io/david/Scrounger/iobroker.vis-materialdesign.svg)
![Bekannte Sicherheitslücken](https://snyk.io/test/github/Scrounger/ioBroker.vis-materialdesign/badge.svg)
![NPM](https://nodei.co/npm/iobroker.vis-materialdesign.png?downloads=true)
![Travis-CI](http://img.shields.io/travis/Scrounger/ioBroker.vis-materialdesign/master.svg)

# IoBroker.vis-materialdesign
## Material Design Widgets für ioBroker VIS
[![paypal] (https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VWAXSTS634G88&source=url)

ioBroker Material Design Widgets basieren auf [Richtlinien für das Materialdesign von Google](https://material.io/design/). Der Adapter verwendet die folgenden Bibliotheken:

* [Google Materialkomponenten für das Web] (https://github.com/material-components/material-components-web)
* [Vuetify] (https://github.com/vuetifyjs/vuetify)
* [chartjs] (https://www.chartjs.org/)
* [runder Schieberegler von Thomasloven] (https://github.com/thomasloven/round-slider)
* [Material Design Icons] (https://materialdesignicons.com/)

## Adaptereinstellungen (Theme Editor)
Ab Version 0.4.0 gibt es eine Einstellungsseite für den Adapter. Sie finden es unter Instanzen in der Benutzeroberfläche des Admin-Adapters

### Allgemeines
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_general.png)

| Einstellung | Beschreibung |
|-------|-----------|
| Dokumentation | Links zur Dokumentation zur Konfiguration der Widgets |
| Globales Skript generieren | Globales Skript für die [Javascript Script Engine](https://github.com/ioBroker/ioBroker.javascript) mit allen Themendatenpunkten erstellen. Auf diese Weise können Farben, Schriftarten und Schriftgrößen bequem in Skripten verwendet werden |
| Sentry | Verwenden Sie Sentry-Bibliotheken, um Ausnahmen und Codefehler automatisch anonym an die Entwickler zu melden. Weitere Informationen und Informationen zum Deaktivieren der Fehlerberichterstattung finden Sie unter [Sentry-Plugin-Dokumentation] (https://github.com/ioBroker/plugin-sentry#plugin-sentry)! |

### Themeneditor
Mit Hilfe des Design-Editors können Sie Farben, Schriftarten und Schriftgrößen für alle Widgets über die Adaptereinstellungen zentral einstellen. Dies wird mit Hilfe der [Bindungen des VIS-Adapters](https://github.com/ioBroker/ioBroker.vis#bindings-of-objects) realisiert. Für jedes Widget werden Datenpunkte (siehe Abbildung unten) mit den festgelegten Werten erstellt. Dies ermöglicht die Verwendung dieser Einstellungen in anderen Widgets (nicht Material Design Widgets) über Bindungen.

##### Datenpunktstruktur
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_datapoints.png)

##### VIS Editor (Alte Widgets wiederherstellen / aktualisieren)
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/vis_editor_theme_restore.gif)

Im VIS-Editor finden Sie für jedes Widget eine Schaltfläche `use theme`. Mit dieser Schaltfläche können Sie die Widgets auf die Verwendung der Themen zurücksetzen. Das heißt, wenn Sie Farben, Schriftarten oder Schriftgrößen geändert haben, können Sie diese mit dieser Schaltfläche zurücksetzen.

Mit Hilfe dieser Schaltfläche ist es auch möglich, Ihre Widgets von Versionen vor 0.4.0 zu aktualisieren, um die Themen zu verwenden.

##### Bindung für Nicht-Material-Design-Widgets verwenden
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_binding.gif)

In den Adaptereinstellungen können Sie den Bindungsbefehl in die Zwischenablage kopieren, indem Sie auf den Standardtext oder die ID in den Tabellen klicken. Diese Bindung kann dann auch für Nicht-Material-Design-Widgets durch Kopieren und Einfügen verwendet werden.

#### Farbthema
Für Farben gibt es zwei Themen - helles Thema und dunkles Thema. Mit dem Datenpunkt `vis-materialdesign.0.colors.darkTheme` können Sie zwischen den beiden Themen wechseln.

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_colors_light.png)

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_colors_dark.png)

Im oberen Bereich können Standardfarben definiert werden. Diese Standardfarben können dann über die Schaltflächen in der Tabelle den einzelnen Widgets zugewiesen werden. Wenn Sie die Standardfarbe ändern, ändert sich dies auch für alle Widgets, die diese Farbe verwenden.
Darüber hinaus können Sie den Widgets unabhängig von den Standardfarben eigene Farben zuweisen.

#### Schriftart-Thema
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_fonts.png)

Standardschriftarten können im oberen Bereich definiert werden. Diese Standardschriftarten können dann über die Schaltflächen in der Tabelle den einzelnen Widgets zugewiesen werden. Wenn Sie die Standardfarbe ändern, ändert sich dies auch für alle Widgets, die diese Farbe verwenden.
Darüber hinaus können Sie den Widgets unabhängig von den Standardfarben eigene Schriftarten zuweisen.

#### Schriftgrößen-Thema
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/settings_fontSizes.png)

Standardschriftgrößen können im oberen Bereich definiert werden. Diese Standardschriftgrößen können dann über die Schaltflächen in der Tabelle den einzelnen Widgets zugewiesen werden. Wenn Sie die Standardfarbe ändern, ändert sich dies auch für alle Widgets, die diese Farbe verwenden.
Darüber hinaus können Sie den Widgets unabhängig von den Standardfarben Ihre eigenen Schriftgrößen zuweisen.

## Online-Beispielprojekt
bereitgestellt von [iobroker.click](https://iobroker.click/index.html), dank bluefox und iobroker.

* <a href="https://iobroker.click/vis/index.html?Material%20Design%20Widgets" target="_blank">VIS Runtime</a> ( <a href="http://iobroker.click:8082/vis/index.html?Material%20Design%20Widgets" target="_blank">alternativ</a> )
* <a href="https://iobroker.click/vis/edit.html?Material%20Design%20Widgets" target="_blank">VIS Editor</a> ( <a href="http://iobroker.click:8082/vis/edit.html?Material%20Design%20Widgets" target="_blank">alternativ</a> )

## Praktische Beispiele
* [Wetteransicht] (https://forum.iobroker.net/topic/32232/material-design-widgets-wetter-view)
* [Skriptstatus] (https://forum.iobroker.net/topic/30662/material-design-widgets-skript-status)
* [Adapterstatus] (https://forum.iobroker.net/topic/30661/material-design-widgets-adapter-status)
* [UniFi-Netzwerkstatus] (https://github.com/Scrounger/ioBroker.vis-materialdesign/tree/master/examples/UnifiNetworkState)

## Fragen und Antworten zu den Widgets
Wenn Sie Fragen zu den einzelnen Widgets haben, schauen Sie sich zunächst die Themen der einzelnen Widgets an

* [Deutsche Threads] (https://forum.iobroker.net/search?term=Material%20Design%20Widgets%3A&in=titles&matchWords=all&by%5B%5D=Scrounger&categories%5B%5D=7&sortBy=topic.title=s& Themen)

### Unterstützter Browser
https://github.com/material-components/material-components-web/blob/master/docs/supported-browsers.md

### Unterstützte Browserfunktion für Vibrationen auf Mobilgeräten
https://developer.mozilla.org/en-US/docs/Web/API/Navigator/vibrate

### IoBroker VIS App
funktioniert momentan nicht, muss von der App implementiert werden, siehe https://github.com/ioBroker/ioBroker.vis.cordova

## Material Design Icons und Bilder
<table><thead><tr><th>Bildschirmfoto</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=6><img src="doc/en/media/material-icons.png"></td><td> Einige der Widgets unterstützen die <a href="https://materialdesignicons.com/" target="_blank">Material Design Icons-</a> Bibliothek. Sie können ein Symbol aus der obigen Liste auswählen oder die Bildauswahl öffnen, indem Sie auf die Schaltfläche rechts neben dem Eingabefeld klicken.<br><br> <b>Bildfarben gelten nur für die Materialdesignsymbole, nicht für ein Bild!</b></td></tr></tbody></table>

## Tasten
### Button Toggle
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/buttons.gif)

### Symbolschaltfläche
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/icon-button.gif)

## Karte
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/cards.png)

## Liste
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/list.gif)

## IconList
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/iconList.gif)

Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung </th></tr></thead><tbody><tr><td rowspan=6><img src="doc/en/media/iconList_settings_common.png"></td><td>Eingabemethode für die Listendaten</td><td> Die Daten für die IconList können über den Editor eingegeben oder eine JSON-Zeichenfolge verwendet werden</td></tr><tr><td> JSON-String: Objekt-ID</td><td> Objekt-ID des Datenpunkts mit JSON-Zeichenfolge. Die JSON-Zeichenfolge muss das folgende Format haben:<pre><code> [ { &quot;background&quot;: &quot;red&quot;, &quot;text&quot;: &quot;text1&quot;, &quot;subText&quot;: &quot;number&quot;, &quot;image&quot;: &quot;harddisk&quot;, &quot;imageColor&quot;: &quot;#ec0909&quot;, &quot;imageActive&quot;: &quot;folder&quot;, &quot;imageActiveColor&quot;: &quot;#5ad902&quot;, &quot;buttonBackgroundColor&quot;: &quot;&quot;, &quot;buttonBackgroundActiveColor&quot;: &quot;&quot;, &quot;listType&quot;: &quot;buttonState&quot;, &quot;objectId&quot;: &quot;0_userdata.0.iconList.buttonState.number&quot;, &quot;buttonStateValue&quot;: &quot;60&quot;, &quot;buttonNavView&quot;: &quot;&quot;, &quot;buttonLink&quot;: &quot;&quot;, &quot;buttonToggleValueTrue&quot;: &quot;&quot;, &quot;buttonToggleValueFalse&quot;: &quot;&quot;, &quot;valueAppendix&quot;: &quot;&quot;, &quot;showValueLabel&quot;: &quot;true&quot;, &quot;statusBarColor&quot;: &quot;green&quot;, &quot;lockEnabled&quot;: &quot;false&quot; }, { &quot;background&quot;: &quot;green&quot;, &quot;text&quot;: &quot;text0&quot;, &quot;subText&quot;: &quot;bool&quot;, &quot;image&quot;: &quot;home&quot;, &quot;imageColor&quot;: &quot;#44739e&quot;, &quot;imageActive&quot;: &quot;home&quot;, &quot;imageActiveColor&quot;: &quot;#44739e&quot;, &quot;buttonBackgroundColor&quot;: &quot;&quot;, &quot;buttonBackgroundActiveColor&quot;: &quot;#a0f628&quot;, &quot;listType&quot;: &quot;buttonToggle&quot;, &quot;objectId&quot;: &quot;0_userdata.0.iconList.buttonToggle.bool0&quot;, &quot;buttonStateValue&quot;: &quot;60&quot;, &quot;buttonNavView&quot;: &quot;&quot;, &quot;buttonLink&quot;: &quot;&quot;, &quot;buttonToggleValueTrue&quot;: &quot;&quot;, &quot;buttonToggleValueFalse&quot;: &quot;&quot;, &quot;valueAppendix&quot;: &quot;&quot;, &quot;showValueLabel&quot;: &quot;false&quot;, &quot;statusBarColor&quot;: &quot;&quot;, &quot;lockEnabled&quot;: &quot;false&quot; } ]</code></pre> Die Eigenschaft <code>listType</code> kann folgende Werte haben:<br> <code>text, buttonState, buttonToggle, buttonToggleValueTrue, buttonToggleValueFalse, buttonNav, buttonLink</code></td></tr></tbody></table>

## Fortschritt
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/progress.gif)

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=6><img src="doc/en/media/progress_settings.png"></td><td> benutzerdefiniertes Etikett</td><td> Für benutzerdefinierte Beschriftungen können Sie die Eigenschaft <code>[#value]</code> , um den tatsächlichen Wert des Datenpunkts <code>[#value]</code> . Um den aktuellen <code>[#percent]</code> können Sie <code>[#percent]</code></td></tr></tbody></table>

## Schieberegler
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/slider.gif)

Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=6><img src="doc/en/media/slider.png"></td><td> initDelay</td><td> Wenn der Schieberegler nach dem Laden der Laufzeit nicht sichtbar oder bedienbar ist, muss dieser Wert erhöht werden. Die Eingabe erfolgt in Millisekunden.<br> Erhöhen Sie beispielsweise um 250 Schritte, bis der Schieberegler funktioniert.</td></tr></tbody></table>

## Runder Schieberegler
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/round_slider.gif)

## Kontrollkästchen
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/checkbox.gif)

## Schalter
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/switch.gif)

## Eingabe
### Text Eingabe
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/input.gif)

MACHEN

### Wählen
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/select.gif)

Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=6><img src="doc/en/media/select_autocomplete_settings.png"></td><td> Methode der Daten des Menüs</td><td> Es gibt drei Methoden, um die Daten des Menüs zu definieren. Zunächst muss es über den Editor definiert werden. Zweitens müssen Sie es über eine JSON-Zeichenfolge definieren. Die dritte Methode besteht darin, sie durch drei Listen für Werte, Beschriftungen und Symbole zu definieren</td></tr><tr><td> Editor: Anzahl der Menüpunkte</td><td> Datenmethode des Menüs: über den Editor<br> Definieren Sie die Anzahl der Menüeinträge. Die einzelnen Menüeinträge können unter Menüpunkt [x] definiert werden.</td></tr><tr><td> JSON-Zeichenfolge</td><td> Datenmethode des Menüs: JSON-Zeichenfolge<br> Hier können Sie eine JSON-Zeichenfolge hinzufügen, um die Menüeinträge zu definieren, oder Bindungen an einen Datenpunkt verwenden, der eine JSON-Zeichenfolge enthält.<br><br> JSON-Zeichenfolge muss das folgende Format haben:<br><pre><code> [ { &quot;text&quot;: &quot;text 0&quot;, &quot;subText&quot;: &quot;sub 0&quot;, &quot;value&quot;: &quot;val0&quot;, &quot;icon&quot;: &quot;account-cancel&quot; }, { &quot;text&quot;: &quot;text 1&quot;, &quot;subText&quot;: &quot;sub 1&quot;, &quot;value&quot;: &quot;val1&quot;, &quot;icon&quot;: &quot;/vis/icon/info.png&quot;, &quot;iconColor&quot;: &quot;red&quot;, &quot;iconColorSelectedTextField&quot;: &quot;red&quot; }, { &quot;text&quot;: &quot;text 2&quot;, &quot;subText&quot;: &quot;sub 2&quot;, &quot;value&quot;: &quot;val2&quot;, &quot;icon&quot;: &quot;facebook-workplace&quot;, &quot;iconColor&quot;: &quot;green&quot; } ]</code></pre></td></tr><tr><td> Werteliste</td><td> Datenmethode des Menüs: Werteliste<br> Definieren Sie die Anzahl der Menüeinträge, indem Sie Werte hinzufügen, die auf den Datenpunkt gesetzt werden. Einträge müssen durch Semikolon getrennt werden</td></tr><tr><td> Werteliste: Labels</td><td> Datenmethode des Menüs: Werteliste<br> Definieren Sie die zugehörigen Beschriftungen der Werte. Einträge müssen durch Semikolon getrennt werden</td></tr><tr><td> Werteliste: Labels</td><td> Datenmethode des Menüs: Werteliste<br> Definieren Sie die zugehörigen Symbole der Werte. Einträge müssen durch Semikolon getrennt werden. Sie können den Bildpfad oder den Namen des Material Design Icons verwenden</td></tr></tbody></table>

### Autocomplete
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/autocomplete.gif)

Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=6><img src="doc/en/media/select_autocomplete_settings.png"></td><td> Methode der Daten des Menüs</td><td> Es gibt drei Methoden, um die Daten des Menüs zu definieren. Zunächst muss es über den Editor definiert werden. Zweitens müssen Sie es über eine JSON-Zeichenfolge definieren. Die dritte Methode besteht darin, sie durch drei Listen für Werte, Beschriftungen und Symbole zu definieren</td></tr><tr><td> Editor: Anzahl der Menüpunkte</td><td> Datenmethode des Menüs: über den Editor<br> Definieren Sie die Anzahl der Menüeinträge. Die einzelnen Menüeinträge können unter Menüpunkt [x] definiert werden.</td></tr><tr><td> JSON-Zeichenfolge</td><td> Datenmethode des Menüs: JSON-Zeichenfolge<br> Hier können Sie eine JSON-Zeichenfolge hinzufügen, um die Menüeinträge zu definieren, oder Bindungen an einen Datenpunkt verwenden, der eine JSON-Zeichenfolge enthält.<br><br> JSON-Zeichenfolge muss das folgende Format haben:<br><pre><code> [ { &quot;text&quot;: &quot;text 0&quot;, &quot;subText&quot;: &quot;sub 0&quot;, &quot;value&quot;: &quot;val0&quot;, &quot;icon&quot;: &quot;account-cancel&quot; }, { &quot;text&quot;: &quot;text 1&quot;, &quot;subText&quot;: &quot;sub 1&quot;, &quot;value&quot;: &quot;val1&quot;, &quot;icon&quot;: &quot;/vis/icon/info.png&quot;, &quot;iconColor&quot;: &quot;red&quot; }, { &quot;text&quot;: &quot;text 2&quot;, &quot;subText&quot;: &quot;sub 2&quot;, &quot;value&quot;: &quot;val2&quot;, &quot;icon&quot;: &quot;facebook-workplace&quot;, &quot;iconColor&quot;: &quot;green&quot; } ]</code></pre></td></tr><tr><td> Werteliste</td><td> Datenmethode des Menüs: Werteliste<br> Definieren Sie die Anzahl der Menüeinträge, indem Sie Werte hinzufügen, die auf den Datenpunkt gesetzt werden. Einträge müssen durch Semikolon getrennt werden</td></tr><tr><td> Werteliste: Labels</td><td> Datenmethode des Menüs: Werteliste<br> Definieren Sie die zugehörigen Beschriftungen der Werte. Einträge müssen durch Semikolon getrennt werden</td></tr><tr><td> Werteliste: Labels</td><td> Datenmethode des Menüs: Werteliste<br> Definieren Sie die zugehörigen Symbole der Werte. Einträge müssen durch Semikolon getrennt werden. Sie können den Bildpfad oder den Namen des Material Design Icons verwenden</td></tr></tbody></table>

## Obere App-Leiste mit Navigationsschublade
Die obere App-Leiste mit Navigationsleiste kann mit der <a href="https://www.iobroker.net/#en/documentation/viz/basic.md">Ansicht in Widget 8</a> kombiniert werden.

<b>Schauen Sie sich die [Beispielprojekt für Material Design Widgets](https://github.com/Scrounger/ioBroker.vis-materialdesign#online-example-project)</b> an, um zu verstehen, wie es funktioniert.

##### Layout modal:
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/topappbar_modal.gif)

##### Layout permanent:
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/topappbar_permanent.gif)

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=3><img src="doc/en/media/topappbar_settings.png"></td><td> Objekt Identifikation</td><td> muss von der Typennummer auf einen Datenpunkt gesetzt werden. Beispielsweise kann dieser Datenpunkt von der <a href="https://www.iobroker.net/#en/documentation/viz/basic.md">Ansicht in Widget 8 verwendet werden</a></td></tr><tr><td> Index der Navigationselemente anzeigen</td><td> Zeigt den Navigationsindex vor der Artikelbezeichnung an. Diese Nummer kann in der <a href="https://www.iobroker.net/#en/documentation/viz/basic.md">Ansicht in Widget 8 verwendet werden</a> , um die Ansicht zu definieren, die angezeigt werden soll, wenn das Element ausgewählt ist</td></tr><tr><td> Anzahl der Navigationselemente</td><td> Definieren Sie die Anzahl der Navigationselemente</td></tr></tbody></table>

### Untermenü
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/drawer_subMenu.png)

##### Seit Version 0.4.0
Seit Version 0.4.0 müssen die Untermenüs durch eine JSON-Zeichenfolge definiert werden:

```
[
	{
		"text": "subitem0",
		"icon": "account",
		"iconColor": "red"
	},
	{
		"text": "subitem1",
		"icon": "home",
		"iconColor": "green",
		"divider": "true"
	},
	{
		"text": "subitem1",
		"divider": "true",
		"icon": "/vis.0/myImages/devices/lxc_iobroker.png",
		"userGroups": ["administrator", "user"],
		"behaviorNotInUserGroup": "disabled"
	}
]
```

<table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> Text</td><td> Text des Eintrags</td><td> Zeichenfolge</td><td></td></tr><tr><td> Symbol</td><td> Symbol oder Bildpfad des Eintritts</td><td> Zeichenfolge</td><td></td></tr><tr><td> iconColor</td><td> Symbolfarbe (funktioniert nicht, wenn Bild verwendet wird)</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> Teiler</td><td> zeige einen Teiler</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> Benutzergruppen</td><td> Benutzergruppen, die diesen Eintrag anzeigen und steuern dürfen.</td><td> Array [Zeichenfolge]</td><td> ID der Benutzergruppen</td></tr><tr><td> behaviourNotInUserGroup</td><td> Eintrag ausblenden oder deaktivieren, wenn der Benutzer nicht Teil der Benutzergruppe ist</td><td> Zeichenfolge</td><td> verstecken, deaktiviert</td></tr></tbody></table>

##### Vor Version 0.4.0
Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung </th></tr></thead><tbody><tr><td rowspan=1><img src="doc/en/media/drawer_subMenu_views.png"></td><td> Anzahl der Untermenüs [x]</td><td> Definieren Sie, ob das Navigationselement Untermenüs und die Anzahl der Untermenüs enthält.</td></tr><tr><td rowspan=1><img src="doc/en/media/drawer_subMenu_labels.png"></td><td> label [x]</td><td> Um den Text der Elemente zu ändern, müssen Sie ein JSON-Objekt mit dem Index des Ansichtsfelds in das Beschriftungsfeld einfügen.<br> Beispiel:<br>

`{"itemText": "Item with Subitems", "subItems": ["subItem1", "subItem2"]}`

Ergebnis: siehe Screenshot</td></tr><tr><td rowspan=1><img src="doc/en/media/drawer_subMenu_icons.png"></td><td> Symbol [x]</td><td> Um die Symbole der Elemente zu ändern, müssen Sie ein JSON-Objekt mit dem Index des Ansichtsfelds in das Symbolfeld einfügen.<br> Beispiel:<br>

`{"itemImage": "/icons-material-svg/hardware/ic_computer_48px.svg", "subItems": ["/vis/widgets/materialdesign/img/IoBroker_Logo.png", "/icons-material-svg/action/ic_android_48px.svg"]}`

Ergebnis: siehe Screenshot </ td> </ tr> </ tbody> </ table>

## Diagramme
### Balkendiagramm
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/barChart.png)

MACHEN

### Kuchendiagramm
MACHEN

### Linienverlaufsdiagramm:
> Erforderlicher Adapter: [SQL] (https://github.com/ioBroker/ioBroker.sql), [Verlauf] (https://github.com/ioBroker/ioBroker.history) oder [InfluxDb](https://github.com/ioBroker/ioBroker.influxdb)!

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/line_history_chart.gif)

Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung </th></tr></thead><tbody><tr><td rowspan=5><img src="doc/en/media/line_hostory_chart_general.png"></td><td> Adapterinstanz</td><td> Instanz für den SQL- oder Verlaufsadapter</td></tr><tr><td> Zeitintervall mit Objekt steuern</td><td> ID eines Datenpunkts zum Ändern des Zeitintervalls des Diagramms.<br><br> Wenn der Datenpunkt vom Typ &#39;Zeichenfolge&#39; ist, muss er <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign/blob/235530e4e54346b5527333ca06ce596519954c67/widgets/materialdesign/js/materialdesign.chart.js#L802">einen der verknüpften Werte enthalten</a><br> Wenn der Datenpunkt vom Typ &#39;Nummer&#39; ist, muss er den Startzeitstempel des Diagramms enthalten.<br><br> Beispielsweise können Sie hier eine Schaltfläche verwenden, um die Anzeige des Diagramms zur Laufzeit zu ändern</td></tr><tr><td> Boolesches Objekt zum Aktualisieren</td><td> ID von adatapoint, um eine manuelle Aktualisierung des Diagramms auszulösen.<br> Beispielsweise können Sie hier eine Schaltfläche verwenden, um das Diagramm zur Laufzeit zu aktualisieren</td></tr><tr><td> Diagramm-Timeout</td><td> Zeitüberschreitung beim Laden der Diagrammdaten. Wenn Sie eine Timeout-Fehlermeldung erhalten, erhöhen Sie diesen Wert</td></tr><tr><td> Debug-Modus</td><td> Wenn Sie Probleme oder Fehler haben, aktivieren Sie den Debug-Modus und hängen Sie die Daten des Konsolenprotokolls (F12) an das Problem an</td></tr><tr><td rowspan=5><img src="doc/en/media/line_hostory_chart_dataset.png"></td><td> Objekt Identifikation</td><td> Datenpunkt-ID mit aktivierter Instanz für den SQL- oder Verlaufsadapter</td></tr><tr><td> Anzeigemethode</td><td> <a href="https://www.iobroker.net/docu/index-195.htm?page_id=198&lang=en#Aggregation">Verknüpfung</a></td></tr><tr><td> max. Anzahl der anzuzeigenden Datenpunkte</td><td> Anzahl der maximal anzuzeigenden Datenpunkte</td></tr><tr><td> Zeitintervall zwischen den Datenpunkten in [s]</td><td> Die optionale Einstellung überschreibt die Einstellung &#39;Anzahl&#39;.<br> Abstand zwischen den einzelnen Datenpunkten in Sekunden.<br> Wenn Sie beispielsweise jede Minute Datenpunkte anzeigen möchten, müssen Sie hier 60 eingeben</td></tr><tr><td> Daten multiplizieren mit</td><td> Optionale Einstellung: Multiplizieren Sie jeden Datenpunkt mit dem angegebenen Wert</td></tr><tr><td><img src="doc/en/media/line_hostory_chart_xAxis_layout.png"></td><td> Zeitformate der x-Achse</td><td> Ändern Sie das Zeitformat der X-Achse. Zeitformate müssen für alle Zeiteinheiten eingegeben werden, <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign/blob/c677220868961b3cf0b153fb8bf04e13b4475c09/widgets/materialdesign/js/materialdesign.chart.js#L805">die folgenden Zeiteinheiten sind zulässig.</a><br> Genehmigte Zeitformate müssen gemäß der Bibliothek moment.js eingegeben werden, <a href="https://momentjs.com/docs/#/displaying/">siehe Link</a></td></tr><tr><td><img src="doc/en/media/line_hostory_chart_tooltip_layout.png"></td><td> Tooltip-Zeitformate</td><td> Ändern Sie das Zeitformat des Tooltips. Zeitformate müssen für alle Zeiteinheiten eingegeben werden, <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign/blob/c677220868961b3cf0b153fb8bf04e13b4475c09/widgets/materialdesign/js/materialdesign.chart.js#L805">die folgenden Zeiteinheiten sind zulässig.</a><br> Genehmigte Zeitformate müssen gemäß der Bibliothek moment.js eingegeben werden, <a href="https://momentjs.com/docs/#/displaying/">siehe Link</a></td></tr></tbody></table>

### JSON-Diagramm
#### Allgemeines
<table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> axisLabels</td><td> Achsenbeschriftung des Graphen</td><td> Array</td><td> Zahlen oder Zeichenfolge</td></tr><tr><td> Grafiken</td><td> Daten von Graphen</td><td> Array [ <a href="#graph">Grafik</a> ]</td><td> siehe Grafik</td></tr></tbody></table>

#### Graph
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> Daten</td><td> Daten des Graphen oder Daten mit Zeitstempel</td><td> Array [Zahlen] | Array [ <a href="#data-with-time-axis">Werte mit Zeitstempel</a> ]</td><td> Nummer</td></tr><tr><td> Art</td><td> Art des Diagramms</td><td> Zeichenfolge</td><td> &#39;line&#39;, &#39;bar&#39;</td></tr><tr><td> legendText</td><td> Text der Legende</td><td> Zeichenfolge</td><td></td></tr><tr><td> Bestellung anzeigen</td><td> Überlagerungsreihenfolge des Diagramms</td><td> Nummer</td><td> 1, 2, ...</td></tr><tr><td> Farbe</td><td> Farbe des Graphen</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> use_gradient_color</td><td> Verwenden Sie eine Verlaufsfarbe</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> Farbverlauf</td><td> Farbverlaufsarray</td><td> Array [ <a href="#gradientcolor">gradientColor</a> ]</td><td> [{Wert: -20, Farbe: &#39;# 7d3c98&#39;}, {Wert: 0, Farbe: &#39;# 2874a6&#39;}]</td></tr><tr><td> tooltip_title</td><td> Titel des Tooltips</td><td> Zeichenfolge</td><td></td></tr><tr><td> tooltip_text</td><td> Übergreifender Text des Tooltips</td><td> Zeichenfolge</td><td></td></tr><tr><td> tooltip_MinDigits</td><td> Maximale Dezimalstellen des Tooltip-Werts</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> tooltip_MaxDigits</td><td> Maximale Dezimalstellen des Tooltip-Werts</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> tooltip_AppendText</td><td> Fügen Sie Text an den Tooltip-Wert an</td><td> Zeichenfolge</td><td></td></tr><tr><td> datalabel_show</td><td> Datenbeschriftungen für Grafik anzeigen</td><td> Zeichenfolge | Boolescher Wert</td><td> false, true, auto</td></tr><tr><td> datalabel_anchor</td><td> Anker von Datenetiketten</td><td> Zeichenfolge</td><td> zentrieren, beginnen, enden</td></tr><tr><td> datalabel_align</td><td> Position des Datenetiketts relativ zum Ankerpunkt</td><td> Zeichenfolge</td><td> links, Start, Mitte, Ende, rechts, oben, unten</td></tr><tr><td> datalabel_offset</td><td> Abstand (in Pixel), um das Datenetikett vom Ankerpunkt wegzuziehen</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> datalabel_text_align</td><td> Textausrichtung des Datenetiketts</td><td> Zeichenfolge</td><td> links, Start, Mitte, Ende, rechts</td></tr><tr><td> datalabel_rotation</td><td> Drehwinkel des Datenetiketts im Uhrzeigersinn (in Grad)</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> datalabel_steps</td><td> Datenbeschriftung bei jedem x-Schritt anzeigen</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> datalabel_minDigits</td><td> minimale Dezimalstellen von Datenetiketten</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> datalabel_maxDigits</td><td> maximale Dezimalstellen von Datenbeschriftungen</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> datalabel_append</td><td> Text an Datenetikett anhängen</td><td> Zeichenfolge</td><td></td></tr><tr><td> datalabel_color</td><td> Datenetikettenfarbe</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> datalabel_fontFamily</td><td> Datenetiketten-Schriftfamilie</td><td> Zeichenfolge</td><td></td></tr><tr><td> datalabel_fontSize</td><td> Schriftgröße der Datenbeschriftung</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> datalabel_backgroundColor</td><td> Hintergrundfarbe des Datenetiketts</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> datalabel_borderColor</td><td> Randfarbe der Datenbeschriftung</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> datalabel_borderWidth</td><td> Breite des Datenetikettenrahmens</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> datalabel_borderRadius</td><td> Randradius der Datenbeschriftung</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr></tbody></table></details>

#### Graph liniendiagramm spfeicifc
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> line_pointStyle</td><td> Punktstil der Linie</td><td> Zeichenfolge</td><td> Kreis, Kreuz, Kreuzrot, Strich, Linie, Rechteck, Rechteck, Rechteck, Stern, Dreieck</td></tr><tr><td> line_pointSize</td><td> Punktgröße der Linie</td><td> Nummer</td><td> 1, 2, 3, ...</td></tr><tr><td> line_pointSizeHover</td><td> Punktgröße der Linie</td><td> Nummer</td><td> 1, 2, 3, ...</td></tr><tr><td> line_PointColor</td><td> Farbe des Linienpunktes</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> line_PointColorBorder</td><td> Randfarbe des Linienpunktes</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> line_PointColorHover</td><td> Schwebefarbe des Linienpunktes</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> line_PointColorBorderHover</td><td> Rand Schwebefarbe des Linienpunktes</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> line_spanGaps</td><td> Zeichnen Sie Linien, wenn die Daten Lücken aufweisen</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> line_steppedLine</td><td> gestufte Linie aktivieren</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> line_Tension</td><td> Glätte der Linie</td><td> Nummer</td><td> 0 - 1</td></tr><tr><td> dicke der Linie</td><td> Dicke der Linie</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> line_UseFillColor</td><td> Verwenden Sie die Füllfarbe unter der Linie</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> line_FillColor</td><td> Füllfarbe unter Linie</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> use_line_gradient_fill_color</td><td> Verwenden Sie die Verlaufsfüllfarbe</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> line_gradient_fill_color</td><td> Farbverlaufsarray</td><td> Array [ <a href="#gradientcolor">gradientColor</a> ]</td><td> [{Wert: -20, Farbe: &#39;# 7d3c98&#39;}, {Wert: 0, Farbe: &#39;# 2874a6&#39;}]</td></tr><tr><td> line_FillBetweenLines</td><td> Füllfarbe bis zur nächsten / vorherigen Zeile</td><td> Zeichenfolge</td><td> &#39;+1&#39;, &#39;-1&#39;, &#39;+2&#39;, ...</td></tr></tbody></table></details>

#### Grafik Balkendiagramm spfeicifc
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> barIsStacked</td><td> gestapelte Stange. Wenn Sie ein kombiniertes Diagramm (Linie + gestapelter Balken) haben, müssen Sie diesen Wert auch für den Liniendatensatz festlegen!</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> barStackId</td><td> ID des Stapels. Balken, die zu einem Stapel kombiniert werden sollen, müssen dieselbe ID haben</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> barColorHover</td><td> Schwebefarbe des Balkens</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> barBorderColor</td><td> Randfarbe des Balkens</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> barBorderWidth</td><td> Dicke der Balkengrenze</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> barBorderColorHover</td><td> Rand Schwebefarbe der Leiste</td><td> Farbe | Array [Farben]</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> barBorderWidthHover</td><td> Schweben Sie die Dicke der Balkengrenze</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr></tbody></table></details>

#### Graph y-Achse
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> yAxis_id</td><td> ID der y-Achse. Wenn Sie eine gemeinsame y-Achse für mehrere Diagrammdaten verwenden möchten, verwenden Sie dieselbe ID.</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_position</td><td> Position der y-Achse</td><td> Zeichenfolge</td><td> links rechts</td></tr><tr><td> yAxis_show</td><td> y-Achse zeigen</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> yAxis_title_text</td><td> Titel der y-Achse</td><td> Zeichenfolge</td><td></td></tr><tr><td> yAxis_title_color</td><td> Überschreiben Sie die Titelfarbe der y-Achse</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> yAxis_title_fontFamily</td><td> Überschreiben Sie die Schriftfamilie der Titel auf der y-Achse</td><td> Zeichenfolge</td><td></td></tr><tr><td> yAxis_title_fontSize</td><td> Überschreiben Sie die Schriftgröße des Titels der y-Achse</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_min</td><td> Minimalwert der y-Achse</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_max</td><td> Maximalwert der y-Achse</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_step</td><td> Schritte der y-Achse</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_minimumDigits</td><td> Mindestanzahl von Dezimalstellen auf der y-Achse</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_maximumDigits</td><td> y-Achse maximale Anzahl von Dezimalstellen</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_maxSteps</td><td> maximale Schritte der y-Achse</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_distance</td><td> y-Achsenwert Abstand zur Achse überschreiben</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_appendix</td><td> Fügen Sie Text an den Wert der y-Achse an</td><td> Zeichenfolge</td><td></td></tr><tr><td> yAxis_color</td><td> Überschreiben Sie die Farbe des y-Achsenwerts</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> yAxis_fontFamily</td><td> Überschreiben Sie die Schriftfamilie der y-Achsenwerte</td><td> Zeichenfolge</td><td></td></tr><tr><td> yAxis_fontSize</td><td> Überschreiben Sie die Schriftgröße des y-Achsenwerts</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> yAxis_zeroLineWidth</td><td> Breite der Nulllinie der y-Achse</td><td> Nummer</td><td> 0,3, 1,5, 4, ...</td></tr><tr><td> yAxis_zeroLineColor</td><td> Nulllinienfarbe der y-Achse</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> yAxis_gridLines_show</td><td> Y-Achsen-Gitterlinien anzeigen</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> yAxis_gridLines_color</td><td> Farbe der Gitterlinien der y-Achse</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> yAxis_gridLines_lineWidth</td><td> Breite der Gitterlinien</td><td> Nummer</td><td> 0 - 1</td></tr><tr><td> yAxis_gridLines_border_show</td><td> Rand der Gitterlinien der y-Achse anzeigen</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> yAxis_gridLines_ticks_show</td><td> Zeige Tick-Intervall-Ticks auf der y-Achse</td><td> Boolescher Wert</td><td> Falsch Richtig</td></tr><tr><td> yAxis_gridLines_ticks_length</td><td> Länge der Y-Achsen-Gitter-Ticks</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr></tbody></table></details>

#### Farbverlauf
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> Wert</td><td> Wert, bei dem Farbe angewendet werden soll</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> Farbe</td><td> Farbe für Wert</td><td> Farbe</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr></tbody></table></details>

### Diagramm mit Zeitachse
JSON Chart unterstützt Daten mit einem Zeitstempel. Um dies zu verwenden, muss das Datenarray Werte für Zeitstempel (x-Achsenwert) und Wert (y-Achsenwert) haben.

#### Werte mit Zeitstempel
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> t</td><td> Zeitstempel - xAxis-Wert</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr><tr><td> y</td><td> Wert für Zeitstempel - yAxis-Wert</td><td> Nummer</td><td> 1, 2, 5, ...</td></tr></tbody></table></details>

#### X-Achseneinstellungen für Daten mit Zeitstempel
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> xAxis_bounds</td><td> Skalengrenzstrategie<br><br> &#39;Daten&#39;: Stellt sicher, dass die Daten vollständig sichtbar sind und Beschriftungen außerhalb entfernt werden<br> &#39;Ticks&#39;: Stellt sicher, dass die Ticks vollständig sichtbar sind und die Daten außerhalb abgeschnitten werden</td><td> String</td><td> Daten, Zecken</td></tr><tr><td> xAxis_timeFormats</td><td> Zeitformate für die x-Achse</td><td> Objekt</td><td> Zeitformate müssen für alle Zeiteinheiten eingegeben werden, <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign/blob/c677220868961b3cf0b153fb8bf04e13b4475c09/widgets/materialdesign/js/materialdesign.chart.js#L805">die folgenden Zeiteinheiten sind zulässig.</a><br> Genehmigte Zeitformate müssen gemäß der Bibliothek moment.js eingegeben werden, <a href="https://momentjs.com/docs/#/displaying/">siehe Link</a></td></tr><tr><td> xAxis_tooltip_timeFormats</td><td> Zeitformate für die x-Achse</td><td> String</td><td> Genehmigte Zeitformate müssen gemäß der Bibliothek moment.js eingegeben werden, <a href="https://momentjs.com/docs/#/displaying/">siehe Link</a></td></tr><tr><td> xAxis_time_unit</td><td> Erzwinge das Zeitformat für die x-Achse</td><td> String</td><td> Folgende Einheiten sind erlaubt, <a href="https://www.chartjs.org/docs/latest/axes/cartesian/time.html#time-units">siehe Link</a></td></tr></tbody></table></details>

## Tabelle
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/table.gif)

### Eingabedaten
Eingabedaten müssen ein JSON-Array von Objekten sein, Beispiel:

```
[
	{
		"img": "/vis.0/myImages/erlebnis_50.png",
		"name": "Empire",
		"betriebszeit": "4h 06m",
		"funk": "5G",
		"ip": "10.0.0.1"
	},
	{
		"img": "/vis.0/myImages/erlebnis_100.png",
		"name": "Handy",
		"betriebszeit": "13m",
		"funk": "5G",
		"ip": "10.0.0.2"
	},
	{
		"img": "/vis.0/myImages/erlebnis_100.png",
		"name": "Harmony Hub - Wohnzimmer",
		"betriebszeit": "18T 07h 21m",
		"funk": "2G",
		"ip": "10.0.0.3"
	}
]
```

#### Steuerelemente
Um ein Steuerelement (Schaltfläche, Kontrollkästchen usw.) in der Zelle der Tabelle zu generieren, müssen Sie ein Objekt anstelle einer Zeichenfolge erstellen.

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/table_control_example.gif)

```
[
	{
		"control": {
			"type": "buttonToggle",
			"oid": "0_userdata.0.MDW.Buttons.bool",
			"buttonText": "&nbsp;off",
			"buttonTextTrue": "&nbsp;on",
			"image": "home",
			"imagePosition": "left",
			"colorBgTrue": "green",
			"lockEnabled": "true"
		},
		"img": "/vis.0/myImages/erlebnis_50.png",
		"name": "Empire",
		"betriebszeit": "4h 06m",
		"funk": "5G"
	}, {
		"img": "/vis.0/myImages/erlebnis_100.png",
		"control": {
			"type": "buttonToggle",
			"oid": "0_userdata.0.MDW.Buttons.bool",
			"buttonText": "off",
			"buttonTextTrue": "on",
			"image": "home",
			"colorBgTrue": "green"
		},
		"name": "Handy",
		"betriebszeit": "13m",
		"funk": "5G",
		"ip": "10.0.0.2"
	}, {
		"img": "/vis.0/myImages/erlebnis_100.png",
		"name": "Harmony Hub - Wohnzimmer",
		"betriebszeit": "18T 07h 21m",
		"funk": "2G",
		"ip": "10.0.0.3"
	}
]
```

##### Vom Editor generieren
Mit dem Editor können Sie ganz einfach Steuerelemente generieren. Erstellen Sie einfach ein unterstütztes Widget, konfigurieren Sie es über den Editor und exportieren Sie die Einstellungen durch Kopieren und Einfügen in die Tabelle wigdet.
Schauen Sie sich den animierten Screenshot unten an:

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/table_controls.gif)

##### Allgemeines
<table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> Art</td><td> Art des Steuerelements</td><td> Zeichenfolge</td><td><ul><li> <a href="#button-toggle-1">buttonToggle</a></li><li> <a href="#button-toggle-vertical">buttonToggle_vertical</a></li><li> <a href="#button-toggle-icon">buttonToggle_icon</a></li><li> <a href="#button-state">buttonState</a></li><li> <a href="#button-state-vertical">buttonState_vertical</a></li><li> <a href="#button-state-icon">buttonState_icon</a></li><li> <a href="#button-link">buttonLink</a></li><li> <a href="#button-link-vertical">buttonLink_vertical</a></li><li> <a href="#button-link-icon">buttonLink_icon</a></li><li> <a href="#progress-1">Fortschritt</a></li><li> <a href="#progress-circular">progress_circular</a></li><li> <a href="#slider-1">Schieberegler</a></li><li> <a href="#slider-round">slider_round</a></li><li> <a href="#switch-1">Schalter</a></li><li> <a href="#checkbox-1">Kontrollkästchen</a></li><li> <a href="#textfield">Textfeld</a></li><li> <a href="#select-1">wählen</a></li><li> <a href="#autocomplete-1">Autocomplete</a></li><li> <a href="#material-design-icons">Material Design Icons</a></li><li> <a href="#html">Html</a></li></ul></td></tr><tr><td> Breite</td><td> Breite in% oder px des Steuerelements</td><td> Zeichenfolge</td><td> 100% | 100px</td></tr><tr><td> Höhe</td><td> Höhe in% oder px des Steuerelements</td><td> Zeichenfolge</td><td> 100% | 100px</td></tr><tr><td> Rowspan</td><td> Zelle, die x Zeilen umfasst</td><td> Nummer</td><td> 1, 2, 3, ...</td></tr><tr><td> Colspan</td><td> Zelle, die x Spalten umfasst</td><td> Nummer</td><td> 1, 2, 3, ...</td></tr><tr><td> vertikaleAlign</td><td> Vertikale Ausrichtung</td><td> Zeichenfolge</td><td> Nach oben | Mitte | Unterseite</td></tr><tr><td> cellStyleAttrs</td><td> CSS-Stilattribute für Zelle</td><td> Zeichenfolge</td><td> ...</td></tr></tbody></table>

##### Button Toggle
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> buttonStyle</td><td> Tastenstil</td><td> Zeichenfolge</td><td> Text | angehoben | nicht erhöht | umrissen</td></tr><tr><td> schreibgeschützt</td><td> schreibgeschützt</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> toggleType</td><td> Art des Umschalters</td><td> Zeichenfolge</td><td> boolean | Wert</td></tr><tr><td> Druckknopf</td><td> Druckknopf</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueOff</td><td> Wert für aus</td><td> Zeichenfolge</td><td/></tr><tr><td> valueOn</td><td> Wert für auf</td><td> Zeichenfolge</td><td/></tr><tr><td> stateIfNotTrueValue</td><td> Geben Sie an, ob der Wert nicht der Bedingung &quot;Ein&quot; entspricht</td><td> Zeichenfolge</td><td> am | aus</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Schaltflächentext</td><td> Schaltflächentext</td><td> Zeichenfolge</td><td/></tr><tr><td> labelTrue</td><td> Beschriften Sie true</td><td> Zeichenfolge</td><td/></tr><tr><td> labelColorFalse</td><td> Etikettenfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelColorTrue</td><td> aktive Etikettenfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelWidth</td><td> Textbreite</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> imageTrue</td><td> aktives Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageTrueColor</td><td> aktive Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconPosition</td><td> Bildposition</td><td> Zeichenfolge</td><td> links | Recht</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> colorBgFalse</td><td> Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorBgTrue</td><td> aktiver Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockEnabled</td><td> Sperren aktivieren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatische Sperre nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn gesperrt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Schaltfläche Vertikal umschalten
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> buttonStyle</td><td> Tastenstil</td><td> Zeichenfolge</td><td> Text | angehoben | nicht erhöht | umrissen</td></tr><tr><td> schreibgeschützt</td><td> schreibgeschützt</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> toggleType</td><td> Art des Umschalters</td><td> Zeichenfolge</td><td> boolean | Wert</td></tr><tr><td> Druckknopf</td><td> Druckknopf</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueOff</td><td> Wert für aus</td><td> Zeichenfolge</td><td/></tr><tr><td> valueOn</td><td> Wert für auf</td><td> Zeichenfolge</td><td/></tr><tr><td> stateIfNotTrueValue</td><td> Geben Sie an, ob der Wert nicht der Bedingung &quot;Ein&quot; entspricht</td><td> Zeichenfolge</td><td> am | aus</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Schaltflächentext</td><td> Schaltflächentext</td><td> Zeichenfolge</td><td/></tr><tr><td> labelTrue</td><td> Beschriften Sie true</td><td> Zeichenfolge</td><td/></tr><tr><td> labelColorFalse</td><td> Etikettenfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelColorTrue</td><td> aktive Etikettenfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> imageTrue</td><td> aktives Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageTrueColor</td><td> aktive Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconPosition</td><td> Bildposition</td><td> Zeichenfolge</td><td> Nach oben | Unterseite</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> colorBgFalse</td><td> Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorBgTrue</td><td> aktiver Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockEnabled</td><td> Sperren aktivieren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatische Sperre nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconTop</td><td> Symbolabstand von oben [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconLeft</td><td> Symbolabstand von links [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn gesperrt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Schaltfläche Symbol umschalten
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> schreibgeschützt</td><td> schreibgeschützt</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> toggleType</td><td> Art des Umschalters</td><td> Zeichenfolge</td><td> boolean | Wert</td></tr><tr><td> Druckknopf</td><td> Druckknopf</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueOff</td><td> Wert für aus</td><td> Zeichenfolge</td><td/></tr><tr><td> valueOn</td><td> Wert für auf</td><td> Zeichenfolge</td><td/></tr><tr><td> stateIfNotTrueValue</td><td> Geben Sie an, ob der Wert nicht der Bedingung &quot;Ein&quot; entspricht</td><td> Zeichenfolge</td><td> am | aus</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> imageTrue</td><td> aktives Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageTrueColor</td><td> aktive Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> colorBgFalse</td><td> Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorBgTrue</td><td> aktiver Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockEnabled</td><td> Sperren aktivieren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatische Sperre nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconTop</td><td> Symbolabstand von oben [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconLeft</td><td> Symbolabstand von links [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockIconBackground</td><td> Hintergrundfarbe des Schlosssymbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockBackgroundSizeFactor</td><td> Wachstumsfaktor der Hintergrundgröße</td><td> Nummer</td><td/></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn gesperrt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Button State
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> buttonStyle</td><td> Tastenstil</td><td> Zeichenfolge</td><td> Text | angehoben | nicht erhöht | umrissen</td></tr><tr><td> Wert</td><td> Wert</td><td> Zeichenfolge</td><td/></tr><tr><td> Schaltflächentext</td><td> Schaltflächentext</td><td> Zeichenfolge</td><td/></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelWidth</td><td> Textbreite</td><td> Nummer</td><td/></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconPosition</td><td> Bildposition</td><td> Zeichenfolge</td><td> links | Recht</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> lockEnabled</td><td> Sperren aktivieren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatische Sperre nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn gesperrt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Schaltflächenstatus vertikal
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> buttonStyle</td><td> Tastenstil</td><td> Zeichenfolge</td><td> Text | angehoben | nicht erhöht | umrissen</td></tr><tr><td> Wert</td><td> Wert</td><td> Zeichenfolge</td><td/></tr><tr><td> Schaltflächentext</td><td> Schaltflächentext</td><td> Zeichenfolge</td><td/></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconPosition</td><td> Bildposition</td><td> Zeichenfolge</td><td> Nach oben | Unterseite</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> lockEnabled</td><td> Sperren aktivieren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatische Sperre nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconTop</td><td> Symbolabstand von oben [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconLeft</td><td> Symbolabstand von links [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn gesperrt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Button State Icon
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> Wert</td><td> Wert</td><td> Zeichenfolge</td><td/></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockEnabled</td><td> Sperren aktivieren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatische Sperre nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconTop</td><td> Symbolabstand von oben [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconLeft</td><td> Symbolabstand von links [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockIconBackground</td><td> Hintergrundfarbe des Schlosssymbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockBackgroundSizeFactor</td><td> Wachstumsfaktor der Hintergrundgröße</td><td> Nummer</td><td/></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn gesperrt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Button Link
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> buttonStyle</td><td> Tastenstil</td><td> Zeichenfolge</td><td> Text | angehoben | nicht erhöht | umrissen</td></tr><tr><td> href</td><td> Verknüpfung</td><td> URL</td><td/></tr><tr><td> openNewWindow</td><td> in neuem Fenster öffnen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> Schaltflächentext</td><td> Schaltflächentext</td><td> Zeichenfolge</td><td/></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelWidth</td><td> Textbreite</td><td> Nummer</td><td/></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconPosition</td><td> Bildposition</td><td> Zeichenfolge</td><td> links | Recht</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Button Link Vertikal
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> buttonStyle</td><td> Tastenstil</td><td> Zeichenfolge</td><td> Text | angehoben | nicht erhöht | umrissen</td></tr><tr><td> href</td><td> Verknüpfung</td><td> URL</td><td/></tr><tr><td> openNewWindow</td><td> in neuem Fenster öffnen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> Schaltflächentext</td><td> Schaltflächentext</td><td> Zeichenfolge</td><td/></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconPosition</td><td> Bildposition</td><td> Zeichenfolge</td><td> Nach oben | Unterseite</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Button Link Icon
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> href</td><td> Verknüpfung</td><td> URL</td><td/></tr><tr><td> openNewWindow</td><td> in neuem Fenster öffnen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> Bild</td><td> Bild</td><td> Benutzerdefiniert</td><td/></tr><tr><td> imageColor</td><td> Bildfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> iconHeight</td><td> Bildhöhe</td><td> Nummer</td><td/></tr><tr><td> colorPress</td><td> Farbe gedrückt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr></tbody></table></details>

##### Fortschritt
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td></td></tr><tr><td> unbestimmt</td><td> unbestimmt - kontinuierlich animiert</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> Mindest</td><td> Mindest</td><td> Zeichenfolge</td><td></td></tr><tr><td> max</td><td> max</td><td> Zeichenfolge</td><td></td></tr><tr><td> umkehren</td><td> Kehrt den Wert um</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> progressRounded</td><td> abgerundete Ecken</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> progressStriped</td><td> gestreift</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> progressStripedColor</td><td> progressStripedColor</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorProgressBackground</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorProgress</td><td> Farbfortschritt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorOneCondition</td><td> Bedingung für Farbe 1 Fortschritt [&gt;]</td><td> Zeichenfolge</td><td></td></tr><tr><td> colorOne</td><td> Farbe 1 Fortschritt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorTwoCondition</td><td> Bedingung für den Fortschritt von Farbe 2 [&gt;]</td><td> Zeichenfolge</td><td></td></tr><tr><td> colorTwo</td><td> Farbe 2 Fortschritt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showValueLabel</td><td> Wert anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueLabelStyle</td><td> Wertbeschriftungsstil</td><td> Zeichenfolge</td><td> progressPercent | progressValue | progressCustom</td></tr><tr><td> valueLabelUnit</td><td> Einheit</td><td> Zeichenfolge</td><td></td></tr><tr><td> valueMaxDecimals</td><td> Dezimalpunkte</td><td> Nummer</td><td></td></tr><tr><td> valueLabelCustom</td><td> valueLabelCustom</td><td> Zeichenfolge</td><td></td></tr><tr><td> Textfarbe</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> textFontSize</td><td> Textgröße</td><td> Nummer</td><td></td></tr><tr><td> textFontFamily</td><td> textFontFamily</td><td> Zeichenfolge</td><td></td></tr><tr><td> Textausrichtung</td><td> Textausrichtung</td><td> Zeichenfolge</td><td> start | Mitte | Ende</td></tr></tbody></table></details>

##### Fortschrittsrundschreiben
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> Mindest</td><td> Mindest</td><td> Zeichenfolge</td><td/></tr><tr><td> max</td><td> max</td><td> Zeichenfolge</td><td/></tr><tr><td> progressCircularSize</td><td> Größe</td><td> Nummer</td><td/></tr><tr><td> progressCircularWidth</td><td> Dicke</td><td> Nummer</td><td/></tr><tr><td> progressCircularRotate</td><td> Startpunkt drehen</td><td> Nummer</td><td/></tr><tr><td> colorProgressBackground</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorProgress</td><td> Farbfortschritt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> innerColor</td><td> Kreis Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorOneCondition</td><td> Bedingung für Farbe 1 Fortschritt [&gt;]</td><td> Nummer</td><td/></tr><tr><td> colorOne</td><td> Farbe 1 Fortschritt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorTwoCondition</td><td> Bedingung für den Fortschritt von Farbe 2 [&gt;]</td><td> Nummer</td><td/></tr><tr><td> colorTwo</td><td> Farbe 2 Fortschritt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showValueLabel</td><td> Wert anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueLabelStyle</td><td> Wertbeschriftungsstil</td><td> Zeichenfolge</td><td> progressPercent | progressValue | progressCustom</td></tr><tr><td> valueLabelUnit</td><td> Einheit</td><td> Zeichenfolge</td><td/></tr><tr><td> valueMaxDecimals</td><td> Dezimalpunkte</td><td> Nummer</td><td/></tr><tr><td> valueLabelCustom</td><td> valueLabelCustom</td><td> Zeichenfolge</td><td/></tr><tr><td> Textfarbe</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> textFontSize</td><td> Textgröße</td><td> Nummer</td><td/></tr><tr><td> textFontFamily</td><td> textFontFamily</td><td> Zeichenfolge</td><td/></tr></tbody></table></details>

##### Schieberegler
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td></td></tr><tr><td> oid-arbeiten</td><td> Arbeitsobjekt-ID</td><td> Zeichenfolge</td><td></td></tr><tr><td> Orientierung</td><td> Orientierung</td><td> Zeichenfolge</td><td> horizontal | vertikal</td></tr><tr><td> reverseSlider</td><td> Schieberegler umkehren</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> knopfgröße</td><td> Knopfgröße</td><td> Zeichenfolge</td><td> knobSmall | knobMedium | knaufBig</td></tr><tr><td> schreibgeschützt</td><td> schreibgeschützt</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> Mindest</td><td> Mindest</td><td> Zeichenfolge</td><td></td></tr><tr><td> max</td><td> max</td><td> Zeichenfolge</td><td></td></tr><tr><td> Schritt</td><td> Schritte</td><td> Zeichenfolge</td><td></td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td></td></tr><tr><td> showTicks</td><td> Schritte zeigen</td><td> Zeichenfolge</td><td> nein | ja | immer</td></tr><tr><td> tickSize</td><td> Anzeigegröße der Schritte</td><td> Nummer</td><td></td></tr><tr><td> tickLabels</td><td> Text der Schritte (durch Kommas getrennt)</td><td> Zeichenfolge</td><td></td></tr><tr><td> tickColorBefore</td><td> Farbe vor dem Regler</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> tickColorAfter</td><td> Farbe nach dem Regler</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorBeforeThumb</td><td> Farbe vor dem Regler</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorThumb</td><td> Farbe des Reglers</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorAfterThumb</td><td> Farbe nach dem Regler</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandText</td><td> Text vorangestellt</td><td> Zeichenfolge</td><td></td></tr><tr><td> prepandTextWidth</td><td> prepandTextWidth</td><td> Nummer</td><td></td></tr><tr><td> prepandTextColor</td><td> Farbe des vorgefertigten Textes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandTextFontSize</td><td> Textgröße vorab erweitert</td><td> Nummer</td><td></td></tr><tr><td> prepandTextFontFamily</td><td> Schriftart des Textes vorangestellt</td><td> Zeichenfolge</td><td></td></tr><tr><td> showValueLabel</td><td> Wert anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueLabelStyle</td><td> Wertbeschriftungsstil</td><td> Zeichenfolge</td><td> sliderPercent | sliderValue</td></tr><tr><td> valueLabelUnit</td><td> Einheit</td><td> Zeichenfolge</td><td></td></tr><tr><td> valueLabelMin</td><td> Text für Wert kleiner als min</td><td> Zeichenfolge</td><td></td></tr><tr><td> valueLabelMax</td><td> Text für Wert größer als min</td><td> Zeichenfolge</td><td></td></tr><tr><td> valueLessThan</td><td> &#39;kleiner als&#39; Bedingung für den Text des Wertes</td><td> Nummer</td><td></td></tr><tr><td> textForValueLessThan</td><td> Text für &#39;kleiner als&#39;</td><td> Zeichenfolge</td><td></td></tr><tr><td> valueGreaterThan</td><td> Bedingung &#39;größer als&#39; für den Text des Werts</td><td> Nummer</td><td></td></tr><tr><td> textForValueGreaterThan</td><td> Text für &#39;größer als&#39;</td><td> Zeichenfolge</td><td></td></tr><tr><td> valueLabelWidth</td><td> Abstandsetikett</td><td> Nummer</td><td></td></tr><tr><td> showThumbLabel</td><td> Etikett anzeigen</td><td> Zeichenfolge</td><td> nein | ja | immer</td></tr><tr><td> thumbSize</td><td> Etikettengröße</td><td> Nummer</td><td></td></tr><tr><td> thumbBackgroundColor</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> thumbFontColor</td><td> Schriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> thumbFontSize</td><td> Schriftgröße</td><td> Nummer</td><td></td></tr><tr><td> thumbFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td></td></tr><tr><td> useLabelRules</td><td> Verwenden Sie die Regeln des Textes</td><td> Boolescher Wert</td><td> false | wahr</td></tr></tbody></table></details>

##### Slider Round
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> oid-arbeiten</td><td> Arbeitsobjekt-ID</td><td> Zeichenfolge</td><td/></tr><tr><td> Mindest</td><td> Mindest</td><td> Zeichenfolge</td><td/></tr><tr><td> max</td><td> max</td><td> Zeichenfolge</td><td/></tr><tr><td> Schritt</td><td> Schritte</td><td> Zeichenfolge</td><td/></tr><tr><td> schreibgeschützt</td><td> nur lesend</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> startAngle</td><td> Startwinkel</td><td> Nummer</td><td/></tr><tr><td> Bogenlänge</td><td> Bogenlänge</td><td> Nummer</td><td/></tr><tr><td> sliderWidth</td><td> Slider Thikness</td><td> Nummer</td><td/></tr><tr><td> handleSize</td><td> Knopfgröße</td><td> Nummer</td><td/></tr><tr><td> handleZoom</td><td> Knopfzoom bei Steuerung</td><td> Nummer</td><td/></tr><tr><td> rtl</td><td> Schiebereglerbewegung von rechts nach links</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> colorSliderBg</td><td> Hintergrund</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorBeforeThumb</td><td> Farbe vor dem Regler</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorThumb</td><td> Farbe des Reglers</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorAfterThumb</td><td> Farbe nach dem Regler</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> valueLabelColor</td><td> Textfarbe des Wertes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showValueLabel</td><td> Wert anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> valueLabelVerticalPosition</td><td> vertikale Textposition des Wertes</td><td> Nummer</td><td/></tr><tr><td> valueLabelStyle</td><td> Wertbeschriftungsstil</td><td> Zeichenfolge</td><td> sliderPercent | sliderValue</td></tr><tr><td> valueLabelUnit</td><td> Einheit</td><td> Zeichenfolge</td><td/></tr><tr><td> valueLabelMin</td><td> Text für Wert kleiner als min</td><td> Zeichenfolge</td><td/></tr><tr><td> valueLabelMax</td><td> Text für Wert größer als min</td><td> Zeichenfolge</td><td/></tr><tr><td> valueLessThan</td><td> &#39;kleiner als&#39; Bedingung für den Text des Wertes</td><td> Nummer</td><td/></tr><tr><td> textForValueLessThan</td><td> Text für &#39;kleiner als&#39;</td><td> Zeichenfolge</td><td/></tr><tr><td> valueGreaterThan</td><td> Bedingung &#39;größer als&#39; für den Text des Werts</td><td> Nummer</td><td/></tr><tr><td> textForValueGreaterThan</td><td> Text für &#39;größer als&#39;</td><td> Zeichenfolge</td><td/></tr></tbody></table></details>

##### Schalter
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> schreibgeschützt</td><td> nur lesend</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> toggleType</td><td> Art der Umschaltung</td><td> Zeichenfolge</td><td> boolean | Wert</td></tr><tr><td> valueOff</td><td> Wert für aus</td><td> Zeichenfolge</td><td/></tr><tr><td> valueOn</td><td> Wert für ein</td><td> Zeichenfolge</td><td/></tr><tr><td> stateIfNotTrueValue</td><td> Zustand, wenn der Wert nicht der Bedingung</td><td> Zeichenfolge</td><td> am | aus</td></tr><tr><td> vibrateOnMobilDevices</td><td> auf mobile Ger�ten vibrieren [s]</td><td> Nummer</td><td/></tr><tr><td> labelFalse</td><td> Beschriftung Falsch</td><td> Zeichenfolge</td><td/></tr><tr><td> labelTrue</td><td> Beschriftung Richtig</td><td> Zeichenfolge</td><td/></tr><tr><td> labelPosition</td><td> labelPosition</td><td> Zeichenfolge</td><td> links | rechts | aus</td></tr><tr><td> labelClickActive</td><td> Beschriftungs-Klick-Einstellungen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> colorSwitchThumb</td><td> Knopffarbe des Schalters</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorSwitchTrack</td><td> Schieberfarbe des Schalters</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorSwitchTrue</td><td> aktiv Schalterfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorSwitchHover</td><td> Schalterfarbe ausgewähltiert / schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> colorSwitchHoverTrue</td><td> Schalterfarbe ausgewähltiert / hover für Aktiviert</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelColorFalse</td><td> Beschriftungsfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelColorTrue</td><td> Beschriftungsfarbe für wahr</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockEnabled</td><td> Verriegeln Eigenschaften</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatisch Verriegeln nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconTop</td><td> Symbolabstand von oben [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconLeft</td><td> Symbolabstand von links [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgr��e</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn verriegelt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Kontrollkästchen
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> schreibgeschützt</td><td> nur lesend</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> toggleType</td><td> Art der Umschaltung</td><td> Zeichenfolge</td><td> boolean | Wert</td></tr><tr><td> valueOff</td><td> Wert für aus</td><td> Zeichenfolge</td><td/></tr><tr><td> valueOn</td><td> Wert für ein</td><td> Zeichenfolge</td><td/></tr><tr><td> stateIfNotTrueValue</td><td> Zustand, wenn der Wert nicht der Bedingung</td><td> Zeichenfolge</td><td> am | aus</td></tr><tr><td> vibrateOnMobilDevices</td><td> auf mobile Ger�ten vibrieren [s]</td><td> Nummer</td><td/></tr><tr><td> labelFalse</td><td> Beschriftung Falsch</td><td> Zeichenfolge</td><td/></tr><tr><td> labelTrue</td><td> Beschriftung Richtig</td><td> Zeichenfolge</td><td/></tr><tr><td> labelPosition</td><td> labelPosition</td><td> Zeichenfolge</td><td> links | Recht</td></tr><tr><td> labelClickActive</td><td> Beschriftungs-Klick-Einstellungen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> colorCheckBox</td><td> Kontrollk�stchen Farbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelColorFalse</td><td> Beschriftungsfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> labelColorTrue</td><td> Beschriftungsfarbe für wahr</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockEnabled</td><td> Verriegeln Eigenschaften</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> autoLockAfter</td><td> automatisch Verriegeln nach [s]</td><td> Nummer</td><td/></tr><tr><td> lockIcon</td><td> Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> lockIconTop</td><td> Symbolabstand von oben [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconLeft</td><td> Symbolabstand von links [%]</td><td> Nummer</td><td/></tr><tr><td> lockIconSize</td><td> Symbolgr��e</td><td> Nummer</td><td/></tr><tr><td> lockIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> lockFilterGrayscale</td><td> Graufilter, wenn verriegelt</td><td> Nummer</td><td/></tr></tbody></table></details>

##### Textfeld
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> Eingabetyp</td><td> Eingabetyp</td><td> Zeichenfolge</td><td> Text | Nummer | Datum | Zeit | Maske</td></tr><tr><td> inputAlignment</td><td> Textausrichtung</td><td> Zeichenfolge</td><td> links | Mitte | Recht</td></tr><tr><td> Eingabemaske</td><td> Eingabemaske</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMaxLength</td><td> inputMaxLength</td><td> Nummer</td><td/></tr><tr><td> inputLayout</td><td> Layout</td><td> Zeichenfolge</td><td> regelmäßig | solo | solo gerundet | solo geformt | gefüllt | gefüllt-gerundet | gefüllt-förmig | umrissen | umrissen gerundet | umrissen</td></tr><tr><td> inputLayoutBackgroundColor</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBackgroundColorHover</td><td> Hintergrundfarbe schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBackgroundColorSelected</td><td> Hintergrundfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColor</td><td> Randfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColorHover</td><td> Randfarbe schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColorSelected</td><td> Rahmenfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputTextFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputTextFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputTextColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelText</td><td> Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputLabelColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelColorSelected</td><td> Textfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputLabelFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputTranslateX</td><td> Versatz x</td><td> Nummer</td><td/></tr><tr><td> inputTranslateY</td><td> Versatz y</td><td> Nummer</td><td/></tr><tr><td> inputPrefix</td><td> vorangestellter Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputSuffix</td><td> angehängter Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputAppendixColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputAppendixFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputAppendixFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> showInputMessageAlways</td><td> immer anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> inputMessage</td><td> Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMessageFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMessageFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputMessageColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showInputCounter</td><td> Zähler anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> inputCounterColor</td><td> Schriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputCounterFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputCounterFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> clearIconShow</td><td> Symbol zum Löschen von Text anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> clearIcon</td><td> Symbol zum Löschen von Text</td><td> Benutzerdefiniert</td><td/></tr><tr><td> clearIconSize</td><td> Größe des Textlöschsymbols</td><td> Nummer</td><td/></tr><tr><td> clearIconColor</td><td> Farbe des Textes Löschsymbol</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandIcon</td><td> vorangestelltes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> prepandIconSize</td><td> Größe des vorangestellten Symbols</td><td> Nummer</td><td/></tr><tr><td> prepandIconColor</td><td> Farbe des vorangestellten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandInnerIcon</td><td> inneres vorangestelltes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> prepandInnerIconSize</td><td> Größe des inneren vorangestellten Symbols</td><td> Nummer</td><td/></tr><tr><td> prepandInnerIconColor</td><td> Farbe des inneren vorangestellten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> appendIcon</td><td> angehängtes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> appendIconSize</td><td> Größe des angehängten Symbols</td><td> Nummer</td><td/></tr><tr><td> appendIconColor</td><td> Farbe des angehängten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> appendOuterIcon</td><td> äußeres angehängtes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> appendOuterIconSize</td><td> Größe des äußeren angehängten Symbols</td><td> Nummer</td><td/></tr><tr><td> appendOuterIconColor</td><td> Farbe des äußeren angehängten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr></tbody></table></details>

##### Wählen
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> Eingabetyp</td><td> Eingabetyp</td><td> Zeichenfolge</td><td> Text | Datum | Zeit</td></tr><tr><td> inputAlignment</td><td> Textausrichtung</td><td> Zeichenfolge</td><td> links | Mitte | Recht</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> inputLayout</td><td> Layout</td><td> Zeichenfolge</td><td> regelmäßig | solo | solo gerundet | solo geformt | gefüllt | gefüllt-gerundet | gefüllt-förmig | umrissen | umrissen gerundet | umrissen</td></tr><tr><td> inputLayoutBackgroundColor</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBackgroundColorHover</td><td> Hintergrundfarbe schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBackgroundColorSelected</td><td> Hintergrundfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColor</td><td> Randfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColorHover</td><td> Randfarbe schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColorSelected</td><td> Rahmenfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputTextFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputTextFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputTextColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelText</td><td> Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputLabelColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelColorSelected</td><td> Textfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputLabelFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputTranslateX</td><td> Versatz x</td><td> Nummer</td><td/></tr><tr><td> inputTranslateY</td><td> Versatz y</td><td> Nummer</td><td/></tr><tr><td> inputPrefix</td><td> vorangestellter Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputSuffix</td><td> angehängter Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputAppendixColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputAppendixFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputAppendixFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> showInputMessageAlways</td><td> immer anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> inputMessage</td><td> Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMessageFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMessageFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputMessageColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showInputCounter</td><td> Zähler anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> inputCounterColor</td><td> Schriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputCounterFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputCounterFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> clearIconShow</td><td> Symbol zum Löschen von Text anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> clearIcon</td><td> Symbol zum Löschen von Text</td><td> Benutzerdefiniert</td><td/></tr><tr><td> clearIconSize</td><td> Größe des Textlöschsymbols</td><td> Nummer</td><td/></tr><tr><td> clearIconColor</td><td> Farbe des Textes Löschsymbol</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> ZusammenbruchIcon</td><td> Menü öffnen Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> kollabierenIconSize</td><td> Größe des Symbols zum Öffnen des Menüs</td><td> Nummer</td><td/></tr><tr><td> kollabierenIconColor</td><td> Farbe des offenen Menüsymbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandIcon</td><td> vorangestelltes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> prepandIconSize</td><td> Größe des vorangestellten Symbols</td><td> Nummer</td><td/></tr><tr><td> prepandIconColor</td><td> Farbe des vorangestellten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandInnerIcon</td><td> inneres vorangestelltes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> prepandInnerIconSize</td><td> Größe des inneren vorangestellten Symbols</td><td> Nummer</td><td/></tr><tr><td> prepandInnerIconColor</td><td> Farbe des inneren vorangestellten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> appendOuterIcon</td><td> äußeres angehängtes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> appendOuterIconSize</td><td> Größe des äußeren angehängten Symbols</td><td> Nummer</td><td/></tr><tr><td> appendOuterIconColor</td><td> Farbe des äußeren angehängten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listDataMethod</td><td> Eingabemethode für die Menüdaten</td><td> Zeichenfolge</td><td> inputPerEditor | jsonStringObject | multistatesObject | valueList</td></tr><tr><td> countSelectItems</td><td> Editor: Anzahl der Menüpunkte</td><td> Nummer</td><td/></tr><tr><td> jsonStringObject</td><td> JSON-Zeichenfolge</td><td> Zeichenfolge</td><td> Bindungen funktionieren nicht!</td></tr><tr><td> valueList</td><td> Werteliste</td><td> Zeichenfolge</td><td/></tr><tr><td> valueListLabels</td><td> Werteliste: Labels</td><td> Zeichenfolge</td><td/></tr><tr><td> valueListIcons</td><td> Werteliste: Bilder</td><td> Zeichenfolge</td><td/></tr><tr><td> listPosition</td><td> Position</td><td> Zeichenfolge</td><td> auto | Nach oben | Unterseite</td></tr><tr><td> listPositionOffset</td><td> Positionsversatz verwenden</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> listItemHeight</td><td> Höhe des Menüpunktes</td><td> Nummer</td><td/></tr><tr><td> listItemBackgroundColor</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemBackgroundHoverColor</td><td> Schwebefarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemBackgroundSelectedColor</td><td> Farbe des ausgewählten Elements</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemRippleEffectColor</td><td> Effektfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showSelectedIcon</td><td> Symbol des ausgewählten Elements anzeigen</td><td> Zeichenfolge</td><td> nein | voranstellen | prepend-inner | Append-Outer</td></tr><tr><td> listIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> listIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listIconHoverColor</td><td> Symbol Schwebefarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listIconSelectedColor</td><td> Symbolfarbe des ausgewählten Elements</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> listItemFont</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> listItemFontColor</td><td> Schriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemFontHoverColor</td><td> Schrift schweben Farbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemFontSelectedColor</td><td> Schriftfarbe des ausgewählten Elements</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemSubFontSize</td><td> zweite Textschriftgröße</td><td> Nummer</td><td/></tr><tr><td> listItemSubFont</td><td> zweite Textschrift</td><td> Zeichenfolge</td><td/></tr><tr><td> listItemSubFontColor</td><td> zweite Textschriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemSubFontHoverColor</td><td> Schwebefarbe des zweiten Textes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemSubFontSelectedColor</td><td> Farbe des zweiten ausgewählten Textes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showValue</td><td> Wert anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> listItemValueFontSize</td><td> Schriftgröße des Wertes</td><td> Nummer</td><td/></tr><tr><td> listItemValueFont</td><td> Schriftart des Wertes</td><td> Zeichenfolge</td><td/></tr><tr><td> listItemValueFontColor</td><td> Schriftfarbe des Wertes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemValueFontHoverColor</td><td> Hover-Schriftfarbe des Werts</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemValueFontSelectedColor</td><td> Schriftfarbe des ausgewählten Werts</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> Wert <b><i>X.</i></b></td><td> Wert des Menüpunktes X.</td><td> Zeichenfolge</td><td/></tr><tr><td> Etikett <b><i>X.</i></b></td><td> Beschriftung des Menüpunktes X.</td><td> Zeichenfolge</td><td/></tr><tr><td> subLabel <b><i>X.</i></b></td><td> Unteretikett des Menüpunktes X.</td><td> Zeichenfolge</td><td/></tr><tr><td> listIcon <b><i>X.</i></b></td><td> listIcon von Menüpunkt X.</td><td> Benutzerdefiniert</td><td/></tr><tr><td> listIconColor <b><i>X.</i></b></td><td> listIconColor von Menüpunkt X.</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr></table></details>

##### Autocomplete
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> oid</td><td> Objekt Identifikation</td><td> Zeichenfolge</td><td/></tr><tr><td> Eingabemodus</td><td> Eingabemodus</td><td> Zeichenfolge</td><td> schreiben | wählen</td></tr><tr><td> Eingabetyp</td><td> Eingabetyp</td><td> Zeichenfolge</td><td> Text | Datum | Zeit</td></tr><tr><td> inputAlignment</td><td> Textausrichtung</td><td> Zeichenfolge</td><td> links | Mitte | Recht</td></tr><tr><td> vibrateOnMobilDevices</td><td> vibrieren auf mobilen Geräten [s]</td><td> Nummer</td><td/></tr><tr><td> inputLayout</td><td> Layout</td><td> Zeichenfolge</td><td> regelmäßig | solo | solo gerundet | solo geformt | gefüllt | gefüllt-gerundet | gefüllt-förmig | umrissen | umrissen gerundet | umrissen</td></tr><tr><td> inputLayoutBackgroundColor</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBackgroundColorHover</td><td> Hintergrundfarbe schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBackgroundColorSelected</td><td> Hintergrundfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColor</td><td> Randfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColorHover</td><td> Randfarbe schweben</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLayoutBorderColorSelected</td><td> Rahmenfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputTextFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputTextFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputTextColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelText</td><td> Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputLabelColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelColorSelected</td><td> Textfarbe ausgewählt</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputLabelFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputLabelFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputTranslateX</td><td> Versatz x</td><td> Nummer</td><td/></tr><tr><td> inputTranslateY</td><td> Versatz y</td><td> Nummer</td><td/></tr><tr><td> inputPrefix</td><td> vorangestellter Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputSuffix</td><td> angehängter Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputAppendixColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputAppendixFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputAppendixFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> showInputMessageAlways</td><td> immer anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> inputMessage</td><td> Text</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMessageFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> inputMessageFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputMessageColor</td><td> Textfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showInputCounter</td><td> Zähler anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> inputCounterColor</td><td> Schriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> inputCounterFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> inputCounterFontFamily</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> clearIconShow</td><td> Symbol zum Löschen von Text anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> clearIcon</td><td> Symbol zum Löschen von Text</td><td> Benutzerdefiniert</td><td/></tr><tr><td> clearIconSize</td><td> Größe des Textlöschsymbols</td><td> Nummer</td><td/></tr><tr><td> clearIconColor</td><td> Farbe des Textes Löschsymbol</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> ZusammenbruchIcon</td><td> Menü öffnen Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> kollabierenIconSize</td><td> Größe des Symbols zum Öffnen des Menüs</td><td> Nummer</td><td/></tr><tr><td> kollabierenIconColor</td><td> Farbe des offenen Menüsymbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandIcon</td><td> vorangestelltes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> prepandIconSize</td><td> Größe des vorangestellten Symbols</td><td> Nummer</td><td/></tr><tr><td> prepandIconColor</td><td> Farbe des vorangestellten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> prepandInnerIcon</td><td> inneres vorangestelltes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> prepandInnerIconSize</td><td> Größe des inneren vorangestellten Symbols</td><td> Nummer</td><td/></tr><tr><td> prepandInnerIconColor</td><td> Farbe des inneren vorangestellten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> appendOuterIcon</td><td> äußeres angehängtes Symbol</td><td> Benutzerdefiniert</td><td/></tr><tr><td> appendOuterIconSize</td><td> Größe des äußeren angehängten Symbols</td><td> Nummer</td><td/></tr><tr><td> appendOuterIconColor</td><td> Farbe des äußeren angehängten Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listDataMethod</td><td> Eingabemethode für die Menüdaten</td><td> Zeichenfolge</td><td> inputPerEditor | jsonStringObject | multistatesObject | valueList</td></tr><tr><td> countSelectItems</td><td> Editor: Anzahl der Menüpunkte</td><td> Nummer</td><td/></tr><tr><td> jsonStringObject</td><td> JSON-Zeichenfolge</td><td> Zeichenfolge</td><td> Bindungen funktionieren nicht!</td></tr><tr><td> valueList</td><td> Werteliste</td><td> Zeichenfolge</td><td/></tr><tr><td> valueListLabels</td><td> Werteliste: Labels</td><td> Zeichenfolge</td><td/></tr><tr><td> valueListIcons</td><td> Werteliste: Bilder</td><td> Zeichenfolge</td><td/></tr><tr><td> listPosition</td><td> Position</td><td> Zeichenfolge</td><td> auto | Nach oben | Unterseite</td></tr><tr><td> listPositionOffset</td><td> Positionsversatz verwenden</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> listItemHeight</td><td> Höhe des Menüpunktes</td><td> Nummer</td><td/></tr><tr><td> listItemBackgroundColor</td><td> Hintergrundfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemBackgroundHoverColor</td><td> Schwebefarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemBackgroundSelectedColor</td><td> Farbe des ausgewählten Elements</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemRippleEffectColor</td><td> Effektfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showSelectedIcon</td><td> Symbol des ausgewählten Elements anzeigen</td><td> Zeichenfolge</td><td> nein | voranstellen | prepend-inner | Append-Outer</td></tr><tr><td> listIconSize</td><td> Symbolgröße</td><td> Nummer</td><td/></tr><tr><td> listIconColor</td><td> Symbolfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listIconHoverColor</td><td> Symbol Schwebefarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listIconSelectedColor</td><td> Symbolfarbe des ausgewählten Elements</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemFontSize</td><td> Schriftgröße</td><td> Nummer</td><td/></tr><tr><td> listItemFont</td><td> Schriftart</td><td> Zeichenfolge</td><td/></tr><tr><td> listItemFontColor</td><td> Schriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemFontHoverColor</td><td> Schrift schweben Farbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemFontSelectedColor</td><td> Schriftfarbe des ausgewählten Elements</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemSubFontSize</td><td> zweite Textschriftgröße</td><td> Nummer</td><td/></tr><tr><td> listItemSubFont</td><td> zweite Textschrift</td><td> Zeichenfolge</td><td/></tr><tr><td> listItemSubFontColor</td><td> zweite Textschriftfarbe</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemSubFontHoverColor</td><td> Schwebefarbe des zweiten Textes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemSubFontSelectedColor</td><td> Farbe des zweiten ausgewählten Textes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> showValue</td><td> Wert anzeigen</td><td> Boolescher Wert</td><td> false | wahr</td></tr><tr><td> listItemValueFontSize</td><td> Schriftgröße des Wertes</td><td> Nummer</td><td/></tr><tr><td> listItemValueFont</td><td> Schriftart des Wertes</td><td> Zeichenfolge</td><td/></tr><tr><td> listItemValueFontColor</td><td> Schriftfarbe des Wertes</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemValueFontHoverColor</td><td> Hover-Schriftfarbe des Werts</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> listItemValueFontSelectedColor</td><td> Schriftfarbe des ausgewählten Werts</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> value0</td><td> value0</td><td> Zeichenfolge</td><td/></tr><tr><td> label0</td><td> label0</td><td> Zeichenfolge</td><td/></tr><tr><td> subLabel0</td><td> subLabel0</td><td> Zeichenfolge</td><td/></tr><tr><td> listIcon0</td><td> listIcon0</td><td> Benutzerdefiniert</td><td/></tr><tr><td> listIconColor0</td><td> listIconColor0</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr><tr><td> value1</td><td> value1</td><td> Zeichenfolge</td><td/></tr><tr><td> label1</td><td> label1</td><td> Zeichenfolge</td><td/></tr><tr><td> subLabel1</td><td> subLabel1</td><td> Zeichenfolge</td><td/></tr><tr><td> listIcon1</td><td> listIcon1</td><td> Benutzerdefiniert</td><td/></tr><tr><td> listIconColor1</td><td> listIconColor1</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr></tbody></table></details>

##### Material Design Icons
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> mdwIcon</td><td> <a href="https://materialdesignicons.com/">materialdesignicon name</a></td><td> Zeichenfolge</td><td> Zuhause, ...</td></tr><tr><td> mdwIconSize</td><td> Größe des Symbols</td><td> Nummer</td><td> 0, 1, 2, ...</td></tr><tr><td> mdwIconColor</td><td> Farbe des Symbols</td><td> Zeichenfolge</td><td> hex (# 44739e), rgb (20, 50, 200), rgba (20, 50, 200, 0,5)</td></tr></tbody></table></details>

##### Html
<details><table><thead><tr><th>Eigentum</th><th> Beschreibung</th><th> Art</th><th> Werte</th></tr></thead><tbody><tr><td> html</td><td> ein beliebiges HTML-Element</td><td> Zeichenfolge</td><td></td></tr><tr><td> oid</td><td> Objekt-ID, die in HTML verwendet werden soll. Verwenden Sie in HTML &#39;[#value]&#39; als Wert</td><td> Zeichenfolge</td><td></td></tr></tbody></table></details>

<br>

### Editoreinstellungen
<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=2><img src="doc/en/media/table_general.png"></td><td> Schalter</td><td> Datenpunkt aus Typzeichenfolge mit Eingabedaten wie oben gezeigt</td></tr><tr><td> Daten als JSON</td><td> Optional können Sie Daten wie oben gezeigt eingeben, wenn kein OID-Datenpunkt festgelegt ist</td></tr><tr><td rowspan=4><img src="doc/en/media/table_column.png"></td><td> colType [x]</td><td> Wenn Bild ausgewählt ist, muss die Objekteigenschaft den Pfad zum Bild haben ( <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign#input-data">siehe oben</a> ).</td></tr><tr><td> Präfix [x]</td><td> Das Präfix für Objekteigenschaft, interne Objektbindung ( <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign#internal-object-binding">siehe unten</a> ) und HTML kann verwendet werden</td></tr><tr><td> Suffix [x]</td><td> Es können Suffixe für Objekteigenschaften, interne Objektbindung ( <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign#internal-object-binding">siehe unten</a> ) und HTML verwendet werden</td></tr><tr><td> Objektname zum Sortieren [x]</td><td> Hier können Sie eine andere Objekteigenschaft definieren, die zum Sortieren verwendet werden soll.</td></tr></tbody></table>

##### Interne Objektbindung
Präfix & Suffix unterstützt die tabelleninterne Objektbindung -> Sie können mit auf andere Objekteigenschaften zugreifen

```
#[obj.'propertyName']
```

Beispiel <a href="https://github.com/Scrounger/ioBroker.vis-materialdesign#input-data">siehe oben</a> .

Ein Beispiel für ein funktionierendes Widget finden Sie hier

* [hier] (https://forum.iobroker.net/topic/26199/test-adapter-material-design-widgets-v0-1-x/113)
* [ical Adapter] (https://forum.iobroker.net/topic/29658/material-design-widgets-table-widget/2)

## Responsive Layout
Es gibt zwei Widgets - Masonry Views und Grid Views - mit denen ein reaktionsfähiges Layout erstellt werden kann (ein Layout für Desktop, Tablet und Mobile). In beiden Widgets sind mehrere `view in widget` integriert.

### Mauerwerksansichten
In Masonry Views sind mehrere `view in widget` integriert, die je nach Breite des Widgets automatisch sortiert werden. Mit diesem Widget ist es möglich, ein ansprechendes Layout zu erstellen (ein Layout für Desktop, Tablet und Handy).
Mauerwerksansichten sind besonders nützlich, wenn die enthaltenen Ansichten unterschiedliche Höhen haben.

<b>Schauen Sie sich die [Beispielprojekt für Material Design Widgets](https://github.com/Scrounger/ioBroker.vis-materialdesign#online-example-project)</b> an, um zu verstehen, wie es funktioniert.

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/masnory.gif)

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung </th></tr></thead><tbody><tr><td rowspan=1><img src="doc/en/media/masonry_resolution_settings.png"></td><td colspan=2>Abhängig von der Breite des Widgets können die Anzahl der Spalten und der Abstand zwischen den Ansichten festgelegt werden. Die Einstellungen können unabhängig voneinander für das Hoch- und Querformat vorgenommen werden. Aktivieren Sie den Auflösungsassistenten unter den allgemeinen Einstellungen, um die Breite der Auflösung für die verschiedenen Geräte zu ermitteln.</td></tr><tr><td rowspan=2><img src="doc/en/media/masnory_settings_views.png"></td><td> Sichtweite [x]</td><td> Definieren Sie die Breite der Ansicht. Zulässige Werte sind number, px,% oder calc. Beispiele: <code>100</code> , <code>100px</code> , <code>55%</code> , <code>calc(60% - 12px)</code></td></tr><tr><td> Sichthöhe [x]</td><td> Hier können Sie die Höhe der verwendeten Ansicht festlegen.<br><br> Wenn Sie möchten, dass die Höhe variabel an die Ansicht angepasst wird, muss diese Eingabe leer sein, und für das Widget mit der höchsten Höhe in der Ansicht muss die Position auf relativ gesetzt werden (siehe Screenshot).<br><br><img src="doc/en/media/masonry_grid_position_settings.png"></td></tr></tbody></table>

### Rasteransichten
In Grid Views sind mehrere `view in widget` integriert, die je nach Breite des Widgets automatisch sortiert werden. Mit diesem Widget ist es möglich, ein ansprechendes Layout zu erstellen (ein Layout für Desktop, Tablet und Handy).
Rasteransichten sind besonders nützlich, wenn die enthaltenen Ansichten dieselbe Höhe haben.

<b>Das Widget &quot;Rasteransicht&quot; enthält insgesamt 12 Spalten. Wenn eine Ansicht eine Breite von 4 Spalten haben soll, müssen Sie in der entsprechenden Ansicht [x] die Spaltenspanne auf 4 setzen.</b>

<b>Schauen Sie sich die [Beispielprojekt für Material Design Widgets](https://github.com/Scrounger/ioBroker.vis-materialdesign#online-example-project)</b> an, um zu verstehen, wie es funktioniert.

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/grid.gif)

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung </th></tr></thead><tbody><tr><td rowspan=1><img src="doc/en/media/grid_settings_resolution.png"></td><td colspan=2> Abhängig von der Breite des Widgets wird festgelegt, ab welcher Breite des Widgets die Regeln für die Spaltenspanne der einzelnen Ansichten [x] und der Abstand zwischen den Ansichten angewendet werden können. Die Einstellungen können unabhängig voneinander für das Hoch- und Querformat vorgenommen werden. Aktivieren Sie den Auflösungsassistenten unter den allgemeinen Einstellungen, um die Breite der Auflösung für die verschiedenen Geräte zu ermitteln.</td></tr><tr><td rowspan=2><img src="doc/en/media/grid_settings_view.png"></td><td colspan=2> Definieren Sie die Spaltenspanne der Ansicht in Abhängigkeit von der aktuellen Auflösungsregel für die Breite.<br> Hier können Sie auch festlegen, ob eine Ansicht nur mit einer Auflösung angezeigt werden soll, die höher oder niedriger als ein definierter Wert ist, oder ob sie über eine Objekt-ID sichtbar sein soll.</td></tr><tr><td> Sichthöhe [x]</td><td> Hier können Sie die Höhe der verwendeten Ansicht festlegen.<br><br> Wenn Sie möchten, dass die Höhe variabel an die Ansicht angepasst wird, muss diese Eingabe leer sein, und für das Widget mit der höchsten Höhe in der Ansicht muss die Position auf relativ gesetzt werden (siehe Screenshot).<br><br><img src="doc/en/media/masonry_grid_position_settings.png"></td></tbody></table>

## Warnungen
Das Warnungs-Widget kann z.B. Anzeigen von Nachrichten im VIS, wie es mit dem Pushover-Adapter funktioniert, jedoch direkt im VIS.

![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/alerts.gif)

Das Alerts-Widget erfordert eine JSON-Zeichenfolge als Objekt, die wie folgt strukturiert sein muss:

```
[
       {
		"text": "we have a new message",
		"backgroundColor": "",
		"borderColor": "darkred",
		"icon": "message-alert-outline",
		"iconColor": "darkred",
		"fontColor": "blue"
	}, {
		"text": "we have a new message",
		"backgroundColor": "#e6b0aa",
		"borderColor": "green",
		"icon": "/vis/img/bulb_on.png",
		"iconColor": "green",
		"fontColor": "gold"
	}, {
		"text": "we have a new message",
		"backgroundColor": "",
		"borderColor": "gold",
		"icon": "alert-outline",
		"iconColor": "gold",
		"fontColor": ""
	}
]
```

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=3><img src="doc/en/media/alerts_settings.png"></td><td> Anzahl der Spalten</td><td> Anzahl der Spalten definieren</td></tr><tr><td> Objekt Identifikation</td><td> Das Objekt muss eine JSON-Zeichenfolge sein, die wie oben beschrieben strukturiert sein muss</td></tr><tr><td> max. Warnungen</td><td> Maximale Anzahl von Warnungen, die angezeigt werden sollen.</td></tr></tbody></table>

Mit dem folgenden Skript können Sie einfache Nachrichten an den Datenpunkt senden, der vom Warnungs-Widget verwendet wird.
Das Skript muss in globale Skripte eingefügt werden. Dann ist es möglich, eine Nachricht mit dem folgenden Befehl zu senden

`materialDesignWidgets.sendTo('datapoint_id', 'message', 'color');`

```


var materialDesignWidgets = {};
materialDesignWidgets.sendTo = function (id, text, backgroundColor = '', borderColor = '', icon = '', iconColor = '', fontColor = '') {
    let json = getState(id).val;

    if (json) {
        try {

            json = JSON.parse(json);

        } catch (e) {
            json = [];
            console.warn('Wert ist kein JSON string! Wert wird ersetzt!');
        }
    } else {
        json = [];
    }

    json.push(
        {
            text: text,
            backgroundColor: backgroundColor,
            borderColor: borderColor,
            icon: icon,
            iconColor: iconColor,
            fontColor: fontColor
        }
    )
    setState(id, JSON.stringify(json), true);
}
```

## Kalender
![Logo](../../../en/adapterref/iobroker.vis-materialdesign/doc/en/media/calendar.gif)

Das Kalender-Widget benötigt eine JSON-Zeichenfolge als Objekt, die wie folgt strukturiert sein muss:

```
[
	{
		"name": "Event",
		"color": "#e74c3c",
		"colorText": "#FFFFFF",
		"start": "2020-01-24",
		"end": "2020-01-26"
	},
	{
		"name": "Meeting",
		"color": "#717d7e",
		"colorText": "#FFFFFF",
		"start": "2020-03-23 16:00",
		"end": "2020-03-24 17:15"
	}
]
```

Nur hex und rgba können als Farben verwendet werden!

Einstellungen, die in der folgenden Tabelle nicht aufgeführt sind, sind selbsterklärend.

<table><thead><tr><th>Bildschirmfoto</th><th> Rahmen</th><th> Beschreibung</th></tr></thead><tbody><tr><td rowspan=2><img src="doc/en/media/calendar_layout.png"></td><td> Wochentage angezeigt werden</td><td> Gibt an, welche Wochentage angezeigt werden sollen. Um nur Montag bis Freitag anzuzeigen, kann ein Wert von <code>1, 2, 3, 4, 5</code> verwendet werden. Um eine Woche ab Montag anzuzeigen, kann ein Wert von <code>1, 2, 3, 4, 5, 6, 0</code> verwendet werden.</td></tr><tr><td> Objekt Identifikation</td><td> Das Objekt muss eine JSON-Zeichenfolge sein, die wie oben beschrieben strukturiert sein muss</td></tr><tr><td rowspan=2><img src="doc/en/media/calendar_timeaxis.png"></td><td> Startstunde</td><td> Die Stunde, ab der Termine in der Wochen- und Tagesansicht angezeigt werden sollen.</td></tr><tr><td> Endstunde</td><td> Die Stunde, bis zu der Termine in der Wochen- und Tagesansicht angezeigt werden sollen</td></tr></tbody></table>

Wenn Sie das Widget mit [Adapter](https://github.com/iobroker-community-adapters/ioBroker.ical) verwenden möchten, können Sie das ical-Objekt mit dem folgenden Skript für die Arbeit mit dem Widget konvertieren.

```
// momentjs is required as dependecies in javascript adapter
const moment = require("moment");

var instances = $(`[id=ical.*.data.table]`);
instances.on(ical2CalendarWidget);

// remove this, if you know to use your own datapoint
let datapointId = 'materialdesignwidgets.calendar.ical2calendar'
createState(datapointId, "[]", {
  read: true,
  write: false,
  desc: "JSON String for Calendar Widget",
  type: "string",
  def: "[]"
});

function ical2CalendarWidget() {
    try {
        let calList = [];

        for (var inst = 0; inst <= instances.length - 1; inst++) {
            let icalObj = getState(instances[inst]).val;

            if (icalObj) {
                for (var i = 0; i <= icalObj.length - 1; i++) {
                    let item = icalObj[i];

                    // extract calendar color
                    let calendarName = item._class.split(' ')[0].replace('ical_', '');

                    let startTime = moment(item._date);
                    let endTime = moment(item._end);

                    let start = startTime.format("YYYY-MM-DD HH:mm");
                    let end = endTime.format("YYYY-MM-DD HH:mm");

                    if (startTime.format('HH:mm') === '00:00' && endTime.format('HH:mm') === '00:00') {
                        // is full-day event
                        if (endTime.diff(startTime, 'hours') === 24) {
                            // full-day event, one day
                            start = startTime.format("YYYY-MM-DD");
                            end = startTime.format("YYYY-MM-DD");
                        } else {
                            // full-day event, multiple days
                            start = startTime.format("YYYY-MM-DD");
                            end = endTime.format("YYYY-MM-DD");
                        }
                    }

                    // create object for calendar widget
                    calList.push({
                        name: item.event,
                        color: getMyCalendarColor(calendarName),
                        colorText: getMyCalendarTextColor(calendarName),
                        start: start,
                        end: end
                    })
                }

                function getMyCalendarColor(calendarName) {
                    // assign colors via the calendar names, use calendar name as set in ical
                    if (calendarName === 'calendar1') {
                        return '#FF0000';
                    } else if (calendarName === 'calendar2') {
                        return '#44739e'
                    } else if (calendarName === 'calendar3') {
                        return '#32a852'
                    }
                }

                function getMyCalendarTextColor(calendarName) {
                    // assign colors via the calendar names, use calendar name as set in ical
                    if (calendarName === 'calendar1') {
                        return '#FFFFFF';
                    } else if (calendarName === 'calendar2') {
                        return '#FFFFFF'
                    } else if (calendarName === 'calendar3') {
                        return '#FFFFFF'
                    }
                }
            }

            // Enter the destination data point that is to be used as object ID in the widget
            setState(datapointId, JSON.stringify(calList), true);
        }
    } catch (e) {
        console.error(`ical2MaterialDesignCalendarWidget: message: ${e.message}, stack: ${e.stack}`);
    }
}

ical2CalendarWidget();
```

## Changelog

<!--
    Placeholder for the next version (at the beginning of the line):
    ### __WORK IN PROGRESS__
-->

### 0.4.2 (2020-12-29)
* (Scrounger) vis-google-fonts dependency removed

### 0.4.1 (2020-12-27)
* (Scrounger): Adapter settings: theme editor implementation completed
* (Scrounger): Progress Widget: condition binding bug fix
* (Scrounger): minimal VIS adapter dependency set to v1.3.6
* (Scrounger): VIS editor: image dialog bug fix
* (Scrounger): Color themes for buttons and dialogs widgets implemented
* (Scrounger): Calendar Widget: week number bug fix
* (Scrougner): icon list: scrollbar bug fix
* (Scrounger): bug fixes

### 0.4.0-beta (2020-12-09)
* (Scrounger): Line History Chart Widget: Breaking Changes !!! aggregate (display) method for every dataset configurable, [see documentation for detailed infos](#line-history-chart)!
* (Scrounger): TopAppBar Widget: Breaking Changes !!! Submenus must now be created using JSON string, [see documentation for detailed infos](#since-version-040)!
* (Scrounger): Adapter settings wiht theme editor added
* (Scrounger): bug fix for compatibility issues with other widget adapters
* (Scrounger): Chechbox Widget: option for border and hover color added
* (Scrounger): Chechbox Widget: ripple effect bug fix
* (Scrounger): Buttons Vertical: text alignment option added
* (Scrounger): added URL support as source for symbols / images
* (Scrounger): HTML Card Widget: option to hide title, subtitle and text added
* (Scrounger): HTML Card Widget: background image refresh options by datapoint added
* (Scrounger): Fixed some errors reported via Sentry
* (Scrounger): Select & Autocomplete Widget: overriding icon color bug fix
* (Scrounger): Select & Autocomplete Widget: overriding icon bug fix
* (Scrounger): Select & Autocomplete Widget: colors bug fixes
* (Scrounger): Select & Autocomplete Widget: option to override the icon color of textfield for selected menu icon
* (Scrounger): Select & Autocomplete Widget: text alignment option added
* (Scrounger): Input Widget: text alignment option added
* (Scrounger): JSON Chart Widget: option to force x-axis time unit added
* (Scrounger): JSON Chart Widget: gradient colors for multipe dataset bug fixes
* (Scrounger): JSON Chart: default tooltip title added
* (Scrounger): JSON Chart: option to use Today / Yesterday for x-axis labeling added
* (Scrounger): JSON Chart: option to use Today / Yesterday for tooltip added
* (Scrounger): JSON Chart: option to change x-axis label distance added
* (Scrounger): Line History Chart: option for point color added
* (Scrounger): Line History Chart: option to use Today / Yesterday for x-axis labeling added
* (Scrounger): Line History Chart: option to use Today / Yesterday for tooltip added
* (Scrounger): Line History Chart: tooption change x-axis label distance added
* (Scrounger): Charts Widget: x-Axis time axis bug fixes
* (Scrounger): Calendar Widget: option to show calendar week numbers in month view added
* (Scrounger): Calendar Widget: option for custom date format added
* (Scrounger): IconList Widget: bug fix for performance issue
* (Scrounger): TopAppBar Widget: options for user groups added
* (Scrounger): Table Widget: html element added
* (Scrounger): Masonry & Grid View Widget: default width for handy portrait and landscape view changed
* (Scrounger): Progress Widget: option for indeterminate style added
* (Scrounger): dependencies updated
* (Scrounger): bug fixes

### 0.3.19 (2020-07-18)
* (Scrounger): Icon Button Widget: background color option for lock icon added
* (Scrounger): possibility to deactivate sentry implemented -> see documentation
* (Scrounger): Fixed some bugs reported via Sentry
* (Scrounger): prevent set value in vis editor
* (Scrounger): Grid & Mansonry Widget: visibilty by resoltuin bug fix
* (Scrounger): IconList Widget: Card Background for whole icon list added
* (Scrounger): Table Wigdet: button link widget added
* (Scrounger): Table Wigdet: material design icon widget added
* (Scrounger): Table Wigdet: alignment option for controls added
* (Scrounger): materialdesignicons library updated to v5.3.45
* (Scrounger): Round Slider lib updated to v0.5.0
* (Scrounger): Round Slider Widget: readonly option added
* (Scrounger): Table Widget: background color hover option added
* (Scrounger): bug fixes

### 0.3.14 (2020-06-01)
* (Scrounger): Table Widget: bug fixes

### 0.3.13 (2020-05-29)
* (Scrounger): Multi State Button Widgets: delay option added
* (Scrounger): Table Widget: option to add ohter Widgets to table added
* (Scrounger): Slider & Round Slider Widget: option to show value in percent added
* (Scrounger): Sentry error handling improved
* (scrounger): Buttons: click bug fix
* (scrounger): MaterialDesingIcons: extension bug fix
* (Scrounger): small bug fixes

### 0.3.11 (2020-05-24)
* (Scrounger): Sentry added
* (Scrounger): Select & Autocomplete Widget: vibrate on mobil devices added
* (Scrounger): List Widget: vibrate on mobil devices added
* (Scrounger): Masonry & Grid Widget: height changed to optional to support widgets using relative position
* (Scrounger): Progress Widget revised
* (Scrounger): Progress Circular Widget added
* (Scrounger): bug fixes

### 0.3.9 (2020-05-20)
* (Scrounger): List Widget: subscribe for nested oids and bindings bug fix
* (Scrounger): Multi State Button Widgets added
* (Scrounger): checkbox: lock option added
* (Scrounger): switch: lock option added
* (Scrounger): bar & pie chart: option for distance between legends points added
* (Scrounger): bar, pie & json chart: tooltip title and value override options added
* (Scrounger): pie chart: orientation change bug fix
* (Scrounger): json & line history chart: stepped line option added
* (Scrounger): table: option for fixed table headline added
* (Scrounger): charts: newline bug fixed
* (Scrounger): charts: tooltip decimal places bug fix


### 0.3.6 (2020-04-29)
* Input, Select, Autocomplete: default input controll buttons removed
* vuetify library updated to v2.2.26 
* JSON Chart: auto mode to show values added
* Line History Chart: auto mode to show values added
* Bar Chart: auto mode to show values added
* Pie Chart: auto mode to show values added
* Button State: lock icon input field bug fix

### 0.3.4 (2020-04-27)
* Select / AutoComplete Widget: Breaking Changes !!! separator for valuelist changed from comma to semicolon
* Pie Chart Widget: support for json string implemented
* Browser Edge: gradient color bug fix

### 0.3.3
* (Scrounger): css file bug fixes
* (Scrounger): Material Design Icons library updated to v5.1.45

### 0.3.2
* (Scrounger): Select & Autocomplete Widget: color option for menu items added
* (Scrounger): setState type bug fixes
* (Scrounger): small bug fixes

### 0.3.0
* (Scrounger): JSON Chart: error handling added
* (Scrounger): IconList: error handling added
* (Scrounger): Line History chart: debug mode & error handling added
* (Scrounger): Select Widget: handling for object with mulitstate added
* (Scrounger): Autocomplete Widget: handling for object with mulitstate added
* (Scrounger): bug fixes

### 0.2.76
* (Scrounger): deprecated Widgets Slider, TopAppBar, Select, Column View removed
* (Scrounger): JSON Chart Widget added
* (Scrounger): Line Chart Widget: starttime by object added
* (Scrounger): Bar Chart Widget: support for json string oid added
* (Scrounger): Chart Widget: min / max decimals for axis, labels and tooltip added
* (Scrounger): Masonry View Widget: sort order added
* (Scrounger): Grid View Widget: sort order added
* (Scrounger): new Dialog Widget added
* (Scrounger): bug fixes

### 0.2.66
* (Scrounger): IconListWidget: button layout options added
* (Scrounger): IconListWidget: lock option for toggle and state function added
* (Scrounger): Alert Widget: visibility depending on resoltuion added
* (Scrounger): Button Widgets: lock option for toggle and state button added
* (Scrounger): Material Design Icon Widget added
* (Scrounger): bug fixes

### 0.2.62
* (Scrounger): List Widget: binding bug fix
* (Scrounger): Select Widget: number bug fix
* (Scrounger): IconList Widget: object id for json string added, html input field removed from editor
* (Scrounger): Input Widget: clear & null bug fix
* (Scrounger): bug fixes

### 0.2.59
* (Scrounger): Buttons Toggle: option for push function added
* (Scrounger): IconList Widget added
* (Scrounger): Alerts Widget: show dummy message in Editor
* (Scrounger): Grid Views Widget added
* (Scrounger): List Widget: color option for switch added
* (Scrounger): List Widget: dynamic generate item using json string
* (Scrounger): Masonry Views Widget: visible condition added
* (Scrounger): Calendar Widget added
* (Scrounger): translation added
* (Scrounger): VIS Editor: Link to Forum widget threads added
* (Scrounger): bug fixes

### 0.2.49
* (Scrounger): new Select Widget added
* (Scrounger): Autocomplete Widget added
* (Scrounger): Alerts Widget added
* (Scrounger): use of Material Design Icons as images added
* (Scrounger): Perfomrance optimized
* (Scrounger): Input Widget added
* (Scrounger): Masonry Views Widget: settings options for mobile phone and tablet added
* (Scrounger): Masonry Views Widget: another chrome bug fix, option for distance between views added
* (Scrounger): Round Slider: vibrate on mobil devices added
* (Scrounger): bug fixes

### 0.2.32
* (Scrounger): Editor translation bug fix
* (Scrounger): Masonry Views Widget: alignment bug fix for chrome
* (Scrounger): Line History Chart Widget: layout option for line values added
* (Bluefox): Russian translation revised

### 0.2.30
* (Scrounger): Masonry Views Widget added
* (Scrounger): Select Widget: background color bug fix
* (Scrounger): Column Views Widget added
* (Scrounger): Button Widgets: icon height bug fix
* (Scrounger): Vuetify API bug fix
* (Scrounger): Chart Widgets: localization added
* (Scrounger): Line History Chart Widget: color options for each y-axis added
* (Scrounger): Line History Chart Widget: x-axis boundary options added
* (Scrounger): Line History Chart Widget: x-axis scaling bug fix
* (Scrounger): TopAppBar Widget: `view in widget 8` removed -> old TopAppBar Widget will be removed in version 0.3.x
* (Scrounger): bug fixes

### 0.2.22
* (Scrounger): library material-components-web updated to v4.0.0
* (Scrounger): Table: support for objects added
* (Scrounger): List: layout checkbox disabled added
* (Scrounger): vuetify slider added -> old slider will be removed in version 0.3.x
* (Scrounger): vuetify library v2.1.15 added
* (Scrounger): bug fixes

### 0.2.9
* (Scrounger): translations added
* (Scrounger): select Widget: color options added
* (Scrounger): slider Widget: color options added
* (Scrounger): bug fixes

### 0.2.7
* (Scrounger): List Widget: types switch readonly, checkbox readonly & button toggle readonly added
* (Scrounger): Line History Chart Widget: bug fix for hide yaxis by legend click if common axis is set
* (Scrounger): Line History Chart Widget: option to append text to yAxis values added
* (Scrounger): Switch Widget: color options added
* (Scrounger): chartjs lib updated to v2.9.3
* (Scrounger): round-slider: lib updated to v0.3.7
* (Scrounger): Table Widget: wordwrap & width option added
* (Scrounger): Chart Widgets: option for background color of diagram area added

### 0.2.4
* (Scrounger): Round Slider Widget bug fixes
* (Scrounger): Line History Chart Widget: null value bug fix
* (Scrounger): Line History Chart Widget: tooltip bug fix
* (Scrounger): Line History Chart Widget: editor translation improved
 
### 0.2.0
* (Scrounger): Round Slider Widget added
* (Scrounger): Icon Button Adition Widget added
* (Scrounger): Button Adition Widget added
* (Scrounger): Line History Chart Widget added
* (Scrounger): Table Widget added
* (Scrounger): Dialog iFrame Widget added
* (Scrounger): Dialog View Widget added
* (Scrounger): Select Widget added
* (Scrounger): colorSchemes for Charts added
* (Scrounger): bug fixes

### 0.1.5
* (Scrounger): bar chart added
* (Scrounger): pie chart added
* (Scrounger): bug fixes

### 0.1.2
* (Scrounger): list: right label option added
* (Scrounger): slider: value text option for lees or greather than added
* (Scrounger): switch: support for non boolean values added
* (Scrounger): checkbox: support for non boolean values added
* (Scrounger): buttons: image position option added
* (Scrounger): toggle buttons: support for non boolean values added
* (Scrounger): topAppBar: z-Index added
* (Scrounger): haptic feedback (vibration) option for mobil browser added
* (Scrounger): editor text fields changed to html
* (Scrounger): mdc-typography font styles added
* (Scrounger): bug fixes

### 0.1.1
* (Scrounger): bug fixes

### 0.1.0
* (Scrounger): Top App Bar Submenu added
* (Scrounger): List added
* (Scrounger): Button vertical State, Link, Nav added
* (Scrounger): Icon Button State, Link, Nav added
* (Scrounger): initialize slider bug fixes
* (Scrounger): moved hard coded styling options to css
* (Scrounger): styling options extended
* (Scrounger): bug fixes

### 0.0.7
* (Scrounger): Top App Bar Layouts added
* (Scrounger): Top App Bar customizing options added
* (Scrounger): Top App Bar Navigation Drawer backdrop layout added
* (Scrounger): Button State added
* (Scrounger): Button Link added

### 0.0.6
* (Scrounger): Top App Bar with Navigation Drawer added
* (Scrounger): Checkbox added
* (Scrounger): bug fixes
 
### 0.0.5
* (Scrounger): icon button Toggle added
* (Scrounger): color pressed for buttons added
* (Scrounger): Slider bug fix & label for value <= min / >= max added
* (Scrounger): translation added

### 0.0.4
* (Scrounger): cards added

### 0.0.3
* (Scrounger): progress added
 
### 0.0.2
* (Scrounger): slider vertical added
* (Scrounger): switch added
* (Scrounger): button toggle added

### 0.0.1
* (Scrounger) initial release

## License
MIT License

Copyright (c) 2020 Scrounger <scrounger@gmx.net>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.