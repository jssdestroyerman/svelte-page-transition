<script lang="ts">
	import { gsap } from 'gsap';

	function spin(node: any) {
		gsap.to(node, {
			rotate: 1080
		});
		return {};
	}
	function spinOut(node: any) {
		gsap.to(node, {
			rotate: -1080
		});
		return {};
	}
</script>

<div class="centered" in:spin out:spinOut>
	<span>transitions!</span>
</div>
<a href="/about">about page</a>

<style>
	.centered {
		position: absolute;
		left: 50%;
		top: 50%;
		transform: translate(-50%, -50%);
	}

	span {
		position: absolute;
		transform: translate(-50%, -50%);
		font-size: 4em;
	}
</style>
