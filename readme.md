# @tomvardasca/rescript-react-testing-library &middot; [![Build Status][actions-image]][actions-url] [![npm][npm-image]][npm-url] [![Codecov][codecov-image]][codecov-url]

> [ReScript](//github.com/rescript-lang/rescript-compiler) bindings for [react-testing-library](//github.com/testing-library/react-testing-library).

## Documentation

[**Read the docs**](//testing-library.com/docs/rescript-react-testing-library/intro) | [Edit the docs](//github.com/testing-library/testing-library-docs/tree/master/docs/bs-react-testing-library)

## Installation

```sh
$ yarn add --dev @tomvardasca/rescript-react-testing-library

# or..

$ npm install --save-dev @tomvardasca/rescript-react-testing-library
```

## Usage

#### Add to `bsconfig.json`

```json
{
  "bs-dev-dependencies": [
    "@tomvardasca/rescript-react-testing-library"
  ]
}
```

#### With [`bs-jest`](//github.com/glennsl/bs-jest)

```ocaml
/* Component_test.re */

open Jest;
open Expect;
open ReactTestingLibrary;

test("Component renders", () =>
  <div style=ReactDOM.Style.make(~color="rebeccapurple", ())>
    <h1> {React.string("Heading")} </h1>
  </div>
  |> render
  |> container
  |> expect
  |> toMatchSnapshot
);
```

## Examples

See [`src/__tests__`](src/__tests__) for some examples.

## Development

```sh
$ git clone https://github.com/tomvardasca/rescript-react-testing-library.git
$ cd rescript-react-testing-library
$ yarn # or `npm install`
```

## Build

```sh
$ yarn build
```

## Test

```sh
$ yarn test
```

## Change Log

> [Full Change Log](changelog.md)

### [v0.9.2](https://github.com/tomvardasca/rescript-react-testing-library/releases/tag/v0.9.2) (2021-02-19)

* Update readme.md ([@tomvardasca](https://github.com/tomvardasca) in [1337603](https://github.com/tomvardasca/rescript-react-testing-library/commit/1337603))
* Update readme credits ([@tomvardasca](https://github.com/tomvardasca) in [3d89f55](https://github.com/tomvardasca/rescript-react-testing-library/commit/3d89f55))

## License

MIT © [Neil Kistner](https://neilkistner.com) and Tomé Vardasca

## Credits

This is a fork of the great work from [Neil Kistner](https://neilkistner.com) on [bs-react-testing-library](https://github.com/wyze/bs-react-testing-library)


[actions-image]: https://img.shields.io/github/workflow/status/tomvardasca/rescript-react-testing-library/CI.svg?style=flat-square
[actions-url]: https://github.com/tomvardasca/rescript-react-testing-library/actions

[npm-image]: https://img.shields.io/npm/v/rescript-react-testing-library.svg?style=flat-square
[npm-url]: https://npm.im/@tomvardasca/rescript-react-testing-library

[codecov-image]: https://img.shields.io/codecov/c/github/tomvardasca/rescript-react-testing-library.svg?style=flat-square
[codecov-url]: https://codecov.io/github/tomvardasca/rescript-react-testing-library
