<script>
    const { bind } = import("svelte/internal");

	let name = "";

	let lAmount = 0;

	var array1 = [8,8,2,7,7,7,7,8,8,2,5,7,5,7,5,7,3,8,3,5,5,5,7,5,3,7,5,7,5,5]
    var array2 = [4,5,5,10,15,20,15,4,5,5,8,6,3,12,5,7,3,15,7,4,2,2,8,6,5,6,12,16,7,2]
    var array3 = []
	let arrayString="";

    function calculateApplejuice(lAmount) {
		let lPrice = 2;
		
		for (let i = 1; i < lAmount; i++) {
			lPrice *= 0.75;
		}
		return lPrice;
	}

	function function23(array1, array2) {
        for(var i=0; i < array1.length; i++){
            array3[i] = array1[i] + " " + array2[i]
    	}
	}
	function function234(arr) {
		function23(array1, array2)
        for(var i=0; i < arr.length; i++){
        }
		arrayString = arr.join(" ")
    }
</script>
<form>
	<input type="text" bind:value="{name}" placeholder="enter name here">
</form>
<h1>Your name: {name}</h1>
<p>The maximum allowed length of a name is 5 characters, your name is {name.length} characters long</p>
<p>Which is <b>{name.length <= 5 ? 'ACCEPTABLE' : 'UNACCEPTABLE'}</b></p>
<button on:click="{function234(array3)}" style="border: 2px solid greenyellow;"> press this button for the secret numbers</button>
<p>{array3}</p>
<p>{arrayString}</p>
<p>Formula:</p>
<img src="https://i.imgur.com/biia5FV.png" alt="facebook jpeg">
<p>Enter juice amount ( L ):</p>
<form action="{calculateApplejuice(lAmount)}">
	<input type="number" bind:value="{lAmount}">
</form>
<p>Cost per liter: {parseFloat(calculateApplejuice(lAmount)).toFixed(2) == 0.00 ? calculateApplejuice(lAmount) : parseFloat(calculateApplejuice(lAmount)).toFixed(2)}€</p>
<p>Total: {lAmount} liters for {parseFloat(lAmount * calculateApplejuice(lAmount)).toFixed(2)}€</p>
