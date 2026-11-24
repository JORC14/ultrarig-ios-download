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

## 📥 Descarga e instalación en iPhone o iPad

Descarga la versión más reciente desde [Releases](https://github.com/JORC14/ultrarig-ios-download/releases).
El archivo `.ipa` se instala mediante *sideloading* en dispositivos compatibles.

### Método 1: Sideloadly (Windows o Mac)

1. Descarga e instala [Sideloadly](https://sideloadly.io/).
2. Conecta el iPhone o iPad a la computadora mediante un cable USB.
3. Abre Sideloadly y arrastra `UltraRig-ios.ipa` a la ventana.
4. Introduce tu Apple ID y pulsa **Start**.
5. En el dispositivo, abre **Ajustes > General > VPN y gestión de dispositivos**, selecciona tu Apple ID y pulsa **Confiar**.

### Método 2: AltStore

1. Envía `UltraRig-ios.ipa` al iPhone o iPad mediante AirDrop, iCloud Drive u otro medio.
2. Abre **AltStore**.
3. En **My Apps**, pulsa **+** y selecciona el archivo `.ipa`.

### Método 3: TrollStore

1. Descarga el archivo `.ipa` desde Safari.
2. Pulsa **Compartir > TrollStore**.
3. Este método depende de que la versión de iOS sea compatible con TrollStore.

---

## 📦 Descargas públicas

Descarga la versión más reciente desde la sección [Releases](https://github.com/JORC14/ultrarig-ios-download/releases).

El archivo `UltraRig-ios.ipa` puede instalarse para pruebas mediante AltStore, Sideloadly o TrollStore, según la firma disponible.
