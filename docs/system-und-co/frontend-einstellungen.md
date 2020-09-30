# Frontend Verhalten

Hier können Sie eine Reihe von Einstellungen treffen die das Verhalten im Frontend der Seite beeinflussen die CCM19 nutzen. Die verfügbaren Einstellungen werden im folgenden erläutert.



![screenshot-2020.09.30-13_09_34-CCM19 - Cookie Consent Management Software (1)](../assets/screenshot-2020.09.30-13_09_34-CCM19%20-%20Cookie%20Consent%20Management%20Software%20(1).jpg)



# Bitte zuerst bestätigen

CCM19 arbeitet sehr hart daran alle möglichen Fallstricke abzudecken - bei der schieren Anzahl an möglichen Überschneidungen mit anderen Skripten oder Problemen können wir leider nicht garantieren dass nach Aktivierung alles 100%ig funktioniert. Alleine die Kombinationsmöglichkeiten der uns bekannten Skripte mit den jeweiligen Einstellmöglichkeiten geht in die Milliarden.

Mit dem Betätigen dieses Hakens bestätigen Sie, dass Sie dies zur Kenntnis genommen haben und dass die Verantwortung für das Funktionieren alleine bei Ihnen oder dem Betreiber der jeweiligen Seite liegt.



> **Prüfen Sie Ihre Seite nach Aktivierung auf Herz und Nieren ob z.B. auch essentielle Funktionen wie Warenkorb, Bezahlfunktionen und alle anderen gewünschten weiter funktionieren**!!!





## Widget aktivieren

Ist dieser Punkt **deaktiviert**, wird das CCM19 Modul im Frontend **nicht** angezeigt und die entsprechend hinterlegten Scripte werden **nicht** ausgeführt. Daten zu unbekannten Cookies und Scripten werden auch bei deaktiviertem Widget weitergesammelt. 

Diese Funktion kann man nutzen um CCM19 auf der Webseite zu installieren, dann alles testen und erst wenn man alle Cookies und Skripte korrekt eingetragen hat CCM19 zu aktivieren.





## Unbekannte Cookies entfernen

CCM19 kann so konfiguriert werden, dass Cookies, die im Tool nicht hinterlegt sind, entfernt werden, sobald sie bemerkt werden.

Das funktioniert natürlich nur für First Party Cookies. Third Party Cookies die z.B. von iframes eingebunden werden können von der eigenen Seite technisch leider nicht angefasst und daher auch nicht gelöscht werden. Das verhindern die Sicherheitseinstellungen in Ihrem Browser - das ist so auch absolut richtig!

Daher muss man diese Skripte oder iframes blocken bevor sie ausgeführt werden - also auch bevor sie die Cookies setzen.



## Javascript und CSS minifizieren

Javascript- und CSS-Code von CCM19 minifizieren um den Seitenaufbau Ihrer Websiten zu beschleunigen. Deaktivieren Sie diese Funktion nur, um die Fehlersuche bei Problemen zu vereinfachen.



## Skripte blockieren

Hier können Sie das Verhalten des Scriptblockers (Menüpunkt [Skripte](skripte.md) ) konfigurieren. Diese Funktion blockiert das Laden von Skripten, die nicht unter der Kontrolle von CCM19 stehen. Auf diese Weise wird das Setzen unerwünschter Cookies automatisch verhindert genauso wie das ausführen unbekannter Skripte.

![screenshot-2020.09.30-13_29_13-CCM19 - Cookie Consent Management Software](../assets/screenshot-2020.09.30-13_29_13-CCM19%20-%20Cookie%20Consent%20Management%20Software.jpg)



### Neue Skripte automatisch blockieren

Wenn dieser Haken aktiviert ist werden von CCM19 neu gefundene Skripte direkt deaktiviert und geblockt. Seien Sie bitte vorsichtig bei diesem Haken, er kann auch notwendige Funktionen unterbinden die Sie evtl. nicht eingetragen haben als erwünscht. 

### Skripte der eigenen Domain auch blockieren

Ist dieser Haken gesetzt werden alle Skripte auch der eigenen Domain blockiert wenn sie neu gefunden werden. Beispiel:

``` javascript
<script type="text/javascript" src="/papoo_git_full/js/main.js" defer="defer"></script>
```

### Inline Skripte auch blockieren

Ist dieser Haken gesetzt werden auch Inline Skripte die als Schnipsel in Ihrer Seite eingebaut sind deaktiviert werden wenn Sie auf der Seite auftauchen - Beispiel:

``` javascript
<script type="application/javascript">
  window.onload = function()
   {
     window.localStorage.clear();
   }
</script>
```



## IFrames blockieren

Verwenden Sie diese Funktion, um zu verhindern, dass externe Ressourcen geladen werden, die über einen Iframe-Container eingebettet sind. Auf diese Weise wird das Setzen unerwünschter Cookies automatisch verhindert. Der Benutzer kann mit dem stattdessen angezeigten Dialog dem Laden des Inhalts zustimmen.

![screenshot-2020.09.30-13_31_47-CCM19 - Cookie Consent Management Software](../assets/screenshot-2020.09.30-13_31_47-CCM19%20-%20Cookie%20Consent%20Management%20Software.jpg)

### Iframe Blockierung aktivieren

Mit dem Haken aktivieren Sie die Blockierung der IFrames - vermutlich offensichtlich...

### Iframe Ausnahmen

Schreiben Sie einen Ausdruck pro Zeile. Iframes, deren HTML-Code einen dieser Textbausteine enthält, werden nicht blockiert. Wenn Sie z.B. youtube eintragen, dann werden Youtube Videos nicht mehr geblockt.

### Vorschaubilder

Bei Einbettungen von den großen Videoportalen wie Youtube oder Vimeo werden Screenshots der Videos als Sperrbild auf der Seite ausgegeben, so dass besser ersichtlich ist was genau im Video passiert. Es wird dabei der von den Portalen bereit gestellte Shot genommem.

Die Bilder werden auf der Seite gechached damit sie nicht bei jedem Seitenaufruf neu abgerufen werden müssen. Der Cache läuft nach 8 Tagen aus. Wollen Sie den Cache früher leeren, klicken Sie einfach auf den Button "Vorschaubild-Cache leeren".