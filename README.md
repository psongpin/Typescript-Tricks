# Typescript Tips and Tricks
Reference for Typescript code snippets


## ReturnType ([reference](https://www.typescriptlang.org/docs/handbook/utility-types.html#returntypetype))
```
const myFunc = () => {
    return "this is a string"
}

type myFuncReturn = ReturnType<typeof myFunc>
```
