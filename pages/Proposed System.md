- ## Components
	- ### XFile
	  Template Language - Design System Language (DSL)
		- XFile are documents that contain the component syntax that get's processed by XElement and compiled by Scully.
		- ```html
		  Front matter
		  (What would be rendered in the server; think data layer)
		  
		  ---
		  
		  <Div @do @clipboardCopy @keychange>
		  
		  <Lifecycle>
		    (up for discussion)
		  
		  <style>
		  	Style the shadow DOM
		  </style>
		  ```
		-
	- ### XElement
	  Library for Web Components (for Web10...which is like Web3...but better)
		- _XElement = Svelte for transitions, Solid for reactivity, Knockout for observables, Qwik for Client-Server relationship, and (no library uses state machines, so...(maybe **XState** or Matt's Robots))_
		- A collection of robust APIs that help abstract the creation of Web Components.
			- **Finite State Machine**
				- A lot of State Library don't operate at an enterprise-level (e.g. Redox).
			- **Fine Grained Reactivity**
			  (i.e Solid)
				- Think Solid for Web Componenets
				- It works similar to Qwik
					- How Qwik does it
						- Serializes the data in the client and the server
						- Once the data loads on the server, it gets sent to the client
						- The client then populates the DOM
					- How XElement does it
						- Serializes the data in the client and the server
						- Once the data loads on the server, it gets sent to the client
						- The client then populates the DOM
			- **Lifecycle Events**
			  APIs and Hooks
				- Ideally we don't want a client-side render.
				- `adoptedCallback` : Invoked each time the custom element is moved to a new document.
				  https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements#using_the_lifecycle_callbacks
				- [[draws/XElement-Layout-2022-07-10.excalidraw]]
				-
			- **Predefined Animation API**
				- Predefined props
				- Meant to further our developer experience.
	- ### Scully
	  Rust-based Compiler
		- Takes XFile Components and compiles them into standards-compliant Web Components.
	- ### Mulder
	  Intermediate Representation
- `src/components/counter.xfile`
- `src/components/counter.story.xfile`