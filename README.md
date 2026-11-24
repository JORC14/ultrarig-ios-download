# UltraRig for iOS (Tank-G & Tank-B)

Versión nativa para iOS de la aplicación **UltraRig**, generada a partir del paquete original de la app móvil y control web para los pedales de guitarra multiefectos **M-VAVE Tank-G v1 y v2**.

---

## 📱 Características y Componentes en iOS

- **Arquitectura:** Capacitor 8 + Swift (SPM - Swift Package Manager)
- **Bundle ID:** `com.ultrarig.app`
- **Permisos Bluetooth configurados:**
  - `NSBluetoothAlwaysUsageDescription`
  - `NSBluetoothPeripheralUsageDescription`
- **Plugin BLE:** `@capacitor-community/bluetooth-le` (CoreBluetooth nativo en iOS)
- **App Plugin:** `@capacitor/app`
- **Icono Oficial:** Renderizado a resolución completa (1024x1024) en `AppIcon.appiconset`
- **Motor Web UI:** Interfaz completa reactiva (con soporte de pantallas retina, landscape/portrait, gráficos de presets, escenas, cadenas paralelas, medidores y cargador de capturas NAM e IRs).

---

## 🛠️ Cómo Abrir y Compilar en Mac (Xcode)

1. Clona o copia esta carpeta a tu Mac.
2. Abre una terminal en la carpeta del proyecto y ejecuta:
   ```bash
   npm install
   npx cap sync ios
   npx cap open ios
   ```
3. En **Xcode**:
   - Selecciona tu equipo de desarrollo (**Signing & Capabilities** -> *Team*).
   - Conecta tu iPhone o iPad (o elige un simulador).
   - Pulsa **Run** (Cmd + R).

---

## ☁️ Compilación Automática en la Nube (.IPA sin Mac)

Este proyecto incluye un workflow de **GitHub Actions** en `.github/workflows/build-ios.yml`.

Para compilar un archivo `.ipa` instalable sin tener una Mac:
1. Sube este proyecto a un repositorio de GitHub (público o privado).
2. Ve a la pestaña **Actions**.
3. Ejecuta el workflow **Build iOS App** (o simplemente haz un push).
4. Al terminar el proceso, descarga el archivo `UltraRig-ios.ipa` listo para instalar mediante **AltStore**, **Sideloadly** o **TrollStore**.

---

## 📦 Descargas públicas

Descarga la versión más reciente desde la sección [Releases](https://github.com/JORC14/ultrarig-ios-download/releases).

El archivo `UltraRig-ios.ipa` puede instalarse para pruebas mediante AltStore, Sideloadly o TrollStore, según la firma disponible.
