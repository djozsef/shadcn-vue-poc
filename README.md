# Shadcn Vue setup PoC

## Start up CLI in docker 

To start the docker container for CLI:
```sh
$ ./cli-docker.sh
```

## Install shadcn-vue

1. Create shadcn-vue project
```sh
$ pnpm create vite@latest frontend -- --template vue-ts
```

2. Install NPM dependencies
```sh
$ cd frontend && pnpm install```

3. Add `tailwindcss` and `autoprefixer` 
```sh
$ pnpm add -D tailwindcss@3.4.17 autoprefixer
```

4. Init `tailwindcss`
```sh
$ pnpm tailwindcss init
```

5. Add this import header in your main css file, `src/style.css` in our case:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

6. Configure the Tailwind template paths in `tailwind.config.js`:
```typescript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['./index.html', './src/**/*.{ts,js,vue}'],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

7. Proceed with official shadcn-vue documentation from step 3: https://www.shadcn-vue.com/docs/installation/vite.html

## Start the project in docker, detached

```sh
$ docker-compose up -d 
```