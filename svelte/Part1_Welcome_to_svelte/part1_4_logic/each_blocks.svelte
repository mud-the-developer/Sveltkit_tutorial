<script>
	let cats = [
		{
			id: 'J---aiyznGQ',
			name: 'Keyboard Cat'
		},
		{
			id: 'z_AbfPXTKms',
			name: 'Maru'
		},
		{
			id: 'OUtn3pvWmpg',
			name: 'Henri The Existential Cat'
		}
	];
</script>

<h1>The Famous Cats of YouTube</h1>

<!-- <ul>
	{#each cats as cat}
	<li>
		<a
			target="_blank"
			href="https://www.youtube.com/watch?v={cat.id}"
		>
			{cat.name}
		</a>
	</li>
	{/each}
</ul> -->

<!-- You can get the current index as a second argument, like so: 
<ul>
	{#each cats as cat,i}
	<li>
		<a
			target="_blank"
			href="https://www.youtube.com/watch?v={cat.id}"
		>
			{i+1}: {cat.name}
		</a>
	</li>
	{/each}
</ul> -->

<!-- each cats as { id, name } — and replace cat.id and cat.name with id and name. -->
	{#each cats as {id, name},i}
	<li>
		<a
			target="_blank"
			href="https://www.youtube.com/watch?v={id}"
		>
			{i+1}: {name}
		</a>
	</li>
	{/each}