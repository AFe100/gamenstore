<template>
	<view class="classlist">
		<view class="content">
			<view class="list" >
				<view class="line" v-for="items in 8">
					<common-apk></common-apk>
				</view>
			</view>
		</view>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
.content{
	padding-top: 15rpx;
	.list{
		padding: 0rpx 40rpx;
		.line{
			padding: 15rpx 0 15rpx;
			border-bottom: 2px solid #eee;
			&:last-child{border-bottom: 0;}
		}
	}
}
</style>
