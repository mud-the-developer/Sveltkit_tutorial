<script>
	import { count } from './writable_stores.js';

	function reset() {
		count.set(0);
	}
</script>

<button on:click={reset}> reset </button>
