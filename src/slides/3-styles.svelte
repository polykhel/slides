<script lang="ts">
    import {Slide} from '@components'
    import Notes from '@lib/components/notes.svelte'
    import Media from '@lib/components/media.svelte'
    import Vertical from '@lib/components/vertical.svelte'
    import Code from '@lib/components/code.svelte'
    import Step from '@lib/components/step.svelte'

    import bootstrapLogo from '@lib/assets/bootstrap-logo.png'
    import foundationLogo from '@lib/assets/foundation-logo.svg'
    import materialLogo from '@lib/assets/material-logo.png'
    import chatLogo from '@lib/assets/chat-logo.svg'
</script>

<Vertical>
    <Slide>
        <div class="title">
            <h1>Streamlining Styling:</h1>
            <h1>
                Tailwind CSS
                <i class="devicon-tailwindcss-plain colored"></i>
                and CSS-in-JS
            </h1>
        </div>

        <Notes>
            <p>
                Let's move on to the world of styling. Tulad ng JavaScript, sobrang dami
                na ring CSS libraries and frameworks ngayon. Sa bawat JavaScript
                framework pa, meron pang sariling/dedicated CSS framework. Of course,
                like JavaScript, you can build your projects with pure CSS, without
                using any library. Pero who has time for that? Also, imagine yung
                maintenance nun kapag medyo lumaki na yung website at sobrang dami na
                CSS files. All the UI libraries and frameworks are some of the most
                popular and latest to come out, which greatly help the developer
                experience and reduce development time.
            </p>
        </Notes>
    </Slide>
    <Slide>
        <div class="grid grid-cols-3 gap-4 mx-auto">
            <Media class="object-contain w-96" src={bootstrapLogo} type="img"></Media>
            <Media class="object-contain w-96" src={foundationLogo} type="img"
            ></Media>
            <Media class="object-contain w-96" src={materialLogo} type="img"></Media>
        </div>

        <Notes>
            First, let's talk about Bootstrap and other frameworks like Foundation and
            Material. Who has heard of Bootstrap? Nung college ako, ito ang uso. And
            for a time, it was the go-to CSS framework sa industry. Explore muna natin
            what Bootstrap has to offer.
        </Notes>
    </Slide>
    <Slide iframe="https://stackblitz.com/edit/nknzfx?embed=1&file=index.html">
        <Notes>
            <p>
                Frameworks like Bootstrap, Foundation and Material are what we call
                component-based framework. They are very "opinionated" with their own
                sets of rules, with default themes and colors, and contains high-level
                components like buttons, forms and lists. In addition sa styles, yung
                mga component na to, meron na ring behavior attached.
            </p>
            <p>
                For example, sa buttons pwede kang maglagay ng data-bs-toggle="button",
                to toggle yung active class. Or a disabled class to make the button
                disabled. Bootstrap and other frameworks does a lot for you, as the
                components are already pre-defined. Gamitin mo lang yung card class,
                magkakaroon ka na ng card-looking component.
            </p>
            <p>
                Here's the catch. As soon as you need something custom, you get stuck
                and sometimes fight with what the framework's trying to do. Of course,
                customizable pa rin naman because we can write our CSS on top of the
                classes Bootstrap provides. But think of it this way, if we override a
                lot, then is there really any point in using the framework? Also, unless
                you really customize it, it will look like other websites created using
                Bootstrap. At first glance, halata mo na Bootstrap ang gamit mo.
            </p>
        </Notes>
    </Slide>
    <Slide animate>
        <h1>
            Tailwind CSS
            <i class="devicon-tailwindcss-plain colored"></i>
        </h1>

        <Notes>
            So enter Tailwind CSS. Tailwind takes a more functional approach by
            providing you with utility classes that can be composed together to build
            components. That's why it's called a utility-first framework. Take note
            that Tailwind is not the first utility-first framework but it is currently
            the most popular.
        </Notes>
    </Slide>
    <Slide>
        <h5>
            Using a traditional approach where custom designs require custom CSS
        </h5>

        <div class="relative rounded-xl overflow-auto p-8">
            <div class="chat-notification">
                <div class="chat-notification-logo-wrapper">
                    <img
                            alt="ChitChat Logo"
                            class="chat-notification-logo"
                            src={chatLogo}
                    />
                </div>
                <div class="chat-notification-content">
                    <h4 class="chat-notification-title">ChitChat</h4>
                    <p class="chat-notification-message">You have a new message!</p>
                </div>
            </div>
        </div>
        <Code lang="html">
            {`
					<div class="chat-notification">
						<div class="chat-notification-logo-wrapper">
							<img class="chat-notification-logo" src="/img/logo.svg" alt="ChitChat Logo">
						</div>
						<div class="chat-notification-content">
							<h4 class="chat-notification-title">ChitChat</h4>
							<p class="chat-notification-message">You have a new message!</p>
						</div>
					</div>
		
					<style>
						.chat-notification {
							display: flex;
							max-width: 24rem;
							margin: 0 auto;
							padding: 1.5rem;
							border-radius: 0.5rem;
							background-color: #fff;
							box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
						}
						.chat-notification-logo-wrapper {
							flex-shrink: 0;
						}
						.chat-notification-logo {
							height: 3rem;
							width: 3rem;
						}
						.chat-notification-content {
							margin-left: 1.5rem;
							padding-top: 0.25rem;
						}
						.chat-notification-title {
							color: #1a202c;
							font-size: 1.25rem;
							line-height: 1.25;
						}
						.chat-notification-message {
							color: #718096;
							font-size: 1rem;
							line-height: 1.5;
						}
					<\/style>
				`}

        </Code>
    </Slide>
    <Slide>
        <h5>
            Using utility classes to build custom designs without writing CSS
        </h5>

        <div class="font-['sans-serif'] font-normal text-base relative rounded-xl overflow-auto p-8">
            <div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
                <div class="shrink-0">
                    <img alt="ChitChat Logo" class="h-12 w-12" src={chatLogo}>
                </div>
                <div>
                    <div class="text-xl font-medium text-black">ChitChat</div>
                    <p class="text-slate-500">You have a new message!</p>
                </div>
            </div>
        </div>
        <Code lang="html">
            {`<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
    <div class="shrink-0">
        <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
    </div>
    <div>
        <div class="text-xl font-medium text-black">ChitChat</div>
        <p class="text-slate-500">You have a new message!</p>
    </div>
</div>
				`}
        </Code>
    </Slide>
    <Slide iframe="https://play.tailwindcss.com/">
        <Notes>
            <p>
                Instead of using the card class like you might in Bootstrap, you combine
                utility classes like flex to make it a flexbox, p to give it a padding,
                m for margin, and others like color, shadows. In addition, every utility
                can be applied conditionally. You have variants like small, medium and
                large for responsive designs along with pseudo-selectors like hover and
                focus to handle state changes, or dark to render different colors when
                dark mode is enabled.
            </p>
            <ol>
                <li>text-green-500</li>
                <li>md:text-blue-500</li>
                <li>hover:uppercase</li>
                <li>dark:bg-black</li>
                <li>first-letter:font-bold</li>
                <li>first-letter:font-bold first-letter:text-4xl</li>
                <li>hover:first-letter:font-bold</li>
                <li>selection:bg-red-500"</li>
            </ol>
            <p>
                However, it does produce some ugly ass html,
                you've got tons of hard-to-read duplicate class names. As your UI grows
                in complexity, code duplication is inevitable. But you can avoid it by
                creating reusable components with CSS-in-JS like styled-components, or
                by using the apply directive in css to take tailwind classes and compose
                them into a single concise class name. Tailwind also has a 'purge'
                feature that removes any unused utility from the final bundle resulting
                in minimal dead code and thus faster page loads.
            </p>
        </Notes>
    </Slide>
    <Slide iframe="https://tailwindcss.com/showcase">
    </Slide>
    <Slide>
        <h1>CSS-in-JS</h1>

        <Notes>
            CSS-in-JavaScript libraries, in a nutshell, allows you to write CSS inside JavaScript. But why?

            <ol>Collision-free selectors -- Styles are written exclusively for one component, so they are effectively
                local in scope. This avoids the issue of duplicate selectors on different CSS files.
            </ol>
            <ol>Dynamic styling -- you can leverage the power of JS, you can use prop values or variables inside the
                styles, instead of writing separate CSS styles for each variation.
            </ol>
            <ol>Code reuse -- since we're building components, these components can be reused without duplicating CSS
                rules
            </ol>
        </Notes>
    </Slide>
    <Slide>
        <h1>Styled Components</h1>

        <Step>
            <Code class="mt-5" lang="jsx">
                {`
                import styled from 'styled-components';

                const StyledButton = styled.button\`
                  background-color: #3498db;
                  color: white;
                  padding: 0.5rem 1rem;
                  border: none;
                  border-radius: 0.25rem;
                \`;

                const App = () => (
                  <StyledButton>Styled Button</StyledButton>
                );
                `}
            </Code>
        </Step>
        <Notes>The first thing that probably comes to mind to most when they hear "CSS-in-JS". This is the most popular
            CSS-in-JS today. It lets you
            define styles as components themselves, facilitating component-level styling and dynamic theming.
        </Notes>
    </Slide>
    <Slide iframe="https://stackblitz.com/edit/stackblitz-starters-cnzxmg?ctl=1&embed=1&file=src%2FApp.js">

    </Slide>
    <Slide>
        <h1>Takeaways</h1>

        <Notes>
            We've explored how Tailwind CSS empowers you to style your app with utility classes. Coupled with CSS-in-JS
            libraries like styled-components,
            we've witnessed the rise of component-level styling. Don't think that these tools are mutually exclusive,
            you can mix and match any way you want to style your app. Some CSS-purist push back
            because ayaw nila ng CSS sa loob ng HTML (na ginagawa ng Tailwind), or ayaw nila ng CSS sa loob ng
            JavaScript. At the end of the day,
            everyone has their own preference. And most of the time, clients don't care how you made your app, but what
            the end-result is.
            And these tools can help you create adaptive, maintainable, and beautifully styled user interface.


            <ol>
                <li>Ant Design - ant.design</li>
                <li>Material Design - mui.com</li>
                <li>Rebass - rebassjs.org</li>
                <li>Chakra - chakra-ui.com</li>
                <li>Tamagui - tamagui.dev</li>
            </ol>
        </Notes>
    </Slide>
</Vertical>

<style>
    .chat-notification {
        display: flex;
        max-width: 24rem;
        margin: 0 auto;
        padding: 1.5rem;
        border-radius: 0.5rem;
        background-color: #fff;
        box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
        0 10px 10px -5px rgba(0, 0, 0, 0.04);
        font-family: sans-serif;
    }

    .chat-notification-logo-wrapper {
        flex-shrink: 0;
    }

    .chat-notification-logo {
        height: 3rem;
        width: 3rem;
    }

    .chat-notification-content {
        margin-left: 1.5rem;
        padding-top: 0.25rem;
    }

    .chat-notification-title {
        color: #1a202c;
        font-size: 1.25rem;
        line-height: 1.25;
    }

    .chat-notification-message {
        color: #718096;
        font-size: 1rem;
        line-height: 1.5;
    }
</style>