 <!-- UseOnlyHook.transparent.png -->

 <p align="center"><img width="250" src="https://usejs.github.io/.github/public/Use.transparent.png"/></p>


# <p align="center">useClickOut</p>
<p align="center">
<a href="#details">
<img src="https://img.shields.io/badge/License-MIT-319046?" alt="License-MIT"/>&nbsp;&nbsp;
<img src="https://img.shields.io/badge/npm-0.1.2-319046?" alt="License-MIT"/></a>


</p>

<br/>

[useClickOut](#useClickOut) is a custom hook that captures the click in and out of an HTML element. It returns an array with three values and has a single argument.

- Returns:<br/>
[ref](#ref) : First value, `Type`: `React.RefObject<HTMLDivElement>`<br/>
[state](#state) : Second  value, `Type`: `boolean`<br/>
 [setState](#setstate) : Third  value, `Type`: `React.Dispatch<React.SetStateAction<boolean>>`<br/>

- Argument<br/>
  [initialState](#initialState): `boolean`<br/>

### Install
```bash 
npm i @use-ts/clickout
```

### Usage

```tsx 
import useClickOut from '@use-ts/clickout'

const Square = () => {

  const [ ref, state, setState ] = useClickOut(false)

  return (<>
    <div 
      ref={ref}
      onClick={() => setState(true)}  
    >
      Click
        {state ? ' Inside ' : ' Outside '}
      the square.
    </div>
  </>)
}

export default Square
```

### Type
> if you need `useClickOut` type, import inside `UseClickOut` braces with first letter capitalized.
```ts
import useClickOut, { UseClickOut } from '@use-ts/clickout'
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