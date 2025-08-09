<template>
	<view class="layout">
		<view class="navbar">
			<view class="statusBar" :style="{height:statusBarHeight+'px'}"></view>
			<view class="titleBar">
				<view class="title">标题</view>
				<navigator url="/pages/search/search" class="search">
					<uni-icons class="icon" type="search" color="#888" size="18"></uni-icons>
					<text class="text">搜索</text>
				</navigator>
			</view>
		</view>
		
		<view class="fill" :style="{height:statusBarHeight+10+'rpx'}">
			
		</view>
	</view>
</template>

<script setup>	
import {ref} from 'vue'

let SYSTEM_INFO = uni.getSystemInfoSync();
let statusBarHeight = ref(SYSTEM_INFO.statusBarHeight)
</script>

<style lang="scss" scoped>
.layout{
	.navbar{
		position: fixed;
		top: 0%;
		left: 0%;
		width: 100%;
		z-index: 10;
		background: linear-gradient(to bottom,#ffbec8,#ffc6ce);
		backdrop-filter: blur(100rpx);
		.statusBar{ }
		.titleBar{
			display: flex;
			align-items: center;
			padding: 0 20rpx;
			height: 80rpx;
			.title{
				font-size: 20px;
				font-weight: 700;
				color: #000;
			}
			.search{
				width: 380rpx;
				height: 50rpx;
				border-radius: 60rpx;
				background: rgba(255,255,255,0.4);
				border: 1px solid #fff;
				margin-left: 30rpx;
				color: #999;
				font-size: 30rpx;
				font-weight: 600;
				display: flex;
				align-items: center;
			}
			.icon{
				margin-left: 5rpx;
			}
			.text{
				padding-left: 10rpx;
			}
		}
	}
	.fill{
		
	}
}
</style>