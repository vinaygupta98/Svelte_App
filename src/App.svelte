<script>
	let count=0
	const Increment =()=>{
	count=count+1
	}
	const Decrement =()=>{
	if(count<1){
		alert("Count can't negative")
	}else{count=count-1}
	}
	$: if (count >= 10) {
	alert(`count is dangerously high!`);
	count = 9;
}
</script>
<div class="container">
	<h1>Click Counter</h1>
	<p>count is {count}</p>
	<button on:click={Increment}>Increase</button>
	<button on:click={Decrement}>Decrease</button>
</div>
<style>
.container{
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}
</style>
