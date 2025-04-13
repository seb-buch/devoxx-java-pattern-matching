<script>
	import Slide from '$lib/Slide.svelte';
	import background from './assets/titleBackground.png';
	import qrCode from './assets/qr-code-presentation.png';
	import feedback from './assets/qr-code-feedback.png';
	import VerticalSpacer from '$lib/VerticalSpacer.svelte';
</script>

<style>

  div {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 1em;

    figure {
      figcaption {
        font-size: 0.8em;
      }

      img {
        max-width: 300px;
        max-height: 300px;
      }
    }
  }

  p.speaker {
    position: absolute;

    a {
      color: var(--r-heading-color);
    }

    bottom: 10px;
    right: 10px;
  }

</style>

<Slide backgroundImage="{background}" leftMargin="400px">
	<VerticalSpacer height="200px" />
	<h1>Merci !</h1>
	<div class="container">
		<figure>
			<img src="{qrCode}" alt="QRcode">
			<figcaption>
				La présentation
			</figcaption>
		</figure>
		<figure>
			<img src="{feedback}" alt="QRcodeFeedback">
			<figcaption>
				Le feedback&nbsp;(session <a
				href="https://mobile.devoxx.com/events/devoxxfr2025/rate-talk/72573"
				target="_blank">#72573</a>)
			</figcaption>
		</figure>
	</div>
	<p class="speaker"><a href="mailto:s.buchoux@groupeonepoint.com">s.buchoux@groupeonepoint.com</a>
	</p>
</Slide>
