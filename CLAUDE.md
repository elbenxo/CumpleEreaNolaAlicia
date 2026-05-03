# Cumple 8 años — Erea, Nola y Alicia

Web de invitación para el cumpleaños conjunto de **Erea, Nola y Alicia** — tres amigas que cumplen 8 años.

## Evento

- **Fecha:** Viernes 5 de junio de 2026
- **Hora:** 18:30 h — 22:00 h
- **Lugar:** Ilusiona Diversia · CC Heron Diversia · Av. de Bruselas 21-23 · 28108 Alcobendas (Madrid)
- **Confirmar asistencia:** antes del 30 de mayo de 2026
- **Hermanos/as:** 13,95 € cada uno, a cargo de la familia. Edad mínima del parque: **4 años**
- **Merienda:** incluida en el cumple (selección de bocadillos variados + bebida + tarta)
- **Alergias:** el parque solo gestiona menú sin gluten (celiaquía). Para cualquier otra alergia o intolerancia, los peques deben venir con su propia merienda

## Cumpleañeras

| Niña   | Símbolo / tagline |
|--------|---|
| Erea   | ☀ Sol — *el sol que trae paz* (su nombre viene del griego *eirene*, paz) |
| Nola   | ✦ Estrella fugaz — *la chispa imposible de atrapar* |
| Alicia | ☾ Luna — *la calma que ilumina la noche* |

## Stack técnico

- **HTML/CSS/JS** puro, single page, sin framework.
- **Tipografía:** Caprasimo (display) + Fraunces (italic accents) + Outfit (body) via Google Fonts.
- **Estética:** Cosmic Dreamscape — fondo nocturno con campo de estrellas, gradientes holográficos (rosa hot pink, cian neón, lavanda, dorado), número 8 gigante con gradiente animado, glassmorphism, sparkles flotantes.
- **Hosting:** GitHub Pages desde rama `main`.
- **Calendario:** Botón que descarga `.ics` con recordatorio el día anterior.
- **Modal de alergias:** se dispara automáticamente si en el formulario se selecciona "Otra alergia o intolerancia", recordando que hay que traer la merienda aparte.
- **RSVP:** Formulario preparado para Google Apps Script — pegar la URL en la constante `SCRIPT_URL` dentro del `<script>` de `index.html` cuando se quiera activar.
- **Sin datos personales públicos:** ni email ni teléfono ni redes sociales aparecen en la página. La confirmación se hace por el formulario o por el canal privado habitual de la familia.
- **No indexable:** la página lleva `<meta name="robots" content="noindex, nofollow, noarchive, nosnippet, noimageindex">` y un `robots.txt` con `Disallow: /`. La URL sigue siendo pública para quien la reciba, pero los buscadores no deben indexarla ni cachearla.

## Despliegue

- **Rama de producción:** `main` (GitHub Pages).
- **URL:** https://elbenxo.github.io/CumpleEreaNolaAlicia/

Cada push a `main` se despliega automáticamente en GitHub Pages (1-2 min).

## Estructura visual

1. **Hero** — número "8" gigante holográfico, "AÑOS DE MAGIA", nombres en serif itálica, pills con fecha/hora/lugar.
2. **Detalles** — fecha, horario (18:30 h — 22:00 h), lugar (con Google Maps + calendario + RSVP), merienda incluida.
3. **Las cumpleañeras** — tres tarjetas con glifo SVG personalizado (Erea: sol, Nola: estrella fugaz, Alicia: luna+estrella).
4. **Programa** — timeline con 3 hitos: Recepción · Fiesta · Fin.
5. **Info útil** — confirmación, hermanos (13,95 €), dress code, regalos, alergias.
6. **RSVP** — tarjeta con borde holográfico animado, formulario completo (alergias en desplegable + popup de aviso si "Otra").
7. **Footer** — estrellas titilando + frase con corazón animado.

## Cosas a personalizar antes de compartir

- [x] Fecha, hora, lugar, coste de hermanos.
- [x] Sin enlaces de WhatsApp ni email para no exponer datos personales en una web pública.
- [ ] Si se desea recoger respuestas en Google Sheets: crear un Apps Script y pegar la URL del web app en la constante `SCRIPT_URL` (línea ~`SCRIPT_URL = ''`).
- [ ] Revisar los taglines de cada cumpleañera por si se quieren personalizar más.
