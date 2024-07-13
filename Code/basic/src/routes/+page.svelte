<script>
	import Nested from './nestedtest.svelte';
	let src = '/static/favicon.png';
	let name = 'Svelte';
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<img {src} alt="{name} dances." />
<h1>Hello {name.toUpperCase()}!</h1>
<p>{@html string}</p>
<Nested answer={42} /> 
<Nested {...{answer: 42}} />
