# Jr Stepper Form

jr-stepper-form is a stepper form builder component for react. The component is design keeping ease of use in mind. The library is very easy to use with only 1 imports.

The library dosen't have any styles included so it dosen't conflict with your own styles.

# Visit my site @

[My Portfolio](https://jamilurrahman.com/)
>

[![NPM](https://img.shields.io/npm/v/jr-stepper-form.svg)](https://www.npmjs.com/package/jr-stepper-form) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save jr-stepper-form

```
![image](https://user-images.githubusercontent.com/33858136/100274375-83e7db00-2f88-11eb-8d61-ece21ebe3df1.png)

## Usage

```jsx
import React from 'react'

import { StepperForm } from 'jr-stepper-form'

const App = () => {
  const sb = (e) => {
    e.preventDefault();
    console.log('hello');
  }
  return (
    <StepperForm maxStep={5} currentStep={0} onSubmit={e => sb(e)}>
      <h1>1</h1>
      <h1>2</h1>
      <h1>3</h1>
      <h1>4</h1>
      <div>
        <h1>5</h1>
        <input type='submit' value="submit">
      </div>
    </StepperForm>
  )
}

export default App


```

## or

```javascript
import React from 'react'

import { StepperForm } from 'jr-stepper-form'

const App = () => {
  const sb = (e) => {
    e.preventDefault()
    console.log('hello')
  }
  const Step1 = () => <h1>STEP 1</h1>
  const Step2 = () => <h1>STEP 2</h1>
  const Step3 = () => <h1>STEP 3</h1>
  const Step4 = () => <h1>STEP 4</h1>
  const Step5 = () => <h1>STEP 5</h1>

  return (
    <StepperForm maxStep={5} currentStep={0} submit={(e) => sb(e)}>
      <Step1 />
      <Step2 />
      <Step3 />
      <Step4 />
      <Step5 />
    </StepperForm>
  )
}

export default App
```

## Props

| name         | type           | isRequired ? | description                                           | start value |
| ------------ | -------------- | ------------ | ----------------------------------------------------- | ----------- |
| currentStep  | number         | true         | current step number or starting step                  | 0           |
| submit       | callback       | true         | on submit method                                      | null        |
| stepperClass | string         | false        | class name for stepper for to customize stepper form  | ' '         |
| maxStep      | number         | true         | max number of steps                                   | null        |
| previousText | any            | false        | button text for previous button or your own component | 'prevoius'  |
| nextText     | any            | false        | button text for next button or your own component     | 'next'      |
| btnClass     | string         | false        | css class for previous and next button                | ' '         |
| children     | react children | true         | might give error if now children passed               | null        |

## HELP

### Styling previous and next button

>previous and next buttons are enclosed in <div> with class name 'btns' as such

```html
      <div className='btns'>
        <button
          className={btnClass ? btnClass : ''}
          onClick={(e) => handlePrev(e)}
        >
          {previousText ? previousText : 'Previous'}
        </button>
        <button
          className={btnClass ? btnClass : ''}
          onClick={(e) => handleNext(e)}
        >
          {nextText ? nextText : 'Next'}
        </button>
      </div>
```
### Styling stepper form

>pass stepperClass='style-class' as props to style stepper form


## License

MIT © [Jamilur-rahman-470](https://github.com/Jamilur-rahman-470)

PORTFOLIO @ [Portfolio](https://jamilurrahman.com)
