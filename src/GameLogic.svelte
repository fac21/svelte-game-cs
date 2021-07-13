{#if user.loggedIn}
	<button on:click={toggle}>
		Log out
	</button>
{:else}
	<button on:click={toggle}>
		Log in
	</button>
{/if}

<!-- If cards match:{#if }
hide both
disappear cards
increment counter by 1

Else if cards do not match: {:else }
alert "Try again"
hide both cards
do not disappear cards
no increment -->
