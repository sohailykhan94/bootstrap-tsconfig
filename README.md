# TSConfig
Basic tsconfig which can be referenced and locally extended in your projects.

# Overview
| Property | Description | Default value |
| --- | --- | --- |
| `allowJs` | Allow JavaScript files to be a part of your program. Use the `checkJS` option to get errors from these files. | `true` |
| `allowSyntheticDefaultImports` | Allow 'import x from y' when a module doesn't have a default export. | `true` |
| `baseUrl` | Specify the base directory to resolve non-relative module names. | `"./src"` |
| `esModuleInterop` | Emit additional JavaScript to ease support for importing CommonJS modules. This enables `allowSyntheticDefaultImports` for type compatibility. | `true` |
| `experimentalDecorators` | Enable experimental support for TC39 stage 2 draft decorators. | `true` |
| `forceConsistentCasingInFileNames` | Ensure that casing is correct in imports. | `true` |
| `isolatedModules` | Ensure that each file can be safely transpiled without relying on other imports. | `true` |
| `jsx` | Specify what JSX code is generated. | `"react"` |
| `lib` | Specify a set of bundled library declaration files that describe the target runtime environment. | `["dom", "dom.iterable", "esnext", "es6"]` |
| `module` | Specify what module code is generated. | `"esnext"` |
| `moduleResolution` | Specify how TypeScript looks up a file from a given module specifier. | `"node"` |
| `noEmit` | Disable emitting file from a compilation. | `true` |
| `noFallthroughCasesInSwitch` | Enable error reporting for fallthrough cases in switch statements. | `true` |
| `noImplicitAny` | Enable error reporting for expressions and declarations with an implied `any` type.. | `true` |
| `noUnusedLocals` | Enable error reporting when a local variables aren't read. | `true` |
| `noUnusedParameters` | Raise an error when a function parameter isn't read | `true` |
| `resolveJsonModule` | Enable importing .json files | `true` |
| `skipLibCheck` | Skip type checking all .d.ts files. | `true` |
| `sourceMap` | Create source map files for emitted JavaScript files. | `true` |
| `strict` | Enable all strict type checking options. | `true` |
| `suppressImplicitAnyIndexErrors` | Suppress `noImplicitAny` errors when indexing objects that lack index signatures. | `true` |
| `target` | Set the JavaScript language version for emitted JavaScript and include compatible library declarations. | `"es2015"` |

# Usage
## Add to package
```
yarn add https://github.com/sohailykhan94/bootstrap-tsconfig -D
```

## Include in local config
### tsconfig.json
```
{
  "extends": "bootstrap-tsconfig/index.json",
  "compilerOptions": {
    "preserveConstEnums": true
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules", "**/*.spec.ts"]
}
```