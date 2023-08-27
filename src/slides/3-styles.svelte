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
        <div class="bg-black bg-opacity-30 text-3xl p-3">
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
        <h5>Using utility classes to build custom designs without writing CSS</h5>

        <div
                class="font-['sans-serif'] font-normal text-base relative rounded-xl overflow-auto p-8"
        >
            <div
                    class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4"
            >
                <div class="shrink-0">
                    <img alt="ChitChat Logo" class="h-12 w-12" src={chatLogo}/>
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

        <Notes
        >In the example above, we’ve used: Tailwind’s flexbox and padding
            utilities (flex, shrink-0, and p-6) to control the overall card layout
            <ul>
                <li>
                    The max-width and margin utilities (max-w-sm and mx-auto) to constrain
                    the card width and center it horizontally
                </li>
                <li>
                    The background color, border radius, and box-shadow utilities
                    (bg-white, rounded-xl, and shadow-lg) to style the card’s appearance
                </li>
                <li>
                    The width and height utilities (w-12 and h-12) to size the logo image
                </li>
                <li>
                    The space-between utilities (space-x-4) to handle the spacing between
                    the logo and the text
                </li>
                <li>
                    The font size, text color, and font-weight utilities (text-xl,
                    text-black, font-medium, etc.) to style the card text
                </li>
                <li>
                    This approach allows us to implement a completely custom component
                    design without writing a single line of custom CSS.
                </li>
            </ul>

            Now I know what you’re thinking, “this is an atrocity, what a horrible
            mess!” and you’re right, it’s kind of ugly. In fact it’s just about
            impossible to think this is a good idea the first time you see it — you
            have to actually try it. But once you’ve actually built something this
            way, you’ll quickly notice some really important benefits: You aren’t
            wasting energy inventing class names. No more adding silly class names
            like sidebar-inner-wrapper just to be able to style something, and no more
            agonizing over the perfect abstract name for something that’s really just
            a flex container. Your CSS stops growing. Using a traditional approach,
            your CSS files get bigger every time you add a new feature. With
            utilities, everything is reusable so you rarely need to write new CSS.
            Making changes feels safer. CSS is global and you never know what you’re
            breaking when you make a change. Classes in your HTML are local, so you
            can change them without worrying about something else breaking. When you
            realize how productive you can be working exclusively in HTML with
            predefined utility classes, working any other way will feel like torture.
        </Notes>
    </Slide>
    <Slide iframe="https://play.tailwindcss.com/">
        <Notes>
            <p>
                You combine utility classes like flex to make it a flexbox, p to give it
                a padding, m for margin, and others like color, shadows. In addition,
                every utility can be applied conditionally. You have variants like
                small, medium and large for responsive designs along with
                pseudo-selectors like hover and focus to handle state changes, or dark
                to render different colors when dark mode is enabled.
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
            <div>
                A common reaction to this approach is wondering, “isn’t this just inline
                styles?” and in some ways it is — you’re applying styles directly to
                elements instead of assigning them a class name and then styling that
                class. But using utility classes has a few important advantages over
                inline styles:

                <ul>
                    <li>
                        Designing with constraints. Using inline styles, every value is a
                        magic number. With utilities, you’re choosing styles from a
                        predefined design system, which makes it much easier to build
                        visually consistent UIs.
                    </li>
                    <li>
                        Responsive design. You can’t use media queries in inline styles, but
                        you can use Tailwind’s responsive utilities to build fully
                        responsive interfaces easily.
                    </li>
                    <li>
                        Hover, focus, and other states. Inline styles can’t target states
                        like hover or focus, but Tailwind’s state variants make it easy to
                        style those states with utility classes.
                    </li>
                </ul>
            </div>
            <p>
                However, it does produce some ugly ass html, you've got tons of
                hard-to-read duplicate class names. As your UI grows in complexity, code
                duplication is inevitable. But you can avoid it by creating reusable
                components with CSS-in-JS like styled-components, or by using the apply
                directive in css to take tailwind classes and compose them into a single
                concise class name.
            </p>
        </Notes>
    </Slide>
    <Slide iframe="https://tailwindcss.com/showcase"></Slide>
    <Slide>
        <h1>CSS-in-JS</h1>

        <Step order="0" type="table">
            <thead>
            <tr>
                <th>Pros</th>
                <th>Cons</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <Step fadeRight order="1" type="td">Scoping</Step>
                <Step fadeLeft order="4" type="td">Performance</Step>
            </tr>
            <tr>
                <Step fadeRight order="2" type="td">Dynamic Styling</Step>
                <Step fadeLeft order="5" type="td">Learning curve</Step>
            </tr>
            <tr>
                <Step fadeRight order="3" type="td">Modularity</Step>
                <Step fadeLeft order="6" type="td">Compatibility</Step>
            </tr>
            </tbody>
        </Step>

        <Notes>
            We know CSS can be written inside CSS files. Also, as inner styles or
            class names inside HTML, just as we saw in Tailwind. But did you know that
            we can also write CSS inside JavaScript files? CSS-in-JavaScript
            libraries, in a nutshell, allows you to write CSS inside JavaScript,
            instead of using separate CSS files. It has some benefits and drawbacks,
            depending on the context and preferences of the developers. Here are some
            of the main reasons why you might want to use CSS-in-JS:

            Pros:
            <ol>
                <li>
                    Scoping: CSS-in-JS libraries can generate unique class names for
                    each component, avoiding the problem of global namespace pollution and
                    style conflicts. This makes it easier to maintain and debug the
                    styles, as well as to reuse components across different projects.
                </li>
                <li>
                    Dynamic styling: you can leverage the power of JS, you can use prop
                    values or variables inside the styles, instead of writing separate CSS
                    styles for each variation. As CSS-in-JS is essentially JavaScript
                    code, you can apply complex logic to your style rules, such as loops,
                    conditionals, variables, state-based styling, and more. Therefore,
                    it’s an ideal solution if you need to create a complicated UI that
                    requires dynamic functionality.
                </li>
                <li>
                    Modularity: CSS-in-JS makes it simple to
                    include styles with components. And this is actually a huge benefit.
                    Nobody likes maintaining entirely separate file trees just for their
                    CSS, or managing CSS files which live in completely separate locations
                    to their corresponding JSX. By bundling the styles with the
                    components, you can achieve better code organization and portability.
                </li>
            </ol>

            Cons:
            <ol>
                <li> Performance: CSS-in-JS libraries may add some overhead to the rendering process, as they need to
                    parse and inject the styles into the DOM at runtime. This can affect the performance and user
                    experience of your app, especially if you have a lot of components or complex styles. Some libraries
                    offer solutions to mitigate this issue, such as server-side rendering or static extraction2.
                </li>
                <li>Learning curve: CSS-in-JS libraries have different syntaxes and APIs than plain CSS. This means that
                    you
                    need to learn a new way of writing styles, which may not be intuitive or familiar to you. Moreover,
                    there
                    are many CSS-in-JS libraries available, each with its own pros and cons3. You need to choose the one
                    that
                    suits your needs and preferences best, which can be overwhelming and time-consuming.
                </li>
                <li>Compatibility: CSS-in-JS libraries may not support all the features and properties of CSS, such as
                    pseudo-elements, media queries, animations, etc. You may need to use additional tools or workarounds
                    to
                    achieve the desired effects. Also, some libraries may not work well with certain JavaScript
                    frameworks or
                    libraries3. You need to check the compatibility and interoperability of your chosen library before
                    using it.
                </li>
            </ol>

            <p>
                In conclusion, CSS-in-JS is a powerful and flexible technique for styling web components, but it also
                comes with some trade-offs. You should weigh the pros and cons carefully before deciding whether to use
                it or not. To learn more about CSS-in-JS, let's explore one of the most popular CSS-in-JS libraries
                today.
            </p>
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
        <Notes
        >The first thing that probably comes to mind to most when they hear
            "CSS-in-JS". This is the most popular CSS-in-JS today. It lets you define
            styles as components themselves, facilitating component-level styling and
            dynamic theming.
        </Notes>
    </Slide>
    <Slide
            iframe="https://stackblitz.com/edit/stackblitz-starters-bcvkzp?ctl=1&embed=1&file=src%2FApp.js"
    ></Slide>
    <Slide>
        <h1>Takeaways</h1>

        <Notes>
            We've explored how Tailwind CSS empowers you to style your app with
            utility classes. Coupled with CSS-in-JS libraries like styled-components,
            we've witnessed the rise of component-level styling. Don't think that
            these tools are mutually exclusive, you can mix and match any way you want
            to style your app. You can combine using Tailwind, style-components, or CSS in your React app. Some
            CSS-purist push back because ayaw nila ng CSS sa
            loob ng HTML (na ginagawa ng Tailwind), or ayaw nila ng CSS sa loob ng
            JavaScript. At the end of the day, everyone has their own preference. Kung ano sa tingin mo mas magpapadali
            sayo or sa mas comfortable ka gawin, go. And
            most of the time, clients don't care how you made your app, but what the
            end-result is. And these tools can help you create adaptive, maintainable,
            and beautifully styled user interface.
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
