<script>
	let name = "Kaitlin";
	let age = 34;

	function incrementAge(){
		age += 1;
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}, I am {age} years old!</h1>
<button on:click="{incrementAge}">Add to age</button>
