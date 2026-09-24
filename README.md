# Alarmas de pago — prototipo móvil

Prototipo estudiantil desarrollado con Expo, React Native y TypeScript a partir de la página **Mobile** del archivo de Figma del proyecto.

La aplicación no usa backend ni realiza pagos reales. Su objetivo es reproducir las pantallas y permitir recorrer el flujo de navegación con controles interactivos.

## Flujos incluidos

- Inicio con alarmas pendientes y pagadas.
- Creación de una alarma y validación de campos.
- Notificación de vencimiento.
- Detalle pendiente y confirmación de pago.
- Detalle pagado y regreso a pendiente.
- Menú de acciones, edición y eliminación.
- Pantallas de éxito y error.

## Ejecutar el proyecto

Requisitos: Node.js y la aplicación Expo Go en un dispositivo Android.

```bash
npm install
npm start
```

Después, escanee el código QR desde Expo Go. También puede usar `npm run android` si tiene un emulador Android configurado.

## Generar el APK

El perfil `preview` de `eas.json` está configurado para producir un APK instalable:

```bash
npx eas-cli@latest login
npx eas-cli@latest build --platform android --profile preview
```

Al terminar, Expo entrega una URL para descargar el archivo `.apk`. La compilación requiere una cuenta gratuita de Expo.

## Verificaciones

```bash
npx tsc --noEmit
npx expo export --platform android
```
