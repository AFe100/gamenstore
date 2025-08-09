<template>
	<view class="preview pageBg">
		<view class="top">
			<view class="left">
				<image class="apkicon" src="/static/logo.png" mode="aspectFill"></image>
			</view>
			<view class="right">
				<view class="apktitle">
					标题
				</view>
				<view class="apkinfo">
					<view class="size">1024Mb</view>
				</view>
				<view class="apktag">
					<uni-tag text="标签" type="default" size="mini"></uni-tag>
				</view>
			</view>
			
		</view>
		
		<view class="meddia">
			<view class="card">
				<view class="rate" @click="clickScore">
					<uni-rate :readonly="true" :value="5" size="38"/>
				</view>
				<view class="like" @click="clickLike">
					<uni-icons :type="isLiked ? 'heart-filled' : 'heart'" size="38" color="#ff607d"></uni-icons>
				</view>
			</view>
		</view>
		
		<view class="bottom">
			<view class="pictitle">
				<view>
				预览
				</view>
			</view>
			<swiper class="apkpic" previous-margin="50rpx" next-margin="40rpx">
				<swiper-item><image src="/commn/images/pre1.jpg" mode="aspectFill"></image></swiper-item>
				<swiper-item><image src="/commn/images/pre2.jpg" mode="aspectFill"></image></swiper-item>
				<swiper-item><image src="/commn/images/pre3.jpg" mode="aspectFill"></image></swiper-item>
				<swiper-item><image src="/commn/images/pre1.jpg" mode="aspectFill"></image></swiper-item>
				<swiper-item><image src="/commn/images/pre2.jpg" mode="aspectFill"></image></swiper-item>
			</swiper>
		</view>
		<view class="text">
			<view class="texttitle">
				<view>
				介绍
				</view>
			</view>
			<view class="textcontent">
				
			</view>
		</view>
		<view class="download">
			下载
		</view>
		
		<uni-popup ref="scorePopup">
			<view class="scorePopup">
				<view class="popHeader">
					<view class="box">
						<view class="poptitle">评分</view>
						<view class="close" @click="clickScoreClose">
							<uni-icons type="closeempty" size="20" color="#999"></uni-icons>
						</view>
					</view>
					<view class="content">
						<uni-rate v-model="userScore" size="40"/>
						<text class="text">{{userScore}}分</text>
					</view>
					
					<view class="footer">
						<button @click="submitScore" :disabled="!userScore" type="default" size="mini">确认评分</button>
					</view>
				</view>
			</view>
		</uni-popup>
	</view>
</template>

<script setup>
import { ref } from 'vue';

const isLiked = ref(false)
const scorePopup = ref(null);
const userScore = ref(0);

//收藏
const clickLike=()=>{
	isLiked.value = !isLiked.value
}
	
//评分弹窗
const clickScore=()=>{
	scorePopup.value.open();
}

//关闭评分弹窗
const clickScoreClose=()=>{
	scorePopup.value.close();
}

//确认评分
const submitScore=()=>{
	console.log("评分了");
}
</script>

<style lang="scss" scoped>
.preview{
	.top{
		display: flex;
		justify-content: flex-start;
		padding-left: 50rpx;
		.left{
			// border: solid red;
			height: 200rpx;
			.apkicon{
				box-shadow: 1px 5px 10px 0px #4646466b;
				border-radius: 30rpx;
				width: 150rpx;
				height: 150rpx;
				margin-top: 6px;
			}
		}
		.right{
			padding-top: 20rpx;
			padding-left: 40rpx;
			// border: solid red;
			width: 58%;
			.apktitle{
				font-weight: 500;
				// border: solid red;
				font-size: 45rpx;
				font-style: arial;
			}
			.apkinfo{
				color: #888;
				align-items: center;
				// padding-left: 5rpx;
				display: flex;
				// border: solid red;
				.star{
					padding-right: 10rpx;
					display: flex;
					align-items: center;
				}
				.size{
					// padding-left: 10rpx;
				}
			}
			.apktag{
				padding-top: 8rpx;
				padding-left: 5rpx;
			}
		}
		
	}
	.meddia{
		display: flex;
		justify-content: center;
		.card{
			height: 120rpx;
			width: 550rpx;
			box-shadow: 1px 5px 10px 0px #4646466b;
			display: flex;
			align-items: center;
			justify-content: center;
			border-radius: 50rpx;
			.rate{
				border-right: 1px solid #9c9c9c;
				display: flex;
				align-items: center;
				padding-right: 10rpx;
			}
			.like{
				display: flex;
				align-items: center;
				padding-left: 10rpx;
				// border: solid red;
			}
		}
	}
	.bottom{
		padding-top: 50rpx;
		.pictitle{
			display: flex;
			align-content: center;
			justify-content: center;
			view{
				width: 90%;
				padding-left: 15rpx;
				border-top: 1rpx solid #b3b3b3;
				font-size: 45rpx;
				font-weight: 600;
			}
		}
		.apkpic{
			height: 540rpx;
			padding-top: 20rpx;
			display: flex;
			flex-direction: column;
			swiper-item{
				// border: solid red;
				display: flex;
				justify-content: center;
				padding-right: 20rpx;
				image{
					width: 100%;
					border-radius: 30rpx;
					box-shadow: 0px 0px 10px 0px #4646466b;
				}
			}
			// justify-content: center;
			
		}
	}
	.text{
		padding-top: 20rpx;
		.texttitle{
			display: flex;
			align-content: center;
			justify-content: center;
			view{
				width: 90%;
				padding-left: 15rpx;
				border-top: 1rpx solid #b3b3b3;
				font-size: 45rpx;
				font-weight: 600;
			}
		}
		.textcontent{
			box-shadow: 1px 5px 20px 0px #4646466b;
			padding: 30rpx 5rpx 0;
			width: 90%;
			margin: 10rpx auto;
			border-radius: 30rpx;
			backdrop-filter: blur(20rpx);
			background: white;
		}
	}
	.download{
	  position: fixed;
	  bottom: 30rpx;
	  left: 50%;
	  transform: translateX(-50%);
	  width: 80%;
	  height: 100rpx;
	  background-color: #007aff;
	  color: #fff;
	  text-align: center;
	  line-height: 90rpx;
	  border-radius: 45rpx;
	  box-shadow: 0 8rpx 20rpx rgba(0, 0, 0, 0.2);
	  font-size: 34rpx;
	  z-index: 999;
	}
	
	
	
	.scorePopup{
		background: #fff;
		padding: 10rpx;
		width: 70vw;
		border-radius: 30rpx;
		height: 300rpx;
		.popHeader{
			.box{
				display: flex;
				align-items: center;
				justify-content: space-between;
				.poptitle{
					padding-left: 230rpx;
					color: #9c9c9c;
					font-size: 30rpx;
					font-weight: 600;
				}
				.close{
					padding: 6rpx 10rpx;
				}
			}
			.content{
				padding: 10rpx 50rpx;
				.text{
					color: #dfdf43;
					padding-left: 185rpx;
				}
			}
			.footer{
				padding-top: 10rpx;
				padding-left: 165rpx;
				button{
					box-shadow: 0 8rpx 20rpx rgba(0, 0, 0, 0.2);
				}
			}
			
		}
	}
}
</style>
