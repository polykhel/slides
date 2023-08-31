<script lang="ts">
	import { Presentation, Slide, Notes } from '@components'
	import Introduction from './slides/1-introduction.svelte'
	import Javascript from './slides/2-javascript.svelte'
	import Styles from './slides/3-styles.svelte'
	import PWA from './slides/4-pwa.svelte'
</script>

<Presentation>
	<Introduction/>
	<Javascript />
	<Styles />
	<PWA />
	<Slide>
		<h1>Hit me up!</h1>
		<p>https://www.linkedin.com/in/mpollente/</p>
		<p>https://twitter.com/polypollens</p>
		<Notes>
			<p>
				If you remember my introduction kanina, I said na I'm passionate about
				sharing my knowledge, and I really mean it. So if ever nahihirapan ka na, or nawawalan ka na
				ng gana sa coding kasi nga sobrang hirap ka na, I can help you. Whether
				sa technical questions or need mo lang ng advice on how to proceed, I'm
				always game.
			</p>
		</Notes>
	</Slide>
	<Slide>
		<h1>FAQs</h1>

        <ol>
            <li>Don't be a frameworker, be an engineer</li>
        </ol>
	</Slide>
</Presentation>
