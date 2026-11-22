# BibliotecaJelly Desktop

Aplicación de escritorio para consultar y sincronizar tu catálogo de Jellyfin sin depender de un servidor web local.

- **Versión:** 0.1.0
- **Plataformas:** Windows x64 y Linux x64
- **Descarga:** [última release](https://github.com/zynerio/BibliotecaJelly-desktop/releases/latest)

Este repositorio contiene únicamente los artefactos de distribución y su documentación. El código fuente no se publica por ahora.

## Descargas de la versión 0.1.0

| Plataforma | Archivo | SHA-256 |
|---|---|---|
| Windows x64 | `BibliotecaJelly_0.1.0_x64-setup.exe` | `61ddb510b813b442f1ce9da2b02344c68362761a1eab95a52723af643dbdfaef` |
| Windows x64 | `BibliotecaJelly_0.1.0_x64_en-US.msi` | `7080e382ca64faf23aeca927d5a3ee9673df5fcd59d6d6294f83f3a0428353af` |

## Instalación

### Windows

- `BibliotecaJelly_0.1.0_x64-setup.exe`: instalador NSIS, instalación por usuario.
- `BibliotecaJelly_0.1.0_x64_en-US.msi`: instalador MSI.

Requiere Windows 10/11 x64 y WebView2. El instalador NSIS descarga WebView2 si no está presente.

### Linux

- `.deb` para Debian/Ubuntu.
- `.AppImage` para distribución portable.

Requiere WebKitGTK 4.1 y las dependencias habituales de Tauri.

## Primeros pasos

1. Abre **Conexión**.
2. Introduce la URL de Jellyfin.
3. Usa API Key o usuario/contraseña.
4. Guarda y pulsa **Sincronizar catálogo**.
5. Opcionalmente, importa una copia de `data/` desde **Ajustes**.

Los datos se guardan en:

```text
%APPDATA%\com.bibliotecajelly.desktop
```

En Linux, en el directorio de datos de la aplicación.

## Actualizaciones

La app consulta el manifiesto del hub:

```text
https://raw.githubusercontent.com/zynerio/BibliotecaJelly/main/manifiesto/desktop.json
```

En **Ajustes → Actualizaciones** se puede buscar una versión nueva y abrir la descarga. No se instala automáticamente.

## Verificación

Los instaladores se publican con SHA-256 en el manifiesto y en el archivo de checksums de la release.

## Créditos

Proyecto personal de **Zynerio**. Cliente no oficial de Jellyfin.
