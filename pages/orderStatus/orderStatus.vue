<template>
	<view>
		<view class="title-box">
			<text class="title-style">预约审批</text>
		</view>
		<view class="nav-box">
			<uni-segmented-control :current="current" :values="items" @clickItem="onClickItem" styleType="text" activeColor="#97e3e3"></uni-segmented-control>
			<view class="content">
				<view v-show="current === 0">
					<uni-card>
						<uni-row class="demo-uni-row">
							<uni-col :span="18">
								<text>申请人：{{approveInfo.name}}</text>
							</uni-col>
							<uni-col :span="6">
								<text class="text-color">审批通过</text>
							</uni-col>
						</uni-row>
						<uni-row class="demo-uni-row">
							<uni-col :span="6">
								<!-- <icon type="waiting" size="14"/> -->
								<text>通行时间:</text>
							</uni-col>
							<uni-col :span="18">
								<text>{{approveInfo.outdate}}--</text>
								<text>{{approveInfo.backdate}}</text>
							</uni-col>
						</uni-row>
						<uni-row class="demo-uni-row">
							<uni-col :span="12">
								<text>外出原因：{{approveInfo.outreason}}</text>
							</uni-col>
						</uni-row>
						<uni-row class="demo-uni-row">
							<uni-col :span="12">
								<text>目的地：{{approveInfo.des}}</text>
							</uni-col>
						</uni-row>
					</uni-card>
				</view>
				<view class="text-other" v-show="current === 1">
					<text>暂无申请</text>
				</view>
				<view v-show="current === 2">
					<uni-card>
						<uni-row class="demo-uni-row">
							<uni-col :span="18">
								<text>申请人：{{approveInfo.name}}</text>
							</uni-col>
							<uni-col :span="6">
								<text class="text-color">审批通过</text>
							</uni-col>
						</uni-row>
						<uni-row class="demo-uni-row">
							<uni-col :span="6">
								<!-- <icon type="waiting" size="14"/> -->
								<text>通行时间：</text>
							</uni-col>
							<uni-col :span="18">
								<text>{{approveInfo.outdate}}--</text>
								<text>{{approveInfo.backdate}}</text>
							</uni-col>
						</uni-row>
						<uni-row class="demo-uni-row">
							<uni-col :span="12">
								<text>外出原因：{{approveInfo.outreason}}</text>
							</uni-col>
						</uni-row>
						<uni-row class="demo-uni-row">
							<uni-col :span="12">
								<text>目的地：{{approveInfo.des}}</text>
							</uni-col>
						</uni-row>
					</uni-card>
				</view>
				<view class="text-other" v-show="current === 3">
					<text>暂无申请</text>
				</view>
				<view class="text-other" v-show="current === 4">
					<text>暂无申请</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				current: 0,
				items: ['全部', '待审批', '通过', '不通过', '已取消'],
				nowDate: new Date(),
				approveInfo: {
					name: '',
					outreason: '',
					des: '',
					outdate: '',
					backdate: ''
				}
			}
		},
		methods: {
			onClickItem(e) {
			      if (this.current != e.currentIndex) {
			        this.current = e.currentIndex;
			      }
			    }
			
		},
		onShow() {
			this.approveInfo = uni.getStorageSync('storage_key');
		}
	}
</script>

<style>
	.title-box {
		position: relative;
		left: 30rpx;
		margin: 20rpx 0;
	}
	
	.tytle-style {
		font-size: 30rpx;
		color: #464646;
	}
	
	.nav-box {
		margin: 20rpx 0;
	}
	
	.text-color {
		color: #00f476;
	}
	
	.text-other {
		display: flex;
		justify-content: center;
		margin-top: 400rpx;
	}
</style>
