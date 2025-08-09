<template>
	<view class="themItem">
		<navigator url="/pages/classlist/classlist" class="box">
			<image class="pic" src="/commn/images/classify1.jpg" mode="aspectFill"></image>
			<view class="mask">RPG</view>
		</navigator>
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
	.themItem{
		.box{
			
			box-shadow:0px 0px 20rpx #686868;
			height: 215rpx;
			width: 340rpx;
			border-radius: 30rpx;
			overflow: hidden;
			position: relative;
			.pic{
				height: 215rpx;
				width: 340rpx;
			}
			.mask{
				width: 80rpx;
				height: 100%;
				position: absolute;
				bottom: 0;
				right: 0;
				background: rgba(0,0,0,0.8);
				color: #fff;
				display: flex;
				align-items: center;
				justify-content: center;
				backdrop-filter: blur(20rpx);
			}
		}
	}
</style>