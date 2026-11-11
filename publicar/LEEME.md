# Terra Açaí — carpeta para publicar en Netlify

## Qué hay aquí

```
publicar/
├── index.html              La web propuesta (el prototipo)
├── presentacion/
│   ├── index.html          La propuesta para el cliente
│   └── presentacion.css
├── _headers                Cabecera noindex para todo el sitio
├── robots.txt              Bloqueo de rastreadores
└── LEEME.md                Este archivo
```

## Cómo subirlo

1. Entra en https://app.netlify.com/drop
2. Arrastra **la carpeta `publicar` entera**, no su contenido suelto.
3. Netlify te da una dirección del tipo `https://algo-aleatorio.netlify.app`.
4. En *Site configuration → Change site name* ponle algo presentable, por ejemplo
   `terra-acai-propuesta`.

Enlace que le mandas al cliente:

```
https://terra-acai-propuesta.netlify.app/presentacion/
```

La web sola queda en la raíz (`/`), y la presentación enlaza a ella desde varios botones.

## Importante

- **La presentación no lleva capturas.** Las ventanas del recorrido, el comparador
  y el teléfono cargan páginas reales dentro de un `iframe`. El panel «Actual» del
  comparador carga `terraacai.es` en vivo, así que refleja siempre el estado real
  de la web actual.
- **Está bloqueada para buscadores** por tres vías: la etiqueta `robots` en el HTML,
  el archivo `_headers` y `robots.txt`. Aun así es una dirección pública: cualquiera
  con el enlace puede verla.
- **Si cambias el prototipo**, acuérdate de volver a copiarlo aquí antes de subirlo:

  ```powershell
  Copy-Item "..\index.html" ".\index.html" -Force
  ```

  El archivo que se edita es `PROYECTS\TERRA\index.html`. El de esta carpeta es
  una copia para publicar.

## Antes de enviárselo al cliente

Repasa la sección «Lo que hemos corregido»: son afirmaciones sobre su web actual y
conviene que las hagas tuyas antes de mandarlas. Y la sección «Lo que necesitamos
de vosotros» es la que te va a desbloquear el proyecto, sobre todo el punto de las
fotografías.
