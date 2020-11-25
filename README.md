# cra-template-tailwindcss

A streamlined [Tailwind CSS](https://tailwindcss.com) template for [Create React App](https://github.com/facebook/create-react-app).

> This template installs and sets up [Tailwind CSS](https://tailwindcss.com) using a [custom react-scripts fork](https://npmjs.com/package/@geoffcodesthings/react-scripts) to allow support for a `postcss.config.js` file.

## Usage

```bash
npx create-react-app --scripts-version @geoffcodesthings/react-scripts --template tailwindcss
```

### Why a custom `react-scripts` fork?

By default, Create React App doesn't allow us to add a `postcss.config.js` file to setup postcss plugins like Tailwind CSS. Adding support for this is fairly trivial, yet it hasn't been implemented in core CRA. Maintaining a custom fork of react-scripts is not ideal, but our options are limited. We could use [postcss-cli](https://github.com/postcss/postcss-cli), but until CRA updates it's `postcss` dependency to postcss 8, we would have to use an older version of `autoprefixer`. We don't want to do this. In this past, this template used [craco](https://github.com/gsoft-inc/craco), but it is outdated and currently incompatible with CRA. So why use a custom fork of `react-scripts`? It's the easiest way to ensure that this template works now and in the future. This way, we can utilize PostCSS to customize Tailwind V2 for our project via our `tailwind.config.js` file.

## License

MIT © [Geoff Selby](https://geoffcodesthings.com)
