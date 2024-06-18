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
		route : function(){
			
		}
	},

	mounted : function(){

		/// required		

		this.sdk = new window.BastyonSdk()

		this.sdk.init().then((applicationInfo) => {
			
		})

		this.sdk.emit('loaded')

		this.sdk.on('changestate', (data) => {
			this.$router.push(this.sdk.getroute(data))
		})

		this.sdk.on('action', (d) => {
		})

		this.sdk.on('balance', (d) => {
		})

		this.sdk.on('state', (d) => {
		})

		this.sdk.on('keyboard', ({height}) => {
		})

		this.sdk.get.appinfo().then(({locale}) => {
		})

	},

	methods : {
	}
}
</script>

<style>

</style>
