<script lang="ts">
    import {Notes, Slide, Step, Vertical} from '@components'
</script>

<Vertical>
    <Slide animate>
        <div class="bg-black bg-opacity-30 text-3xl p-3">
            <h1>Progressive Web Apps (PWAs)</h1>
            <sub>Elevating User Experience with Progressive Web Apps</sub>
        </div>
    </Slide>
    <Slide animate>
        <div class="bg-black bg-opacity-30 text-3xl p-3">
            <h1>Progressive Web Apps (PWAs)</h1>
            <sub>Elevating User Experience with Progressive Web Apps</sub>
        </div>
        <Step class="mt-5 bg-black bg-opacity-30">PWAs use web technologies like HTML, CSS, JavaScript, WebAssembly* to
            create
            native-like experiences for users.
        </Step>
        <Step class="bg-black bg-opacity-30">PWAs can work offline, send push notifications, access hardware features,
            and run in web browsers, just like websites.
        </Step>
        <Step class="bg-black bg-opacity-30">PWAs can be published online via HTTPS, or optionally submitted to app
            stores like Microsoft Store, Apple App Store, or Google Play.
        </Step>
        <Step class="bg-black bg-opacity-30">PWAs have lower development cost and maintenance than traditional apps, as
            they share one codebase across platforms.
        </Step>

        <Notes>
            <ol>
                <li>(read quote) Esentially, PWAs are web apps, which functions like a native app. They are made in the
                    same way.
                    WebAssembly is a low-level assembly-like
                    language that can be run on the browser. You can write code with C,C++,C#, Java, Rust and compile it
                    to WebAssembly. I was gonna cover this in this presentation pero medyo
                    mahaba na kaya maybe next, I'd love to discuss this further.
                </li>
                <li>(step first) Because PWAs are like native apps, they can do these things (read quote)</li>
                <li>PWAs can be installed on your desktop or mobile using your browser or from app stores</li>
                <li>PWAs are made from HTML, CSS and JS, one codebase that can work any device, from mobile through
                    desktop
                </li>
            </ol>
        </Notes>
    </Slide>
    <Slide transition="slide">
        <h2>Core requirements</h2>
        <div class="bg-black bg-opacity-20">
            <ul>
                <li>an app is generally considered a PWA if it:
                    <ol>
                        <li>runs over HTTPS</li>
                        <li>has a manifest.json file</li>
                        <li>has a service worker</li>
                        <li>is responsive, smooth and "app-like"</li>
                    </ol>
                </li>
                <li>a <span class="text-green-700">good</span> PWA will be able to run while offline by caching core
                    assets (HTML, CSS, JS, logos, etc.)
                </li>
            </ul>
        </div>
    </Slide>
    <Slide>
        <h1>Let's make a PWA!</h1>
    </Slide>
</Vertical>
