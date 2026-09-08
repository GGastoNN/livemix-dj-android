# LiveMix DJ

MVP Android para mezclar dos canciones en vivo y controlar la interfaz con dispositivos MIDI por USB o Bluetooth LE.

## Alcance del MVP

- Dos decks con selección de audio local, reproducción, seek y pitch.
- Crossfader de potencia constante.
- Hot cue por deck.
- Detección de controladores MIDI USB/BLE mediante la API MIDI de Android.
- Mapeo MIDI editable en `MidiMapping.kt`.
- Workflow de GitHub Actions que genera un APK debug.

> Bluetooth se usa para **MIDI/control**. Para la salida de audio en directo se recomienda USB o cable: Bluetooth añade demasiada latencia para monitorización y beatmatching.

## Abrir y compilar

1. Abre el repositorio en Android Studio (JDK 17).
2. Sincroniza Gradle.
3. Ejecuta en un dispositivo Android 10 o posterior.
4. Concede acceso a los archivos de audio y conecta un controlador MIDI class-compliant.

En GitHub, ve a **Actions → Android APK → Run workflow**. El APK aparecerá como artefacto `livemix-debug-apk`.

## Publicar en GitHub

```bash
git remote add origin https://github.com/TU_USUARIO/livemix-dj.git
git branch -M main
git push -u origin main
```

## Próximas etapas

- Motor nativo Oboe/Superpowered para time-stretch con key lock y latencia profesional.
- Waveforms precalculadas, BPM, beat-grid y sync.
- EQ de 3 bandas, filtros, loops y efectos.
- Preescucha/cue con interfaz de audio multicanal USB.
- Editor visual de mapeo MIDI y perfiles por controlador.
- Firma del APK/AAB y publicación en Play Store.

## Licencia

Apache-2.0. No incluye música ni codecs propietarios.
