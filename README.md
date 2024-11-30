# Firmenökosystem-Spiel

Ein browserbasiertes, interaktives Endlosspiel, das ein komplettes Firmenökosystem simuliert. Mitarbeiter, Geschäftsleitung und Kunden sind KI-Agenten, die sich selbst weiterentwickeln. Das Spiel umfasst zahlreiche Abteilungen, Aufgaben und realistische Simulationen wie Wetter, Verkehr und Lagerlogik.

---

## **Features**

### Gameplay:
- **Abteilungsbasierte Simulation**:
  - Abteilungen: Technik, Vertrieb, Verwaltung, Buchhaltung, Lagerlogistik.
  - Jede Abteilung hat spezifische Aufgaben, Räume und Verantwortlichkeiten.
- **Fahrzeuge**:
  - Jeder Techniker und Vertriebler hat ein Firmenfahrzeug (auch privat nutzbar).
  - Fahrzeuge haben Lebensdauer, Zustand und müssen bei Schäden ersetzt werden.
- **DMS-Workflow**:
  - Vertrieb und Technik arbeiten gemeinsam an DMS-Projekten (z. B. SharePoint, Kindermann-Displays).
- **Möbelmontage**:
  - Techniker bauen Möbel auf, transportieren sie und installieren sie vor Ort.
- **Geschäftsführer**:
  - Führt Meetings, entscheidet über Fahrzeugersatz und reagiert emotional auf Spielereignisse.

### Simulationen:
- **Lagerlogik**:
  - Lager für große Pakete wie Kopiersysteme und Möbel.
  - KI-Lageristen kümmern sich um Ein- und Auslagerungen.
- **Wetter- und Verkehrssystem**:
  - Zufällige Ereignisse wie Staus oder schlechtes Wetter beeinflussen das Spiel.
- **Physik**:
  - Möbelbewegungen, Fahrzeugschäden und mehr basieren auf realistischer Physik.

### Technische Features:
- **Frontend**:
  - Erbaut mit **React** und **Three.js** für eine interaktive 3D-Darstellung.
- **Backend**:
  - Node.js-Server mit **Express** und **MongoDB** zur Datenhaltung.
- **Hosting**:
  - Kostenlos hostbar auf Plattformen wie **Render** (Backend) und **Vercel** (Frontend).

---

## **Verzeichnisstruktur**

Das Projekt ist in Backend und Frontend unterteilt:

/game_project ├── /server               # Backend │   ├── app.js            # Haupt-Serverdatei │   ├── vehicleModel.js   # Fahrzeugmodell │   ├── vehicleDamage.js  # Fahrzeugschäden │   ├── teamMeetings.js   # Team-Meetings │   ├── ceoReactions.js   # CEO-Reaktionen │   ├── warehouse.js      # Lagerlogik │   ├── dmsWorkflow.js    # DMS-Workflows │   ├── vehicleLifecycle.js  # Lebensdauer von Fahrzeugen │   └── temporaryEffects.js  # Zeitlich begrenzte Effekte ├── /src                  # Frontend │   ├── index.html        # Einstiegspunkt │   ├── app.js            # Haupt-Frontendlogik │   ├── /components       # React-Komponenten │   │   ├── Vehicles.js   # Fahrzeugverwaltung │   │   ├── CEOVisual.js  # CEO-Visualisierung │   │   ├── TeamMeetings.js  # Team-Meetings │   │   ├── Warehouse.js  # Lagerverwaltung │   │   └── ...           # Weitere Komponenten │   └── /assets           # Medien (z. B. Bilder, Audio) ├── package.json          # Abhängigkeiten und Skripte └── README.md             # Projektbeschreibung

---

## **Installation**

### Voraussetzungen
- **Node.js** und **npm** installiert.
- GitHub-Account für Hosting und Versionskontrolle.

### Schritte
1. **Repository klonen**:
   ```bash
   git clone https://github.com/DeinBenutzername/firmenoekosystem-spiel.git
   cd firmenoekosystem-spiel

2. Abhängigkeiten installieren:

npm install


3. Backend starten:

node server/app.js


4. Frontend starten:

Öffne /src/index.html in einem Browser (bei Vercel oder GitHub Pages automatisch bereitgestellt).

---

API-Endpunkte

Das Backend stellt folgende API-Endpunkte bereit:

Fahrzeuge:

GET /api/vehicles: Liste aller Fahrzeuge.

POST /api/vehicles/damage: Schaden melden.


Lager:

GET /api/warehouse: Inventar anzeigen.

POST /api/warehouse/store: Artikel einlagern.


Team-Meetings:

POST /api/meetings: Ein Meeting abhalten.



---

Technologien

Frontend: React, Three.js

Backend: Node.js, Express

Datenbank: MongoDB (Atlas)

Physik-Engine: Cannon.js / Ammo.js



---

Hosting-Vorschläge

Frontend: Vercel oder GitHub Pages

Backend: Render oder Railway

Datenbank: MongoDB Atlas



---

Lizenz

Dieses Projekt steht unter der MIT-Lizenz. Sie können es frei verwenden und anpassen.


---

Autor

Dieses Spiel wurde von Irsan Sefer erstellt.
Kontakt: seferirsan@gmail.com
