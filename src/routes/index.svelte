<script lang="ts">
	import { parse } from 'speclang';

	let input = `test {
    hello world {}
    foo = "bar"
  }`;
	let output: string;

	async function test() {
		output = await parse(input);
	}
</script>

<main>
	<h1>Specific Language REPL</h1>
	<div>
		<textarea bind:value={input} rows="12" />
		<button on:click={test}>parse</button>
	</div>
	<hr />
	<pre>{output}</pre>
</main>
