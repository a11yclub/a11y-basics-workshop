# Absatz

* Lesbare Schriftart
	* Sans-Serif auf dem Bildschirm besser lesbar als Serif
	* Großzügige Ober- und Unterlängen sowie deutlich unterschiedliche Glyphen (auch Spiegelungen "db") kommen Lesebehinderten entgegen
* Optimale Satzbreite
	* Relativ zur Schriftart anzugeben (`em`)
	* `45-70 em` bei einspaltigem Text
* Blocksatz ist zu vermeiden: Schwer lesbar durch unregelmäßige Wortabstände
* Zeilenabstand: Ca. 1,5-fache Schriftgröße gem. WCAG
* Kontrast
	* Kontrasteinstufung gem. WCAG *TODO: ?*
	* Toos zur Kontrastmessung *TODO: Links*
	* http://jxnblk.com/grays/
	* Kevin Marks: [How the Web Became Unreadable](https://backchannel.com/how-the-web-became-unreadable-a781ddc711b6#.k7sy34mzg)
* Inline Links
	* Deutliche, visuelle Unterscheidung vom übrigen Text
		* Konvention: Unterstreichung
		* Ausschließlich farbliche Unterscheidung grenzt Farbfehlsichtigkeiten aus
	* Klare Hervorhebung des aktuell fokusierten Links z.B. durch `a:focus { background-color: #012345 }`
	* Hinweis auf externe Verknüpfungen ist Guter Ton
		* Automatisches Icon + textlicher Hinweis per Generated Content *TODO: Code*
* Text
	* Faustregeln für's Schreiben:
		* Kurze Worte, Sätze und Absätze
		* Aktive statt passive Formulierungen
		* Redundanz und Wiederholung vermeiden
		* Satz- und Absatzlängen variieren, um Monotonie zu vermeiden und Fokus zu fordern

> Everyting but content is an enhancement