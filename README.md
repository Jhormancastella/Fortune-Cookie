# 🍪 Galleta de la Fortuna — Aplicación Web Interactiva

> *“Toca la galleta para descubrir tu destino”*  
> Una experiencia mágica, cultural y divertida inspirada en la tradición china de las galletas de la fortuna.

🔗 **¡ Pruébalo en vivo aquí: [https://jhormancastella.github.io/Fortune-Cookie/](https://jhormancastella.github.io/Fortune-Cookie/) **

---

## 🌟 Descripción General

**Galleta de la Fortuna** es una aplicación web interactiva que simula la experiencia de romper una galleta de la fortuna china. Al hacer clic en la galleta, se revela un mensaje aleatorio: predicción, consejo, inspiración, broma o números de la suerte — todo con animaciones suaves, diseño visual impactante y soporte multilingüe (español, inglés y chino).

Ideal para uso recreativo, como herramienta de motivación diaria o incluso como easter egg en sitios web. ¡Perfecta para compartir en redes sociales o usar como fondo de pantalla interactivo!

---

## 🎨 Características Principales

### ✅ Animaciones Fluidas y Efectos Visuales
- **Animación de rotura** con transición suave entre galleta intacta y rota.
- **Efecto de despliegue del pergamino** con entrada desde abajo y escala.
- **Luces flotantes y faroles chinos** animados en el fondo.
- **Dragones flotantes** en la cabecera con efecto de levitación.

### 🌐 Soporte Multilingüe (i18n)
- Idiomas disponibles: **Español (ES)**, **Inglés (EN)**, **Chino (ZH)**.
- Traducciones completas de:
  - Título y subtítulo.
  - Instrucciones.
  - Botones y mensajes del sistema.
  - Categorías y contenido de los mensajes (predicciones, consejos, etc.).
- Persistencia de idioma mediante `localStorage`.

### 💡 Contenido Dinámico y Aleatorio
- **Más de 100 mensajes únicos** distribuidos en 5 categorías:
  - Predicciones (`predictions`)
  - Consejos (`advice`)
  - Inspiración (`inspiration`)
  - Bromas (`jokes`)
  - Números de la suerte (`luckyNumbers`)
- Selección aleatoria de categoría y mensaje en cada interacción.
- Mensajes adaptados por idioma.

### 🖼️ Diseño Visual Estilizado
- Paleta de colores inspirada en la cultura china: rojo oscuro, dorado, crema.
- Fondo con gradiente y patrones radiales sutiles.
- Elementos decorativos: dragones, faroles, pergamino texturizado.
- Tipografía elegante con Google Fonts (`Noto Sans SC`).

### 📱 Responsive Design
- Adaptado a dispositivos móviles, tabletas y escritorio.
- Ajuste automático de tamaños, márgenes y ocultación de elementos no críticos en pantallas pequeñas.
- Menú de idioma reubicado y compactado en móvil.

### ⚙️ Interactividad Intuitiva
- Click en la galleta → revela mensaje.
- Botón “Otra galleta” → reinicia animación y genera nuevo mensaje.
- Menú desplegable de idioma con hover y click.
- Cursor cambiante y efectos hover en botones.

---

## 🧩 Arquitectura del Código

### 📁 Estructura del Proyecto

```
galleta-de-la-fortuna/
├── index.html           # HTML principal
└── (todo embebido en un solo archivo)
```

> El proyecto está completamente autocontenido en un único archivo HTML, incluyendo CSS, JavaScript y recursos externos (fuentes, iconos, imágenes).

---

## 🛠️ Tecnologías Utilizadas

| Tecnología             | Propósito                                                                 |
|------------------------|---------------------------------------------------------------------------|
| **HTML5**              | Estructura semántica del documento.                                       |
| **CSS3**               | Estilos, animaciones, layout flexible, responsive design.                 |
| **JavaScript ES6+**    | Lógica interactiva, generación de mensajes, manejo de idiomas.            |
| **Font Awesome 6.4.0** | Iconos (reiniciar, flechas, etc.).                                        |
| **Google Fonts**       | Fuente `Noto Sans SC` para soporte de caracteres chinos y estética moderna.|
| **Cloudinary**         | Hosting de imágenes de la galleta (intacta y rota).                       |

---

## 📜 Funcionalidades Detalladas

### 1. **Romper la Galleta**
- Al hacer clic, se activa una secuencia de animaciones:
  1. La galleta intacta gira 180° y desaparece.
  2. La galleta rota aparece con opacidad 1.
  3. El mensaje de fortuna se despliega con fade-in y escala.
- Se bloquea el clic hasta que se reinicie.

### 2. **Generar Mensaje Aleatorio**
- Se selecciona una categoría aleatoria (`predictions`, `advice`, `inspiration`, `jokes`, `luckyNumbers`).
- Dentro de esa categoría, se elige un mensaje aleatorio.
- Si es `luckyNumbers`, se muestra un encabezado especial y los números en formato listado.

### 3. **Cambio de Idioma**
- Menú desplegable con tres banderas y códigos de idioma.
- Al cambiar, se actualizan todos los textos de la interfaz.
- Se guarda la preferencia en `localStorage`.
- Los mensajes mostrados previamente se actualizan dinámicamente si cambia el idioma.

### 4. **Reiniciar la Experiencia**
- Botón “Otra galleta” restaura la galleta intacta.
- Oculta el mensaje actual.
- Habilita nuevamente el clic en la galleta.

### 5. **Animaciones y Efectos Visuales**
- **Faroles chinos**: balanceo continuo con diferentes retardos.
- **Dragones**: levitación suave con keyframes.
- **Botón de reinicio**: efecto de brillo lateral al pasar el mouse.
- **Fondo**: patrón radial sutil en tonos dorados.

---

## 📦 Recursos Externos

### 🔗 Imágenes de la Galleta (Cloudinary)
- Galleta intacta:  
  `https://res.cloudinary.com/dipv76dpn/image/upload/v1759626950/undefined_Quiero_una_versi%C3%B3n_d_b3r2sc.png`
- Galleta rota:  
  `https://res.cloudinary.com/dipv76dpn/image/upload/v1759626950/undefined_Galleta_de_la_fortun_pqfrtx.png`

> Las imágenes están optimizadas y cargadas desde CDN para velocidad.

### 🎵 Fuentes y Iconos
- **Fuente**: `Noto Sans SC` (Google Fonts) — soporte de caracteres chinos.
- **Iconos**: Font Awesome 6.4.0 (CDN) — usado para el botón de reinicio y flecha del menú.

---

## 📱 Vista Previa en Dispositivos

### 📱 Móvil (≤ 600px)
- Encabezado más compacto.
- Faroles ocultos.
- Menú de idioma ajustado a la derecha con posición relativa.
- Tamaños de fuente reducidos.
- Padding y márgenes ajustados para mejor legibilidad.

### 💻 Escritorio (> 600px)
- Full layout con decoración completa.
- Animaciones visibles en toda su expresión.
- Texto más grande y espaciado.

---

## 📝 Mensajes de Fortuna (Resumen)

### 🌈 Predicciones (`predictions`)
> Ejemplos:
> - “Uno de tus sueños se hará realidad muy pronto.”
> - “Recibirás una noticia que cambiará tu destino.”
> - “Encontrarás el amor en un lugar inesperado.”

### 🧭 Consejos (`advice`)
> Ejemplos:
> - “Ten paciencia, la gran muralla no se construyó en un día.”
> - “No juzgues cada día por la cosecha que recoges, sino por las semillas que plantas.”
> - “La humildad abre más puertas que la arrogancia.”

### 💫 Inspiración (`inspiration`)
> Ejemplos:
> - “Eres más fuerte de lo que crees y más capaz de lo que imaginas.”
> - “El éxito es la suma de pequeños esfuerzos repetidos día tras día.”
> - “Haz de cada día una obra maestra.”

### 😄 Bromas (`jokes`)
> Ejemplos:
> - “¿Por qué los peces son tan inteligentes? ¡Porque nadan en escuelas!”
> - “¿Qué le dice un techo a otro? Techo de menos.”
> - “¿Por qué Superman llevaba los calzoncillos por fuera? ¡Por fuera era Superman, por dentro era Clark Kent!”

### 🍀 Números de la Suerte (`luckyNumbers`)
> Ejemplos:
> - “3, 7, 21, 33, 42, 58”
> - “8, 14, 23, 35, 47, 56”
> - “5, 12, 19, 27, 39, 61”

---

## 📂 Archivo README.md

Este archivo es el **README.md completo** que describe la aplicación en detalle, ideal para repositorios públicos (GitHub, GitLab, etc.) o documentación interna.

---

## 🚀 Cómo Usar / Implementar

### 1. **Como Página Web Independiente**
Solo copia y pega el código HTML en un archivo `.html` y ábrelo en cualquier navegador moderno.

```bash
touch fortune-cookie.html
nano fortune-cookie.html   # o usa tu editor favorito
# pega el código completo
# luego abre en el navegador
```

### 2. **Como Componente Integrado**
Puedes extraer partes del código (CSS, JS, HTML) para integrarlo en un sitio existente.

### 3. **Personalización**
- Cambia los colores en `:root` (variables CSS).
- Modifica los mensajes en el objeto `fortuneMessages`.
- Agrega nuevas categorías o idiomas.
- Reemplaza las imágenes de la galleta por otras.

---

## 📬 Contacto y Créditos

**Autor**:  
Jhorman Jesús Castellanos Morales

**Créditos Visuales**:  
- Imágenes de galleta: Cloudinary (hosting externo).
- Iconos: Font Awesome (CC BY 4.0).
- Fuentes: Google Fonts (Open Source).

---

## 🔄 Futuras Mejoras (Roadmap)

- [ ] Compartir mensaje en redes sociales (Twitter, WhatsApp).
- [ ] Modo “Modo Oscuro” con toggle.
- [ ] Sonido ambiental al romper la galleta.

---

## 📊 Estadísticas del Proyecto

| Métrica                | Valor                          |
|------------------------|--------------------------------|
| Líneas de código       | ~1,000+                        |
| Idiomas soportados     | 3 (ES, EN, ZH)                 |
| Mensajes únicos        | 125+                           |
| Animaciones            | 6+ (dragones, faroles, galleta, scroll, botón, etc.) |
| Tamaño total del HTML  | ~150 KB (minificado posible)   |

---

## 🎉 ¡Disfruta tu Destino!

> *“La vida no se trata de esperar a que pase la tormenta, sino de aprender a bailar bajo la lluvia.”*

¡Rompe tu primera galleta y deja que el destino te sorprenda!

---

✅ **Listo para usar, compartir y modificar.**


---

## 🏆 Derechos Reservados

© 2025 — **Todos los derechos reservados**  
**Autor**: Jhorman Jesús Castellanos Morales  
**Proyecto original y exclusivo** — No autorizado su uso comercial sin permiso expreso.

🔗 **Versión en vivo disponible en:**  
👉 [https://jhormancastella.github.io/Fortune-Cookie/](https://jhormancastella.github.io/Fortune-Cookie/)
