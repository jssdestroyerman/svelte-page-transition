<script lang="ts">
	import { gsap } from 'gsap';

	function anim(node: any) {
		gsap.from(node, {
			x: -160,
			delay: 1
		});
		return {};
	}
	function animOut(node: any) {
		gsap.to(node, {
			x: -160,
			duration: 1
		});
		return {
			/* GSAP's duration is in seconds. Svelte's is in miliseconds */
			duration: 1 * 1000
		};
	}
</script>

<div in:anim out:animOut>
	<h1>about page</h1>
	<a href="/">home page</a>
</div>

<style>
	div {
		color: red;
	}
</style>
