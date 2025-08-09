<template>
	<view class="userLayout pageBg">
		<view class="userInfo">
			<view class="avatar">
				<image src="/static/logo.png" mode="aspectFill"></image>
			</view>
			<view class="nickname">name</view>
		</view>
		
		<view class="section">
				<view class="list">
					<navigator url="/pages/classlist/classlist">
						<view class="row">
							<view class="left">
								<uni-icons type="download-filled" size="20" color="#28b389"></uni-icons>
								<view class="text">我的下载</view>
							</view>
							<view class="right">
							<uni-icons type="right" size="20" color="#28b389"></uni-icons>
							</view>
						</view>
					</navigator>
					<navigator url="/pages/classlist/classlist">
						<view class="row">
							<view class="left">
								<uni-icons type="heart-filled" size="20" color="#28b389"></uni-icons>
								<view class="text">我的收藏</view>
							</view>
							<view class="right">
							<uni-icons type="right" size="20" color="#28b389"></uni-icons>
							</view>
						</view>
					</navigator>
					<navigator url="/pages/classlist/classlist">
						<view class="row">
							<view class="left">
								<uni-icons type="star-filled" size="20" color="#28b389"></uni-icons>
								<view class="text">我的评分</view>
							</view>
							<view class="right">
							<uni-icons type="right" size="20" color="#28b389"></uni-icons>
							</view>
						</view>
					</navigator>
					<view class="row">
						<view class="left">
							<uni-icons type="email-filled" size="20" color="#28b389"></uni-icons>
							<view class="text">问题反馈</view>
						</view>
						<view class="right">
						<uni-icons type="right" size="20" color="#28b389"></uni-icons>
						</view>
					</view>
				</view>
		</view>
		
		<view class="section">
				<view class="list">
					<view class="row">
						<view class="left">
							<uni-icons type="flag-filled" size="20" color="#28b389"></uni-icons>
							<view class="text">常见问题</view>
						</view>
						<view class="right">
						<uni-icons type="right" size="20" color="#28b389"></uni-icons>
						</view>
					</view>
				</view>
		</view>
		
	</view>
</template>

<script setup>
	
</script>

<style lang="scss" scoped>
.userLayout{
	.userInfo{
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		padding: 100rpx 0 0rpx;
		.avatar{
			width: 160rpx;
			height: 160rpx;
			border-radius: 50%;
			overflow: hidden;
			image{
				width: 100%;
				height: 100%;
			}
		}
		.nickname{
			font-size: 44rpx;
			color: black;
			padding: 20rpx 0;
		}
	}
	
	.section{
		overflow: hidden;
		border-radius: 20rpx;
		width: 690rpx;
		margin: 30rpx auto;
		box-shadow: 0 0 30rpx rgba(0,0,0,0.05);
		.list{
			.row{
				background-color: #fff;
				display: flex;
				justify-content: space-between;
				align-items: center;
				padding: 0 30rpx;
				height: 100rpx;
				border-bottom: 1px solid #eee;
				&:last-child{border-bottom: 0;}
				.left{
					display: flex;
					align-items: center;
					.text{
						padding-left: 20rpx;
						color: #666;
					}
				}
				.right{
					display: flex;
					align-items: center;
				}
			}
		}
	}
}
</style>

