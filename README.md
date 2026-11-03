# SUPER16 — Android starter

Starter nativo Android per Xiaomi Redmi Note 9 (e dispositivi Android compatibili).

## Cosa fa questa prima build
- Anteprima dalla fotocamera posteriore
- Registrazione video MP4 Full HD quando supportata dal dispositivo
- Registrazione audio con microfono
- Salvataggio in `Movies/SUPER16`
- Interfaccia essenziale ispirata a una cinepresa documentaristica

## Cosa NON fa ancora
Questa è la **prima base funzionante della camera**, non ancora l'emulazione 16mm completa.
Non applica ancora grana, gate weave, flicker, halation o una curva colore filmica al file registrato.
Non forza 24 fps: CameraX seleziona la qualità supportata dal dispositivo e il frame rate dipende dal profilo encoder/camera.
Questi effetti vanno implementati nel passaggio successivo con una pipeline GPU/Media3 o un encoder OpenGL dedicato e verificati sul Redmi Note 9.

## Requisiti
- Android Studio recente
- Android SDK 35
- JDK 17
- Connessione internet al primo sync Gradle

## Come aprire
1. Estrai lo ZIP.
2. Apri la cartella `SUPER16-Android` in Android Studio.
3. Attendi il completamento di Gradle Sync.
4. Collega il Redmi Note 9 via USB e abilita Opzioni sviluppatore > Debug USB.
5. Premi Run.

Concedi i permessi Fotocamera e Microfono. I video vengono salvati nella galleria sotto `Movies/SUPER16`.

## Nota dispositivo
La RAM e la versione Android si possono verificare sul telefono in Impostazioni > Info sistema / Info telefono. Il progetto usa `minSdk 23`; la compatibilità effettiva va verificata sul firmware installato.
