* JavaScript nur als interaktive Aufwertung, nicht als Betriebsvoraussetzung
* mögliche Ursachen für fehlenden JavaScript-Support
    * Skript hat Fehler (auch vorangehendes Drittanbieter-Skript)
    * Skripte werden blockiert (Content Blocker, Proxy, Firewall etc.)
    * Laden eines Skripts schlägt fehl (serverseitiges Problem)
    * JavaScript-Support wurde clientseitig deaktiviert (unwahrscheinlich)
* Skripte nach Möglichkeit nicht-blockierend und / oder am Ende des Dokuments laden

**Beispiel mit `loadJS()`**

```html
<head>
    <script>
      // loadJS-Methode inline einbinden
      function loadJS( src ){ ... }

      // Laden eines Skripts per loadJS()
      loadJS('pfad/zum/script.js');
    </script>
</head>
```

**Links**

* [loadJS](https://github.com/filamentgroup/loadJS) (Filament Group)