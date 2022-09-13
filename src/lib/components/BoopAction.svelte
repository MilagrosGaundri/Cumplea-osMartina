<script lang="ts">
	import boop from '$lib/js/boop.js';
	export let boopParams:any;
	let isBooped = false;
	
	// Is there a more Svelte-y way to do this?
	function setIsBooped(val:any) {
		isBooped = val;
	}
	
	function triggerBoop() {
		isBooped = true;
	}
</script>

<!-- trigger onclick so demo works on mobile -->
<span on:focus={triggerBoop} on:click={triggerBoop}  use:boop={{isBooped, ...boopParams, setter: setIsBooped}}>
	<slot/>
</span>