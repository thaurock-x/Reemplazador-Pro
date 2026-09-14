<div align="center">

  <h1>🔄 Reemplazador de Texto PRO</h1>
  <p><strong>Herramienta web optimizada para procesamiento, manipulación y reemplazo masivo de cadenas de texto</strong></p>

  [![Version](https://img.shields.io/badge/version-1.0.0-10b981.svg?style=for-the-badge)](https://github.com/tu-usuario/reemplazador-texto-pro)
  [![License](https://img.shields.io/badge/license-MIT-064e3b.svg?style=for-the-badge)](LICENSE)
  [![JavaScript](https://img.shields.io/badge/javascript-ES6+-f7df1e.svg?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/es/docs/Web/JavaScript)
  [![Client--Side](https://img.shields.io/badge/privacy-100%25_client_side-047857.svg?style=for-the-badge)](#-privacidad)

  <br />

  <a href="#-características">Características</a> •
  <a href="#-modo-de-uso">Modo de Uso</a> •
  <a href="#-arquitectura-y-tecnología">Arquitectura</a> •
  <a href="#-instalación">Instalación</a> •
  <a href="#-licencia">Licencia</a>
</div>

---

## 📌 Descripción

**Reemplazador de Texto PRO** es una solución web liviana y *zero-dependency* diseñada para realizar modificaciones de texto de manera rápida, precisa y masiva desde el navegador. 

Permite ejecutar búsquedas simples mediante texto plano o Expresiones Regulares (RegEx), así como procesar diccionarios de reemplazos en lote mediante una sintaxis estructurada por líneas.

---

## ✨ Características Principales

- 🎯 **Reemplazo Simple & RegEx:** Soporte para coincidencia exacta, distinción entre mayúsculas/minúsculas (case sensitivity) y evaluación de patrones mediante Expresiones Regulares.
- ⚡ **Reemplazo Masivo por Lotes:** Permite definir múltiples reglas de sustitución en formato `buscar=reemplazo` para procesar listas complejas en un solo clic.
- 📊 **Contador de Coincidencias:** Muestra en tiempo real el total de sustituciones realizadas tras cada operación.
- 📋 **Copiado Universal e Inmune:** Implementa una estrategia de copiado híbrida (`navigator.clipboard` + *fallback* con `execCommand`) para garantizar compatibilidad en entornos HTTP, HTTPS y dispositivos móviles.
- 💾 **Exportación Directa a `.txt`:** Generación y descarga inmediata del resultado en formato UTF-8 mediante Blob API.
- 🔒 **100% Privado:** Todo el procesamiento ocurre en memoria dentro del navegador. Ningún dato es transmitido a servidores externos.

---

## 📖 Modo de Uso

### 1. Reemplazo Simple
1. Pega tu texto en el área principal.
2. Ingresa la palabra o patrón a **Buscar** y el valor por el cual deseas **Reemplazar**.
3. Opcionalmente activa:
   - **Sensible a mayúsculas:** Para respetar exactamente el uso de cajas.
   - **Usar Regex:** Para evaluar patrones complejos (ej: `\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b`).
4. Haz clic en **Reemplazar**.

### 2. Reemplazo Masivo (Diccionario)
Ingresa reglas compuestas por pares clave-valor separados por el signo `=`. Cada regla debe ir en una nueva línea:

```text
hola=adiós
rojo=azul
2024=2025
```
---

### 🛠️ Arquitectura:

flowchart TD

    A[Texto de Entrada] --> B{Selección de Operación}
    B -- Reemplazo Simple --> C[Escape de Caracteres / RegEx Engine]
    B -- Reemplazo Masivo --> D[Parser de Reglas por Línea 'key=value']
    C --> E[Evaluación RegExp & Conteo de Coincidencias]
    D --> E
    E --> F[Actualización del DOM y Estadísticas]
    F --> G[Opciones de Salida]
    G --> H[📋 Copiar al Portapapeles]
    G --> I[💾 Descargar archivo .txt]

---

### ​📄 Licencia:

<div align="center">
Desarrollado con 💚 por <strong>Thaurock</strong>
</div>

