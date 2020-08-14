<template>
<b-modal id="ganador" hide-header hide-footer centered>
	<p>¡{{ title }}!</p>
	<b-button
	@click="nuevaPartida"
	variant="success"
	block>
		Nueva partida
	</b-button>
</b-modal>
</template>
<script>
export default {
	props: ['nos_score', 'ellos_score'],
	computed: {
		title() {
			if (this.nos_score == 30) {
				return 'Ganamos nosotros'
			}
			return 'Ganaron ellos'
		}
	},
	methods: {
		nuevaPartida() {
			this.$emit('nuevaPartida')
		}
	}
}
</script>
<style scpoed lang="sass">
p 
	font-size: 1.4em
	font-weight: bold
	text-align: center
</style>