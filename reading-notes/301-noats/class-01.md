# Class 01 *Reading Notes*

## *Component Based Architecture*

* What is a “component”?
  * A component is a modular software object that contains a specific functionality and can be reused to save time and money. They are designed to be modified and to interact with other components

* What are the characteristics of a component?
  * Reusability - Componenents should be able to be reused for different needs across multiple applications
  * Replaceability - Components should be able to be replaced with other components as needed
  * Not Context Specific - Components should be useable across many contexts and environments
  * Extensible - Components can be extended to prvided new behavior
  * Encapsulated − A component allows the caller to use its functionality without exposing the details of the internal processes, internal variables, or its state
  * Independent − Components are designed to have minimal dependencies on other components

* What are the advantages of using component-based architecture?
  * Ease of deployment − As new versions become available, existing versions can be easily replaced with no impact on the existing components
  * Reduced cost − The use of third-party components allows you to spread the cost of development and maintenance
  * Ease of development − Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system
  * Reusable − The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems
  * Modification of technical complexity − A component modifies the complexity through the use of a component container and its services
  * Reliability − The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse
  * System maintenance and evolution − Easy to change and update the implementation without affecting the rest of the system
  * Independent − Components posess independency and flexible connectivity and can be developed by different groups in parallel. This increases development productivity

## *Props and thier use in React*

* What is “props” short for?
  * "Props" is short for properties, which are objects used to pass data between parent and child

* How are props used in React?
  * Props are used to pass info from parent components to child components
  1. Create a parent component
  2. Pass data as a "prop"
  3. Render the prop data

* What is the flow of props?
  * The flow of props is uni-directional, from parent to child

## Things I would like to know more about

* What is the benefit of using props?
  * It appears that you still have to manually change the data in the parent component, so how does this save time? I suppose you could implement this in some sort of loop to iterate on the data contained in the prop...

* Information taken from : <https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm> & <https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0>
