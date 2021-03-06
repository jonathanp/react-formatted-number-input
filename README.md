# React formatted number input

A higher order component for formatting values in input elements as numbers

![Tests][tests-badge]
[![Code Coverage][coverage-image]][coverage-url]
[![NPM version][npm-image]][npm-url]

## Install

```
$ npm install --save react-formatted-number-input
```

## Usage

```ts
import React from "react";
import { createFormattedNumberInput } from "react-formatted-number-input";

const FancyInput = React.forwardRef((props, ref) => {
  return (
    <div>
      <input ref={ref} {...props} />
    </div>
  );
});

const FormattedNumberInput = createFormattedNumberInput(FancyInput, {
  precision: 2
});

const Demo = () => {
  const [value, setValue] = React.useState();

  return <FormattedNumberInput value={value} onChange={setValue} />;
};
```

## License

MIT © [Jonathan Svenheden](https://github.com/svenheden)

[coverage-image]: https://img.shields.io/codecov/c/gh/svenheden/react-formatted-number-input.svg
[coverage-url]: https://codecov.io/gh/svenheden/react-formatted-number-input
[npm-image]: https://img.shields.io/npm/v/react-formatted-number-input.svg
[npm-url]: https://npmjs.org/package/react-formatted-number-input
[tests-badge]: https://github.com/svenheden/react-formatted-number-input/workflows/Tests/badge.svg
