# Mostre fotografiche – web app

## 1. Metterla online (GitHub Pages, gratis)
1. Crea un account su github.com (se non lo hai).
2. Nuovo repository → nome ad es. `mostre` → Public → Create.
3. "uploading an existing file" → trascina tutti i file di questa cartella
   (index.html, manifest.webmanifest, sw.js, icon.svg, icon-180.png, icon-192.png, icon-512.png) → Commit.
4. Settings → Pages → Source: "Deploy from a branch", Branch: `main`, cartella `/ (root)` → Save.
5. Dopo 1–2 minuti l'app è su `https://<tuo-utente>.github.io/mostre/`.

## 2. Installarla
- **Android (Chrome):** apri l'indirizzo → menu ⋮ → "Installa app" / "Aggiungi a schermata Home".
- **iPhone (Safari):** apri l'indirizzo → Condividi → "Aggiungi alla schermata Home".
- **Computer (Chrome/Edge):** icona "Installa" nella barra degli indirizzi.

## 3. Sincronizzazione telefono ↔ computer
1. Su GitHub: Settings → Developer settings → Personal access tokens → Tokens (classic)
   → Generate new token (classic) → spunta solo **gist** → scadenza a piacere → Generate. Copia il token.
2. Nell'app: "Impostazioni sincronizzazione e backup" → incolla il token → "Salva e sincronizza".
3. Ripeti il punto 2 sull'altro dispositivo con lo stesso token: l'app trova i dati da sola.

Dopo la configurazione l'app sincronizza da sola all'apertura e dopo ogni modifica;
il pulsante **Sincronizza** forza una sincronizzazione immediata
(pallino verde = collegato, rosso = errore, grigio = non configurato).
I dati stanno in un Gist segreto `mostre-fotografiche.json` del tuo account.

## Backup su file
"Esporta file" salva un .json; "Importa file" lo unisce ai dati presenti (non cancella nulla).

## Aggiornare l'app
Se modifichi i file, cambia `VERSION` in `sw.js` (es. `mostre-v2`) così i dispositivi scaricano la nuova versione.
