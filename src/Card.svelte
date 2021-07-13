<script>
	let images = [
		{ id: '64862888', name: 'Chisha' },
		{ id: '69358550', name: 'Safia' },
        { id: '63958540', name: 'Antonio' },
		{ id: '72794385', name: 'Amy' },
        { id: '43413852', name: 'Gregor' },
		{ id: '56611067', name: 'Chun' },
        { id: '31373245', name: 'Jo' },
		{ id: '52172604', name: 'Nafisa' },
        { id: '54359248', name: 'Craig' },
		{ id: '23028288', name: 'Michael' },
        { id: '36102515', name: 'Maryam' },
        { id: '72445011', name: 'Mariya' },
        { id: '60395899', name: 'Neville' },
        { id: '57327617', name: 'Evgeny' },
        { id: '59439482', name: 'Saki' },
        { id: '9408641', name: 'Oli' },
        { id: '9094166', name: 'Oliver' },
        { id: '61861015', name: 'Rosie' },
        { id: '63476393', name: 'Sevda' },
        { id: '37059', name: 'Dan' },
        { id: '22013117', name: 'Yvonne' },
	];
    let totalImages = [...images,...images];

    let count = 0;
	function incrementCount() {
		count += 1;
	}
</script>

<main>
<h2> Test how good your memory is and match the pictures!</h2>

<ul>
	{#each totalImages as {id, name}, i}
        <button on:click={incrementCount}>
		<img src="https://avatars.githubusercontent.com/u/{id}?v=4" alt="{name}'s github profile picture">
			 <!-- {i+1} :{name} -->
            </button>
	{/each}
</ul>
</main>

<style>
    img{

    width: 100px;
    transition: all 0.3s ease;
	/* transform: rotateY(180deg); */

  /* aspect-ratio: 1/1; */
  /* object-fit: cover; */
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
</style>
