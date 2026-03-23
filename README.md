# SSG Build Script Implementation

1. **`ssg/build.js`**:
   - Updated the import of the `App` component to include the `.js` extension (`./App.js`).
   - Added logic to generate the static HTML page:
     - Read the `index.html` template.
     - Rendered the React `App` component to a static HTML string using `renderToStaticMarkup`.
     - Injected the rendered HTML into the `<!-- ROOT -->` placeholder in the template.
     - Created a `dist` directory (or cleared its existing contents if it was already there).
     - Saved the final generated HTML to `dist/index.html`.

2. **`ssg/index.html`**:
   - Removed the `<script type="module" src="index.js"></script>` tag, as the JavaScript is now purely being used to generate the static markup at build time and no longer needs an entry point in the browser.

3. **`ssg/App.js`**:
   - Updated the heading text from `"Hello from SSG"` to `"Hello Frontend Masters"`.
   - Reformatted the file for better readability.

4. Run `node build.js` to generate the static HTML page.

## SSR Implementation

1. **`ssr/server.js`**:
   - Updated the import of the `App` component to include the `.js` extension (`./App.js`).
   - Added logic to generate the static HTML page:
     - Read the `index.html` template.
     - Rendered the React `App` component to a static HTML string using `renderToStaticMarkup`.
     - Injected the rendered HTML into the `<!-- ROOT -->` placeholder in the template.
     - Created a `dist` directory (or cleared its existing contents if it was already there).
     - Saved the final generated HTML to `dist/index.html`.

2. **`ssr/index.html`**:
   - Removed the `<script type="module" src="index.js"></script>` tag, as the JavaScript is now purely being used to generate the static markup at build time and no longer needs an entry point in the browser.

3. **`ssr/App.js`**:
   - Updated the heading text from `"Hello from SSR"` to `"Hello Frontend Masters"`.
   - Reformatted the file for better readability.

4. Run `node server.js` to start the server.

## React Server Components Implementation

1. Install dependencies: `npm install`

`react-server-dom-webpack` is an internal React package that provides the React Server Components (RSC) implementation for DOM environments using Webpack as the bundler

`createFromFetch` allows us to turn a fetch request to an API endpoint into a React component directly. This is the magic of React server components and probably one you'll never write by hand again - your framework will always do this for you. But I wanted to demystify what it's doing for you. You make a request to an API endpoint, get a promise, and hand it to React to render

2. Run `npm run dev:client` and `npm run dev:server` to start the development server.
