# nuxt-server-components
This is a small project to detail the basics on how the Nuxt server components works.

![abstract illustration of the server render world](https://cdn.midjourney.com/fe419895-da3f-4af8-bef2-06ceaa0323fb/0_2.webp)
<small>_artwork generated by Midjourney_</small>

Besides Nuxt itself it uses:
- [ascii-faces]() to render the ASCII smileys
- [Pico.css](https://picocss.com/) for a quick and effortless page styling

## Try it locally
Just the same old few CLI commands to get started locally on your machine:

```bash
$ git clone https://github.com/moebiusmania/nuxt-server-components
$ cd nuxt-server-components
$ npm ci
$ npm run dev
```

## About Nuxt server components
Since early 2023 Nuxt started implementing an experimental version of their approach of the Island architecture, including full server components.

The core idea behind the server components is that, as the word implies, they are rendered **only** on server side, as opposed of the current "standard" implementation of SSR which include an hydration (_a re-render of the app/component_) on client side.

This helps reduce the JS payload sent to customers browsers thus making the application more performant.

This comes at the cost of the server component not being able to be interactive, but another cool thing is that if a server component receives props from the parent component, **when the props changes, the component is re-rendered on the server and a new static HTML chunk is sent to the browser and replace the old one**.

If you are interested you can check the [official roadmap of the feature](https://github.com/nuxt/nuxt/issues/19772).

## License
Published under the MIT license.