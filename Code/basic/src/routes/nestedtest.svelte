<script>
	export let answer = "Unset default value";
	let test = answer;
	let count = 0;
	$: doubled = count * 2;
  $: console.log(`the count is ${count}`);
  $: {
    console.log(`the count is ${count}`);
    console.log(`this will also be logged whenever count changes`);
  }
  $: if (count >= 10) {
		alert('count is dangerously high!');
		count = 0;
	}
	function increment() {
		count += 1;
	}
</script>

<button on:click={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>
<p>{count} doubled is {doubled}</p>
<p>The answer is {answer}</p>
<p>The answer is {test}</p>
