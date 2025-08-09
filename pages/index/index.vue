<template>
	<view class="homeLayout pageBg">
		<custom-nav-bar></custom-nav-bar>
		<view class="banner">
			<swiper circular indicator-dots indicator-color="rgba(255,255,255,0.5)"
			indicator-active-color="#fff" autoplay>
				<swiper-item v-for="item in 3">
					<image src="/commn/images/banner1.jpg" mode="aspectFill"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="box">
			<view class="recommend" v-for="item in 4">
				<common-apk></common-apk>
			</view>
		</view>		
	</view>
</template>

<script>
	
</script>

<style lang="scss" scoped>
	.homeLayout{
		.banner{
			width: 780rpx;
			padding-top: 100rpx;
			swiper{
				width: 750rpx;
				height: 340rpx;
				&-item{
					width: 100%;
					height: 100%;
					padding: 0 18rpx;
					image{
						width: 100%;
						height: 340rpx;
						border-radius: 20rpx;
					}
					
				}
			}
		}
		.box{
			display: flex;
			flex-wrap: wrap;
			.recommend{
				margin-left: 16rpx;
				margin-top: 20rpx;
				width: 350rpx;
			}
		}
	}
	
</style>
