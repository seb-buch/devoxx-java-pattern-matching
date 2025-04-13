<script>
	import Slide from '$lib/Slide.svelte';
	import background from './assets/titleBackground.png';
</script>

<style>
  div {
    position: relative;
    height: 600px;
    width: calc(100% - 650px);
    margin-left: 650px;
    margin-top: 200px;
  }

  p.title {
    font-family: var(--r-heading-font), sans-serif;
    color: var(--r-heading-color);
    font-weight: normal;
    text-transform: none;
    font-size: 72px;
  }

  p {
    color: var(--r-main-color);
    text-align: left;
  }

  p.right {
    margin-left: calc(100% - 550px);
    text-transform: uppercase;
  }

  p.speaker {
    padding-top: 3em;
  }

  p.company {
    padding-top: 0.5em;
    color: var(--r-heading-color);
  }

  p.pre-heading {
    font-size: 1.3em;
  }
</style>

<Slide backgroundImage="{background}">
	<div>
		<p class="pre-heading">Java &amp; Languages</p>
		<p class="title">Comment rendre son code Java plus expressif et robuste avec le pattern
			matching</p>
		<p class="speaker right">Sébastien Buchoux</p>
		<p class="company right">Onepoint</p>
	</div>
</Slide>
