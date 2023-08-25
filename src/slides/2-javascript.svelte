<script lang="ts">
	import { Slide } from '@components'
	import Notes from '@lib/components/notes.svelte'
	import Step from '@lib/components/step.svelte'
	import Media from '@lib/components/media.svelte'
	import Vertical from '@lib/components/vertical.svelte'
	import Code from '@lib/components/code.svelte'

	import componentBased from '@lib/assets/component-based.png'
</script>

<Vertical>
	<Slide>
		<div>
			<h1>Rise of JavaScript Frameworks and Component-Based Architecture</h1>
		</div>
		<Notes>
			<p>
				Welcome to the forefront of modern front-end development, where
				JavaScript frameworks are king. Frameworks such as React, Angular,
				Vue.js, Svelte are now synonymous with contemporary web applications.
				Imagine creating animations, dynamic content loading, form validation,
				using pure JavaScript? Possible pa rin naman, kasi under-the-hood
				JavaScript lang ang gamit ng mga frameworks and libraries, pero take
				into context the tight deadlines and fast-paced content delivery of the
				industry, using these frameworks significantly reduce development time
				and complexity.
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
				Before anything, let's try to build it using pure JavaScript. Any web
				developer needs to have solid understanding of vanilla js, but even if
				you're a JS expert, attempting to build a non-trivial app with it is
				disastrous to say the least. Let's take a look at how a simple todo app
				is created.
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
		<p>
			React, developed by Facebook in 2013, is the most-used & downloaded
			library for building user interfaces
		</p>

		<Step class="mt-5 text-base">
			Its component-based architecture and virtual DOM enable efficient updates
			to the UI. React is known for its simplicity and flexibility.
		</Step>
		<Step class="text-base">
			React is an excellent choice for projects of all sizes, from small
			applications to complex web platforms. It's particularly suitable for
			building single-page applications (SPAs) and mobile applications using
			React Native.
		</Step>
		<Step class="text-base">
			It's heavily used by major companies like Facebook, Instagram, and Airbnb,
			Netflix.
		</Step>
		<Step>
			<div class="flex justify-center items-center mt-10">
				<Media
					type="iframe"
					width="560"
					height="315"
					src="https://www.youtube.com/embed/8pDqJVdNa44"
					title="YouTube video player"
					frameborder="0"
					allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
					allowfullscreen
				></Media>
			</div>
		</Step>

		<Notes>
			The most popular framework or library today. Made by Facebook in 2013
		</Notes>
	</Slide>

	<Slide>
		<h1>Component-Based Architecture</h1>
		<Media type="img" src={componentBased}></Media>

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
                <ul>
                    {todos.map(todo => (<li key={todo}>{todo}</li>))}  
                </ul>

                <form onSubmit={addTodo}>
                    <input type="text" placeholder="What needs to be done?" ref={todoText} />
                    <input type="submit" value="Add Todo" />
                </form>

                </div>
            );
            }

            export default App;
            `}
		</Code>

		<Notes>JSX</Notes>
	</Slide>
	<Slide
		iframe="https://stackblitz.com/edit/stackblitz-starters-bjwidc?ctl=1&embed=1&file=src%2FApp.js"
	></Slide>

	<Slide>
		<h1 class="text-red-600">
			Angular
			<i class="devicon-angularjs-plain colored"></i>
		</h1>

		<p>
			Angular, developed by Google, is a comprehensive framework for building
			dynamic web applications. It includes features like two-way data binding,
			dependency injection, and a robust CLI. Angular leverages TypeScript for
			static typing and enhanced tooling.
		</p>

		<Step class="mt-5 text-base">
			Angular is well-suited for large-scale applications and projects with
			complex requirements. It's particularly beneficial for projects that
			require strong architectural patterns, scalability, and TypeScript's
			benefits.
		</Step>
		<Step class="text-base">Used by Google, Microsoft, Samsung, Ubisoft</Step>
	</Slide>
	<Slide
		iframe="https://stackblitz.com/edit/stackblitz-starters-qezzny?ctl=1&embed=1&file=src%2Fapp%2Fapp.component.ts"
	></Slide>

	<Slide>
		<h1 class="text-green-700">
			Vue.js
			<i class="devicon-vuejs-plain colored"></i>
		</h1>

		<p>
			Vue.js is a progressive JavaScript framework designed for building user
			interfaces. Its simplicity and approachability make it a great choice for
			both beginners and experienced developers. Vue.js offers two-way data
			binding, component reusability, and a smooth learning curve.
		</p>

		<Step class="mt-5 text-base">
			Vue.js is a versatile framework that can be used for a wide range of
			projects. It's especially recommended for projects where rapid development
			and a gentle learning curve are important factors.
		</Step>
		<Step class="text-base">Upwork, Gitlab, Nintendo, 9gag</Step>
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
		iframe="https://stackblitz.com/edit/vitejs-vite-5kfmhx?ctl=1&embed=1&file=src%2Fcomponents%2FTodo.vue"
	></Slide>

	<Slide>
		<h1 class="text-red-600">
			Svelte
			<i class="devicon-svelte-plain colored"></i>
		</h1>

		<p>
			Svelte is an innovative framework that compiles components into highly
			efficient JavaScript during build time. This approach results in smaller
			bundle sizes and better runtime performance. Svelte takes care of
			optimizing code, leading to faster applications.
		</p>

		<Step class="mt-5 text-base">
			Svelte is an excellent choice when performance is a critical concern. It's
			also well-suited for small to medium-sized projects where rapid
			development and minimal runtime overhead are important.
		</Step>
		<Step class="text-base">Apple Music, Ikea, Forbes</Step>
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
	</Slide>
	<Slide
		iframe="https://stackblitz.com/edit/vitejs-vite-w4rgar?ctl=1&embed=1&file=src%2FApp.svelte"
	>
		<Notes
			>JavaScript frameworks and component-based architecture have fueled the
			creation of remarkable applications that span industries. From social
			media platforms to e-commerce giants, the influence of these advancements
			is evident in the seamless experiences they deliver.</Notes
		>
	</Slide>
</Vertical>
