# Galería con diálogo de imagen — ejercicio 16.3 (Astro)

Ejercicio / entrega de examen: la galería de animes del 16.2, pero al hacer clic en una imagen se abre en grande.

## Qué hace

- Grid con el top de animes (datos en `db.json`)
- Cada post es un componente `Post.astro`
- Al clicar la imagen se abre un `<dialog>` con la foto y el título
- Se cierra clicando fuera del contenido

## Cómo probarlo

```sh
pnpm install
pnpm dev
```

```sh
pnpm build
pnpm preview
```

Demo: https://astro-16-3-carrusel.netlify.app

## Cómo lo construí

- Misma base que el ejercicio de componentes: página + `Post` + Tailwind
- Añadí `ImageDialog.astro` para el modal
- La lógica está en `src/lib/initImageDialog.ts`: busca el clic en `[data-image-trigger]`, rellena src/título y llama a `showModal()`
- Tipado básico del post en `src/lib/types.ts`

## Cómo comprobarlo

No hay tests. En el navegador abro la demo o `pnpm dev`, clico varias imágenes y miro que el diálogo se abra y se cierre bien.

---

Moussi Joelle · [github.com/moussijoelle](https://github.com/moussijoelle)
