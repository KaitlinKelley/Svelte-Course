<script>
import { loop_guard } from "svelte/internal";


	let name = "Kaitlin";
	let age = 34;

	// $: means labelled statement/dynamic statement
	//svelte will re-run this code anytime the value of name is changed via the button
	$: uppercaseName = name.toUpperCase();

	$: console.log(name);

	$: if(name === "Max"){
		age = 31;
	}

	function incrementAge(){
		age += 1;
	}

	function changeName(){
		name = "Max";
	}

	function nameInput(event){
		const enteredValue = event.target.value;
		name = enteredValue;
	}

</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {uppercaseName}, I am {age} years old!</h1>
<button on:click="{incrementAge}">Add to age</button>
<!-- <button on:click="{changeName}">Change Name</button> -->
<input type="text" value="{name}" on:input="{nameInput}">
