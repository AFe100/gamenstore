<template>
	    <view class="applist">
	    	<view>
	    		<image class="appicon" src="/static/image/photo.jpg" mode="scaleToFill" loadingIcon="hourglass"></image>
	    		<view class="appinfo">
	    			<view class="title">测试</view>
					<view class="tag">
						<uni-tag text="标签" type="primary" size="mini" inverted="true" />
					</view>
	    		</view>
				
				
	    	</view>
	    </view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
    .applist{
    	width: 350rpx;
    	height: 320rpx;
    	display: flex;
    	align-items: center;
    	justify-content: center;
		// margin-top: 20rpx;
		border-radius: 10rpx;
		overflow: hidden;
		box-shadow: 1px 5px 20px 0px #4646466b;
    	view{
    		width: 100%;
    		height: 100%;
    		display: flex;
			flex-direction: column;
    		.appicon{
    			width: 408rpx;
    			height: 312rpx;
    		}
    		.appinfo{
				// border: solid red;
    			flex: 1;
    			height: 50%;
    			font-size: 35rpx;
    			color: black;
				margin-top: 5rpx;
				margin-left: 8rpx;
					.title{
						text-align: bottom;
					}
					.tag{
						width: fit-content;
						margin-bottom: 5rpx;
					}
    		}
    	}
    }
</style>