<template>
	<view>
		<!-- 标题 -->
		<view class="title">
			<text class="title-text">通行预约</text>
		</view>
		<!-- 姓名 -->
		<view class="name-box">
			<text>姓名：</text>
			<input class="input" type="text" v-model="name" />
		</view>
		<!-- 学号 -->
		<view class="number-box">
			<text>学号：</text>
			<input class="input" type="text" />
		</view>
		<!-- 性别 -->
		<view class="sex-box">
			<text>性别：</text>
			<select>
			       <option>男</option>
			       <option>女</option>
			</select>
		</view>
		<!-- 联系电话 -->
		<view class="phone-box">
			<text>联系电话：</text>
			<input class="input" />
		</view>
		<!-- 外出原因 -->
		<view class="out-box">
			<text>外出原因：</text>
			<input class="outreason-input" v-model="outreason" />
		</view>
		<!-- 目的地 -->
		<view class="des-box">
			<text>目的地：</text>
			<input class="input" v-model="des" />
		</view>
		<!-- 预计外出时间 -->
		<view class="outtime-box">
			<text>预计外出时间：</text>
			<uni-datetime-picker type="datetime" v-model="outdate" />
		</view>
		<!-- 预计返回时间 -->
		<view class="backtime-box">
			<text>预计返回时间：</text>
			<uni-datetime-picker type="datetime" v-model="backdate" />
		</view>
		<!-- 所属学院 -->
		<view class="belong-box">
			<text>所属学院：</text>
			<input class="input" type="text" />
		</view>
		<!-- 预计通行校区 -->
		<view class="school-box">
			<text>预计通行校区：</text>
			<select>
			       <option>南望山校区</option>
			       <option>未来城校区</option>
			</select>
		</view>
		<!-- 确定按钮 -->
		<view class="button-box">
			<button type="primary" @click="ok">确定</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name: '',
				outreason: '',
				des: '',
				outdate: '',
				backdate: ''
			}
		},
		methods: {
			ok() {
				uni.setStorage({
					key: 'storage_key',
					data: {
						name: this.name,
						outreason: this.outreason,
						des: this.des,
						outdate: this.outdate,
						backdate: this.backdate
					},
					success: function () {
						console.log('success');
					}
				});
			}
		}
	}
</script>

<style>
	.title {
		display: flex;
		justify-content: center;
		margin: 10rpx;
	}
	
	.title-text {
		font-size: 40rpx;
		color: #000000;
	}
	
	.name-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.number-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.sex-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.out-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.des-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.outtime-box {
		display: flex;
		flex-direction: column;
		margin: 50rpx 20rpx;
		width: 700rpx;
		height: 100rpx;
	}
	
	.backtime-box {
		display: flex;
		flex-direction: column;
		margin: 50rpx 20rpx;
		width: 700rpx;
		height: 100rpx;
	}
	
	.phone-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.belong-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.school-box {
		display: flex;
		flex-direction: column;
		margin: 30rpx 20rpx;
		width: 700rpx;
		height: 80rpx;
	}
	
	.button-box {
		margin: 30rpx 20rpx;
		width: 700rpx;
	}
	
	.input {
		border: solid #bababa;
		width: 700rpx;
		height: 60rpx;
	}

	.outreason-input {
		border: solid #bababa;
		width: 700rpx;
		height: 200rpx;
	}
</style>
