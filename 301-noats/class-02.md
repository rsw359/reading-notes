# Class 01 *Reading Notes*

## React Lifecycle

1. Based on the diagram, render occurs before componentDidMount
2. The very first thing to happen in the lifecycle of an event is
3. These things occur in the following order:
    - constructor
    - render
    - react updates(caused by changes to props or state)
    - componentDidMount
    - componentWillUnmount happens in its own phase when removing a compronent from the DOM

4. componentDidMount is called after the render has taken place. This method is used to run statements that depend on the component having been rendered already. This method causes the component to be rerendered, but that is not apparent to the end user

## React State vs Props

1. You can pass the things that you want to be rendered to the props in the same fashion as you would pass arguments into a function.
2. The big difference beetween state and props is that state is handled and updated inside the component, while props are handled outside the component.
3. When the state f a component is changed, it is re-rendered
4. Things that are updated within the function, such as counters can be stored in the state. Changes that a users make to a form can also be stored in the state. Any changes that are made within the component are stored within the state.

## Things I would like to know more about

I would like to see what other types of things can be stored in the state of a component, and what the limits of these changes are.
