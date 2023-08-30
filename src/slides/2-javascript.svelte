<script lang="ts">
	import { Slide } from '@components'
	import Notes from '@lib/components/notes.svelte'
	import Step from '@lib/components/step.svelte'
	import Media from '@lib/components/media.svelte'
	import Vertical from '@lib/components/vertical.svelte'
	import Code from '@lib/components/code.svelte'
	import Fit from '@lib/components/fit.svelte'

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
				Let's move on to our first topic. (read title) Ano nga ba ang JavaScript
				framework? JavaScript frameworks are like the Avengers of web
				development. They are powerful, popular and sometimes hard to keep track
				of. But why do we need them when we have plain old JavaScript? Well,
				plain JavaScript is like Iron Man without his suit. It can do some cool
				things, but it's not very efficient, scalable or maintainable.
				JavaScript frameworks provide us with tools and features that make our
				code more organized, reusable and interactive. They also help us deal
				with browser compatibility issues, security risks and performance
				optimization. In short, JavaScript frameworks make our lives easier and
				our websites better.
			</p>
		</Notes>
	</Slide>

	<Slide>
		<h1>Component-Based Architecture</h1>
		<Media src={componentBased} type="img"></Media>

		<Notes>
			<p>
				The core concept most of these frameworks use is what we call
				component-based architecture. Component-based architecture is a way of
				building web applications by breaking them down into smaller, reusable
				pieces of code called components. For example, a component could be a
				button, a menu, a form, or a chart. Components can be nested, composed,
				and styled to create complex user interfaces with minimal code
				duplication and maximum flexibility. This is different from the
				traditional way of building web pages, where each page is a monolithic
				piece of code that contains all the HTML, CSS, and JavaScript for the
				entire page.
			</p>
			<p>
				A component is usually a UI element such as a button, pop-up, or
				navigation bar. You only need to create a component once and you can
				reuse it in any context within the application.
			</p>
		</Notes>
	</Slide>
	<Slide>
		<Fit class="bg-black bg-opacity-30 p-3" type="div"
			>Which JavaScript framework is the best?
		</Fit>

		<Notes>
			<p>
				Which framework is the best? You see this question asked a lot of times
				on StackOverflow, reddit, or other forums. If we go by downloads, React
				wins. Based on Github stars, Vue is the best. But Svelte is the most
				loved framework according to the 2021 StackOverflow survey. Spoiler
				alert, they are all good & bad. There's no absolute best framework. It's
				all in the preference of the users. In order to determine which makes
				you happy, let's make something with all of them. We're going to build a
				Todo app for Vanila JS, React, Angular, Vue and Svelte. In the process,
				you'll learn the tradeoffs between each of these frameworks so you can
				make the best choice for your next project.
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
				Let's try to build it first using vanilla JavaScript. As you can see
				here, we have a form with an input and a button to submit the form. Then
				we have an unordered list for the todos.
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
				One thing that all frameworks have and vanilla js doesn't is to bind or
				connect your html to the javascript. In vanilla, we need to grab the
				html elements from the DOM. Now that we have access to the HTML elements
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
				This is our function to add the todo text. It accepts a todoText as its
				argument. Now this is where it gets complicated with vanilla. In order
				to update the UI, we need to manually create a new list item element by
				calling document create element, then we need to update its inner html
				to the to-do text and finally append it to the unordered list in the
				DOM.
			</p>
			<p>
				Now that we have a function in place, we need to register an event
				listener on the form's on submit event. When that event is fired, this
				function will always be called. We'll first call prevent default to
				prevent the browser's default behavior, in this case, we need to prevent
				it from refreshing the page then call the add to do function with the
				current value in the text input.
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
		<Fit class="bg-black bg-opacity-30 text-blue-400">
			React
			<i class="devicon-react-original colored"></i>
		</Fit>
		<Step class="mt-5 bg-black bg-opacity-30" type="div">
			<ul>
				<Step type="li">A JavaScript library for creating user interfaces</Step>
				<Step type="li">Open-source and component-based</Step>
				<Step type="li"
					>Created by Facebook and used in many popular products
				</Step>
				<Step type="li">
					Works by creating a virtual DOM in memory and updating only the
					changed parts
				</Step>
				<Step type="li"
					>Uses JSX, a syntax that combines JavaScript and XML
				</Step>
				<Step type="li">Minimal and non-opinionated</Step>
				<Step type="li">By far the most popular framework</Step>
			</ul>
		</Step>
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
			<ul>
				<li>
					React is a JavaScript library that allows you to create user
					interfaces in a declarative and efficient way.
				</li>
				<li>
					It is open-source and component-based, meaning that you can reuse UI
					elements across your application.
				</li>
				<li>
					React was created by Facebook and is used in many popular products
					like WhatsApp and Instagram.
				</li>
				<li>
					React works by creating a virtual DOM in memory, which is a
					representation of the actual DOM. React js compares the virtual DOM
					with the real DOM and only updates the parts that have changed. This
					makes React fast and responsive.
				</li>
				<li>
					React also uses a syntax called JSX, which is a mix of JavaScript and
					XML. JSX lets you write HTML-like code in your JavaScript files,
					making it easier to create and maintain UI components.
				</li>
				<li>
					React is minimal by design and relies on the open-source community to
					handle other concerns like routing, animation, and state management.
				</li>
				<li>
					Its popularity alone makes it a great skill to learn, because there
					are abundance of employers looking to hire React developers.
				</li>
			</ul>
		</Notes>
	</Slide>

	<Slide>
		<h1 class="text-blue-400">
			React
			<i class="devicon-react-original colored"></i>
		</h1>

		<Code lang="jsx" lines="1-33|4|7|7,26-28|21-24|13-17|10,22">
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

		<Notes>
			<p>
				This code is a React component that renders a simple To-Do List
				application. The component has a single function named App that returns
				a JSX element. The App function uses React Hooks to manage the state of
				the application.
			</p>
			<p>
				The useState hook is just a function that will return us with two
				values: the first item is the value of the the to-do list as reactive
				state, which means any time it's updated the UI will re-render to show
				the latest state and then the second item is a function to update the
				state.
			</p>
			<p>
				Going down to the JSX, we can loop all of the todo items in the array
				and render them out directly in the UI as a list item. This is the power
				of JSX, you can use JavaScript in HTML.
			</p>
			<p>
				Above that, we have our html form. The cool thing about React is we can
				bind an event directly to this form using onsubmit, then on the right
				side of it we can reference a function that will be called whenever the
				submit event fires.
			</p>
			<p>
				The addTodo function is an event handler that is called when the form is
				submitted. It prevents the default form submission behavior and adds the
				value of the input field to the todos array.
			</p>
			<p>
				The useRef hook is used to create a reference variable named todoText.
				This reference variable is used to store the value of the input field in
				the form.
			</p>
			<p>
				The JSX element returned by the App function contains a form with an
				input field and a submit button. The input field has a placeholder text
				“What needs to be done?” and its value is stored in the todoText
				reference variable. The submit button has a label “Add Todo”.
			</p>

			<p>
				Below the form, there is an unordered list element that displays all the
				to-do items stored in the todos array using the map method.
			</p>
		</Notes>
	</Slide>
	<Slide
		iframe="https://stackblitz.com/edit/stackblitz-starters-bjwidc?ctl=1&embed=1&file=src%2FApp.js"
	></Slide>

	<Slide>
		<Fit class="bg-black bg-opacity-30 text-red-600">
			Angular
			<i class="devicon-angularjs-plain colored"></i>
		</Fit>

		<Step type="div" class="mt-5 bg-black bg-opacity-30">
			<Step>
				Angular, developed by Google, is a comprehensive framework for building
				dynamic web applications. It includes features like two-way data
				binding, dependency injection, and a robust CLI. Angular leverages
				TypeScript for static typing and enhanced tooling.
			</Step>

			<Step class="mt-5">
				Angular is well-suited for large-scale applications and projects with
				complex requirements. It's particularly beneficial for projects that
				require strong architectural patterns, scalability, and TypeScript's
				benefits.
			</Step>
			<Step class="mt-5">Steep learning curve</Step>
			<Step class="mt-5">Used by Google, Microsoft, Samsung, Ubisoft</Step>
		</Step>

		<Notes>
			<p>
				Just like React, Angular has a component-based structure. You can
				manipulate, nest, and reuse them as you need. To write an application on
				Angular, you will need to use TypeScript. Basically, it is a superset of
				JavaScript that uses the same syntax but also supports static typing and
				classes. The system of types is incredibly versatile as well: with
				TypeScript, you get access modifiers, enums, generics, hybrid types, and
				much more. TypeScript has its benefits - static type checking can be
				very useful for large-scale applications, and can be a big productivity
				boost for developers with backgrounds in Java and C#.
			</p>
			<p>
				Angular’s learning curve is much steeper. The API surface of the
				framework is huge and as a user you will need to familiarize yourself
				with a lot more concepts before getting productive. Concepts like RxJS,
				dependency injection, or NgModules. The complexity of Angular is largely
				due to its design goal of targeting only large, complex applications -
				but that does make the framework a lot more difficult for
				less-experienced developers to pick up.
			</p>
		</Notes>
	</Slide>
	<Slide
		iframe="https://stackblitz.com/edit/stackblitz-starters-qezzny?ctl=1&embed=1&file=src%2Fapp%2Fapp.component.ts"
	></Slide>

	<Slide>
		<Fit class="bg-black bg-opacity-30 text-green-700">
			Vue.js
			<i class="devicon-vuejs-plain colored"></i>
		</Fit>

		<Step type="div" class="mt-5 bg-black bg-opacity-30">
			<Step>
				Created by Evan You in 2014 as a lightweight alternative to AngularJS
			</Step>
			<Step>
				Uses HTML, CSS and JavaScript as the basic technologies, and has a clear
				and intuitive syntax
			</Step>
			<Step>
				Has a rich ecosystem of official libraries that provide additional
				functionality, such as routing, state management, testing, animation,
				etc.
			</Step>
			<Step>
				Has a tiny size (20 KB gzipped), a virtual DOM for fast rendering, a
				reactivity system for data binding, and single-file components for
				modularity
			</Step>
			<Step>
				As a progressive framework, it can be easily integrated with other
				frameworks or libraries, such as React, Angular, Bootstrap, etc.
			</Step>
			<Step>
				Has some drawbacks, lack of support for large-scale projects risk of and over flexibility, limited resources
			</Step>
			<Step>
				Used by companies like Adobe, Behance, Alibaba, Gitlab, Xiaomi, etc.
			</Step>
		</Step>

		<Notes>
			<ul>
				<li>
					As Evan You worked in Google, he used AngularJS for a few projects. He
					realized that using AngularJs seemed to heavy to do simple tasks.
				</li>
				<li>
					Vue.js uses HTML, CSS and JavaScript as the basic technologies, and
					has a clear and intuitive syntax. You can easily add Vue.js to any web
					page with a script tag, or use a CLI tool to set up a project with
					webpack or other bundlers.
				</li>
				<li>
					Vue.js has a rich ecosystem of official libraries that provide
					additional functionality, such as routing, state management, testing,
					animation, etc. These libraries are well-maintained and documented,
					and work seamlessly with the core library.
				</li>
				<li>
					Vue.js is one of the smallest frameworks in terms of file size, which
					means faster loading and better performance. The core library is only
					20 KB gzipped, and you can also use tree-shaking to remove unused code
					from your bundle.
				</li>
				<li>
					Vue.js uses a virtual DOM to render the UI, which is an abstraction of
					the real DOM that allows for faster and more efficient updates.Vue.js
					supports single-file components, which are files that contain HTML,
					CSS and JavaScript code for a single component. This makes the code
					more modular, reusable and readable, as you can see the structure and
					logic of each component in one place.
				</li>
				<li>
					Vue.js can be easily integrated with other frameworks or libraries,
					such as React, Angular, Bootstrap, etc. You can use Vue.js as a part
					of a larger application, or as a complete solution for your front-end.
					Vue.js also allows you to use different languages or tools for your
					code, such as TypeScript, JSX, Sass, etc.
				</li>
				<li>
					Drawbacks:
					<ol>
						<li>
							**Lack of support for large-scale projects**: Vue.js is designed
							to be simple and flexible, but this can also lead to some problems
							when working on large-scale or complex projects. For example,
							Vue.js does not enforce a strict structure or convention for your
							code, which can result in inconsistency or confusion among
							developers.
						</li>
						<li>
							**Risk of over flexibility**: Vue.js offers many options and
							features for developers to customize their code and UI, but this
							can also result in over flexibility or abuse of some features. For
							example, some developers may use too many directives or computed
							properties in their code, which can make it hard to read or debug.
							Some developers may also use too many third-party libraries or
							plugins in their project, which can increase the complexity and
							dependency of their code.
						</li>
						<li>
							**Limited resources**: Compared to other frameworks like React or
							Angular, Vue.js has fewer resources available for learning or
							development. For example, there are fewer tutorials, courses,
							books or blogs on Vue.js than on other frameworks. There are also
							fewer developers who are experienced or proficient in Vue.js than
							in other frameworks.
						</li>
						<li>
							**Lack of experienced developers**: As Vue.js is relatively new
							and less popular than other frameworks, it may be harder to find
							or hire developers who are skilled in Vue.js. This can affect the
							quality and speed of your development process, as well as the
							maintenance and support of your project.
						</li>
					</ol>
				</li>
			</ul>
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
		iframe="https://stackblitz.com/edit/vitejs-vite-5kfmhx?ctl=1&embed=1&file=src%2Fcomponents%2FTodo.vue"
	></Slide>

	<Slide>
		<Fit class="text-red-600">
			Svelte
			<i class="devicon-svelte-plain colored"></i>
		</Fit>

		<Step type="div" class="mt-5 bg-black bg-opacity-30">
			<Step class="mt-5">StackOverflow's Most Loved Framework of 2021</Step>
			<Step>
				Svelte is a JavaScript framework for building user interfaces that shifts most of the work to a compile step, resulting in faster and smaller web applications.
			</Step>
			<Step>
				Svelte does not use a virtual DOM or other runtime abstractions. It generates plain JavaScript code that updates the DOM directly, minimizing the overhead and improving the responsiveness of your app.
			</Step>

			<Step>
				Drawbacks include immature tools, young ecosystem, compiler complexity
			</Step>
			<Step>The New York Times, Philips, Rakuten, GoDaddy, Apple Music, Ikea, Forbes</Step>
		</Step>

		<Notes>
			<ul>
				<li>
					- **Immature tools**: Svelte is still a young framework and its tooling is not as mature as other frameworks. For example, IDE support, dev tools, and testing libraries are still in development or have limited features.
				</li>
				<li>
					- **Young ecosystem**: Svelte has a smaller community and fewer open-source libraries than other frameworks. You may not find a ready-made solution for some of your needs and have to build it yourself or wait for the ecosystem to grow.
				</li>
				<li>
					- **Compiler complexity**: Svelte relies on a compiler to transform your components into JavaScript. This adds some complexity and potential issues to your development process, such as debugging, source maps, and compatibility.
				</li>
			</ul>
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
			wanted to learn Svelte so I made this in Svelte. One of the quickest ways
			to learn besides reading the documentation, is using it.
		</Notes>
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
