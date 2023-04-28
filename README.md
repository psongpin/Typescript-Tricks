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
