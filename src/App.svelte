<script>
	let people = [
		{ name: 'park', beltColor: 'black', age: 18, id: 1 },
		{ name: 'geom', beltColor: 'red', age: 39, id: 2 },
		{ name: 'jang', beltColor: 'orange', age:50, id: 3 }
	];

	const handleClick = (id) => {
		// delete the person from people
		console.log(id);
	};
</script>

<main>
	<!-- <div>
		<h4>{people[0].name}</h4>
		<p>{people[0].beltColor}</p>
	</div>
	<div>
		<h4>{people[1].name}</h4>
		<p>{people[1].beltColor}</p>
	</div>
	<div>
		<h4>{people[2].name}</h4>
		<p>{people[2].beltColor}</p>
	</div>   -->

	{#each people as person (person.id)}
		<div>
			<h4>{person.name}</h4>
			<p>{person.age} years old, {person.beltColor} belt.</p>
			<button on:click={handleClick(person.id)}>delete</button>
		</div>
		{:else}
		   <p>There are no people to show...</p>
	{/each}
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