<!-- BANNER DE PROMOCIÓN DEL CANAL -->
> ### 🌊 ¡Únete a nuestro canal de Telegram!
> **Proyecto Ola Digital** es una iniciativa para potenciar el aprendizaje técnico y el software libre.
> 📢 **[¡Haz clic aquí para unirte al Canal de Telegram!](https://t.me/ProyectoOlaDigital)**
> 📦 *Descarga los ejecutables portátiles listos para usar en Windows y Linux sin necesidad de compilar código ni instalar dependencias.*

---

# Descargador de Videos — GUI (Proyecto Ola Digital)

Descargador de videos con interfaz gráfica moderna para **Linux**.
Soporta: YouTube, Facebook, Instagram, X (Twitter) y TikTok.

`Flet 0.84` · `Python 3.12` · `yt-dlp`

## ⚠️ Compatibilidad y Arquitecturas

| Sistema Operativo | Arquitectura | Estado |
|---|---|---|
| **Linux** | 64 bits | ✅ Soportado |

> **Nota importante:** Este es un programa de escritorio empaquetado nativamente. No funciona en dispositivos móviles.

---

## 🛠️ Guía para Desarrolladores

### Requisitos previos
Para trabajar en el entorno de desarrollo, asegúrate de tener instalado Python 3.12 y las dependencias:

`pip install -r requirements.txt`

**Configuración de FFmpeg (Requerido para modo HD y MP3):**
* **Linux:** Instala mediante `sudo apt install ffmpeg` o `sudo dnf install ffmpeg`.

### Ejecución y Empaquetado
* **Modo desarrollo:** `python main.py`
* **Generar ejecutable:** `python empaquetar.py`
  * El ejecutable resultante se genera en la carpeta `dist/DescargadorVideos/`.
  * Para distribución, comprime dicha carpeta en un archivo `.zip`.

---

## 🚀 Distribución y Releases
Para una gestión limpia del repositorio, los ejecutables **no** se suben directamente a la rama principal. Se recomienda el uso de **GitHub Releases**:

1. Ve a la pestaña **Releases** en este repositorio.
2. Crea una **New Release**.
3. Sube los archivos `.zip` generados con la nomenclatura estándar:
    - `Descargador_Lin64.zip`
   
---

## 📥 Guía de Instalación para Usuarios

### Linux (64 bits)
1. Descarga el `.zip` correspondiente a tu arquitectura.
2. Descomprime: `unzip Descargador_Lin64.zip`
3. Otorga permisos: `chmod +x DescargadorVideos`
4. Ejecuta: `./Descargador_Lin64`

---

## ⚙️ Configuración Avanzada

### Modos de descarga
| Modo | Descripción | Requiere FFmpeg |
|------|-------------|-----------------|
| **HD** | Máxima calidad disponible | Sí |
| **WhatsApp** | H.264, máx 480p, ligero | No |
| **MP3** | Solo audio 192kbps | Sí |

### Descarga de contenido privado
Para descargar videos privados (Instagram/Facebook), coloca un archivo `cookies.txt` en la misma carpeta que el ejecutable. La app lo detecta automáticamente.
* *Recomendación:* Usa la extensión **"Get cookies.txt LOCALLY"** en tu navegador para exportar el archivo correctamente.

---

## 📂 Estructura del proyecto
<small>
<pre>
descargador_gui/
├── main.py          ← App principal (Flet)
├── empaquetar.py    ← Script de empaquetado
├── README.md        ← Documentación
├── cookies.txt      ← Opcional (No subir a GitHub por seguridad)
└── assets/          ← Íconos y recursos gráficos
</pre>
</small>
