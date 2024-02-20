# Rolling The Music 🎤

Todo lo que necesitas para construir un proyecto Svelte, impulsado por [`create-svelte`](https://github.com/sveltejs/kit/tree/main/packages/create-svelte).

## Creación de un proyecto


Si estás viendo esto, probablemente ya hayas completado este paso. ¡Felicitaciones!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Desarrollo

Una vez que hayas creado un proyecto e instalado las dependencias con `npm install` (o `pnpm install` o `yarn`), inicia un servidor de desarrollo:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Construcción

Para crear una versión de producción de tu aplicación:

```bash
npm run build
```

Puedes previsualizar la construcción de producción con `npm run preview`.

> Para desplegar tu aplicación, es posible que necesites instalar un [adaptador](https://kit.svelte.dev/docs/adapters) para tu entorno de destino.