# Asesor Académico de Investigación con IA (v2.2.0) 🤖📚

¡Bienvenido al repositorio del **Asesor Académico de Investigación**! Este es un entorno de acompañamiento inteligente y multimodal diseñado para guiar a estudiantes de pregrado, posgrado y doctorado en la estructuración, redacción y validación de sus tesis o proyectos de grado, bajo los lineamientos institucionales de la UNAD.

El sistema opera de forma **100% local** en tu computador utilizando **Ollama** (con el modelo Llama 3.2) y la interfaz de terminal de **Claude Code**, garantizando la privacidad absoluta de tus datos y textos de investigación.

---

## 📋 Características Principales

- **Inicialización Inteligente (`/init`):** Analiza tu espacio de trabajo y genera la memoria del proyecto en un archivo `CLAUDE.md`.
- **Diagnóstico Multidimensional:** Evalúa tus borradores en tiempo real señalando aciertos (✅), mejoras (⚠️) y vacíos críticos (❌).
- **Sistema de Cohesión Obligatorio:** Integra una matriz de 7 conectores académicos obligatorios por párrafo para asegurar la fluidez del texto.
- **Ingeniería de Citación:** Domina y valida estilos internacionales (APA 7.ª ed., IEEE, Vancouver, Chicago) con verbos de reporte dinámicos.
- **Trazabilidad Completa:** Registra de forma íntegra cada diagnóstico en una bitácora automatizada (`REGISTRO_AVANCE.md`) para el seguimiento del tutor.
- **Fase de Evaluación Final:** Autoevalúa de forma orientativa el documento final contra la rúbrica oficial de proyecto de grado de la UNAD (100 puntos) y exporta un informe técnico.

---

## 🛠️ Requisitos del Sistema

- **Sistemas Operativos:** Windows 10 u 11 (64 bits).
- **Hardware Mínimo:** 8 GB de memoria RAM (Se recomiendan 16 GB) y 10 GB de espacio libre en disco.
- **Software Base:** Node.js (versión 18 o superior).

---

## 🚀 Instalación y Configuración Rápida

Sigue estos sencillos pasos en tu terminal (PowerShell) para desplegar el entorno por primera vez:

### 1. Instalar Ollama y descargar el modelo de IA
Descarga el instalador desde [ollama.com](https://ollama.com) o ejecútalo por terminal:
```bash
winget install Ollama.Ollama
```
Una vez abierto Ollama en segundo plano, descarga el modelo oficial:
```bash
ollama pull llama3.2
```

### 2. Instalar Claude Code
```bash
npm install -g @anthropic-ai/claude-code
```

### 3. Configurar las Habilidades del Asesor
Clona este repositorio o copia los archivos de la carpeta `.claude/skills` dentro de la ruta de tu usuario en Windows:
```text
C:\Users\TuUsuario\.claude\skills\asesor-academico-multimodal\
```
Asegúrate de que los archivos `SKILL.md`, `WELCOME.md` y `REGISTRO_AVANCE.md` queden alojados en esa ruta.

---

## 📖 Modo de Uso

1. Abre la terminal dentro de la carpeta donde tienes tu tesis o proyecto.
2. Inicia la interfaz local del asistente:
   ```bash
   claude --model llama3.2
   ```
3. **Punto de partida (Primera Vez):** Escribe el comando de inicialización absoluta para mapear tu proyecto:
   ```text
   > /init
   ```
4. El asesor te solicitará los metadatos de tu investigación (Nivel, Modalidad, Estilo de citación, Título y Objetivos). Rellena los datos y el entorno se configurará automáticamente con un progreso inicial del `0%`.

5. **Interactúa y comparte:** Envía tus borradores o ideas usando frases clave como *"revisa mi avance"*, *"corrige esta sección"* o *"ayuda con el marco teórico"*.

> ⚠️ **Nota importante:** El asesor funciona bajo una estricta política de **restricción ante la redacción desde cero**. Su función es corregir y robustecer tu propio trabajo escrito, no redactar textos completos por ti.

---

## 📁 Documentación Adjunta

Para obtener explicaciones detalladas y resolver dudas avanzadas, consulta la carpeta `/docs` de este repositorio:
- [**Manual de Usuario (PDF)**](./docs/Manual_Usuario.pdf): Guía práctica paso a paso para estudiantes con ejemplos de interacción en consola y tablas de conectores.
- [**Manual Técnico (PDF)**](./docs/Manual_Tecnico.pdf): Detalles profundos de la arquitectura del protocolo, variables de entorno y solución de errores en la terminal.

---

## 📄 Licencia

Este proyecto está bajo el protocolo de código abierto y acompañamiento académico multimodal. Queda libre para su uso y adaptación por parte de la comunidad estudiantil e investigadores.

