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

## 📥 Instalación obligatoria mediante AltStore Classic

UltraRig debe instalarse mediante **AltStore Classic**. Descarga el archivo desde [Releases](https://github.com/JORC14/ultrarig-ios-download/releases).

### Requisitos

- iPhone o iPad compatible.
- Una computadora Windows o Mac para la configuración inicial.
- Un Apple ID.
- **AltServer** instalado en la computadora.
- El archivo `UltraRig-ios.ipa` descargado.

### 1. Instalar AltServer

1. Descarga AltServer desde la [página oficial de AltStore](https://altstore.io/).
2. En Windows, instala también iCloud y iTunes desde Apple, no las versiones de Microsoft Store.
3. En Mac, abre AltServer y permite los componentes que solicite macOS.
4. Ejecuta AltServer y deja su icono activo en la barra de tareas o barra de menús.

### 2. Instalar AltStore Classic en el iPhone

1. Conecta el iPhone o iPad a la computadora con un cable USB.
2. Desbloquea el dispositivo y pulsa **Confiar** si aparece el aviso.
3. En Windows, abre iTunes y activa **Sincronizar con este iPhone mediante Wi‑Fi**. En Mac, activa **Mostrar este iPhone al usar Wi‑Fi** en Finder.
4. Pulsa el icono de **AltServer**.
5. Selecciona **Install AltStore > tu iPhone o iPad**.
6. Introduce el Apple ID que se usará para firmar la aplicación.
7. Espera a que AltStore aparezca en la pantalla de inicio.

### 3. Confiar en el desarrollador

1. En el iPhone abre **Ajustes > General > VPN y gestión de dispositivos**.
2. Pulsa el perfil que muestra tu Apple ID.
3. Pulsa **Confiar en [tu Apple ID]** y confirma.
4. En iOS 16 o posterior, abre **Ajustes > Privacidad y seguridad > Modo desarrollador**, actívalo y reinicia el dispositivo si lo solicita.

### 4. Instalar UltraRig desde AltStore

1. Descarga `UltraRig-ios.ipa` desde el enlace de Releases.
2. Pulsa **Compartir** y selecciona **AltStore**. También puedes guardar el archivo en **Archivos**.
3. Abre **AltStore** y entra en **My Apps**.
4. Pulsa el botón **+** de la esquina superior.
5. Selecciona `UltraRig-ios.ipa` en la app **Archivos**.
6. Introduce el Apple ID si AltStore lo solicita.
7. Espera a que termine la firma y la instalación.
8. Abre UltraRig desde la pantalla de inicio.

### 5. Actualizar UltraRig

1. Descarga la nueva versión `.ipa` desde Releases.
2. Abre **AltStore > My Apps**.
3. Pulsa **+** y selecciona el nuevo archivo.
4. AltStore instalará la actualización sobre la versión anterior cuando uses el mismo Apple ID y el mismo identificador de aplicación.
5. No borres la versión anterior antes de actualizar si quieres conservar los datos locales.

### 6. Renovar la aplicación

Con una cuenta Apple gratuita, las aplicaciones de AltStore normalmente caducan después de 7 días. Mantén AltServer abierto en la computadora y el iPhone en la misma red Wi‑Fi, o conectado por USB, y pulsa **Refresh All** en **AltStore > My Apps** antes de que caduque.

Si necesitas refrescar aplicaciones directamente desde el iPhone sin tener la computadora disponible, usa SideStore + LocalDevVPN siguiendo su [guía oficial](https://docs.sidestore.io/docs/installation/install.html). Ese es un método distinto de AltStore Classic.

---

## 📦 Descargas públicas

Descarga la versión más reciente desde la sección [Releases](https://github.com/JORC14/ultrarig-ios-download/releases).

El archivo `UltraRig-ios.ipa` debe instalarse mediante **AltStore Classic** siguiendo las instrucciones detalladas de este README.
