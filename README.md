# @erboladaiorg/eum-doloribus-delectus

[![npm version](https://img.shields.io/npm/v/@erboladaiorg/eum-doloribus-delectus.svg)](https://npmjs.org/package/@erboladaiorg/eum-doloribus-delectus)

Easy and small child_process.spawn.

- Promise-based
- Cross-platform
- Pass stdin as an argument
- Rejects on stderr by default, even if exit code is 0

## Install

```sh
$ npm install --save @erboladaiorg/eum-doloribus-delectus
```

## Usage

```typescript
(
  command: string,
  args?: string[],
  options?: Options,
  spawnOptions?: any,
): Promise<{
  stdout: string
  stderr: string
}>
```

```js
import spawn from '@erboladaiorg/eum-doloribus-delectus'

const { stdout, stderr } = await spawn('printf', ['please?'])

assert.equal(stdout, 'please?')
assert.equal(stderr, '')
```

## Options

- `rejectOnError: boolean` - Throws an error if stderr is non-empty. Default: true.
- `stdin: string` - Send stdin to the spawned child process.
- `stdout: (data: string) => void` - Stream stdout by chunk.
- `stderr: (data: string) => void` - Stream stderr by chunk.

## License

ISC © [Raine Revere](https://github.com/raineorshine)
