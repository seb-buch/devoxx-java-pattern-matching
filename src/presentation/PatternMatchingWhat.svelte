<script>
	import Slide from '$lib/Slide.svelte';
	import VerticalSpacer from '$lib/VerticalSpacer.svelte';
	import background from './assets/slideBackground.png';
</script>

<style>
  ul {
    list-style-type: none;
  }

  p.arrow {
    font-size: 3em;
    color: var(--r-heading-color);
    padding: 0.5em 0;
  }
</style>

<Slide backgroundImage="{background}" leftMargin="200px;">
	<h3>C'est quoi le <em>pattern matching</em>&nbsp;?</h3>
	<VerticalSpacer height="2em;" />
	<p>
		Le <em>pattern matching</em> (filtrage par motif) est une fonctionnalité permettant
		de <b>vérifier</b> une <b>structure de données</b> et d'en <b>extraire</b> son contenu.
	</p>

	<p class="arrow fragment" data-fragment-index="1">&darr;</p>
	<p class="fragment" data-fragment-index="1">
		Le <em>pattern matching</em> est supporté par un langage de programmation s'il:
	</p>
	<ul>
		<li class="fragment">contient des <b>structures de données</b>...</li>
		<li class="fragment">... pouvant être <b>vérifier/extraites</b> à l'aide d'une syntaxe dédiée
		</li>
	</ul>
</Slide>
