<script lang="ts">
	import { Presentation, Slide } from '@components'
	import Notes from '@lib/components/notes.svelte'
	import Step from '@lib/components/step.svelte'
	import Media from '@lib/components/media.svelte'
	import Vertical from '@lib/components/vertical.svelte'
	import Code from '@lib/components/code.svelte'
</script>

<Presentation>
	<Slide>
		<h1 class="font-bold">
			Latest Tech Advancements in Software Engineering / Web Development
		</h1>
		<Notes>
			<p>
				Hello, everyone. Thank you for inviting me today to talk to you about
				the latest tech advancements in software engineering and web
				development. As we all know, tech is a very dynamic field, where new
				technologies emerge every year or months to solve complex problems,
				improve user experience, and create innovative products. Some of the
				latest trends that I will cover today are: front-end advancements like
				the rise of JavaScript frameworks, Progressive Web Apps, image
				containerization and orchestration using tools like Docker and
				Kubernetes, WebAssembly (Wasm) and especially the rise of generative AI.
			</p>
		</Notes>
	</Slide>
	<Slide>
		<h2 class="uppercase">Hello There</h2>
		<Step>
			<Step grow>
				<span class="text-lg">Michael Pollente</span>
			</Step>
		</Step>
		<Step fadeLeft>
			<Step highlightGreen>
				<span class="text-base"
					>Software Engineer at Exist Software Labs, Inc.</span
				>
			</Step>
		</Step>
		<Step fadeUp>
			<Media class="my-0 mx-auto" type="img" src="/static/assets/aboutme.gif"
			></Media>
		</Step>

		<Notes>
			<p>
				Hello There - I'm honored to be your resource speaker for this session.
				My name is Michael Pollente. PUP graduate nung 2016. Total of 7 years of
				experience na sa industry. Nagsimula ako sa DICT bilang Java trainee,
				na-absorb, nag-self-study ng Spring, Angular para makasabay as a junior
				developer.
			</p>
			<p>
				Now, isa nang full-stack developer sa Exist Software Labs. Specializing
				sa Java and Spring para sa back-end, and Angular para naman sa
				front-end. Part ako ngayon ng department na nagha-handle ng clients sa
				financial and insurance industry, so naging part na ako sa pag-create ng
				webapps and/or mobile apps para sa iba't ibang banks and insurance
				providers.
			</p>
			<p>
				A little bit about myself: I like pressing buttons. :D Passion ko na
				software development ngayon, unlike before nung college ako na
				unmotivated ako kasi di talaga ako magaling mag-program. Pero nung
				na-expose ako sa industry, na-realize ko na masaya pala talaga 'to. Lalo
				na kapag nakikita mong gumagana yung ginawa mo at nagagamit ng maraming
				tao at na-iimprove yung experience nila. Part ng passion na yun ay ang
				pag-keep up sa latest trends sa software development, which is a very
				dynamic field kaya medyo mahirap ilista ngayon.
			</p>
			<p>
				Namili na lang ako ng tingin ko relevant sa inyo bilang college students
				na magandang ma-expose na kayo before pa pumasok sa industry.
			</p>
		</Notes>
	</Slide>
	<Slide>
		<blockquote>
			&ldquo;The pace of technological change is accelerating, and it's only
			going to get faster. The only way to keep up is to be constantly learning
			and adapting.&rdquo;
		</blockquote>

		<Notes>
			<p>
				I don't know who said this because I can't find any direct quote pero I
				remember reading this somewhere before and it resonated with me. This
				speaks directly to the heart of our topic today - the dynamic world of
				software engineering and web development. Tech is rapidly evolving. From
				new programming languages, frameworks, methodologies, and paradigms
				emerge regularly. Marami ngang memes sa JavaScript community how we keep
				seeing new frameworks every few months. As programmers and web
				developers, we find ourselves in the forefront of this constant change
				and the only way to keep up is constantly learning.
			</p>
			<p>
				But there's a big disclaimer: that as a person with a life other than
				your work, you have to understand that it's impossible to keep up with
				every single new thing. What's most important is you prioritize and
				adapt at your own pace. After all, learning is a lifelong journey. For
				example, instead of attempting to master every thing, focus on learning
				the fundamentals. While tools may change, the core principles remain
				relatively constant. Personally, I'm not a master of everything I'm
				going to talk about later, pero I keep myself updated through
				newsletters, blog, etc. Kasi (wala lang) nag-eenjoy akong mag-try ng new
				things.
			</p>
		</Notes>
	</Slide>
	<Vertical>
		<Slide animate>
			<h1>Evolution of Front-end Development</h1>
			<sub
				>Navigating the Evolution: From Static Pages to Dynamic, Interactive Web
				Apps</sub
			>
		</Slide>
		<Slide animate iframe="https://wiby.me/">
			<div class="group relative">
				<div
					class="absolute w-2/5 shadow-md bg-black bg-opacity-90 text-white p-5 text-lg text-left transition-opacity duration-300 opacity-100 group-hover:opacity-0"
				>
					<h1>Evolution of Front-end Development</h1>
					<sub
						>Navigating the Evolution: From Static Pages to Dynamic, Interactive
						Web Apps</sub
					>
				</div>
			</div>
		</Slide>
		<Slide animate animateRestart iframe="https://paolofornasier.com/">
			<div class="group relative">
				<div
					class="absolute w-2/5 shadow-md bg-black bg-opacity-90 text-white p-5 text-lg text-left transition-opacity duration-300 opacity-100 group-hover:opacity-0"
				>
					<h1>Evolution of Front-end Development</h1>
					<sub
						>Navigating the Evolution: From Static Pages to Dynamic, Interactive
						Web Apps</sub
					>
				</div>
			</div>
		</Slide>
		<Slide animate>
			<h1>Evolution of Front-end Development</h1>
			<sub
				>Navigating the Evolution: From Static Pages to Dynamic, Interactive Web
				Apps</sub
			>
			<Step class="mt-10">
				Rise of JavaScript Frameworks and Component-Based Architecture
			</Step>
			<Step class="mt-2">Tailwind CSS and CSS-in-JS</Step>
			<Step class="mt-2">Responsive Web Design and Mobile-First Approach</Step>
			<Step class="mt-2">Web Accessibility and Inclusive Design</Step>
			<Step class="mt-2">Progressive Web Apps (PWA)</Step>
			<Step class="mt-2">WebAssembly (Wasm)</Step>
			<Step class="mt-2">GraphQL</Step>
		</Slide>

		<Notes>
			<p>
				Before we look at where we are today, explore muna natin yung evolution
				of software and web development. In the early days, web development was
				synonymous with basic HTML pages and limited interactivity. Dati kasi
				ang focus lang ng mga website is to present information rather creating
				immersive user experiences. (scroll down, discuss the static website)
			</p>
			<p>
				Fast forward to today and see how we can create very dynamic and
				interactive websites (scroll down, discuss interactive website). This is
				just an example of what's possible today, if you want more inspiration,
				you can go this website https://awwwards.com that features and rates
				websites based on different categories.
			</p>
			<p>
				So what made this evolution possible? This is what we're going to
				discuss today: we're going to discuss (fade the topics one by one)
			</p>
		</Notes>
	</Vertical>
	<Vertical>
		<Slide>
			<h1>Rise of JavaScript Frameworks and Component-Based Architecture</h1>

			<Notes>
				<p>
					Welcome to the forefront of modern front-end development, where
					JavaScript frameworks are king. Frameworks such as React, Angular,
					Vue.js, Svelte are now synonymous with contemporary web applications.
					Imagine creating animations, dynamic content loading, form validation,
					using pure JavaScript? Possible pa rin naman, kasi under-the-hood
					JavaScript lang ang gamit ng mga frameworks and libraries, pero take
					into context the tight deadlines and fast-paced content delivery of
					the industry, using these frameworks significantly reduce development
					time and complexity.
				</p>
				<p>
					The core concept most of these frameworks use is what we call
					component-based architecture. Instead of building these monolithic
					pages, we utilize pierce together reusable components to build our
					application. Each component encapsulates specific functionality, like
					one form or one modal can be component, even these controls can be
					their own component which we can reuse on any other page, and can be
					combined like building blocks.
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
					disastrous to say the least. Let's take a look at how a simple todo
					app is created.
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
					bind or connect your html to the javascript. In vanilla, we need to
					grab the html elements from the DOM.
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
					scale very well. If we're going to add routing or animation, we need
					to implement them from scratch. That's why most developers choose to
					build their apps using frameworks.
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
				Its component-based architecture and virtual DOM enable efficient
				updates to the UI. React is known for its simplicity and flexibility.
			</Step>
			<Step class="text-base">
				React is an excellent choice for projects of all sizes, from small
				applications to complex web platforms. It's particularly suitable for
				building single-page applications (SPAs) and mobile applications using
				React Native.
			</Step>
			<Step class="text-base">
				It's heavily used by major companies like Facebook, Instagram, and
				Airbnb, Netflix.
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
			<Media type="img" src="/static/assets/component-based.png"></Media>
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
				dynamic web applications. It includes features like two-way data
				binding, dependency injection, and a robust CLI. Angular leverages
				TypeScript for static typing and enhanced tooling.
			</p>

			<Step class="mt-5 text-base">
				Angular is well-suited for large-scale applications and projects with
				complex requirements. It's particularly beneficial for projects that
				require strong architectural patterns, scalability, and TypeScript's
				benefits.
			</Step>
			<Step class="text-base"
				>Used by Google, Microsoft, Samsung</Step
			>
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
				interfaces. Its simplicity and approachability make it a great choice
				for both beginners and experienced developers. Vue.js offers two-way
				data binding, component reusability, and a smooth learning curve.
			</p>

			<Step class="mt-5 text-base">
				Vue.js is a versatile framework that can be used for a wide range of
				projects. It's especially recommended for projects where rapid
				development and a gentle learning curve are important factors.
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
				Svelte is an excellent choice when performance is a critical concern.
				It's also well-suited for small to medium-sized projects where rapid
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
		<Slide iframe="https://stackblitz.com/edit/vitejs-vite-w4rgar?ctl=1&embed=1&file=src%2FApp.svelte"></Slide>
	</Vertical>
</Presentation>
