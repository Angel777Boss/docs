---
title: Informationen zum Paketieren mit GitHub-Aktionen
intro: 'In {{ site.data.variables.product.prodname_actions }}kannst Du Workflows einrichten, um Pakete zu erstellen und sie zu {{ site.data.variables.product.prodname_registry }} oder einem anderen Paket-Hosting-Anbieter hochzuladen.'
product: '{{ site.data.reusables.gated-features.actions }}'
redirect_from:
  - /actions/automating-your-workflow-with-github-actions/about-packaging-with-github-actions
versions:
  free-pro-team: '*'
  enterprise-server: '>=2.22'
---

{{ site.data.reusables.actions.enterprise-beta }}
{{ site.data.reusables.actions.enterprise-github-hosted-runners }}

### Informationen zu Paketierungsschritten

Die Paket-Erstellung ist ein üblicher Bestandteil des Workflows bei der kontinuierlichen Integration oder bei der kontinuierlichen Auslieferung. Nach dem Erstellen und Testen der Anwendung wird ein lauf- oder bereitstellungsfähiges Artefakt als Paket erstellt. Beispielsweise kann ein Workflow zur kontinuierlichen Integration für ein Java-Projekt `mvn package` ausführen, um eine JAR-Datei zu erstellen. Oder ein CI-Workflow für eine Node.js-Anwendung kann einen Docker-Container erzeugen.

Je nach Art der Anwendung, die Du erstellst, kann dieses Paket für manuelle Tests lokal heruntergeladen, Benutzern zum Herunterladen zur Verfügung gestellt oder in einer Staging- oder Produktionsumgebung bereitgestellt werden.

### Paket-Erstellung in Workflows zur kontinuierlichen Integration

Das Erstellen eines Pakets am Ende eines Workflows zur kontinuierlichen Integration kann während des Code-Reviews bei einem Pull-Request hilfreich sein. Nach dem Erstellen und Testen Deines Codes kann ein Paketierungsschritt ein lauf- oder bereitstellungsfähiges Artefakt erzeugen. Dein Workflow kann dieses Artefakt dann übernehmen und als Teil des Workflows hochladen.

Wenn Du nun einen Pull-Request überprüfst, kannst Du Dir den Ablauf des Workflows ansehen und das erzeugte Artefakt herunterladen.

![Dropdown-Menü zum Herunterladen von Artefakten](/assets/images/help/repository/artifact-drop-down.png)

Dadurch kannst Du den Code im Pull-Request auf Deinem Rechner ausführen, was beim Debuggen oder Testen des Pull-Requests helfen kann.

### Workflows zum Veröffentlichen von Paketen

Außer Paket-Artefakte zum Testen in einem Workflow zur kontinuierlichen Integration zum Testen hochzuladen, kannst Du auch Workflows erstellen, die Dein Projekt bauen und Pakete in einer Paket-Registry veröffentlichen.

* **Pakete auf {{ site.data.variables.product.prodname_registry }} publizieren**  {{ site.data.variables.product.prodname_registry }} kann als Paket-Hosting-Dienst für viele Paket-Arten fungieren. Du kannst Deine Pakete entweder an alle auf {{ site.data.variables.product.prodname_dotcom }} oder private Pakete nur an Mitarbeiter oder an eine Organisation weitergeben. Weitere Informationen findest Du unter „[Informationen zu {{ site.data.variables.product.prodname_registry }}](/github/managing-packages-with-github-packages/about-github-packages)“.

  Vielleicht willst Du Pakete bei jedem Push in den Master-Brach in {{ site.data.variables.product.prodname_registry }} veröffentlichen. Auf diese Weise können Entwickler in Deinem Projekt immer den neuesten Build aus Master ausführen und testen, indem sie ihn von {{ site.data.variables.product.prodname_registry }} installieren.

* **Pakete in einer Paket-Registry veröffentlichen** Bei vielen Projekten werden neue Versionen immer in einer Paket-Registry veröffentlicht. Beispielsweise kann ein Projekt, das eine JAR-Datei erstellt, neue Versionen in das Zentral-Repository von Maven hochladen. Oder ein .NET-Projekt kann ein NuGet-Paket erzeugen und es in die NuGet-Galerie hochladen.

  Du kannst dies automatisieren, indem Du einen Workflow erstellst, der bei jeder Release-Erstellung Pakete in einer Paket-Registry veröffentlicht. Weitere Informationen findest Du unter „[Releases erstellen](/github/administering-a-repository/creating-releases)“.

### Weiterführende Informationen

- „[Node.js-Pakete veröffentlichen](/actions/automating-your-workflow-with-github-actions/publishing-nodejs-packages)“