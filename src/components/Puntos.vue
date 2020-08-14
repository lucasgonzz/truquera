<template>
	<div class="puntos">
		<img 
		v-for="fosforo in score"
		:key="fosforo"
		:class="`fosforo p${fosforo}`"
		src="@/assets/fosforo.png" 
		:alt="`fosforo ${fosforo}`">

		<div class="separador" v-show="score > 15"></div>
	</div>
</template>
<script>
export default {
	props: ['score']
}
</script>
<style lang="sass">
.puntos
	margin: auto  
	height: 300px
	width: 60px
	position: relative
	// border-width: 0 3px 0 3px 
	// border-style: solid
	// border-color: #FFF
	display: flex
	align-items: center
	
.fosforo
	position: absolute
	width: 4px
	height: 30px
.p1 
	top: 0px
	right: 10px
.p2
	transform: rotate(-90deg)
	top: -15px
	left: 28px
.p3
	transform: rotate(-180deg)
	top: 0px
	left: 10px
.p4
	transform: rotate(-270deg)
	top: 16px
	left: 28px
.p5
	transform: rotate(-315deg)
	top: 0px
	left: 28px

.p6 
	top: 50px
	right: 10px
.p7
	transform: rotate(-90deg)
	top: 35px
	left: 28px
.p8
	transform: rotate(-180deg)
	top: 50px
	left: 10px

.p9
	transform: rotate(-270deg)
	top: 66px
	left: 28px

.p10
	transform: rotate(-315deg)
	top: 50px
	right: 44%
	left: 28px

.p11 
	top: 100px
	right: 10px
.p12
	transform: rotate(-90deg)
	top: 85px
	left: 28px
.p13
	transform: rotate(-180deg)
	top: 100px
	left: 10px
.p14
	transform: rotate(-270deg)
	top: 116px
	right: 28px
.p15
	transform: rotate(-315deg)
	top: 100px
	left: 28px

.separador
	border: 1.5px solid rgba(255,255,255,.7)
	width: 100%

.p16 
	top: 170px
	right: 10px
.p17
	transform: rotate(-90deg)
	top: 155px
	left: 28px
.p18
	transform: rotate(-180deg)
	top: 170px
	left: 10px
.p19
	transform: rotate(-270deg)
	top: 186px
	right: 28px
.p20
	transform: rotate(-315deg)
	top: 170px
	right: 28px

.p21 
	top: 220px
	right: 10px
.p22
	transform: rotate(-90deg)
	top: 205px
	right: 28px
.p23
	transform: rotate(-180deg)
	top: 220px
	left: 10px
.p24
	transform: rotate(-270deg)
	top: 236px
	right: 28px
.p25
	transform: rotate(-315deg)
	top: 220px
	left: 28px

.p26 
	top: 270px
	right: 10px
.p27
	transform: rotate(-90deg)
	top: 255px
	left: 28px
.p28
	transform: rotate(-180deg)
	top: 270px
	left: 10px
.p29
	transform: rotate(-270deg)
	top: 286px
	left: 28px
.p30
	transform: rotate(-315deg)
	top: 270px
	left: 28px
</style>