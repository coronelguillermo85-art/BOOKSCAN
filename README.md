# 📖 BOOK//SCAN

**Analizador de libros con IA — resumen, ficha bibliográfica y slides, en un solo archivo HTML.**

Subís un libro (PDF, EPUB, MOBI, DOCX o TXT), en el idioma que sea, y te devuelve:

- 📋 **Ficha del libro** — título, autor, editorial, año, tema, género, idioma original y páginas
- 📝 **Resumen extenso** — estilo bloc de notas, en varios párrafos
- 🎞 **Slides navegables** — 8 a 12 diapositivas con los conceptos o capítulos clave
- ⬇️ Todo descargable como `.txt`

Sin importar en qué idioma esté escrito el libro (inglés, portugués, alemán, etc.), la salida siempre se genera en **español**.

## ✨ Características

- **100% client-side** — un solo archivo `.html`, sin backend, sin instalación, sin build
- **Multi-formato**: PDF, EPUB, MOBI, DOCX, TXT
  - PDF vía [pdf.js](https://mozilla.github.io/pdf.js/)
  - DOCX vía [Mammoth.js](https://github.com/mwilliamson/mammoth.js)
  - EPUB descomprimido con [JSZip](https://stuk.github.io/jszip/), leyendo el spine del OPF
  - MOBI con un parser propio (PalmDOC/MOBI clásico, sin dependencias)
- **Multi-proveedor de IA** — elegís el motor desde la UI:
  - Google Gemini (gratis)
  - Groq
  - OpenAI
  - Anthropic (Claude)
  - Cualquier endpoint compatible con la API de OpenAI (OpenRouter, Mistral, Ollama local, etc.)
- **Tu API key nunca sale de tu navegador** — se guarda en `localStorage`, solo se usa para llamar directo al proveedor elegido
- Diseño responsive (celu y desktop) con estética synthwave/cyberpunk

## 🚀 Uso

1. Descargá `pdf_summarizer.html` (o el nombre que le hayas puesto al archivo)
2. Abrilo con doble clic en cualquier navegador — no requiere servidor ni instalación
3. Elegí el motor de IA y pegá tu API key (gratis en [aistudio.google.com](https://aistudio.google.com) para Gemini)
4. Soltá el libro o tocá para elegirlo
5. Tocá **ESCANEAR LIBRO**
<img width="837" height="547" alt="image" src="https://github.com/user-attachments/assets/4f582926-aadc-48e8-8cd4-d4faa1bccbc4" />

También podés servirlo con **GitHub Pages** para tener un link público fijo.

## ⚠️ Limitaciones conocidas

- Archivos con DRM no se pueden leer (ni PDF, ni EPUB, ni MOBI)
- MOBI: solo formatos clásicos (PalmDOC), no KF8/AZW3 puro
- PDFs escaneados como imagen (sin texto seleccionable) no se pueden procesar — no incluye OCR
- Algunos proveedores de IA pueden bloquear libros con temática sensible según sus propios filtros de contenido

## 🛠️ Stack

HTML + CSS + JavaScript vanilla. Librerías vía CDN: pdf.js, JSZip, Mammoth.js.

## 📄 Licencia



---

Parte del ecosistema [Sensitive Lab](#).
