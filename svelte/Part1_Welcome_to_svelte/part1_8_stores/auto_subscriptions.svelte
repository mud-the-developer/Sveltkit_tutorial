<!-- The app in the previous example works, but there's a subtle bug
     — the store is subscribed to, but never unsubscribed.
      If the component was instantiated and destroyed many times,
       this would result in a memory leak. -->

<script>
	import { onDestroy } from 'svelte'
	import { count } from './writable_stores.js';
	import Incrementer from './Incrementer.svelte';
	import Decrementer from './Decrementer.svelte';
	import Resetter from './Resetter.svelte';

	let count_value;

	const unsubscribe = count.subscribe((value) => {
		count_value = value;
	});
	onDestroy(unsubscribe);
</script>

<h1>The count is {count_value}</h1>

<Incrementer />
<Decrementer />
<Resetter />
