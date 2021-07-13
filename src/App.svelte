<script>
	import Card from './Card.svelte';
	import Logo from './Logo.svelte';
	export let name;
		let count = 0;

	function incrementCount() {
		count += 1;
	}
		let user = { loggedIn: false };

	function toggle() {
		user.loggedIn = !user.loggedIn;
	}

</script>

<main>
    <header>
	<Logo/>
	  <h1>The Famous Cards of {name} </h1>

    </header>
	<p>Visit the <a href="https://github.com/fac21">FAC21 github repository</a> to view all the awsome projects they have created!</p>

	<button on:click={incrementCount}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
	</button>

{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{:else}
	<button on:click={toggle}>
		Log in
	</button>
{/if}
	<Card/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
