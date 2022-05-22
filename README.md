# SimpleProcess

Simple node child process wrapper for typescript

## Description

Executes a process async redirecting all output to the default stdout/stderr.

```typescript
export const simpleProcess = async (executable: string, args: string[] ): Promise<boolean>
```

### Parameters

- `executable` e.g. 'gulp'
- `args` e.g. `['clean']`
- *returns* `true` if successfull otherwise `false`

## Example

```typescript
import { simpleProcess } from '@mauriora/simpleprocess';

const runServe = async (): Promise<boolean> => simpleProcess('gulp', ['serve', '--nobrowser']);

if( await runServe()) {
    exit(0);
} else {
    exit(1);
}

```
