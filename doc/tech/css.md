# Responsive Design

* Content Breakpoints („Tweakpoints“)
* In relativen Maßeinheiten definieren, damit Abhängig von Schriftgrößen (`em`)

# Visually Hidden

```css
.visually-hidden {
	position: absolute;
	width: 1px;
	height: 1px;
	overflow: hidden;
	clip: rect(1px, 1px, 1px, 1px);
}
```