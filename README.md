# 💍 Invitación Digital de Boda Interactiva | Sofía & Mateo

> Experiencia web interactiva *mobile-first* diseñada con Vanilla JavaScript, Tailwind CSS y animaciones CSS 3D para invitaciones de eventos de alta gama.

[![Live Demo](https://img.shields.io/badge/Demo-Ver%20en%20Vivo-success?style=for-the-badge&logo=vercel)](https://galvanfran1234.github.io/micol-casamiento/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/es/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![CSS 3D](https://img.shields.io/badge/CSS3-3D%20Transforms-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/es/docs/Web/CSS/CSS_transforms/Using_CSS_transforms)

---

## ✨ Características Principales

- ✉️ **Apertura de Sobre 3D (Unboxing Experience):** Interacción inicial con solapas físicas simuladas en CSS 3D, forro botánico vectorial y sello de lacre interactivo (*wax seal*).
- 🔄 **Tarjeta Flippable 360°:** Efecto 3D de doble faz (`preserve-3d` y `backface-visibility: hidden`) con ilustraciones vectoriales botánicas personalizadas en SVG.
- 🎵 **Motor de Audio con Manejo Avanzado de Políticas de Autoplay:**
  - Desbloqueo de `AudioContext` de la Web Audio API ante el primer gesto del usuario en Safari/iOS WebKit.
  - Soporte de contingencia (*fallback*) para el switch físico de silencio en dispositivos Apple.
  - Controlador de volumen personalizado y botón de muteo con feedback visual reactivo.
- ⏳ **Cuenta Regresiva en Tiempo Real:** Cálculo dinámico de días, horas, minutos y segundos restantes hacia la fecha del evento.
- 📅 **Integración con Google Calendar:** Generación dinámica de eventos con fecha, hora, descripción y locaciones preconfiguradas.
- 🗺️ **Deep Linking a Google Maps:** Acceso directo a las coordenadas del templo y el salón de recepción.
- 📋 **Portapapeles con Fallback de Compatibilidad:** Copiado de alias bancario/CBU utilizando `navigator.clipboard` moderno con fallback a `document.execCommand` para contextos no seguros, acompañado de *toast feedback*.
- 📲 **Confirmación de Asistencia (RSVP):** Conexión directa y preformateada hacia WhatsApp.

---

## 🛠️ Tecnologías Utilizadas

- **Frontend:** HTML5 Semántico, Vanilla JavaScript (ES6+ sin dependencias pesadas para maximizar rendimiento y velocidad de carga).
- **Estilos:** [Tailwind CSS](https://tailwindcss.com/) + CSS 3D Transitions & Transforms (`perspective`, `rotateX`, `rotateY`).
- **Iconografía & Gráficos:** SVG vectoriales puros embebidos para cero impacto en solicitudes de red.
- **Tipografía Editorial:** Google Fonts (*Cormorant Garamond*, *Alex Brush*, *Montserrat*).

---

## 🚀 Desafíos Técnicos Superados

### 1. Política de Autoplay de Audio en Navegadores Móviles (iOS/WebKit)
Los navegadores móviles modernos bloquean la reproducción automática de audio si no está directamente atada a un gesto explícito de usuario. Para garantizar una experiencia fluida con música de fondo:
- Se vinculó el inicio del audio al evento de apertura del sobre interactivo (`click` / `touch`).
- Se implementó la reanudación preventiva del subsistema de audio (`AudioContext.resume()`).
- Se diseñó un sistema de rescate de interacción (`armNextInteractionAudioUnlock`) que aprovecha cualquier scroll o toque posterior si el navegador rechaza la primera promesa.

### 2. Animaciones 3D fluidas a 60 FPS en Dispositivos de Gama Media/Baja
- Uso estricto de propiedades aceleradas por hardware GPU (`transform: rotateX/rotateY/translate3d` y `opacity`).
- Eliminación de reflujos de renderizado (*layout thrashing*) evitando alterar dimensiones (`width`, `height`, `top`, `left`) durante las transiciones.

---

## 💻 Instalación y Uso Local

1. Clona el repositorio:
   ```bash
   git clone https://github.com/galvanfran1234/micol-casamiento.git
   cd micol-casamiento
   ```

2. Ábrelo en tu navegador favorito:
   - Puedes abrir directamente `index.html` en el navegador, o
   - Usar una extensión como **Live Server** en VS Code o ejecutar `npx serve .`.

---

## 👤 Autor

Desarrollado con dedicación por **Franco Galván**.  
- LinkedIn: [Tu perfil de LinkedIn](#)
- GitHub: [@galvanfran1234](https://github.com/galvanfran1234)
