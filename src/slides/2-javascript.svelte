<script lang="ts">
	import {Slide} from '@components'
	import Notes from '@lib/components/notes.svelte'
	import Step from '@lib/components/step.svelte'
	import Media from '@lib/components/media.svelte'
	import Vertical from '@lib/components/vertical.svelte'
	import Code from '@lib/components/code.svelte'

	import componentBased from '@lib/assets/component-based.png'
</script>

<Vertical>
	<Slide>
		<div class="bg-black bg-opacity-30 text-3xl p-3">
			<h1>🔥 Rise of JavaScript Frameworks 🔥</h1>
			<h1>and Component-Based Architecture</h1>
		</div>
		<Notes>
			<p>
				Let's move on to our first topic. We'll talk about one of the main
				factors how we can build immersive user experiences quickly and
				effectively. Let's start with why would we need JavaScript frameworks in the first place. It's perfectly
				possible to code without using them – however, a well-chosen framework will make your work a lot easier.
				Furthermore, they are free and open-source, so there's no risk in trying, now is there?

				First and foremost, it improves your efficiency. Think of it as a shortcut of sorts: you have to write
				less code manually, as there are functions and patterns already pre-written and ready for you to use.
				Some components of a website do not need to be custom-made, therefore, you can just pre-built ones and
				build on them. Without the need to work on basic yet time-consuming tasks, you can concentrate on
				building unique features and perfecting specific details.

				The next advantage of JavaScript frameworks comes from its huge user base. Most of the time, you have
				extensive documentation, support groups, community blogs, and forums. Users are quick to test new
				updates and report bugs, which means the issues are detected and resolved without hassle.
			</p>
			<p>
				The core concept most of these frameworks use is what we call
				component-based architecture. Instead of building these monolithic
				pages, we utilize pierce together reusable components to build our
				application. Each component encapsulates specific functionality, like
				one form or one modal can be component, even these controls can be their
				own component which we can reuse on any other page, and can be combined
				like building blocks.
			</p>
		</Notes>
	</Slide>

	<Slide>
		<h1>Component-Based Architecture</h1>
		<Media src={componentBased} type="img"></Media>

		<Notes>
			At the core of this transformation is the concept of component-based
			architecture. Instead of building monolithic pages, we craft applications
			by piecing together reusable components. Each component encapsulates
			specific functionality and can be combined like building blocks to form
			intricate interfaces. This approach not only improves the efficiency of
			development but also enhances maintainability and encourages collaboration
			among teams.
			<p>
				A component is usually a UI element such as a button, pop-up, or
				navigation bar. You only need to create a component once and you can
				reuse it in any context within the application.
			</p>
			<p>
				Let's explore some of the most popular JavaScript frameworks today by
				building a simple Todo app for each one.
			</p>
		</Notes>
	</Slide>

	<Slide animate>
		<h1 class="text-yellow-200">
			Vanilla JavaScript
			<i class="devicon-javascript-plain colored"></i>
		</h1>

		<Code lang="js">
			{`
                <html lang="en">
                <body>
                    <form> 
                        <input name="todo" type="text">
                        <input type="submit" value="Add Todo">
                    </form>
                    <ul id="todos"></ul>

                    <script>

                    <\/script>
                </body>
                </html>
              `}
		</Code>

		<Notes>
			<p>
				Let's try to build it first using pure JavaScript. Any web developer
				needs to have solid understanding of vanilla JS.
			</p>
			<p>
				(after all code is discussed)
				But even if you're a JS expert, attempting to build a non-trivial app
				with it is disastrous to say the least. Let's take a look at how a
				simple todo app is created.
			</p>
		</Notes>
	</Slide>
	<Slide animate>
		<h1 class="text-yellow-200">
			Vanilla JavaScript
			<i class="devicon-javascript-plain colored"></i>
		</h1>

		<Code lang="js">
			{`
                <html lang="en">
                <body>
                    <form> 
                        <input name="todo" type="text">
                        <input type="submit" value="Add Todo">
                    </form>
                    <ul id="todos"></ul>

                    <script>
                        // Get DOM elements
                        const form  = document.querySelector('form');
                        const input = document.querySelector("[name='todo']");
                        const todoList = document.getElementById('todos');
                    <\/script>
                </body>
                </html>
              `}
		</Code>

		<Notes>
			<p>
				One thing that all frameworks have and vanilla js doesn't have is to
				bind or connect your html to the javascript. In vanilla, we need to grab
				the html elements from the DOM.
			</p></Notes
		>
	</Slide>
	<Slide animate>
		<h1 class="text-yellow-200">
			Vanilla JavaScript
			<i class="devicon-javascript-plain colored"></i>
		</h1>

		<Code lang="js" lines="15-20|16|17|18|23-26|1-29">
			{`
                <html lang="en">
                <body>
                    <form> 
                        <input name="todo" type="text">
                        <input type="submit" value="Add Todo">
                    </form>
                    <ul id="todos"></ul>

                    <script>
                        // Get DOM elements
                        const form  = document.querySelector('form');
                        const input = document.querySelector("[name='todo']");
                        const todoList = document.getElementById('todos');

                        function addTodo(todoText) {
                            const li = document.createElement('li')
                            li.innerHTML = todoText;
                            todoList.appendChild(li);
                            input.value = ''
                        }

                        // Events
                        form.onsubmit = (event) => {
                            event.preventDefault();
                            addTodo(input.value);
                        }
                    <\/script>
                </body>
                </html>
              `}
		</Code>

		<Notes>
			<p>
				Now this is where it gets complicated with vanilla. In order to update
				the UI, we need to manually create a new list item element by calling
				document create element, then we need to update its inner html to the
				to-do text and finally append it to the unordered list in the DOM.
			</p>
		</Notes>
	</Slide>
	<Slide
		iframe="https://stackblitz.com/edit/js-ve5hsm?ctl=1&embed=1&file=index.html"
	>
		<Notes>
			<p>
				We just built a to-do app with vanilla JS, but this is not going to
				scale very well. If we're going to add routing or animation, we need to
				implement them from scratch. That's why most developers choose to build
				their apps using frameworks.
			</p>
		</Notes>
	</Slide>

	<Slide>
		<h1 class="text-blue-400">
			React
			<i class="devicon-react-original colored"></i>
		</h1>
		<div class="mt-5 bg-black bg-opacity-30">
			<p>
				React, developed by Facebook in 2011 (open-source and available to the public in 2013), is the most-used
				&
				downloaded
				library for building user interfaces
			</p>

			<Step class="mt-5">
				Its component-based architecture and virtual DOM enable efficient updates
				to the UI. React is known for its simplicity and flexibility.
			</Step>
			<Step class="mt-5">
				React is an excellent choice for projects of all sizes, from small
				applications to complex web platforms. It's particularly suitable for
				building single-page applications (SPAs) and mobile applications using
				React Native.
			</Step>
			<Step class="mt-5">
				It's heavily used by major companies like Facebook, Instagram, Airbnb,
				Netflix.
			</Step>

		</div>
		<Step>
			<div class="flex justify-center items-center mt-10">
				<Media
						allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
						allowfullscreen
						frameborder="0"
						height="315"
						src="https://www.youtube.com/embed/8pDqJVdNa44"
						title="YouTube video player"
						type="iframe"
						width="560"
				></Media>
			</div>
		</Step>

		<Notes>
			The most popular framework or library today. Facebook developers started working on it to simplify their own
			work at first.
			React is based on reusable components. To put it simply, these are blocks of code that can be classified as
			either classes or functions. Each component represents a specific part of a page, like a logo, a button, or
			an input box. The parameters they take are called props, which stands for properties. You can call your
			components in a certain order, place one inside the other, and create the look you like.

			<p>Speaking of syntax, most developers agree that React is easy to learn if you already know JavaScript.
				There's extensive documentation to guide you, full of handy examples. The community is very large.</p>
		</Notes>
	</Slide>

	<Slide>
		<h1 class="text-blue-400">
			React
			<i class="devicon-react-original colored"></i>
		</h1>

		<Code lang="jsx">
			{`
            import { useRef, useState } from 'react';
            import './App.css';

            function App() {

              // State
              const [todos, setTodos] = useState([]);

              // Binding
              const todoText = useRef();

              // Events
              function addTodo(event) {
                  event.preventDefault();
                  const next = [...todos, todoText.current.value];
                  setTodos(next);
              }

              return (
                  <div>
                    <form onSubmit={addTodo}>
                       <input type="text" placeholder="What needs to be done?" ref={todoText} />
                       <input type="submit" value="Add Todo" />
                    </form>

                    <ul>
                      {todos.map(todo => (<li key={todo}>{todo}</li>))}
                    </ul>
                 </div>
              );
            }

            export default App;
            `}
		</Code>

		<Notes>JSX</Notes>
	</Slide>
	<Slide
			iframe="https://stackblitz.com/edit/stackblitz-starters-mr9hqi?ctl=1&embed=1&file=src%2FApp.js"
	></Slide>

	<Slide>
		<h1 class="text-red-600">
			Angular
			<i class="devicon-angularjs-plain colored"></i>
		</h1>

		<div class="mt-5 bg-black bg-opacity-30">
			<p>
				Angular, developed by Google, is a comprehensive framework for building
				dynamic web applications. It includes features like two-way data binding,
				dependency injection, and a robust CLI. Angular leverages TypeScript for
				static typing and enhanced tooling.
			</p>

			<Step class="mt-5">
				Angular is well-suited for large-scale applications and projects with
				complex requirements. It's particularly beneficial for projects that
				require strong architectural patterns, scalability, and TypeScript's
				benefits.
			</Step>
			<Step class="mt-5">Used by Google, Microsoft, Samsung, Ubisoft</Step>
		</div>

		<Notes>
			Just like React, Angular has a component-based structure. You can manipulate, nest, and reuse them as you
			need.

			To write an application on Angular, you will need to use TypeScript. Basically, it is a superset of
			JavaScript that uses the same syntax but also supports static typing and classes. The system of types is
			incredibly versatile as well: with TypeScript, you get access modifiers, enums, generics, hybrid types, and
			much more. TypeScript has its benefits - static type checking can be very useful for large-scale
			applications, and can be a big productivity boost for developers with backgrounds in Java and C#. After
			you're done, an ahead-of-time compiler compiles your code into clean JavaScript. This way,
			you can create a more robust project which will work in any OS and any host.

			Angular’s learning curve is much steeper. The API surface of the framework is huge and as a user you will
			need to familiarize yourself with a lot more concepts before getting productive. The complexity of Angular
			is largely due to its design goal of targeting only large, complex applications - but that does make the
			framework a lot more difficult for less-experienced developers to pick up.
		</Notes>
	</Slide>
	<Slide
			iframe="https://stackblitz.com/edit/stackblitz-starters-892zzs?ctl=1&embed=1&file=src%2Fapp%2Fapp.component.ts"
	></Slide>

	<Slide>
		<h1 class="text-green-700">
			Vue.js
			<i class="devicon-vuejs-plain colored"></i>
		</h1>

		<div class="mt-5 bg-black bg-opacity-30">
			<p>
				Vue.js is a progressive JavaScript framework designed for building user
				interfaces. Its simplicity and approachability make it a great choice for
				both beginners and experienced developers. Vue.js offers two-way data
				binding, component reusability, and a smooth learning curve.
			</p>

			<Step class="mt-5">
				Vue.js is a versatile framework that can be used for a wide range of
				projects. It's especially recommended for projects where rapid development
				and a gentle learning curve are important factors.
			</Step>
			<Step class="mt-5">Upwork, Gitlab, Nintendo, 9gag</Step>
		</div>

		<Notes>
			As Evan You worked in Google, he used Angular for a few projects. While he liked the possibilities it gave
			him, the overall system seemed too heavy for the simple tasks at hand. Therefore, it's only natural that the
			first thing most developers notice when trying the Vue.js framework he created and released in 2014 is how
			incredibly lightweight it is. With a file of just around 20 kilobytes in size, you can download and start
			using Vue.js in literal seconds.
		</Notes>
	</Slide>
	<Slide>
		<h1 class="text-green-700">
			Vue.js
			<i class="devicon-vuejs-plain colored"></i>
		</h1>
		<Code lang="js">
			{`
            <script setup>
                import { ref } from 'vue'

                const todos = ref([]);
                const todoText = ref('');

                const addTodo = () => {
                    todos.value = [...todos.value, todoText.value];
                }
            <\/script>

            <template>
                <form @submit.prevent="addTodo">
                    <input v-model="todoText" placeholder="What needs to be done?">
                    <button type="submit">Add Todo</button>
                </form>

                <ul>
                    <li v-for="todo in todos" :key="todo">{{todo}}</li>
                </ul>
            </template>

            <!-- Add "scoped" attribute to limit CSS to this component only -->
            <style scoped>
            <\/style>
            `}
		</Code>
	</Slide>
	<Slide
			iframe="https://stackblitz.com/edit/vitejs-vite-nigz2d?ctl=1&embed=1&file=src%2Fcomponents%2FTodo.vue"
	></Slide>

	<Slide>
		<h1 class="text-red-600">
			Svelte
			<i class="devicon-svelte-plain colored"></i>
		</h1>

		<div class="mt-5 bg-black bg-opacity-30">
			<p>
				Svelte is an innovative framework that compiles components into highly
				efficient JavaScript during build time. This approach results in smaller
				bundle sizes and better runtime performance. Svelte takes care of
				optimizing code, leading to faster applications.
			</p>

			<Step class="mt-5">StackOverflow's Most Loved Framework of 2021</Step>
			<Step class="mt-5">
				Svelte is an excellent choice when performance is a critical concern. It's
				also well-suited for small to medium-sized projects where rapid
				development and minimal runtime overhead are important.
			</Step>
			<Step class="mt-5">Apple Music, Ikea, Forbes</Step>
		</div>

		<Notes>
			Svelte is a JavaScript framework that has been gaining popularity among developers in recent years. It is
			known for its simplicity, performance, and ease of use. Svelte is often compared to other popular frameworks
			such as React and Vue.js.

			In a comparison of Svelte vs. Vue, ProCoders 1 notes that Svelte is based on a tool for compiling components
			at the build stage, allowing you to load only what is needed to display your application on the page. This
			means there is no virtual DOM, no frameworks on top of frameworks, and no framework at runtime. This is the
			main difference between Svelte and Vue, and the main argument in the Svelte vs. React vs. Angular vs. Vue
			battle.

			Kinsta 2 notes that both Svelte and React follow component-based development architecture, but the
			difference comes in the fact that React utilizes JSX, whereas Svelte is a language in itself composed of the
			three standard languages: HTML, CSS, and JavaScript. Moreover, Svelte code is much more easily read and has
			no unnecessary code.

			Twilio 3 compares Svelte and React and shows how to build a basic app with both frameworks. LogRocket Blog 4
			examines the syntactical differences between Svelte and Vue, comparing how they work under the hood.

			Overall, Svelte’s simplicity and performance make it an attractive op
		</Notes>
	</Slide>
	<Slide>
		<h1 class="text-red-600">
			Svelte
			<i class="devicon-svelte-plain colored"></i>
		</h1>
		<Code lang="svelte">
			{`
            <script>
                import { onMount } from 'svelte';

                let todos = [];
                let todoText = '';

                function addTodo() {
                    todos = [...todos, todoText];
                    todoText = '';
                }
            <\/script>

            <main>
                <form on:submit|preventDefault={addTodo}>
                    <input bind:value={todoText} placeholder="What needs to be done?">
                    <input type="submit" value="Add todo">
                </form>
                <ul>
                    {#each todos as todo}
                        <li>{todo}</li>
                    {/each}
                </ul>
            </main>

            <style>
            <\/style>
            `}
		</Code>

		<Notes>
			Fun fact: this presentation was made in Svelte, powered by Animotion and
			reveal.js. So kung sawa ka na sa PowerPoint, you can now also code your
			presentations! reveal.js can be used without any JavaScript framework, I
			wanted to learn Svelte so I made this in Svelte. One of the quickest ways to learn besides reading the
			documentation, is using it.
		</Notes>
	</Slide>
	<Slide
			iframe="https://stackblitz.com/edit/vitejs-vite-qln8tf?ctl=1&embed=1&file=src%2FApp.svelte"
	>
		<Notes
			>JavaScript frameworks and component-based architecture have fueled the
			creation of remarkable applications that span industries. From social
			media platforms to e-commerce giants, the influence of these advancements
			is evident in the seamless experiences they deliver.</Notes
		>
	</Slide>
</Vertical>
