# React Fundamentals
- ##### What is imperative programming?
	it is a style of programming
	we describe how a program should accomplish a task
	we describe every step by step
- ##### ==What declarative programming?==
	it is a style of programming
	we describe what you want the program to accomplish
	
	we do not describe how,
	we do not tell the program how to do such tasks the step by step
	instead the program knows how to do it
	so we only tell what we want to the program.
	
	we can write code in such a style
	because the declarative code is always built on top of imperative code.
	and when we think about it
	it is so true, because at the end of day, 
	we need to tell the computer to do what we want step by step.
	
	React helps us to write code in a declarative style.
	so that we can focus on managing states of the system, the user interface
	not so so much focus on how and when to update the interface step by step
	
	so we deal with managing states of the system
	and React deals with the actual DOM tree and how to update the tree in the most efficient way
	
	so we can think 
	React is an imperative code written by other developers 
	so that we can write code in a declarative style
- ##### ==What is React==
	it is a library for building user interfaces.
	
	one of the differences of React from old libraries such as jQuery
	is that it helps developers 
	by letting us focus on states of the system
	while it focuses on how to actually update DOM
	
	it is called declarative programming
	
	it is a style of programming
	we describe what you want the program to accomplish
	
	we do not describe how,
	we do not tell the program how to do such tasks the step by step
	instead the program knows how to do it
	so we only tell what we want to the program.
	
	we can write code in such a style
	because the declarative code is always built on top of imperative code.
	and when we think about it
	it is so true, because at the end of day, 
	we need to tell the computer to do what we want step by step.
	
	React helps us to write code in a declarative style.
	so that we can focus on managing states of the system, the user interface
	not so so much focus on how and when to update the interface step by step
	
	so we deal with managing states of the system
	and React deals with the actual DOM tree and how to update the tree in the most efficient way
	
	so we can think 
	React is an imperative code written by other developers 
	so that we can write code in a declarative style
	
	also React dose update DOM it in the most efficient way possible,
	DOM manipulation can be time-consuming and computational
	so React really cares about how to update DOM in the most efficient way
	reconciliation is one of the things that React really cares about.
	and React even has an engine, reconciler, for it, it is called Fiber
	and React's reconciliation algorithm using Fiber Tree is really smart.	
	
	but because of its abstraction, 
	Junior developers have difficulties to understand how React actually works,
	
	for example,
	some developers think 
	JSX is a part of JS or browser, so that JS engine or browser can understand JSX.
	like how junior developers think DOM API is a part of JS in the beginning
	
	some developers memorize the rules of hooks,
	we know that we should not call hook functions inside conditionals or loops 
	and we can only call them at the top level 
	because order of execution of hooks matter
	
	but junior developers do not often know why it matters, so they memorize the rule
	but you do not actually have to memorize it 
	once you understand Hooks are stored as a linked list on the Fiber Node
	
	and even tho we developers do not have to write code in the imperative way
	we need to have in-depth knowledge of React's internal workings, like its reconciliation algorithm and Fiber engine
	to optimize performance or to debug in complex applications
- ##### ==Disadvantages of React==
	it is very easy to use
	because it is declarative,
	React helps us to write code in a declarative style.
	so that we can focus on managing states of the system, the user interface
	not so so much focus on how and when to update the interface step by step
	
	but because of its abstraction, 
	Junior developers have difficulties understanding how React actually works
	
	for example,
	some developers think 
	JSX is a part of JS or browser, so that JS engine or browser can understand JSX.
	like how junior developers think DOM API is a part of JS in the begining
	
	some developers memorize the rules of hooks,
	we know that we should not call hook functions inside conditionals or loops 
	and we can only call them at the top level 
	because order of execution of hooks matter
	
	but junior developers do not often know why it matters, so they memorize the rule
	but you do not actually have to memorize it 
	once you understand Hooks are stored as a linked list on the Fiber Node
	
	when we traverse a linked list, order is really important, 
	
	for example,
	if we wrap our hooks inside a condition, 
	we might have different number of hooks and different order on re-render.
	and that means that we can miss or skip a node on our linked list
	so React cannot reference the correct hook when React traverses the liked-list
	so we always want to call hooks at the top level
	
	and even tho we developers do not have to write code in the imperative way
	because React takes care of it
	we need to have in-depth knowledge of React's internal workings, like its reconciliation algorithm
	to optimize performance or to debug in complex applications
	
	but its abstraction often distract developers
- ##### What is the difference between React and React DOM?  
	**React** is a core library 
	
	React provides the fundamental and universal functionalities for building user interfaces	
	
	React deals with building components and managing states, and handling the component lifecycle.

	it provides functions such as 
	React.createElement(), React.Component, React.Children
	
	on the other hand,
	
	React DOM is a DOM-specific library 
	
	ReactDOM helps components to be rendered on DOM
	
	ReactDOM provides functionality specific to browsers
	it provides functions such as
	render() and createPortal()
- What is the purpose of render method of react-dom?
	we use the function to render a React element into the DOM.
	it return a reference to the component. 
	If the React element was previously rendered into the container,
	it will perform an update on it
# JSX
- ##### Whta is JSX?
	we can define a tree 
	with various syntax and ways like objects and array
	
	but we frontend developers use markup, html, to define a DOM tree.
	so we are familiar with using markup when it comes to defining a tree
	
	React is all about dealing with Trees
	React deals with DOM tree and Fiber Tree
	we developers deal with React element tree
	we can create a React element using a function provided by React
	but it would be nice if we had a way to deal with Tree in a easier and familiar way 
	
	so JSX came in,
	We can think of JSX as an extension to the JS syntax.  
	we use JSX to define a tree data structure.
	
	in other words,
	we can use JSX to define a react element tree.  
	we can make use of JS functions instead of JSX  
	but JSX provides a more intuitive syntax  
	that is easier for developers to use  
	  
	JS engine itself dose not understand JSX 
	since it is an extension, and not a part of JS itself,  
	  
	so instead we have a preprocessor (or transpiler like Babel) 
	to covert our JSX code into standard JS code
	
	so as i said, JSX is a way of defining tree data structures using markup as a part of a js file 
	So that means other libraries and frameworks can also choose to use JSX as well
- ##### What is React.Fragment(JSX Fragment)?
	so we can return Strings, Numbers, Booleans, null, undefined and Arrays of React Elements in a component
	
	but when it come to React elements
	we cannot return multiple elements
	we can only return a single element
	
	so if we want to return multiple elements, 
	we need to wrap them with a single parent element
	  
	we can use div for it
	but actually it is discouraged to use div
	div has no meanings at all
	div is the last thing we frontend developers want to use
	also extra div can affect CSS styling.
	  
	so instead we can use JSX Fragment(React Fragment),  
	JSX Fragments don't create a new DOM element to group elements
	so it dose not hurt the styling 
	or add unnecessary complexity to our component tree
- JSX Expression / Primary Expression
	we can inject the actual JS code inside of JSX 
	Using curly braces
