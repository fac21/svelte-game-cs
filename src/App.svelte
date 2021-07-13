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
	<button> Start Game</button>
	<button on:click={incrementCount}>
	 {count} {count === 1 ? 'move' : 'moves'}
	</button>
	<!-- <button> Start Game</button>

{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{:else}
	<button on:click={toggle}>
		Log in
	</button>
{/if} -->

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
button {
		background: #E2E8F0;
		color: #64748B;
		border: unset;
		border-radius: 6px;
		padding: .75rem 1.5rem;
		cursor: pointer;
        margin:0.25rem;


	}
	button:hover {
		background: #CBD5E1;
		color: #475569;
	}
	button:focus {
		background: #94A3B8;
		color: #F1F5F9;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
