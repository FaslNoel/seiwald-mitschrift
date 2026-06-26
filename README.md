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

## Grundkenntnisse

Die Path-Umgebungsvariable ist eine Liste von Verzeichnissen in Ihrem Betriebssystem. Sie teilt dem System mit, wo nach ausführbaren Programmen oder Befehlen gesucht werden soll, ohne dass Sie den vollständigen Dateipfad eingeben müssen.

CRUD:

- Create - POST
- Read - GET
- Update - PUT (überschreiben) / PATCH (ergänzen)
- Delete - DELETE

_Superset_: Übermenge  
cd: _change directory_ (Wechseln des Verzeichnisses)
