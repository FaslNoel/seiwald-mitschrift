# seiwald-mitschrift

Das ist die README.md-Datei. MD steht für Markdown. Markdown ist eine heutzutage weitverbreitete Auszeichnungssprache. (_Markup Language_, [Wikipedia](https://de.wikipedia.org/wiki/Auszeichnungssprache)).

Weitere bekannte Auszeichnungssprachen sind

- Hypertext Markup Language (HTML)
- Extensible Markup Language (XML)
- Yet Another Markup Language (YAML, YML)

## Installation von Node.js

Javascript läuft unter normalen Umständen in einer Browser-Sandbox (nur im Browser). Seit ca. 2010 gibt es eine Laufzeitumgebung (_Runtime Environment_) für JS, damit man auch serverseitig JS programmieren und ausführen kann: [Node.js](https://nodejs.org/).

LTS-Version (_Long Term Support_) installieren.

## Installation von pnpm

Der standardmäßige _Pakage Manager_ für Node.js ist npm (_node package manager_). Eine etwas modernere und inzwischen beliebtere Variante ist [pnpm](https://pnpm.io/) (performant npm).  
_Package Manager_ ermöglichen die Installation von Softwarepaketen.

## Installation von Strapi

Installation mit dem Skript `npm create strapi`. Daraufhin führt uns das CLI (_Command Line Interface_) durch die Installation. Falls bei der Installation sogenannte `build scripts` nicht ausgeführt werden können, schlägt die CLI die Fehlerbehandlung selbstständig vor:

1. Wechsel in das Installationsverzeichnis (z.B. mit `cd my-strapi-project`).
2. Neuerlicher Versuch der Installation mit `pnpm install`. Dieser scheitert in der Regel - die Build-Skripte können müssen mit `pnpm approve-builds` freigegeben werden.

### Typescript

Typescript ist eine statisch typisierte Version von Javascript. In JS gibt es keine Typen, in TS schon. Jeder JS-Code ist auch ein gültiger TS-Code. Bsp.:

- JS: let x=3;
- Java: double y=4.2;
- TS: let z: number = 5;

## Datenbanken

Crawfoot Notation (--<- und mehr): Dient der Visualisierung von Beziehungen von Tabellen. Bild auf Teams.

## VibeCoding / AgenticEngineering mit VS-Code und Github Copilot

VibeCoding passiert in VS-Code in erster Linie über die neu eingeführte Agent View. Dort können alle Anpassungen des "_Coding Harness_" vorgenommen werden. Wir können unseren _Harness_ mit verschiedenen Methoden anpassen:

- **MCP-Server**  
  MCP steht für _Model Context Protocoll_. Es ist ein Standard, der von Anthropic entwickelt wurde. Mithilfe von MCP können Chatbots/LLMs (_Large Language Models_) auf zusätzliche Tools zugreifen, die sie zu Experten in einem bestimmten Themenbereich machen.

  ## Javascript-Frontendentwicklung mit Frameworks (Svelte, React, Vue, Angular, ...)

  Frontend-Entwicklung

## Grundkenntnisse

Die Path-Umgebungsvariable ist eine Liste von Verzeichnissen in Ihrem Betriebssystem. Sie teilt dem System mit, wo nach ausführbaren Programmen oder Befehlen gesucht werden soll, ohne dass Sie den vollständigen Dateipfad eingeben müssen.

CRUD:

- Create - POST
- Read - GET
- Update - PUT (überschreiben) / PATCH (ergänzen)
- Delete - DELETE

_Superset_: Übermenge  
cd: _change directory_ (Wechseln des Verzeichnisses)  
JDK: _Java Development Kit_ (Java-Entwicklungsumgebung)  
SDK: _Software Development Kit_ (Software-Entwicklungsumgebung)
_System Installer_ (Systeminstallationsprogramm): Es wird für alle Benutzer des Systems installiert.  
_User Installer_ (Benutzerinstallationsprogramm): Es wird nur für einen Benutzer installiert. Andere Benutzer haben keinen Zugriff darauf. _System Installer_(Systeminstallationsprogramm):

---

# 4BHK SWP

## Aufbau einer Website: (DOM/html-Document Object Model-Tree)

### - html = Wurzel (Root)

#### --> head:

- title
- links (css)
- OS (SEO)

#### --> body (document.body)

- ...

## Frontend Frameworks

Sie nehmen die Liste heraus und packen html, css und js in eine Datei. Es gibt verschiedene UI-Komponenten. Komponenten sind vollkommen eigenständig.

- list = ["Brot", "Kaffee", "Bier"]  
  JS --> Daten + Funktionen
- Template (Vorlage) --> html

```html
<ul>
  {for item inList}
  <li>{item}</li>
  {endfor}
</ul>
```

### Svelte

- Komponentenbasiert (single File)
- Komponenten haben Module (script, style, markup)
- deklerativ:

Metaframeworks:

- Next (React)
- Nuxt (Vue)
- SvelteKit (Svelte)

**_Unterschied Zuweisung und Mutation_**

- **Zuweisung**: Das Zuweisen eines neuen Wertes zu einer Variablen. Beispiel in JavaScript:

  ```javascript
  let x = 5; // Zuweisung
  x = 10; // Neue Zuweisung
  ```

  ```html
  Parent:svelte
  <script>
    import Child from "./Child.svelte";
  </script>

  <ul>
    <Child prop="xyz"> </Child>
  </ul>
  ```

  Geschwungene Klammern `{}` werden in Svelte verwendet, um JavaScript-Ausdrücke innerhalb des HTML-Markups einzubetten.

- **Mutation**: Das Ändern des Inhalts eines bestehenden Objekts oder Arrays, ohne die Referenz zu ändern. Beispiel in JavaScript:

- **Wichtige Runen in JavaScript:**

- $state()
- $derived()
- $effect() "Konstruktor für ein "svelte-File" => SFC

  ```javascript
  let arr = [1, 2, 3];
  arr.push(4); // Mutation des Arrays
  ```

  **Select Bindings:**

```javascript
  <script>
	let questions = [
		{
			id: 1,
			text: `Where did you go to school?`
		},
		{
			id: 2,
			text: `What is your mother's name?`
		},
		{
			id: 3,
			text: `What is another personal fact that an attacker could easily find with Google?`
		}
	];

	let selected = $state();

	let answer = $state('');

	function handleSubmit(e) {
		e.preventDefault();

		alert(
			`answered question ${selected.id} (${selected.text}) with "${answer}"`
		);
	}
</script>

<h2>Insecurity questions</h2>

<p>{selected?selected.text : "nix"}</p>
<p>
	selected question {selected
		? selected.id
		: '[waiting...]'}
</p>
```

## Github

- node.modules nie auf Github hochladen.
- .env auch nie auf Github hochladen.
- In der package.json steht, welche Abhängigkeiten das Projekt benötigt. Diese sollten nicht manuell verändert werden, sondern über den Paketmanager (z.B. npm oder yarn) installiert werden.
- _Dependencies_: Sind für das Projekt während der Laufzeit notwendig.
- _Dev Dependencies_: Braucht man nur während der Entwicklung.

## Grundkenntnisse

- _Cross-Site Scripting (XSS):_ Eine Sicherheitslücke, bei der Angreifer schädlichen Code in Webseiten einschleusen können.
- Bedingte Verzweigungen (_Conditionals_) in Svelte werden mit `{#if ...}{/if}` umgesetzt. Beispiel:
- Aria (_Accessible Rich Internet Applications_): Dienen der Barrierefreiheit und helfen dabei, Webinhalte für Menschen mit Behinderungen zugänglich zu machen.
- _Stack (Last In, First Out - LIFO):_ Ein Datenstrukturprinzip, bei dem das zuletzt hinzugefügte Element zuerst entfernt wird.
- _Queue (First In, First Out - FIFO):_ Ein Datenstrukturprinzip, bei dem das zuerst hinzugefügte Element zuerst entfernt wird.
- anonyme Funktion: Eine Funktion ohne Namen, die oft als Argument an andere Funktionen übergeben wird.

---

# Historische Entwicklung von WebDev

Webdevelopment hat im Laufe der letzten rund 35 Jahre einige Evolutionsstufen durchlaufen:

1. Statische Websites (HTML, CSS, ggf. JavaScript-Dateien) - initiale Phase des Webdevelopments, bei der Inhalte fest im HTML-Code verankert sind. Dominant in den 1990er-Jahren.

2. Dynamische Websites (mit serverseitiger Programmiersprache - PHP, Python, NodeJS - und Datenbankanbindung). Dominant in den 2000er-Jahren.

3. _Single-Page Applications_ (SPAs) - mit JavaScript-Frameworks erstellte "Webapps", die ähnliche Funktionen wie klassische Desktop-Anwendungen bzw. Handy-Apps bieten. Dominant in den 2010er-Jahren.
