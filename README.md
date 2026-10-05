# Referenz-Landingpages

Sechs Demo-Websites für Kundenakquise – live unter **https://ramos61.github.io/landingpage-demo/**

| Branche | Ordner | Demo |
|---|---|---|
| Handwerk & Bau | `handwerk/` | Meisterbau Krüger – dunkel, Hero-Video, Vorher/Nachher-Slider |
| Heizung & Sanitär | `haustechnik/` | Volkmann Haustechnik – Förder-Rechner, 24/7-Notdienst |
| Praxis & Gesundheit | `zahnarzt/` | Praxis Dr. Sommer – hell, Team-Portraits, Online-Termin |
| Bestattung | `bestatter/` | Weidenhof Bestattungen – würdevoll, Trauerfall-Hilfe, Vorsorge |
| Beratung & Agentur | `dienstleister/` | Meridian – editorial, Studio-Film, Hover-Bildvorschau |
| Restaurant & Gastronomie | `restaurant/` | Osteria Olivo – Holzofen-Video, Speisekarte, Reservierung |

Alle Firmen sind erfunden. Fotos und Videos sind KI-generiert (Higgsfield: GPT Image 2.5, Kling 3.0).

## Aufbau

- Jede Seite ist eine eigenständige `index.html` (CSS und JS eingebettet), Medien liegen in `<ordner>/media/`.
- Fotos als WebP (max. 1920 px), Hero-Videos als stumme H.264-Loops (unter 1,2 MB).
- `.nojekyll` sorgt dafür, dass GitHub Pages die Dateien unverändert ausliefert.

## Neue Medien hinzufügen

1. Zeile in `media-sources.txt` ergänzen: `<zielpfad> <url>` (z. B. `handwerk/media/team.webp https://…png`).
2. Committen und pushen – der Workflow `.github/workflows/fetch-media.yml` lädt die Datei, optimiert sie
   (WebP bzw. MP4 als nahtloser Loop) und committet das Ergebnis automatisch. Vorhandene Dateien werden nicht überschrieben.
