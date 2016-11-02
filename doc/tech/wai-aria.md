# Allgemein

* ARIA ist eine semantische Ergänzung zu HTML, kein Reparaturset für eine mangelhafte HTML-Grundstruktur
* wo immer ein Ziel mit semantischem HTML erreicht werden kann, soll dies auch geschehen (ARIA als „Last Ressort“ betrachten)

# Konzepte

* **Landmark Roles**: für die semantische Zuweisung von Rollen an HTML-Konstrukte, die ansonsten nicht existieren würden (z.B. Slider, Tree Views, Tab-Liste etc.)
* **ARIA Attribute**: Einfache ARIA-Attribute wie `aria-required` oder `aria-invalid` zur Beeinflussung des Accessibility Trees
* **Live Regions**: Um dynamische Änderungen des Dokumentinhaltes an den Accessibility Tree weiterzugeben
* **States und Properties**: Nützlich, um z.B. Web Components mit eigener JavaScript-Logik zugänglich zu machen und für den Accessibility Tree zu erschließen

# Nützliche Attribute

* `aria-hidden="true"` auf Elementen, die nicht verlesen werden sollen
* `aria-label="..."` um ein Screenreader-lesbares Label zu vergeben; wird zuerst verlesen

**Beispiel**

```html
<!-- Label für eine SVG-Grafik (bei fehlendem inliegenden Label -->
<svg role="img" arial-label="Logo des Accessibility Clubs">...</svg>

<!-- Verstecktes Unicode-Zeichen -->
<button>
    <span aria-hidden="true">☰</span>
    Menu
</button>

<!-- Menü mit lesbarem Label -->
<nav class="toc" aria-label="contents">
    <ul>
        <li><a href="#about">Über uns</a></li>
        <li><a href="#products">Produkte</a></li>
        <li><a href="#contact">Kontakt</a></li>
    </ul>
</nav>
```

* `aria-required="true"` auf Formularelementen, die Pflichtfelder sind
* `aria-invalid="true"` um ein Formularelement als ungültig zu markieren
* `aria-describedby="#id"` um auf eine extern liegende Beschreibung zu verweisen; zuletzt verlesen

**Beispiel**

```html
<form action="register.php">
    <!-- Negativ validiertes Pflichtfeld -->
    <label for="username">Benutzername</label>
    <input type="text" name="username" value="" aria-required="true" aria-invalid="true"/>

    <!-- Ungültiges Passwort -->
    <label for="password">Passwort</label>
    <input type="text" id="password" aria-invalid="true" aria-describedby="password-hint">
    <div id="password-hint">Dein Passwort muss mindestens 6 Zeichen lang sein</div>
</form>
```

* `aria-selected="true"` für ausgewählte Links
* `aria-labelledby="true"` um auf ein extern liegendes Label zu verweisen

**Beispiel**

```html
<div class="tab-interface">
    <ul role="tablist">
        <li role="presentation"><a href="#panel1" id="tab1" role="tab" aria-selected="true">Erster Tab</a></li>
        <li role="presentation"><a href="#panel2" id="tab2" role="tab" tabindex="-1">Zweiter Tab</a></li>
        <li role="presentation"><a href="#panel3" id="tab3" role="tab" tabindex="-1">Dritter Tab</a></li>
    </ul>
    <div role="tabpanel" id="panel1" aria-labelledby="tab1"><!-- Tabinhalt 1 --></div>
    <div role="tabpanel" id="panel2" aria-labelledby="tab2"><!-- Tabinhalt 2 --></div>
    <div role="tabpanel" id="panel3" aria-labelledby="tab3"><!-- Tabinhalt 3 --></div>
</div>
```