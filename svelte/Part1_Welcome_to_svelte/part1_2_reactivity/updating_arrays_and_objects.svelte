<script>
	let numbers = [1, 2, 3, 4];

	function addNumber() {
		// numbers.push(numbers.length + 1);
    // numbers = numbers;
    numbers = [...numbers, numbers.length + 1] //But there's a more idiomatic solution:
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
  // You can use similar patterns to replace pop, shift, unshift and splice.


</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
	Add a number
</button>
