# YIQ

Returns white when a color is dark and black when a color is light. 🎨

[![Build Status](https://circleci.com/gh/lffg/yiq.svg?style=svg)](https://circleci.com/gh/lffg/yiq)
[![NPM](https://img.shields.io/npm/v/yiq.svg?logo=npm)](https://npmjs.org/package/yiq)
![Uses TypeScript](https://img.shields.io/badge/Uses-Typescript-294E80.svg)

## Installing

```shell
yarn add yiq

# If you're using NPM:
# npm install yiq --save
```

## Basic Usage

Just call the `yiq` function after importing it:

```typescript
import yiq from 'yiq'

console.log(yiq('#fff')) // #000
console.log(yiq('#000')) // #fff
```

## API

### `yiq`

`yiq` — Returns a light color when a color is dark and black color when a color is light.

#### Description

```typescript
function colorYiq(
  colorHex: string,
  options?: {
    white: string
    black: string
  }
): string
```

The second argument (options) should be used to define the colors that the function will return:

```typescript
yiq('#fff', {
  white: '#f0f0f0',
  black: '#333'
}) // #333
```

The default options are:

- `options.white`: `#fff`;
- `options.black`: `#000`.

## Authors and License

[lffg](https://github.com/lffg) and [contributors](https://github.com/lffg/yiq/graphs/contributors).

MIT License, see the included [MIT](https://github.com/lffg/yiq/blob/master/LICENSE) file.
