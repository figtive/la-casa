# :house_with_garden: La Casa

[![GitHub Actions Status](https://github.com/figtive/la-casa/actions/workflows/build.yml/badge.svg)](https://github.com/figtive/la-casa/actions/workflows/build.yml)

## Service

|   Name    | Stack                 |
| :-------: | --------------------- |
| Front-end | TypeScript, SvelteKit |

## Develop

To begin developing, simply run the development server (do not use `yarn`):

```shell
$ npm install
$ npm run dev
```

### Personal Page

Create a svelte file, the name of the file will be used as the route for the file. For example, `bogos.svelte` page can be accessed on `/bogos`. The name of the file is case-sensitive.

If you want to create a reusable component, you can create more svelte files in the `../lib/{name}/` directory. The file naming for components file is to use CamelCase to differentiate custom component with the default HTML components.

## License

This project is licensed under the [MIT License](https://github.com/figtive/la-casa/blob/master/LICENSE).
