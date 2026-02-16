# 📖 Descripción del Proyecto: Boletín QWASI

## 🌟 Propósito
El **Generador de Boletines QWASI** es una herramienta interna diseñada para agilizar la creación y envío de comunicaciones técnicas y legales por correo electrónico. Su objetivo es permitir que el personal de la agencia genere correos profesionales, con un formato consistente y compatible con clientes de escritorio como Outlook y Gmail, sin depender de servicios de suscripción externos.

## 🎯 Público Objetivo
- Personal administrativo y técnico de la agencia.
- Consultores de las áreas de **Seguridad y Salud en el Trabajo (SST)** y **Medio Ambiente**.

## 🏗️ Arquitectura Técnica
- **Framework**: [Astro](https://astro.build/) (v5.14.0). Seleccionado por su ligereza y enfoque en el rendimiento.
- **Frontend**: HTML5, CSS3 Vainilla y JavaScript (ES6+).
- **Persistencia**: LocalStorage de HTML5 para el almacenamiento de borradores en el navegador.
- **Generación de Email**: Motor de renderizado en cliente que utiliza tablas HTML y estilos en línea para máxima compatibilidad con clientes de correo antiguos.

## ✨ Funcionalidades Clave

### 1. Editor Dinámico de Bloques
Permite añadir, eliminar y reordenar temas de interés. Cada tema incluye:
- **Título del Tema**: Campo de texto libre.
- **Clasificación de Área**: Selector para SST o Medio Ambiente.
- **Editor de Texto Rico**: Soporte para **negrita**, *cursiva* y listas no ordenadas.
- **Enlace de Acción**: URL opcional para "Leer más".

### 2. Clasificación por Áreas Especializadas
El sistema permite etiquetar cada noticia o regulación bajo las dos categorías principales de la agencia. Estas etiquetas aparecen visualmente destacadas en el correo enviado, facilitando la lectura por parte del cliente.

### 3. Autoguardado Inteligente
Toda la información digitada en el formulario se guarda en tiempo real en la memoria local del navegador (`localStorage`). Esto permite que el usuario pueda cerrar la herramienta y retomar el trabajo exactamente donde lo dejó.

### 4. Simulador de Email
Panel lateral que muestra una previsualización en tiempo real de cómo se verá el boletín una vez enviado, simulando la interfaz de un cliente de correo.

### 5. Exportación de Un Solo Clic
Botón dedicado para copiar el HTML generado al portapapeles. Utiliza la API moderna de Clipboard con un fallback para navegadores antiguos, asegurando que el contenido se pegue correctamente en Outlook con todos los estilos preservados.

## 🛠️ Estructura de Archivos
- `src/components/newsletter/NewsletterForm.astro`: Componente principal (Monolito) que contiene la lógica del formulario, estilos, gestión del estado y generador de HTML.
- `src/components/newsletter/EmailPreview.astro`: Contenedor para la visualización previa del boletín.
- `src/layouts/Layout.astro`: Estructura base HTML y sistema de diseño (design tokens).
- `src/pages/index.astro`: Página principal de la aplicación.
- `review.md`: Análisis técnico de fortalezas y debilidades.
- `README.md`: Guía de instalación y uso rápido.

---

**© 2026 QWASI - Gestión Profesional de Información.**
