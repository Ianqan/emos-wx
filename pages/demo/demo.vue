<template>
	<view>
		<view>{{username}}</view>
		<view v-for = "one in tel">{{one}}</view>
		<view v-if = "age >= 18">
			<button @tap = "signup()">Sign Up</button>
		</view>
		<view>
			<input type="text" v-model = "address" placeholder = "address">
		</view>
		<view>{{address}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				username: "Ian",
				tel: ['13312345678', '18612345678'],
				age: 20,
				address: ""
			}
		},
		methods: {
			signup: function() {
				uni.showToast({
					title: "Signed up"
				})
			}
		}
	}
</script>

<style>

</style>
