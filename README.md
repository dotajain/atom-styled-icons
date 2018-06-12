# atom-styled-icons

Iconography for ATOM styled Icons and React.js

## Install

`npm install atom-styled-icons`

or

`yarn add atom-styled-icons`

## Usage

```javascript
import { Facebook } from 'atom-styled-icons';

<Facebook />
<Facebook color='plain' />
<Facebook size='large' />
<Facebook size='xlarge' />
```

Visit our [site](https://dotajain.github.io/atom-styled-icons/) for more icons.

## Customize

The theme for the icon supports different colors and sizes. The default definition is:

```
  color: '#666666',
  colors: {},
  size: {
    large: '48px',
    xlarge: '96px',
  },
```

You can customize sizing and/or colors by specifying your own theme context.
The `colors` property allows you to use color names. For
instance: `colors: { brand: '#ff0000' }` would allow you to use
`<ZoomOut color='brand' />`.

For example:

```javascript
  import { ThemeContext } from 'atom-styled-icons';
  ...
  const theme = {
    color: '#333333',
    colors: { brand: '#ff0000' },
  };
  return (
    <ThemeContext.Provider value={theme}>
      <ZoomOut color='brand' />
    </ThemeContext.Provider>
  );
  ...
```

or

```javascript
  import { ThemeProvider } from 'styled-components';
  ...
  const theme = {
    color: '#333333'
    colors: { brand: '#ff0000' },
  };
  return (
    <ThemeProvider theme={theme}>
      <ZoomOut color='brand' />
    </ThemeProvider>
  );
  ...
```

## Build

To build this library, execute the following commands:

  1. Install NPM modules

    $ npm install (or yarn install)

  2. Run pack

    $ npm run dist

  3. Test and run linters:

    $ npm run check

  4. Generate React icons:

    $ npm run generate-icons
