<script setup>
    import {Notes, Slide, Step} from '@components';
</script>


<Slide>
    <h1>Q&A</h1>

    <Step>
    <ol>
        <li>What are the benefits of using JavaScript frameworks for web development?</li>
        <li>How do I choose the best JavaScript framework for my project?</li>
        <li>What is Tailwind CSS and how does it differ from other CSS frameworks?</li>
        <li>What is CSS-in-JS and why should I use it?</li>
        <li>What are PWAs and what are their advantages?</li>
    </ol>
    </Step>

    <Notes>
        <ol>
            <li>JavaScript frameworks provide a structured and organized way of creating dynamic and interactive web
                applications. They offer features such as data binding, routing, state management, component-based
                architecture, and code reuse that make web development faster, easier, and more maintainable.
            </li>
            <li>
                There is no definitive answer to this question, as different frameworks have different strengths and
                weaknesses, and the best choice depends on your project requirements, preferences, and experience.
                However, some general factors to consider are:

                - The size and complexity of your project: Larger and more complex projects may benefit from more robust and mature frameworks like Angular or React, while smaller and simpler projects may prefer lighter and faster frameworks like Vue or Svelte.
                - The learning curve and documentation of the framework: Some frameworks have a steeper learning curve than others, depending on your familiarity with the concepts and syntax they use. You should also check the quality and availability of the documentation and tutorials for the framework you want to learn.
                - The popularity and community support of the framework: More popular frameworks tend to have more resources, libraries, tools, and developers available to help you with your project. You can check the popularity of a framework by looking at its GitHub stars, npm downloads, Stack Overflow questions, etc.
                - The performance and compatibility of the framework: Different frameworks have different approaches to rendering, updating, and optimizing the user interface. You should test the performance of your framework on different browsers, devices, and network conditions, and compare it with other frameworks using tools like Lighthouse or WebPageTest.
                - The future prospects and updates of the framework: You should also consider the stability and innovation of the framework you choose. How often does it release new versions? How backward-compatible are they? How well does it adapt to new web standards and technologies?
            </li>
            <li>
                Tailwind CSS is a utility-first CSS framework that provides low-level classes that can be composed to
                create any design. Unlike other CSS frameworks that provide predefined components and styles, Tailwind
                CSS gives you full control over the appearance and behavior of your elements. Tailwind CSS also
                integrates well with JavaScript frameworks and supports responsive design, dark mode, custom theming,
                and more.

                - It reduces the amount of CSS code you have to write by providing a set of utility classes that cover most common use cases.
                - It allows you to customize your design without having to override or modify the framework's classes or variables.
                - It encourages consistency and scalability by following a design system based on spacing, colors, typography, etc.
                - It enables rapid prototyping and iteration by allowing you to change your design directly in your HTML code.
            </li>
            <li>
                CSS-in-JS is a technique that allows you to write CSS code inside your JavaScript files, using either
                inline styles or tagged template literals. This way, you can scope your styles to specific components,
                avoid naming conflicts, use dynamic values based on props or state, and leverage the power of JavaScript
                for styling logic. CSS-in-JS also enables code splitting, server-side rendering, and automatic vendor
                prefixing.

                - It improves the modularity and reusability of your components by keeping your styles together with your logic and markup.
                - It eliminates the need for external style sheets or preprocessors like Sass or Less.
                - It allows you to use JavaScript features like variables, functions, loops, conditionals, etc. for writing complex styles.
                - It supports dynamic theming and styling based on user input or context.
            </li>
            <li>PWAs are Progressive Web Apps that combine the best of web and native apps. They are web applications
                that can be installed on your device, work offline, send push notifications, access device features, and
                provide a native-like user experience. PWAs are fast, reliable, and engaging, and can help you reach a
                wider audience, increase user retention, and improve conversion rates.

                - They are cross-platform and cross-browser compatible. You only need to write one codebase for all devices and browsers.
                - They are easy to install and update. Users can install them from their browser without having to go through an app store or download anything.
                - They are resilient to network conditions. They can work offline or on low-quality networks using service workers and caching strategies.
                - They are immersive and interactive. They can use native features like camera, microphone, geolocation, etc., as well as web APIs like Web Push, Web Share, Web Payments, etc.
                - They are discoverable and shareable. They can be indexed by search engines, linked from social media, and shared via QR codes or URLs.
            </li>
        </ol>
    </Notes>
</Slide>
