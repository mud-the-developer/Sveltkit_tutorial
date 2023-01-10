<script>
	import { count } from './writable_stores.js';

	function increment() {
		count.update((n)=>n+1);
	}
</script>

<button on:click={increment}> + </button>
