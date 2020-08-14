<template>
	<b-container fluid>
		<ganador
		:nos_score="nos_score"
		:ellos_score="ellos_score"
		@nuevaPartida="nuevaPartida"></ganador>
		<b-row>
			<b-col class="col-logo" cols="8" md="12">
				<img src="@/assets/logo.png" alt="Logo" class="logo">
			</b-col>
			<b-col cols="6" md="2">
				<p class="title">Nos</p>
				<puntos :score="nos_score"></puntos>
				<botones 
				:score="nos_score"
				@up="upNosScore"
				@down="downNosScore"></botones>
			</b-col>
			<b-col cols="6" md="2">
				<p class="title">Ellos</p>
				<puntos :score="ellos_score"></puntos>
				<botones 
				:score="ellos_score"
				@up="upEllosScore"
				@down="downEllosScore"></botones>
			</b-col>
		</b-row>
	</b-container>
</template>
<script>
import Puntos from '@/components/Puntos'
import Botones from '@/components/Botones'
import Ganador from '@/components/Ganador'
export default {
	components: {
		Puntos,
		Botones,
		Ganador,
	},
	data() {
		return {
			nos_score: 0,
			ellos_score: 0
		}
	},
	watch: {
		nos_score() {
			if (this.nos_score == 30) {
				this.$bvModal.show('ganador')
			}
		},
		ellos_score() {
			if (this.ellos_score == 30) {
				this.$bvModal.show('ganador')
			}
		}
	},
	methods: {
		upNosScore() {
			if (this.nos_score < 30) {
				this.nos_score++ 
			} else {
				this.resetScore()
			}
		},
		upEllosScore() {
			if (this.ellos_score < 30) {
				this.ellos_score++ 
			} else {
				this.resetScore()
			}
		},
		downNosScore() {
			this.nos_score--
		},
		downEllosScore() {
			this.ellos_score--
		},
		nuevaPartida() {
			this.nos_score = 0
			this.ellos_score = 0
			this.$bvModal.hide('ganador')
		},
		resetScore() {
			this.nos_score = 0
			this.ellos_score = 0
		}
	}
}
</script>
<style lang="sass">
.row
	background: linear-gradient(rgba(0,0,0,.1), rgba(0,0,0,.5))
	display: flex
	justify-content: center
	height: 100vh
.col-logo
	height: 15%
	display: flex
	align-items: center
	// margin-top: 30px
	.logo
		width: 100%
		@media screen and (min-width: 772px)
			width: 50%
			margin: auto
.title
	color: rgba(255,255,255,.7)
	font-size: 2em
	margin-bottom: .5em
.col-6
	padding: 0
	height: 85%
</style>