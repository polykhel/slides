<script lang="ts">
	import { Slide } from '@components'
	import Notes from '@lib/components/notes.svelte'
	import Step from '@lib/components/step.svelte'
	import Media from '@lib/components/media.svelte'
	import Vertical from '@lib/components/vertical.svelte'

	import aboutme from '@lib/assets/aboutme.gif'
</script>

<Slide>
	<div class="title">
		<h1 class="font-bold">The Future of Web Development:</h1>
		<h1 class="font-bold">
			JavaScript Frameworks, Streamlined Styling, and PWAs
		</h1>
	</div>
	<Notes>
		<p>
			Hello, everyone. Thank you for inviting me today to talk to you about the
			latest tech advancements in software engineering and web development. As
			we all know, tech is a very dynamic field, where new technologies emerge
			every year or months to solve complex problems, improve user experience,
			and create innovative products. Some of the latest trends that I will
			cover today are: front-end advancements like the rise of JavaScript
			frameworks, Progressive Web Apps, image containerization and orchestration
			using tools like Docker and Kubernetes, WebAssembly (Wasm) and especially
			the rise of generative AI.
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
		<Media class="my-0 mx-auto" type="img" src={aboutme}></Media>
	</Step>

	<Notes>
		<p>
			Hello There - I'm honored to be your resource speaker for this session. My
			name is Michael Pollente. PUP graduate nung 2016. Total of 7 years of
			experience na sa industry. Nagsimula ako sa DICT bilang Java trainee,
			na-absorb, nag-self-study ng Spring, Angular para makasabay as a junior
			developer.
		</p>
		<p>
			Now, isa nang full-stack developer sa Exist Software Labs. Specializing sa
			Java and Spring para sa back-end, and Angular para naman sa front-end.
			Part ako ngayon ng department na nagha-handle ng clients sa financial and
			insurance industry, so naging part na ako sa pag-create ng webapps and/or
			mobile apps para sa iba't ibang banks and insurance providers.
		</p>
		<p>
			A little bit about myself: I like pressing buttons. :D Passion ko na
			software development ngayon, unlike before nung college ako na unmotivated
			ako kasi di talaga ako magaling mag-program. Pero nung na-expose ako sa
			industry, na-realize ko na masaya pala talaga 'to. Lalo na kapag nakikita
			mong gumagana yung ginawa mo at nagagamit ng maraming tao at na-iimprove
			yung experience nila. Part ng passion na yun ay ang pag-keep up sa latest
			trends sa software development, which is a very dynamic field kaya medyo
			mahirap ilista ngayon.
		</p>
		<p>
			Namili na lang ako ng tingin ko relevant sa inyo bilang college students
			na magandang ma-expose na kayo before pa pumasok sa industry.
		</p>
	</Notes>
</Slide>
<Slide>
	<blockquote>
		&ldquo;The pace of technological change is accelerating, and it's only going
		to get faster. The only way to keep up is to be constantly learning and
		adapting.&rdquo;
	</blockquote>

	<Notes>
		<p>
			I don't know who said this because I can't find any direct quote pero I
			remember reading this somewhere before and it resonated with me. This
			speaks directly to the heart of our topic today - the dynamic world of
			software engineering and web development. Tech is rapidly evolving. From
			new programming languages, frameworks, methodologies, and paradigms emerge
			regularly. Marami ngang memes sa JavaScript community how we keep seeing
			new frameworks every few months. As programmers and web developers, we
			find ourselves in the forefront of this constant change and the only way
			to keep up is constantly learning.
		</p>
		<p>
			But there's a big disclaimer: that as a person with a life other than your
			work, you have to understand that it's impossible to keep up with every
			single new thing. What's most important is you prioritize and adapt at
			your own pace. After all, learning is a lifelong journey. For example,
			instead of attempting to master every thing, focus on learning the
			fundamentals. While tools may change, the core principles remain
			relatively constant. Personally, I'm not a master of everything I'm going
			to talk about later, pero I keep myself updated through newsletters, blog,
			etc. Kasi (wala lang) nag-eenjoy akong mag-try ng new things.
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
		<Step class="mt-2">Progressive Web Apps (PWA)</Step>
		<Step class="mt-2">WebAssembly (Wasm)</Step>
		<Step class="mt-2">GraphQL</Step>
	</Slide>

	<Notes>
		<p>
			Before we look at where we are today, explore muna natin yung evolution of
			software and web development. In the early days, web development was
			synonymous with basic HTML pages and limited interactivity. Dati kasi ang
			focus lang ng mga website is to present information rather creating
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
			So what made this evolution possible? This is what we're going to discuss
			today: we're going to discuss (fade the topics one by one)
		</p>
	</Notes>
</Vertical>
