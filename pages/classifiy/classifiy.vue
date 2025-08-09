<template>
	<view class="classLayout pageBg">
		<custom-nav-bar></custom-nav-bar>
		<view class="classify">
			<theme-item v-for="item in 8"></theme-item>
		</view>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
.classLayout{
	padding-top: 80rpx;
	.classify{
		padding-left: 20rpx;
		padding-top: 30rpx;
		display: grid;
		grid-row-gap: 20px;
		grid-template-columns: repeat(2,1fr);
	}
}

</style>
