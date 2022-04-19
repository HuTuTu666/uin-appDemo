<template>
	<view class="content">
		<!-- 系统标题 -->
		<view class="text-area">
			<text class="title">通行预约系统</text>
		</view>
		<!-- 滚动栏 -->
		<view class="uni-margin-wrap">
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
				<swiper-item class="swiper-item">
					<view>
						<image class="item" src="/static/top.png"></image>
					</view>
				</swiper-item>
				<swiper-item class="swiper-item">
				 	<view>
						<image class="item" src="/static/top.png"></image>
					</view>
				</swiper-item>
				<swiper-item class="swiper-item">
				 	<view>
						<image class="item" src="/static/top.png"></image>
					</view>
				</swiper-item>
			</swiper>
		</view>
		<!-- 四个功能按钮 -->
		<view class="fourIcon">
			<view class="icon-view" @click="orderApply">
				<image class="icon" src="/static/p1.png"></image>
				<figcaption>预约申请</figcaption>
				<!-- <text class="icon-title">预约申请</text> -->
			</view >
			<view class="icon-view" @click="orderStatus">
				<image class="icon" src="/static/p2.png"></image>
				<figcaption>预约状态</figcaption>
				<!-- <text class="icon-title">预约状态</text> -->
			</view>
			<view class="icon-view" @click="outNews">
				<image class="icon" src="/static/p3.png"></image>
				<figcaption>外出须知</figcaption>
				<!-- <text class="icon-title">外出须知</text> -->
			</view>
			<view class="icon-view" @click="orderApprove">
				<image class="icon" src="/static/p4.png"></image>
				<figcaption>预约审批</figcaption>
				<!-- <text class="icon-title">预约审批</text> -->
			</view>
		</view>
		<!-- 更多服务 -->
		<view class="more-service">
			<text class="more-service-style">更多服务</text>
		</view>
		<!-- 服务详情 -->
		<view class="service">
			<view class="service-item">
				<text class="text1-style">返校申请</text>
				<text class="text2-style">按学校通知时间返校</text>
			</view>
			<view class="service-item">
				<text class="text1-style">信息上报</text>
				<text class="text2-style">健康打卡，每日报平安</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 2000,
				duration: 500,
			}
		},
		onLoad() {
			
		},
		methods: {
			orderApply() {
				uni.navigateTo({
					url: '../orderApply/orderApply'
				})
			},
			orderStatus() {
				uni.navigateTo({
					url: '../orderStatus/orderStatus'
				})
			},
			outNews() {
				uni.navigateTo({
					url: '../outNews/outNews'
				})
			},
			orderApprove() {
				uni.navigateTo({
					url: '../orderApprove/orderApprove'
				})
			}
		}
	}
</script>

<style>
	.content {
		/* display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center; */
	}
	
	.text-area {
		display: flex;
		justify-content: center;
	}
	
	.title {
		font-size: 35rpx;
		color: #464646;
	}
	
	.uni-margin-wrap {
			width:700rpx;
			height: 300rpx;
			margin-top: 20rpx;
			position: relative;
			left: 25rpx
		}
		
	.swiper {
		width:700rpx;
		height: 300rpx;
	}
	.swiper-item {
		display: block;
		width:700rpx;
		height: 300rpx;
		text-align: center;
	}
	
	.item {
		width:700rpx;
		height: 300rpx;
		border-radius:33rpx;
	}
	
	.fourIcon {
		height: 220rpx;
		display: flex;
		flex-direction: row;
		align-items: center;
		margin-top: 50rpx;
		justify-content: space-around;
	}
	
	.icon-view {
		height: 220rpx;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	
	.icon{
		height: 120rpx;
		width: 120rpx;
	}
	
	.icon-title {
		font-size: 25rpx;
		color: #464646;
	}
	
	.more-service {
		margin-top: 50rpx;
		position: relative;
		left: 25rpx
	}
	
	.more-service-style {
		font-size: 35rpx;
		font-weight: 500;
		color: #464646;
		left: 100rpx;
	}
	
	.service {
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-around;
		margin-top: 50rpx;
	}
	
	.service-item {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		background-color: #e8e8e8;
		padding: 20rpx 120rpx 20rpx 10rpx;
		line-height: 1.8;
	}
	
	.text1-style {
		font-size: 30rpx;
		font-weight: 500;
		color: #464646;
	}
	
	.text2-style {
		font-size: 20rpx;
		color: #8f8f94;
	}
</style>