- What is transpiler?
	transpiler 
	converts 
	the text of code written in one syntax 
	into a different syntax that dose the same thing.
	
	we use trasnpiler to help ourselves
	to convert code that is easier for us to read and write 
	into something that JS engine understands
	
	JSX is one of the examples,
	we can use JSX to define a react element tree.  
	we can make use of JS functions instead of JSX  
	but JSX provides a more intuitive syntax  
	that is easier for developers to use  
	
	JS engine itself dose not understand JSX 
	since it is an extension, and not a part of JS itself,  
	  
	so instead we have a preprocessor (or transpiler like Babel) 
	to covert our JSX code into standard JS code
# ==Fiber/Reconciliation/Rendering==
- ##### What is DOM Tree?
	so we define a web page by documents, a markup, HTML
	and browser converts the HTML, document, into a collection of objects.
	that is DOM.
	
	DOM represents HTML elements that define a web page.
	
	we can use DOM tree to interact with what users see on the screen.
- ##### What is a React element?
	React element is an object
	this object has a type
	the type represents the real DOM element,
	or the type could be a function, a component, that returns more React elements when called.
	
	React element is much lightweight compared to the real DOM element,
	(it has less properties and methods)
	
	so we can think of React element 
	as a object that represents a real DOM element.
- ##### What is a React element tree?
	we can think of a React element tree 
	as a collection of React elements, objects,
	Like how DOM tree is a collection of DOM elements.
	
	React wants the developers work with a React element tree instead of the real DOM tree
	
	so that we can focus on managing states of the system, the user interface
	not so so much focus on how and when to update the interface step by step
	
	so we deal with managing states of the system
	and React deals with the actual DOM tree and how to update the tree in the most efficient way
	
	So we use a React element tree to express what we want the DOM to look like
	
	then, React looks at the React element tree and DOM tree
	to update DOM in the most efficient way possible.
	it it called reconciliation
	
	reconciliation is about traversing a tree
	React traverses trees and compare them 
	by the end of tree traversing,  
	React knows how the DOM tree should look like and the minimal set of changes to update DOM tree
	so a renderer like react-dom or react-native applies the changes to update the UI
- ##### What is reconciliation?
	so React really cares about how to update DOM in the most efficient way
	reconciliation is one of the things that React really cares about.	
	
	reconciliation is about traversing a tree
	React traverses trees and compare them 
	by the end of tree traversing,  
	React knows how the DOM tree should look like and the minimal set of changes to update DOM tree
	so a renderer like react-dom or react-native applies the changes to update the UI
- ##### ==What is Fiber Tree?==
	React deals with 3 trees
	
	a DOM tree
	DOM tree is a collection of DOM elements.
	we can use DOM tree to interact with what users see on the screen.
	
	a React element tree 
	React element tree is a collection of React elements, 
	React element is an object
	this object has a type
	the type represents the real DOM element,
	or the type could be a function, a component, that returns more React elements when called.
	
	React wants the developers work with a React element tree instead of the real DOM tree
	because React wants to handle updating DOM while we focus on managing states of the system
	So we use a React element tree to express what we want the DOM to look like
	
	
	a Fiber Tree
	
	so React really cares about how to update DOM in the most efficient way
	reconciliation is one of the things that React really cares about.	
	
	reconciliation is about traversing a tree
	React traverses trees and compare them by the end of tree traversing,  
	React knows how the DOM tree should look like and the minimal set of changes to update DOM tree
	so a renderer like react-dom or react-native applies the changes to update the UI
	
	So it is really important for React to have a fast and efficient traversal algorithm
	
	React uses the Fiber Tree as part of its reconciliation process.
	Fiber Tree consists of Fiber Nodes, Fiber Node is an object  
	Fiber tree is not destroyed nor re-created unlike React element tree, it is updated.
	
	So React uses Fiber Node to store data as props, states and a reference to the corresponding DOM element  
	  
	Fiber Node have two states, current and work-in-progress
	so Fiber Node is either current or work-in-progress
	the current essentially matches the current state of the DOM
	the work-in-progress matches the latest state of the React element tree
	
	so we can say that 
	React takes the branches of the React Element Tree that have changed
	and attaches them to the Fiber Tree as a work-in-progress branch.
	and both current and work-in-process nodes have a reference to one another as an alternative.
	
	so React can jump back and forth between them when comparing them.
	React can discover what changes are made by comparing the current and work-in-progress.  
	  
	React also reuses the old current after it discovers all the changes, React swaps workInProgress and current  
	so, workInProgress becomes current and current becomes workInProgress.  
	
	so Fiber Node helps React traverse trees
	but not only that it also helps React to split the rendering work 
	
	actually React used to have a stack reconciler before Fiber
	it worked well but it caused frames to drop  
	
	In a UI, actually it’s not necessary for every update to apply immediately.  
	different types of updates have different priorities	
	For example, 
	an animation should be updated faster than static and textual content.
	
	but stack reconciler recursively traverses the tree on the execution stack.
	the work could not be split.
	so basically Stack reconciler tried to do so much work at once without prioritizing them.  
	  
	so if the React renderer takes more than  
	frame rate, the time interval that devices refresh their screens,  
	to render something on the screen  
	the browser dropped that frame.
	  
	Fiber came into play solves such problems 
	Fiber can assign priority to different types of work
	Fiber can pause work and come back to it later or abort work if it’s no longer needed  
	
	Fiber Tree is a singly-linked list
	Fiber engine doesn’t perform recursive traversal on the Fiber Tree, like Stack reconciler did
	Instead, it performs a parent-first, depth-first traversal.  
	parent-first means that 
	we start at the root of the tree and works its way down to child nodes. 
	and parent node is processed before its children
	Depth-first means that 
	the traversal goes as deep as possible down one branch of the tree before backtracking
	
	so react actually can split the work using the traversal algorithm
	and the work is actually split by nodes.
	so we can actually think Fiber Node is a unit of work.  
	
	So basically React executes Fiber Node, the unit of work  
	React has an internal timer for frame rate.  
	and when the frame time runs out,
	
	React pauses executing the Fiber Node, the current unit of work,  
	and lets the browser render whatever is finished at that point.
	
	Then, in the next frame,  
	React picks up where it left off and continues traversing the tree.  
	Then, when it has enough time,  
	it commits the workInProgress tree and completes the render.
