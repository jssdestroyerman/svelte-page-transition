<script lang="ts">
	import { gsap } from 'gsap';

	function anim(node: any) {
		gsap.from(node, {
			x: -100
		});
		return {};
	}
	function animOut(node: any) {
		gsap.to(node, {
			x: -100
		});
		return {};
	}
</script>

<div in:anim out:animOut>
	<h1>about page</h1>

	<a href="/">home page</a>
</div>
