<p align="center">
  <img src="villin.svg" alt="Villín, mascota del CIFP Villa de Agüimes" width="180">
</p>

# Villín · Asistente virtual del CIFP Villa de Agüimes

Villín es un asistente informativo por reglas, hecho con un único archivo HTML y JavaScript. No usa inteligencia artificial generativa ni servidores: responde con la información publicada en la web del centro, por lo que no inventa respuestas y no tiene coste de mantenimiento.

**Probarlo:** https://35014664.github.io/villin/

## Qué sabe

Ciclos formativos por familia profesional y departamentos, horario y trámites de Secretaría, reclamación de notas, convalidaciones, matrícula y acceso, FCT, FP Dual, bolsa de empleo, Erasmus+, calidad (EQAVET), orientación (DIOP), becas, redes del centro, Radio Entérate, Aula AtecA, Restaurante Aulaga, equipo directivo, historia, documentos institucionales y redes sociales.

## Cómo funciona

Todo está en `index.html`:

1. La base de conocimiento es el array `KB`: cada tema tiene palabras clave (`k`), la respuesta en HTML (`a`) y temas sugeridos (`s`).
2. Al escribir, el texto se pasa a minúsculas y se le quitan tildes y signos. Cada tema puntúa por coincidencia de palabras, frases, raíces y erratas leves (distancia de edición).
3. Gana el tema con más puntos. Si no hay coincidencia, remite a Secretaría.

## Cómo añadir o corregir información

Edita `index.html` en GitHub (icono del lápiz), localiza el tema dentro de `KB` y cambia su texto o sus palabras clave. En 1-2 minutos GitHub Pages publica el cambio.

## Incrustarlo en WordPress (edublog)

Con el plugin Advanced iFrame, en un bloque de **Shortcode**:

```
[advanced_iframe src="https://35014664.github.io/villin/?embed=1" width="400" height="650" scrolling="no" frameborder="0" transparency="true"]
```

El parámetro `?embed=1` oculta la página de presentación y deja solo el botón flotante y el chat.

## Mascota

Villín está dibujado a partir del logotipo del centro (las tres piezas amarilla, azul y gris) en estilo cómic. Es un SVG vectorial: `villin.svg`.

## Aviso

La información es orientativa y procede de https://www3.gobiernodecanarias.org/medusa/edublog/cifpvilladeaguimes/. Para trámites oficiales, consulta siempre con Secretaría (928 599 141 · administracion@cifpvilladeaguimes.es).
