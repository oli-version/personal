<script>
	import Contact from './Contact.svelte';
	import Madlibs from './Madlibs.svelte';
	import Age from './Age.svelte';
	let name = 'Oliver';
	let nick = 'zlby';
	let user = '';
</script>

<svelte:head>
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/fork-awesome@1.2.0/css/fork-awesome.min.css" integrity="sha256-XoaMnoYC5TH6/+ihMEnospgm0J1PM/nioxbOUdnM8HY=" crossorigin="anonymous">
</svelte:head>

<main>
	{#if user === ''}
		<h1>Let me introduce myself</h1>
		<p>Hello [your name], my name is {name}, but you might know me as {nick}</p>
	{:else if user !== ''}
		<h1>Let me introduce myself</h1>
		<p>Hello {user}, my name is {name}, but you might know me as {nick}</p>
	{/if}
	<input bind:value={user} placeholder="your name">
</main>
<br>
<br>
<br>
<Contact/>
<!-- <br>
<br>
<br>
<Madlibs/> -->
<br>
<br>
<br>
<Age/>

<style>

</style>