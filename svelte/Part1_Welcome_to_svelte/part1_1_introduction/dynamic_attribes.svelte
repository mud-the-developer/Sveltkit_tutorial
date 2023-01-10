<script>
	let src = '/image.gif';
	let name = 'Rick Astley';
</script>

<img src={src}/>
<!-- img element should have an alt attribute -->
<img src={src} alt="A man dances."/>

<img {src} alt="A man dances." />
<!-- if name and value is same, can use {name} -->

<img {src} alt="{name} dances." />