# $CAR gasless auction and token contracts


## Development Process

Development follows these processes outlined in [development process](docs/development_process.md)

---

## Project Installation, building and running

Git clone, then from the project root execute

#### Install

To retrieve the project dependencies and before any further tasks will run correctly

```shell
npm ci
```

#### Husky Git Commit Hooks

To enable Husky commit hooks to trigger the lint-staged behaviour of formatting and linting the staged files prior
before committing, prepare your repo with `prepare`.

```shell
npm run prepare
```

#### Build and Test

```shell
npm run build
npm test
```

If you make changes that don't get picked up then add a clean into the process

```shell
npm run clean
npm run build
npm test
```

### Hardhat

If you want to avoid using the convience scripts, then you can execute against Hardhat directly.

#### All tests

Target to run all the mocha tests found in the `/test` directory, transpiled as necessary.

```shell
npx hardhat test
```

#### Single test

Run a single test (or a regex of tests), then pass in as an argument.

```shell
 npx hardhat test .\test\sample.test.ts
```

#### Scripts

The TypeScript transpiler will automatically as needed, execute through HardHat for the instantiated environment

```shell
npx hardhat run .\scripts\sample-script.ts
```

### Logging

Logging is performed with Bunyan

#### Bunyan CLI

To have the JSON logging output into a more human-readable form, pipe the stdout to the Bunyan CLI tool.

```shell
npx hardhat accounts | npx bunyan
```

## Sequence Diagram Rendering

To create or update the renders for the Plant UML sequence diagrams

#### Ensure Java is installed

```shell
java -version
```

The output will vary depending on OS, however if it fails claiming Java is not found, then you must install before proceeding.

#### Generate renders for all Plant UML documents under `docs/spec`

```shell
npm run plant
```
