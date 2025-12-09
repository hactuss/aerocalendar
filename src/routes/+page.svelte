<script>
	const date = new Date();
	const k = 25;
	let day_string = '';
	function day(d) {
		switch (d.getDay()) {
			case 2:
				return 'Tuesday';
				break;
			case 3:
				return 'Wednesday';
				break;
		}
	}
</script>

<main>
	<h1>Aero Calendar</h1>
	<p>Hactuss</p>
	<h3>{date.getDay() + '.' + date.getMonth() + '.' + date.getFullYear()}</h3>
	{#each date as datet, k}
		<div id="Datebox">
			<p>{datet}</p>
			<h2>{day(date)}</h2>
		</div>
	{/each}
</main>

<style lang="scss">
	main {
		width: 100%;
		height: 100%;
	}
	#Datebox {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		border: solid 1px black;
	}
</style>
