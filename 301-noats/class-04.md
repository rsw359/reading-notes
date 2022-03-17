# Class 03 *Reading Notes*

## React Forms

1. A controlled component is a form element that can be controlled by React due to its state being mutable

2. We update the state with of the form their as soon as the users enter them because the handler in react runs with every keystroke

3. We can target what the user is entering by having the state set to an empty string that is targeting the value entered into the target field i.e `this.setState({value: event.target.value});`

## The Conditional (Ternary) Operator

1. We use the ternary function to shorten if conditionals to a single line of code
2. x ===y ? console.log(true) : console.log(false)