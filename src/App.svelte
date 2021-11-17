<script>
	import Contact from './Contact.svelte';
	import Madlibs from './Madlibs.svelte';
	import Age from './Age.svelte';
	import About from './About.svelte';
	import Hobies from './Hobies.svelte';
	import Server from './Server.svelte';
	let name = 'Oliver';
	let nick = 'zlby';
	let user = '';
	let setName = false;
	let target = '_blank'

	function setN() {
		setName = true;
	}
</script>

<svelte:head>
	<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/fork-awesome@1.2.0/css/fork-awesome.min.css" integrity="sha256-XoaMnoYC5TH6/+ihMEnospgm0J1PM/nioxbOUdnM8HY=" crossorigin="anonymous">
</svelte:head>

<main>
	<center>
		<h1>Under Construction</h1>
	</center>
	<!-- {#if setName === true}
		<h1>Welcome to my wierd world</h1>
		<p>Hello {user}, welcome to my website. I often remake my website every ½ month,<br>but I'm hoping this one will stay.
		The reason this one should stay is because<br>it is made with <a href="https://svelte.dev">svelte</a>. On this website
		you can learn about me and my interests.
		</p>
		<br>
		<br>
		<About/>
		<br>
		<br>
		<Hobies/>
		<br>
		<br>
		<Server/>
	{:else if setName === false}
		<center>
			<p>Your Name:</p>
			<input type="text" placeholder="name" bind:value={user}>
			<br><button style="width: 175px;" on:click={setN}>Continue</button>
		</center>
	{/if}
	{#if user === ''}
		<h1>Let me introduce myself</h1>
		<p>Hello [your name], my name is {name}, but you might know me as {nick}</p>
	{:else if user !== ''}
		<h1>Let me introduce myself</h1>
		<p>Hello {user}, my name is {name}, but you might know me as {nick}</p>
	{/if}
	<input bind:value={user} placeholder="your name">
	<div class="footer">
		Made with <i class="fa fa-heart"></i> by zlby <br>
		Source code <a href="https://github.com/zlbyapi/personal">on github</a>
	</div>-->
</main>
<!-- <br>
<br>
<br>
<Contact/>
<br>
<br>
<br>
<Madlibs/>
<br>
<br>
<br>
<Age/> -->

<style>

</style>