- ##### What is Fiber engine?/ Fiber reconciliation algorithm?
	Fiber is an engine, a reconciler inside React
	Fiber is responsible for reconciliation  
	
	so React really cares about how to update DOM in the most efficient way
	reconciliation is one of the things that React really cares about.	
	
	reconciliation is about traversing a tree
	React traverses trees and compare them by the end of tree traversing,  
	React knows how the DOM tree should look like and the minimal set of changes to update DOM tree
	so a renderer like react-dom or react-native applies the changes to update the UI
	
	So it is really important for React to have a fast and efficient traversal algorithm
	
	React uses the Fiber Tree as part of its reconciliation process.
	Fiber Tree consists of Fiber Nodes, Fiber Node is an object  
	Fiber tree is not destroyed nor re-created unlike React element tree, it is updated.
	
	So React uses Fiber Node to store data as props, states and a reference to the corresponding DOM element  
	  
	Fiber Node have two states, current and work-in-progress
	so Fiber Node is either current or work-in-progress
	the current essentially matches the current state of the DOM
	the work-in-progress matches the latest state of the React element tree
	
	so we can say that 
	React takes the branches of the React Element Tree that have changed
	and attaches them to the Fiber Tree as a work-in-progress branch.
	and both current and work-in-process nodes have a reference to one another as an alternative.
	
	so React can jump back and forth between them when comparing them.
	React can discover what changes are made by comparing the current and work-in-progress.  
	  
	React also reuses the old current after it discovers all the changes, React swaps workInProgress and current  
	so, workInProgress becomes current and current becomes workInProgress.  
	
	so Fiber Node helps React traverse trees
	but actually Fiber Node is much useful than that, it helps React to split the rendering work 
	
	actually React used to have a stack reconciler before Fiber
	it worked well but it caused frames to drop  
	
	In a UI, actually it’s not necessary for every update to apply immediately.  
	different types of updates have different priorities	
	For example, 
	an animation should be updated faster than static and textual content.
	
	but stack reconciler recursively traverses the tree on the execution stack.
	the work could not be split.
	so basically Stack reconciler tried to do so much work at once without prioritizing them.  
	  
	so if the React renderer takes more than  
	frame rate, the time interval that devices refresh their screens,  
	to render something on the screen  
	the browser dropped that frame.
	  
	Fiber came into play solves such problems 
	Fiber can assign priority to different types of work
	Fiber can pause work and come back to it later or abort work if it’s no longer needed  
	
	Fiber Tree is a singly-linked list
	Fiber engine doesn’t perform recursive traversal on the Fiber Tree, like Stack reconciler did
	Instead, it performs a parent-first, depth-first traversal.  
	parent-first means that 
	we start at the root of the tree and works its way down to child nodes. 
	and parent node is processed before its children
	Depth-first means that 
	the traversal goes as deep as possible down one branch of the tree before backtracking
	
	so react actually can split the work using the traversal algorithm
	and the work is actually split by nodes.
	so we can actually think Fiber Node is a unit of work.  
	
	So basically React executes Fiber Node, the unit of work  
	React has an internal timer for frame rate.  
	and when the frame time runs out,
	
	React pauses executing the Fiber Node, the current unit of work,  
	and lets the browser render whatever is finished at that point.
	
	Then, in the next frame,  
	React picks up where it left off and continues traversing the tree.  
	Then, when it has enough time,  
	it commits the workInProgress tree and completes the render.
- ##### Rendering in React? / Rendering phases
	Rendering in React has 2 phases
	
	1.render/reconciliation phase
	
	reconciliation is about traversing a tree
	React traverses trees and compare them by the end of tree traversing,  
	React knows how the DOM tree should look like and the minimal set of changes to update DOM tree
	
	2.commit phase
	
	By the end of the reconciliation,  
	so a renderer like react-dom or react-native applies the changes to update the UI
	
	that is the commit phase
- ##### Lifecycle of components / Mounting, updating and unmounting?
	Components go through various lifecycle phases
	Mounting, updating and unmounting
	
	Mounting,
	when component' corresponding DOM nodes get attached in the DOM tree for the first time.
	we say component is mounted.
	it is mounting phase.
	
	updating,
	when there are changes in a component because of states or props
	React reflects the changes in the DOM accordingly
	it is updating phase.
	
	Unmounting,
	when component is removed from the latest state of React element tree
	the corresponding Dom nodes are removed, 
	then we cay say the component is unmounted.
	
	but unmounting dose not necessarily mean that the DOM nodes will also be removed.
	it really depends on reconciliation process, the Fiber engine and Fiber Tree
	if another added component returns very similar looking structure.
	the DOM elements dose not get removed.
	because React's job is to find the smallest set of changes to update DOM
- ##### Explain lifecycle methods?
	when it comes to class components,
	class components have lifecycle methods, they belong to one specific phase,
	in each phase, React calls lifecycle methods that belong to the phase.
	we can implement such methods to manage states across lifecycle of a class components
	
	constructor  
	This is the first method called when an instance is created in the mounting phase
	we usually initialize state here
	
	shouldComponentUpdate
	this method is called before a component re-renders.
	we can tell React if the component should be updated or not based on its new props and state 
	we use such method to prevent unnecessary re-rendering  
	
	componentWillUnmount  
	This method is called just before a component is removed from the DOM.  
	to clean up resources like event listeners
