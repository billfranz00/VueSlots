<template>
	<div>
		<h3>The Author</h3>
		<button @click="counter++">Increase!</button>
		<p>{{ counter }}</p>
	</div>
</template>

<script type="text/javascript">
	export default {
		data: function() {
			return {
				counter: 0
			}
		},
		destroyed() {
			console.log('I have been destroyed ;(');
		},
		deactivated() {
			console.log('Author Deactivated!!!');
		},
		activated() {
			console.log("Activation ;0");
		}
	}
</script>

<style type="text/css">
	
</style>