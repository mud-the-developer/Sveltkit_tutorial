<script>
	import Inner from './Inner.svelte';

	function handleMessage(event) {
		alert(event.detail.text);
	}
</script>

<Inner on:message={handleMessage} />


<!-- You can also try changing the event name to something else. 
    For instance, change dispatch('message') to dispatch('myevent') in Inner.svelte and 
    change the attribute name from on:message to on:myevent in the App.svelte component. -->