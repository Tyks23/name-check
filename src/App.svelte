<script>
	let name = "";
</script>
<form>
	<input type="text" bind:value="{name}" placeholder="enter name here">
</form>
<h1>Your name: {name}</h1>
<p>The maximum allowed length of a name is 5 characters, your name is {name.length} characters long</p>
<p>Which is <b>{name.length <= 5 ? 'ACCEPTABLE' : 'UNACCEPTABLE'}</b></p>