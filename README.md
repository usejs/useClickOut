 <!-- UseOnlyHook.transparent.png -->

 <p align="center"><img width="250" src="https://usejs.github.io/.github/public/Use.transparent.png"/></p>


## <p align="center">useClickOut</p>

`useClickOut` is a custom hook that captures the click in and out of an HTML element. It returns an array with three values and has a single argument.

- Returns:
   - `ref` : First value, `Type`: `React.RefObject<HTMLDivElement>`
   - `state` : Second  value, `Type`: `boolean`
   - `setState` : Third  value, `Type`: `React.Dispatch<React.SetStateAction<boolean>>`

- Argument
  - `boolean`

### Install
```bash 
npm i useclickout
```

### Usage

```tsx 
import useClickOut from 'useclickout'

const Square = () => {

  const [ ref, state, setState ] = useClickOut(false)

  return (<>
    <div 
      ref={ref}
      onClick={() => setState(true)}  
    >
      Click
        {state ? 'Inside' : 'Outside'}
      the square.
    </div>
  </>)
}

export default Square
```

### Type
> if you need `useClickOut` type, import inside `UseClickOut` braces with first letter capitalized.
```ts
import useClickOut, { UseClickOut } from 'useclickout'
```

```ts
type UseClickOut = (initialState:boolean) => [
  React.RefObject<HTMLDivElement>,
  boolean,
  React.Dispatch<React.SetStateAction<boolean>>
]
```

<br/>
<br/>
<br/>

<p align="center">Use.js &copy; 2022 | License MIT</p>