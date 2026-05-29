#Laboratorio 1. EXTRA.

En la versión desktop encontramos 4 bloques definidos: header, nav, main y footer.
Se encuentran posicionados por medio de `grid` en un espacio que ocupa todo la vista de la pantalla.

```
body {
  background-color: $color-background;
  font-family: roboto, sans-serif;
  display: grid;
  grid-template-rows: auto 1fr auto;
  height: 100vh;
}
```

- El `header` dividido en una toolbar que desaparece en la versión mobile y una barra con el nombre de la app, con el uso de `flex`.

- El `nav` se queda fijo (`position: sticky` que aplicamos en el contenedor para que se mantenga el alto). En desktop los ítem se colocan en columna para pasar a row cuando la resolución es menor de 768px.

- El `main` funciona como contenedor de las `.card`, que se ordenan de forma fluida con `flex`. Esto nos permite que cuando la resolución sea menor de 768px cambie su disposición cambiando a `flex-direction: column` y modificando la alineación de los componentes de la `.card`.

```
.list {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  justify-content: space-evenly;
  gap: 15px;
}
```

- El `footer`ocupa un lugar fijo al final de la página.
