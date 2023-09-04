<script lang="ts">
	import {Slide} from '@components'
	import Notes from '@lib/components/notes.svelte'
	import Step from '@lib/components/step.svelte'
	import Media from '@lib/components/media.svelte'
	import Vertical from '@lib/components/vertical.svelte'

	import aboutme from '@lib/assets/aboutme.gif'
</script>

<Slide>
	<div class="bg-black bg-opacity-30 text-3xl p-3">
		<h1 class="font-bold">The Future 🚀 of Web Development:</h1>
		<h1 class="font-bold">
			JavaScript Frameworks 🔥<br> Streamlined Styling 🎨<br> and PWAs 📱
		</h1>
	</div>
	<Notes>
		<p>Hello, everyone. Good afternoon. This is my first time to give a talk like this, so forgive me if I make some
			mistakes along the way.
		</p>
		<p>
			Nabigay na topic sakin is to discuss the latest tech advancements in software engineering and web
			development.
			I planned to discuss sana yung mga advancements sa frontend, backend, devops, cloud, even yung emergence ng
			generative AI.
			Pero habang ginagawa ko yung presentation, sa front-end pa lang sobrang dami na pwedeng
			ma-discuss kaya nilimit ko na lang yung
			presentation ko today to the latest trends in front-end development. We'll
			talk about the rise of JavaScript frameworks and component-based architecture,
			new ways style your web apps using utility libraries like Tailwind CSS and CSS-in-JS solutions, and how to
			make PWAs or progressive web apps. We're going to build a PWA later.
		</p>
	</Notes>
</Slide>
<Slide transition="fade" transitionSpeed="slow">
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
		<p>Before anything else, magbibigay lang ako ng short introduction.</p>
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
			yung experience nila.
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
			I remember reading this somewhere before and it resonated with me. This
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
			etc. kasi I enjoy trying new things, which I also like sharing.
		</p>
	</Notes>
</Slide>
<!--<Vertical>
	<Slide animate class="bg-black bg-opacity-30 text-3xl p-3">
		<h1>Evolution of Front-end Development</h1>
		<sub
			>Navigating the Evolution: From Static Pages to Dynamic, Interactive Web
			Apps</sub
		>
		<Notes>
			<p>
				Before we look at where we are today, explore muna natin yung evolution of
				web development. In the early days, web development was
				synonymous with basic HTML pages and limited interactivity. Dati kasi ang
				focus lang ng mga website is to present information rather creating
				immersive user experiences. (scroll down, discuss the static website)
			</p>
		</Notes>
	</Slide>
	<Slide iframe="https://wiby.me/">
		<Notes>http://www.rsrich.force9.co.uk/zetec-turbo/</Notes>
	</Slide>
	<Slide iframe="https://tailwindcss.com/showcase">
		<Notes>
			<p>
				Fast forward to today. Let's explore some modern websites we have today. These are all made with Tailwind CSS, a tool we're going to talk about later.
				Look at how interactive this website is. Uses videos, custom fonts, animations, etc. Look at wappalyzer
			</p>
		</Notes>
	</Slide>
</Vertical>-->
