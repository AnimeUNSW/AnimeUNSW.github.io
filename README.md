# animeunsw.net
## Developing

Make sure you have [Deno](https://deno.land/) installed and have installed dependencies with `deno i`, to then start a development server:

```bash
deno task dev

# or start the server and open the app in a new browser tab
deno task dev -- --open
```

## Building

To create a production version of your app:

```bash
deno task build
```

You can preview the production build with `deno task preview`.

This repository has an Action to automatically build and deploy on push to `main`! Please only push to `main` when you are ready to deploy.
