# Typescript Tips and Tricks
Reference for Typescript code snippets


## [ReturnType](https://www.typescriptlang.org/docs/handbook/utility-types.html#returntypetype)
```tsx
const myFunc = () => {
    return "this is a string"
}

type myFuncReturn = ReturnType<typeof myFunc>
```

## [Parameters](https://www.typescriptlang.org/docs/handbook/utility-types.html#parameterstype)
```tsx
const myFunc = (
  param1: String,
  param2?: {
    prop1?: string
    prop2?: {
      subProp1?: string
      subProp2?: string
    }
  }
) => {
  return undefined
}

type MyFuncParams = Parameters<typeof myFunc>
type Param1 = MyFuncParams[0]
type Param2 = MyFuncParams[1]
```

## [Awaited](https://www.typescriptlang.org/docs/handbook/utility-types.html#awaitedtype)
```tsx
const myFunc = () => {
  return Promise.resolve({
    id: 12345,
    firstName: "Paul Simon",
    lastName: "Ongpin",
  })
}

type PromiseReturn = ReturnType<typeof myFunc>
type ResolvedValue = Awaited<PromiseReturn>
```

## [keyof](https://www.typescriptlang.org/docs/handbook/2/keyof-types.html#the-keyof-type-operator)
```tsx
const libraryRepos = {
  react: "https://github.com/facebook/react",
  vue: "https://github.com/vuejs/",
  angular: "https://github.com/angular",
}

type LibraryReposKeys = keyof typeof libraryRepos
// "react" | "vue" | "angular"
```
