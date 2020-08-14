<template>
	<div class="botones">
		<b-button variant="danger" size="sm">
			<i class="icon-minus" @click="down"></i>
		</b-button>
		<b-button variant="success" size="sm">
			<i class="icon-plus" @click="up"></i>
		</b-button>
	</div>
</template>
<script>
export default {
	props: ['score'],
	methods: {
		up() {
			this.$emit('up')
		},
		down() {
			if (this.score > 0) {
				this.$emit('down')
			}
		},
	}
}
</script>
<style lang="sass">
.botones 
	position: absolute
	width: 100%
	bottom: 1em
	display: flex
	justify-content: space-around
	button
		&:active
			transform: scale(.9)
		// background: none
		// border: 4px solid #FFF
		border-radius: 50%
		color: #FFF
		font-size: 1.5em
		&:focus
			outline: none
</style>