- ##### ==What is Virtual DOM?==
	The virtual DOM (VDOM) is a general programming concept  
    The virtual DOM is the representation of a UI  
    The virtual DOM is synced with the “real” DOM  
      
      
    Virtual DOM is more of a pattern/concept than a specific technology  
      
    But, when it comes to React,  
    Virtual DOM is usually associated with [React elements](https://legacy.reactjs.org/docs/rendering-elements.html) since they are the objects representing the user interface.  
      
    however,  
    Fiber Tree also holds additional information about the React Element tree such as props and states and so on  
      
    They can also be considered a part of “virtual DOM” implementation in React.
# State
- ##### ==What is State?==
	State is data that represents the current state of the system.
	we can say that UI reflects the state of the system
	
	states are usually fully controlled by the component  
	it is not accessible to any other component 
	till the owner component decides to pass it.
	the state changes over the lifecycle of the component
	whenever the state changes, the component re-renders
- ##### Types of States?
	local state
	local state is specific to a particular component
	states are fully controlled by the component  
	it is not accessible to any other component 
	till the owner component decides to pass it.
	
	global state
	global state is shared across multiple components
	
	user authentication status, user preferences, and data fetched from APIs that multiple components need to access.
	they can be treated as global states
- ##### How do we manage states in React?
	in case of local states,
	functional components	use hooks to manage states
	class components handle states with this this keyword and lifecycle methods
	
	when comes to global state,
	we make use of state management libraries such as Recoil
- ##### When do we use state management libraries?
	when it comes to global states
	we make use of state management libraries such as Recoil
	
	we usually use state management libraries for 2 reasons
	
	when we want to share states across multiple components without them being related in the component tree.
	when data flow gets complex that we need to simplify it
	
	also when we asynchronously fetch data
	they provide useful functionalities such as caching and good error handling
- ##### What is Recoil?
	it is a state management library.
	Recoil is simple to use and intuitive to manage and share state.
	 
	Recoil optimizes re-renders
	it tracks dependencies between components and state atoms.
	so that only the components affected by state changes are re-rendered.
- How can we keep the immutability of State?
	avoid mutating the object 
	create a new object and make changes to the object
	
	spread operator or array methods are useful 
- How dose React know when there is a change in states?
	React shallowly compares two objects 
	so React compares references instead of contents
	if the objects have the different reference
	React thinks the state is changed.
# Component
- ##### ==What is a component?==
	component is a function
	that returns React elements
	Component is a building block for the React application  
	Components have their own props, state, and lifecycle  
- ##### What is the difference between React element and Component?
	React element is an object
	this object has a type
	the type represents the real DOM element,
	or the type could be a function, a component, that returns more React elements when called.
	
	React element is much lightweight compared to the real DOM element,
	(it has less properties and methods)
	
	so we can think of React element 
	as a object that represents a real DOM element.	
	
	on the other hand,
	
	component is a function
	that returns React elements
	Component is a building block for the React application  
	Components have their own props, state, and lifecycle  
# Props
- ##### What is pure function?
	pure functions are functions 
	that do not have side-effects outside of themselves
	and always return the same output with the same input
- ##### What is Props?
	we can think of Props as an argument passed to a component.
	we pass data from a parent component to a child component using the object, props.
	props can be used to configure the behavior of a component
	
	Props is immutable, read-only
	
	React application is built on top of components, and they are functions, 
	there are class components but class is also essentially a function in JS.
	as one of the evidences if we make a class and use typeof operator it says it is indeed a function, the same result with instanceof operator.
	
	and there are two types of functions, pure functions and impure functions.
	
	Pure functions are much predictable and reliable than impure functions.
	they do not have side-effects outside of themselves
	they always return the same output with the same input
	
	so if our application is going to be built on top of functions
	React want the functions to be pure 
	because React want our application to be predictable and reliable
	
	so React has a few features that help us our functions to stay pure
	one of them is freezing the props object.
	because pure functions do not have side-effects, so they do not change the values outside themselves.
	
	but if we de-structure the values out of the props object
	we are basically assigning the value to another variable
	and we can change the newly created variable
- ##### difference between props and states?
	State is data that represents the current state of the system.
	we can say that UI reflects the state of the system
	
	states are usually fully controlled by the component  
	it is not accessible to any other component 
	till the owner component decides to pass it.
	the state changes over the lifecycle of the component
	whenever the state changes, the component re-renders
	
	on the other hand,
	
	we can think of Props as an argument passed to a component.
	we pass data from a parent component to a child component using the object, props.
	props can be used to configure the behavior of a component
	
	Props is immutable, read-only
- ##### What is key props?
	key is a special prop
	we use key props when we deal with a list of elements.
	
	React uses key props to identify which items in a list have changed, added or removed.
	so we can say that key props acts as an identifier for an element.
	since it is an identifier, keys should be unique among its siblings.	
	
	React compares the previous list and the changed list
	React uses the same DOM nodes from the previous rendering when items have the same key, so that React dose not have to re-create the entire list
- ##### Why do we use key props?
	If we do not pass a key prop, React uses Index as a key prop
	
	but when React uses Index as a key, React cannot identify the changes correctly
	
	for instance, if we add an item at the beginning of the list
	now item that used to have 0 as a key has 1 as a key instead of 0
	the added item uses 0 as a key.
	so now key cannot act as an identifier anymore.
	
	React identifies items by key 
	So it thinks that the added item is same item at index 0 in the previous array
	So it uses the same DOM node from the previous rendering.
	Even tho it is newly added.
	and it thinks that the item at end of index is the added one.
	since this item uses index that is not recognized by React in the previous rendering
	
	so we are recommended not to use Index as a key prop
	we can only use index as a key
	when we are certain that the list will be static and never be re-ordered or filtered.
- ##### ==What is uni directional data?==
	Data can only move in one direction
	
	Data only moves down the tree
	Props are always passed down the tree not up to the tree
	
	Parent can give a child the ability to update data in the parent
	but its just giving the child a reference to something that parent owns.
	essentially, the data is uni directional, data lives in one part of the tree
	And are passed down to its children  
	
	since data only flows in one direction,
	it it much easier for us to predict and follow data flow.
	This is fundamentally how data flows in React.
- ##### What is Props Drilling?
	props drilling refers to a situation 
	where we have many nested components in between, we pass props down from a parent component to a child component.
	
	props drilling can make the code harder to read, maintain, and debug 
	since we have to pass props down manually at every layer and we need to track how props are being passed through multiple layers.
- ##### How do we solve Props Drilling?
	we can use Context API to share states across multiple components.
	
	or we can make use of a state manage libraries such as a recoil to manage states as a global state
## Context API
- ##### ==What is Context API?==
	we can use Context API to share stats across multiple components
	without having to pass states down manually at every level.
	we can use Context API to solve prop drilling
- ##### ==What is the disadvantages of Context API?==
	all components inside of Provider re-renders when the value props changes regardless of whether they use that specific value. 
	
	it might be confusing at first 
	because we say the children re-render when the value props changes even tho they do not use the props
	
	but actually it is wrong. 
	the children re-render because the parent re-renders, 
	so actually we can say that the components that use value props re-render 
	not necessarily because the props has changed 
	but because the parent component re-renders
	
	However, if we use context API over multiple layers
	so we might cause unnecessary re-renders in every layer
	
	to solve such a problem
	we can split contexts into smaller pieces
- ##### What is the difference between Context API and State management libraries?
	they look like they serve the same purpose
	they are essentially different, their focus is different
    
    Context API is about sharing states across multiple components
    Context API has nothing to do with managing states, we essentially manually manage the states using Hooks such as useState and useReducer
    
    on the other hand,
    
    State management libraries such as Recoil is focused on managing states in an efficient way
# Class Component
- ##### ==difference between Class Component and Function Component?==
	syntax is different
	
	we define functional components with function
	we define class components with class keyword, the component extends from React.component class.
	
	since class component extends from React.component,
	class components can implement lifecycle methods and manage states using this keyword.
	
	on the other hand,
	
	we cannot make use of lifecycle methods or this keyword in functional components 
	
	so that's how hooks came into play
	hook functions came into play to power up functional components.
	functional components were stateless.
	since it had no way to work with states
	
	but since the hooks
	now functional components have a way to manage states
	we can think hook functions powered up functional components to work with states.
- ##### What is HOC / Enhanced Component?
	A Higher-Order Component is a component that takes a component and returns a new component with enhanced functionality. 
	
	we can use such functions for many use cases such as Props manipulation and Render hijacking.
	we mostly use it to share common logic across components
	
	but then 
	we need to introduce unnecessary layers in our component tree.
	so it makes the component tree complex and harder to manage.
	
	since Hooks,
	we make use of custom hooks instead render-props pattern and higher oder functions to share common logic across components
- ##### What is render-props pattern?
	render-props pattern is
	a pattern for sharing code across components using a prop render

	the parent component pass a render function as a prop
	and the child component uses the function for rendering
	we do not have to the prop named render, tho it is convention
	function names can be anything as long as 
	the component knows what function to call for rendering
	we mostly use it to share common logic across components
	
	but then 
	we need to introduce unnecessary layers in our component tree.
	so it makes the component tree complex and harder to manage.
	
	since Hooks,
	we make use of custom hooks instead render-props pattern and higher oder functions to share common logic across components
- What is render hijacking in react?  
	we can control what a component will output  
	by wrapping the component with another one,
	we inject additional props or make other changes
	
	this is render hijacking  
	  
	we can use higher order components for render hijacking  
# Hooks
* ##### What is a Hook? / Rules for using Hooks? / Reasons behind the rules? / What if we do not follow the rules?
	when we talk about hook, 
	we usually refer to the hook functions provided by React.
	
	hook functions came into play to power up functional components.
	functional components were stateless.
	since it had no way to work with states
	
	but since the hooks
	now functional components have a way to manage states
	we can think hook functions powered up functional components to work with states.
	
	hook functions create objects called hook instances, hooks
	States are stored in the hooks
	and Hook is stored in the corresponding Fiber Node
	
	React element tree keep being re-created and destroyed
	Fiber tree is not destroyed nor re-created unlike React element tree, it is updated.
	React stores states on Fiber Node where more persistent throughout updates.
	
	since it is an object, hook has its own properties such as state and next	
	Next is actually a reference to the next Hook in a component
	Each hook points to the next hook
	so it is actually a linked list attached to a Fiber Node
	
	actually there are a few rules associated with hooks
	
	first,
	we should not call hook functions inside conditionals or loops, we can only call them at the top level, because order of execution of hooks matter
	
	this rule might seem odd at first but
	
	we can actually understand why the order of execution of hook functions matters
	once you understand Hooks are stored as a linked list on the Fiber Node
	
	when we traverse a linked list, order is really important, 
	
	for example,
	if we wrap our hooks inside a condition, 
	we might have different number of hooks and different order on re-render.
	and that means that we can miss or skip a node on our linked list
	so React cannot reference the correct hook when React traverses the liked-list
	
	so we always want to call hooks at the top level
	
	and we can only use hooks inside a functional component
	
	this rule also makes sense, 
	since Hooks are stored inside the Fiber Node  
	so Fiber Node represents either the current state of the DOM or the latest state of the React element tree
	React uses the Fiber Tree as part of its reconciliation process.
	so it would not make any sense to use hooks somewhere else 
	
	also it makes sense to use them only inside functional components
	since hook functions came into play to power up functional components to be stateful.
- ##### What is a custom hook?
	custom hook is a hook built by developers
	it is a function, name starts with `use` 
	
	we crate custom hooks
	to abstract complex stateful logic and keep them in one place
	and reuse the code across multiple components.
	
	many libraries make use of custom hooks to share code such as React Query
	
	and custom hooks made it easy for us to share logic across components.
	
	before hooks,
	we made use of render-props pattern and higher order components to share logic across components
	
	but then 
	we needed to introduce unnecessary layers in our component tree.
	so it made the component tree complex and harder to manage.
- What is React Query?
	React Query is a library 
	it helps us to simplify complex data management tasks
	
	React Query provides a set of hooks to help us 
	with fetching, caching, synchronizing, and updating data
	
	`useQuery` to fetch data from APIs
	`useMutation` to perform mutations.
	
	React Query automatically stores and invalidates data 
	and Cached data can be reused across components 
	so we do not need a global state management libraries to manage data
	
	The library automatically synchronizes data in the background 
	so that the cached data is always up to date
	and we do not have to manually re-fresh data
- ##### What are the positive changes since the React Hook?/ What are the advantages of Hooks?
	hook functions came into play to power up functional components.
	functional components were stateless.
	since it had no way to work with states
	
	but since the hooks
	functional components have a way to manage states
	we can think hook functions powered up functional components to work with states.
	
	in a class component,
	we make use of lifecycle methods for managing states
	so we have to split the logic across lifecycle methods 
	so the unrelated logic often ends up being placed together.
	
	But, with Hooks,
	we can actually organize related logic in one place
	we can make our own custom hooks, and keep related logic inside
	and custom hooks made it easy for us to share logic across components.
	
	before hooks,
	we made use of render-props pattern and higher order components to share logic across components
	
	but then 
	we needed to introduce unnecessary layers in our component tree.
	so it made the component tree complex and harder to manage.
- ##### ==Do Hooks cover all use cases for classes?==
	React Docs say that there are some of lifecyce methods that hooks can’t cover
	
	getSnapshotBeforeUpdate, getDerivedStateFromError, componentDidCatch
	
	but hooks can cover most of use cases
	also we can use useEffect to mimic the behavior of lifecycle methods in class components.
- ##### How can you mimic lifecycle methods of a class component in a functional component?
	we can make use of useEffect Hook
	
	Components have are 3 phases, mounting, updating and unmounting.
	
	a callback passed to an useEffect hook always runs in the mounting phase.
	depending on the dependency array given, 
	the callback runs in the updating phase.
	lastly, cleanup function always runs in the unmounting phase.
	
	we can mimic lifecycle methods of a class component using such feature.
- What is side effects in a component?
	side effects are tasks that have nothing to deal with rendering 
	such as data fetching, setting up document title, manipulating DOM
- the difference between useEffect and useLayoutEffect?
	we use them to handle side effects in functional components.
	
	they differ in terms of when they are executed and how they can impact the rendering process.
	
	`useEffect` callback is executed asynchronously after the rendering.
	
	on the other hand,
	
    `useLayoutEffect` callback is executed synchronously immediately after the rendering but before the browser paints the screen. 
     we use `useLayoutEffect` when we handle synchronous side effect that interacts with the layout, like measuring DOM elements.
     
    `useEffect` runs asynchronously so it dose not affect rendering performance
    but `useLayoutEffect` runs synchronously before the browser paints the screen so it can affect rendering performance if the side effect is time-consuming.
- What is useRef?
	`useRef` is a Hook
	
	we make use of the hook to create a reference to a DOM element or any other value. 
	
	we can get a reference to a DOM element and access and interact with DOM elements directly
	
	we can control user-given inputs with such a hook as well
- What is Portal?
	we make use use of a portal 
	to render a component inside other DOM node than the parent component
	
	Portals can be useful when it comes to modals, dialogs and tooltips
- ##### When do we use useState and useReducer?
	Both are used to manage states in functional components.
	
	we useState to manage simple states
	useReducer to manage complex states with complex logic
	
	for example,
    when we manage primitives useState is good enough  
    when we mange Object or array, reducer can be better  
      
    when we have multiple state transitions 
    which means when we have complex logic for updating states  
    useReducer is a good choice  
    since we can keep all the related logic in one place.
- ##### Why do we use setState instead of directly mutating the state?
	If we update states directly, the UI dose not get re-rendered.   
	setState signals to React that the state has changed,  
	Without setState, React doesn't know the state is changed.
- ##### What are the properties of setState 
	If we update states directly, the UI dose not get re-rendered.   
	setState signals to React that the state has changed,  
	Without setState, React doesn't know the state is changed.
	
    React group multiple setState calls into a single update for better performance if possible
    this minimizes unnecessary re-renders.  
    
    we can think that setState is like sending a request than an immediate command. 
    so the state may not change immediately after setState() is called. 
    so when updating a state depends on the previous state  
    we better make use of a updater function
- ==Types of Hooks?==
	useState to manage states
	
	useReducer to manage complex states with complex logic
	
	useEffect to handle side effects such data fetching and event handlers 
	or to mimic the behavior of lifecycle methods in class components.
	
	useRef to create a reference to a DOM element or any other value.
	
	useMemo to memoize a value from heavy computation
	
	useCallback to memoize a function so that we can reuse the function
	
	useLayoutEffect, similar to useEffect,
	but it runs synchronously immediately after the rendering but before the browser paints the screen. 
	we use `useLayoutEffect` when we handle synchronous side effect that interacts with the layout, like measuring DOM elements.
     
	useContext to access to the context values defined by a Context Provider.    	
# CSR
- ##### ==What is SSR?==
	SSR stands for Server-Side Rendering
	
	basically rendering happens on the server-side
	when a user requests a web page, we render a web page on the server and send the fully rendered HTML to the clients
	
	it has a few advantages compared to CSR
	
	for example,
	user experience can be very different depending on the devices when it comes to CSR
	because rendering on browser side can be resource-intensive, not all of devices can handle such tasks
	but if server renders a page, all of users can have consistent user experience regardless of its devices
	
	also Search engines can easily crawl web pages 
	since browsers receive a fully constructed HTML page from the server in the initial response
- ##### ==What is CSR?==
	CSR stands for Client-Side Rendering, 
	
	basically rendering happens on the client-side
	when a user requests a web page, the browser renders the web page.
	the server initially sends a minimal HTML page along with JavaScript and other assets, and browsers use such resources to dynamically render pages
	
	it has a few advantages compared to SSR
	
	for example,
	
	users can have a smoother and more interactive user experience once the page is loaded. 
	Users can navigate between pages without page being fully reloaded
	
	also CSR can reduce server load. the server doesn't need to pre-render HTML for each page request.
- ##### ==What is Client-Side-Routing?==
	basically, we handle navigation within a browser on the client side
	
	Instead of sending a request to the server for each page change, 
	the application uses JavaScript to manage navigation transitions.
	
	this way, users can have a smoother and more interactive user experience since Users can navigate between pages without page being fully reloaded
	
	one challenge is that search engines cannot index the URLs since changes to the URL don't necessarily result in a new request to the server.
- ##### ==What dose `react-dom/server` package do? / What are `react-dom/server` APIs for?==
	The react-dom/server APIs helps us to render React components on the server.  
	we use such APIS to to generate the initial HTML.  
	we do not often use such API directly
	Frameworks such as Next.js and Remix make use of such APIs  
- ##### ==When do you use hydrateRoot?==
	We can use hydrateRoot  
	to display React components inside a browser DOM node whose HTML content was previously generated (on the server side) by react-dom/server.
	
	(React will attach to the HTML that exists inside the domNode,  
	and take over managing the DOM inside it.  
	hydrateRoot() expects the rendered content to be identical with the server-rendered content.)  
- ##### ==What is hydration?==
	hydration is the process of converting pre-rendered HTML from the server into a fully interactive application.  
	
	So first, 
	
	the server sends the fully rendered HTML to the client, this is called server-side rendering.  
	After the initial server-side rendering, when the page reaches the client-side (browser).  
	React needs to take over to make the page interactive.  
	So React will "hydrate" the HTML sent by the server,  
	by attaching event listeners and setting up the virtual DOM to manage updates.  
	
	This approach combines the benefits of both server-side rendering and client-side rendering.
- ##### ==What is Hydration mismatch?==
	hydration mismatch refers to a situation  
	when we have a mismatch between the server-rendered HTML and the client-
	side rendered content during the hydration process.
	
	This can lead to unexpected errors  
	for examples, event handlers can get attached to the wrong elements.
	
	So we need to fix them by finding the reasons behind
	
	Hydration mismatch often happens  
	when we use browser-only APIs in rendering logic.
	Or when we use browser-environment-specific checks (e.g. typeof window !== 'undefined’) in rendering logic.  
	or when we render different data on the server and the client.
# Controlled and uncontrolled components
- ##### What is Controlled components?
	In controlled components, 
	
	the form elements such as input fields are controlled by React state.
	we can say we control the user-given input/value through the state.
	
	every time value changes, the state changes.
	so when we need to filter values 
	or we need to make a change to the user interface based on the value
	
	we use controlled components.
- ##### What is Uncontrolled components?
	In uncontrolled components, 
	the form elements are not directly controlled by React state.
	the value of the input element is handled by the DOM itself.
	To access the value of the input element, 
	we can use useRef hook to get a reference to the form element
	
	so when we do not need to filter the value, every time value changes.
	or when user interface dose not depend on the value, 
	we can avoid unnecessary re-renders 
	by getting a reference to the form element instead of directly managing the value through state
- What is the difference between controlled and uncontrolled components?
# Memoization
- ##### ==What is Memoization in React?/ How Memoization work in React?==
	Memoization is a technique to optimize the performance of a component 
	
	React cache the results of expensive calculations 
	and reuses the results when the component re-renders with the same dependencies
	
	we can avoid unnecessary recalculations
	this can improve the rendering performance
	
	we can use useMemo and useCallback hooks to memoize values and functions.
	
	we do not have to worry about stale cache 
	since React ensures that cached results are only used 
	when the given dependencies are not changed.
- ##### What is useMemo?
	useMemo caches a result of expensive operations 
	such as time-consuming and resource intensive operations 
	
	React reuses the result if items in the given dependency array did not change.
- ##### What is useCallback?
	useCallback caches a function
	so that we do not re-create the same function 
	every time component re-renders
	
	when we pass a function to an optimized child component
	every time the parent component re-renders, we also re-create functions
	so when we pass a function as a prop and it leads to re-rendering of a memoized child component as well.
	
	in such cases, we can use useCallback to prevent unnecessary re-renders.
	
	so that React reuses the same function if items in the given dependency array did not change.
- ##### What is the difference between useMemo and useCallback?
	they both are used to cache values
	but what they cache is different.
	useMemo caches a result of expensive operations 
	useCallback caches a function.
- ##### What dose `shouldComonentUpate` method do?/ `PureComponent` / `React.memo`
	The `shouldComponentUpdate` method is a lifecycle method
	
	the method is called before a component re-renders.
	we can tell React if the component should be updated or not based on its new props and state 
	we use such method to prevent unnecessary re-rendering  
	
	But incorrect implementations can lead to bugs and unexpected behavior.
	
	so instead of implementing the method on our own,
	
	we can use `PureComponent`
	`PureComponent` extends from `Component` class
	and it implements `shouldComponentUpdate`
	
	the method shallowly compares the states and props
	and return true only when there is a change.
	so that when there is no changes the component will not re-render.
	
	but React recommends functional components over class components
	so we can use React.memo API to achieve the same thing
	we wrap a functional component with memo API
	This API prevents unnecessary re-rendering by shallowly comparing the previous props and new props.
- ##### What are the differences between `PureComponent` and `Component`?
	Both are classes
	and we use both classes to create a class component
	but `PureComponent` class is more optimized for re-rendering performance
	
	`PureComponet` is a subclass of `Component`
	and the class implements `shouldComponentUpdate`
	
	the method is called before a component re-renders.
	we can tell React if the component should be updated or not based on its new props and state 
	we use such method to prevent unnecessary re-rendering  
	
	But incorrect implementations can lead to bugs and unexpected behavior.
	
	so instead of implementing the method on our own,
	
	we can use `PureComponent`
	the method shallowly compares the states and props
	and return true only when there is a change.
	so that when there is no changes the component will not re-render.
# Event Handling
- ##### Event Bubbling , Event Capturing and Event Propagation
	Event Propagation is about how event are passed through the DOM tree
	
	there are two phases in the Event propagation
	Event Bubbling and Event Capturing
	
	Bubbling is about how event is passed up to the parent element from the child element
	
	Capturing is about	how event is passed down to the child element from the parent element
- ##### Event Delegation
	Assigning an event handler to a parent element
	so that parent element can handle events from the children
- ##### Event handling in React
	React manages events using event propagation
	
	React puts a single listener on the root element
	it puts a listener on root even tho it can put the listener higher up 
	in case we have multiple roots on a single page
	
	now the event listener is responsible for dealing with all of the events happening inside of our root element. 
	every event inside of our root element is passed up to the root element
	
	we  developers deal with react elements instead of real DOM elements
	we cannot attach event handlers to the real DOM element instead we attach event handlers to react elements
	
	so React delegates all those functions to the single event listener to handle.
	
	when we define a function
	We do not have to do anything special to tell React what the target element is 	
	the event listener on the Root element knows what function to call when event happens
	
	and React also mimics event propagation like bubbling
	it means that 
	we can delegate event handlers to a parent react element 
	to handle event from children.
	
	This makes us think like if events bubble up to the parent React element.
	Even though, in reality, they are bubbled up to the root element and managed at the root element.
- ##### What is Synthetic event object in React?
	synthetic event is an object 
	we can think of it as a wrapper that wraps the browser's native event object
	
	Different browsers deal with events differently
	Event objects have differently named properties and methods.
	So react generalizes the way we deal with Event in browsers 
	by wrapping a native event with synthetic event object.
	
	So that our code always works.
# React 18
- ##### ==What is React.StrictMode? why dose it render twice?==
	`React.StrictMode` is a tool(component) in React
	it helps us 
	to catch and identify potential issues 
	in the application during the development process. 
	
	For instance,  
	Certain lifecycle methods are deprecated and they are considered unsafe
	With StrictMode, React gives a warning  
	if any of the class components use unsafe lifecycle methods
	
	also, 
	it invokes certain functions and component methods twice. 
	this way, 
	it can identify components with unintentional side-effects
	and it checks if the components don't produce the same output on each render
	
	`React.StrictMode` is used in development process 
	to catch and identify potential issues 
	so they don't impact the performance of your production application.
- ##### ==What are the features of React 18?==
	**Concurrent rendering.**

	React now renders concurrently in the background without blocking the main thread.  
	This means that the UI can continue to respond to user input in the middle of a large rendering task  
	  
	**Automatic batching**
	
	React groups multiple state updates into a single re-render  
	this is called automatic batching.  
	  
	Before 18, updates were only batched inside React event handlers.
	But now updates inside promises, setTimeout, native event handlers, and other events are also batched automatically.  
	This helps to optimize the performance  
	since React effectively reduces the number of unnecessary re-renders
- ##### What are the new hooks of React 18?
	useTransition() and useDeferredValue() are new hooks
	we use such hooks  
	when state updates are not urgent,  
	so that we want to give other state updates more priority  
	  
	we can say direct interaction, what the user is interacting with, such as typing, clicking, pressing are urgent.  
	
	for example, 
	lets say user is online shopping  
	when the user changes quantity and size  
	user expects the changes to be reflected right away  
	so it is urgent.  
	but when user adds the product to the cart
	Maybe user will not pay so much attention to the cart right away  
	so we can say it is less urgent.
	
	we can mark less urgent state updates using such hooks
	
	With useTransition,  
	We wrap state updates inside the given function by the hook
	we are marking them as less urgent updates
	So that other urgent state updates can take priority in the rendering timeline.
	
	useDeferredValue is similar,  
	but we use useDeferredValue mostly when we deal with third-party libraries  
	we sometimes don’t have control over the corresponding setState call  
	we can pass setState as a prop if it was our code  
	but maybe the state came from a third-party library.  
	so third party library handles the state update  
	This is when **useDeferredValue** can be used.
	we wrap the value inside the hook.
# Additional
- ##### ==What is webpack?==
	Webpack is a module builder
	so Webpack is used to bundle multiple modules, scripts, and assets 
	into a single or multiple output files
	so we only need Webpack during development.
	
	web applications usually have several different script and libraries, 
	and these libraries may have dependencies on other libraries. 
	so we not only need to load these scripts 
	but also load them in the right order	
	
	Webpack can help us with the bundling process 
	webpack analyzes the dependencies of modules and 
	generates efficient bundles that load in the correct order. 
- ##### What is Babel?
	Babel is a JavaScript transpiler. 
	
	Not every browser supports modern JavaScript,
	older web browsers or environments, 
	they do not support the latest language features.
	
	so we have transpiler such as Babel that helps us with such problems.
	so Babel converts modern JavaScript code 
	into a backwards-compatible version of JavaScript
	so that we can execute our code in such old browsers.
	
	also Babel can help us with converting JSX into JS code
	so that we can use a markup language inside JS files
	even tho JS engine dose not support JSX, since JSX is not a part of JS, or ECMASCript
	Babel transpiles JSX into JS code that JS engine understands.
- ##### What is Suspense?
	it is a component by React
	we can such a component to wrap asynchronous components
	such lazy-loading components or when fetching data
	this component allows us to have a fallback UI 
	to display while the component is loading,
	
	this allows us to separate the loading phase and the actual content,
	this helps us to have more organized code.
- ##### ==What is import(), what is lazy()?==
	we use import to dynamically load modules
	dynamic import enables code splitting and lazy loading
	
	lazy loading mean that we do not load the module until we actually use it

	When static import is slow and it increases the memory usage, and it is less likely that we will need the code
	then we use lazy loading
	
	we can think Lazy loading is a part of code splitting. 
	the code is already split by logic, 
	so we want to split how we are going to load the code
	so we load things when they are needed. 
	In this way, we can improve performance. 
	
	Although the overall amount of loading time may be the same, 
	but the initial loading time can be improved
- ##### What is code splitting?
	Code splitting is a technique
	we split the code into smaller, more manageable chunks. 
	and we load those small chucks of code on demand, as needed
	so we split the code by logic
	and we split the loading process as well.
	
	code splitting has a few advantages
	
	since we only need the code that is needed during the initial loading
	loading speed is faster,
	
	and since the chucks are small
	It is easier for us to manage, update, and test specific parts of the application independently.
- ##### What is Error-boundary?
	When an error occurs in a React component, 
	it can propagate up the component tree, potentially leading to the entire application crashing. 
	
	Error boundaries can catch and handle errors at a higher level in the component tree.
	
	it displays a fallback UI instead of the component tree that crashed.
	
	preventing the application from breaking and allowing you to display a fallback UI or provide error information.
	
	
	A class component becomes an error boundary 
	if it defines a new lifecycle method called componentDidCatch(error, info) or static getDerivedStateFromError() :
# Testing
# Additional2
- ==What is Expo?==
	Expo is a React framework for building universal Android, iOS, and web apps.
- What are the different ways to style a React component?
	Inline Styling  
	JavaScript object
	CSS Stylesheet
- How to pass data between react components?
	Parent Component to Child Component (using props)
	props
	
	Child Component to Parent Component (using callbacks)  
	callbacks, children can pass data to parents
	parents pass setState functions down to children.
- What is Lifting State Up in React?
	When several components need to share the same data  
	we can lift the data up to their closest common ancestor.  
	instead of maintaining the state separately in both of the child components.
- Explain conditional rendering in React.
	Conditional rendering is about dynamically displaying different components based on conditions
	  
	We can use if-else conditional and switch statement
	
	since we can embed expressions in JSX,
	we can also use ternary operators, Logical AND(&&) operator
	or an object, we can map certain values to components.
- What is switching component?
	switching component manages rendering of different pages based on conditions.  
	we can use various techniques  
	such as conditional rendering and routing
	or an object, we can map certain values to components.
- What is React Router?
	React Router is a library for routing in React.  
	we can build a single-page web application in React.  
	with React Router, we can navigate pages without refreshing.  
	we can change the browser URL and keep the user interface in sync with the URL.
- **When to use a Class Component over a Function Component?**
	After Hooks,
	react docs recommends to use Function components over Class components. 
	But If we want to make use of functionalities that hook cannot cover yet
	we can use class component
- What is children prop?
	We can pass components as a prop to other components
	And it is called children.
	We put children between component's opening and closing tag  
	to pass components as children prop.
- Why React uses className over class attribute?  
	class is a keyword in JavaScript,  
	so React uses className as a property name instead of class.
- What are stateless components?
	If a component dose not have states  
	if a component is independent of states  
	it is a stateless component.  
	
	we usually use a functional component for creating stateless components.  
	In fact, before Hooks,  
	all functional components used to be called stateless  
	since they had no way to manage states,  
- What are stateful components?
	If a component dose have states
	if a component is dependent of states
	it is a stateful component. 
	
	Functional components and class components both can be stateful.
- How to apply validation on props in React?
	There is a library prop-types  
	it used to be part of React.  
	we can check all props that we set on components to make sure they have correct type
	
	If the type is incorrect, we get warnings
- What are the recommended ways for static type checking?/Does React Hook work with static typing?
	type-checking system is not mandatary in React.

	but it's common to use type checking tools, such as TypeScript
	it performs type checking at compile time
	we can avoid type-related bugs much easily before we run code  
	this makes development easier
- Can you force a component to re-render without calling setState?
	we can use forceUpdate() API to trigger re-rendering
	but it is recommended to avoid forceUpdate()
- How to conditionally apply class attributes?
	We can use string template and ternary operator together.
	`<div className={'btn-panel ' + (this.props.visible ? 'show' : 'hidden')}>`
- **What are the possible return values from a functional component and render method in a class component**
	we can return React elements and JSX fragment
	We can also return boolean, undefined, null, string, number and array of React elements
	
	booleans and falsy values such as false, null, undefined are valid children 
	but they don't render anything. 
	we need to convert it to string to display them
- What are the common folder structures for React?
	Mostly, I group them by routes.  
	so that I can have all related files CSS, JS and tests all together in the same folder.
- What is a wrapper component?
	Wrapper component wraps another component to add additional functionality, styling, and contents to the wrapped components.
	
	HOC is the wrapper component
- What are the benefits of new JSX transform?/How is the new JSX transform different from old transform??  
	we can use JSX without importing React packages
- What is state mutation and how to prevent it?
	We accidentally can mutate states without using setState function.
	we can use const keyword use useState hook function in the first place.
	and avoid using array and object as a state using useState
- How do you set default value for uncontrolled component?
	you can specify a defaultValue attribute instead of value
	We can use a defaultValue attribute for input, textArea, checkbox and radio
- Does React support all HTML attributes?
	both standard or custom DOM attributes are fully supported.
- How JSX prevents Injection Attacks?
	React DOM escapes values embedded in JSX before rendering them.  
	so anything that’s not explicitly written in the application will not be injected. Everything is converted to a string before being rendered.
- Why do you not need error boundaries for event handlers?
	Error boundaries do not catch errors inside event handlers.
	React doesn’t need error boundaries to recover from errors in event handlers. Unlike the render method and lifecycle methods, the event handlers don’t happen during rendering. So if they throw, React still knows what to display on the screen.
- ==What is NextJS and major features of it?==
	Next.js is a popular framework for static and server‑rendered application.
	it supports Server-rendering
	Automatic code splitting for faster page loads
	page based routing
- In which scenarios error boundaries do not catch errors?
	- Inside Event handlers
	- Asynchronous code using **setTimeout or requestAnimationFrame** callbacks
	- During Server side rendering
	- When errors thrown in the error boundary code itself
- ==Can you describe about componentDidCatch lifecycle method signature?==
	The **componentDidCatch** lifecycle method is invoked 
	after an error has been thrown by a descendant component.
- What is React lazy function?
	React.lazy function lets you render a dynamic import as a regular component. 
- ==What is Shallow Renderer in React testing==
	Shallow rendering is useful for writing unit test cases in React. 
	It lets you render a component _one level deep_ 
	and assert facts about what its render method returns, 
	without worrying about the behavior of child components, which are not instantiated or rendered.    
- ==How to listen to state changes?==
	we can use componentDidUpdate lifecycle method
	it is called when state changes. 
	or we can use useEffect and have the states i want to listen to inside the dependency array
- How to re-render the view when the browser is resized?
	You can use the useState hook to manage the width and height state variables, 
	and the useEffect hook to add and remove the resize event listener.
- ==What are the lifecycle methods going to be deprecated in React v16?==
	componentWillMount()
	componentWillUpdate()
- How do you memoize a component
	we have a React.memo. 
	we wrap the component using React.memo
	It provides a higher order component which memoizes component unless the props change. 
- ==What is Vite?==
	Vite is a build tool and development server
	It's designed to make development fast and efficient 
	by providing development server startup 
