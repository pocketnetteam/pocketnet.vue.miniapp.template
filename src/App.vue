<template>
	<div>
		Template
	</div>
</template>

<script>


export default {
	name: 'App',
	components: {
		
	},

	data : function(){
		return {
			sdk : null
		}
	},

	computed : {
	},

	mounted : function(){

		/// required		

		this.sdk = new window.BastyonSdk()

		this.sdk.init().then(() => {
			
		})

		this.sdk.emit('loaded')

		this.sdk.on('changestate', (data) => {
			this.$router.push(this.sdk.getroute(data))
		})

		this.sdk.on('action', () => {
		})

		this.sdk.on('balance', () => {
		})

		this.sdk.on('state', () => {
		})

		this.sdk.on('keyboard', () => {
		})

		this.sdk.get.appinfo().then(() => {
		})

	},

	methods : {
	}
}
</script>

<style>

</style>
