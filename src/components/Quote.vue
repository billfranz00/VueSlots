<template>
	<div>
		<!-- <p>{{ quote }}</p> -->
		<div class="title">
			<slot name="title"></slot>
			<span><slot name="subtitle">The Subtitle</slot></span>
		</div>
		<div>
			<!-- <slot name="content"></slot> -->
			<slot></slot>
		</div>
	</div>
</template>

<script type="text/javascript">
	export default {
		// props: ['quote']
	}
</script>

<style type="text/css" scoped>
	div {
		border: 1px solid #ccc;
		box-shadow: 1px 1px 2px black;
		padding: 30px;
		margin: 30px auto;
		text-align: center;
	}

	h2 {
		color: red;
	}

	.title {
		font-style: italic;
	}

	span {
		color: #ccc;
	}
</style>