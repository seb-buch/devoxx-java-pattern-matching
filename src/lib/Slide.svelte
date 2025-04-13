<script lang="ts">
	import type { Options } from 'reveal.js';
	import type { Snippet } from 'svelte';

	interface Props {
		transitionStyle?: Required<Options>['transition'] | null,
		transitionSpeed?: Required<Options>['transitionSpeed'] | null,
		autoAnimate?: boolean | null;
		autoAnimateID?: string | null;
		autoAnimateRestart?: boolean | null;
		backgroundImage?: string | null;
		backgroundSize?: 'cover' | null;
		leftMargin?: string;
		children: Snippet;
	}

	let {
		transitionStyle = null,
		transitionSpeed = null,
		children,
		autoAnimate = null,
		autoAnimateRestart = null,
		autoAnimateID = null,
		backgroundImage = null,
		backgroundSize = 'cover',
		leftMargin = '0px'
	}: Props = $props();

</script>
<style>
  section {
    --left-margin: 200px;
    height: 100%;

  }

  div {
    padding-left: var(--left-margin);
    width: calc(100% - var(--left-margin));
  }
</style>
<section data-transition="{transitionStyle}" data-transition-speed="{transitionSpeed}"
				 data-auto-animate={autoAnimate}
				 data-auto-animate-id="{autoAnimateID}" data-auto-animate-restart={autoAnimateRestart}
				 data-background-image={backgroundImage} data-background-size={backgroundSize}>
	<div style="width: calc(100% - {leftMargin}); padding-left: {leftMargin};">
		{@render children()}
	</div>
</section>
