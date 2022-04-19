<template>
	<view>
		<view class="box-one" >
			<text class="first-title">校园出入预约须知</text>
		</view>
		<view class="box-two">
			<!-- <uni-title title="外出须知" type="line"></uni-title> -->
			<view class="second-title-box">
				<text class="second-title">外出须知</text>
			</view>
			<view class="p-box">
				<p class="p-style">1.坚持非必要不外出，非必要不离汉，确需外出要履行请假报备手续，返校后要第一时间向培养单位报告。</p>
				<p class="p-style">2.如实报备外出事由、外出时间和外出地点，按照请假时间进出学校，按照请假事由和外出地点点对点活动，不得私自改变行程路线，原则上不得夜不归宿或校外留宿。</p>
				<p class="p-style">3.严格遵守疫情防控要求，履行疫情防控个人责任，做好自我健康监测，若有发热、咳嗽等疑似症状时，要及时向培养单位报告。</p>
				<p class="p-style">4.做好个人防护，全程佩戴口罩，在公共场所保持安全社交距离，避免前往人员密集场所。</p>
				<p class="p-style">5.如因谎报、瞒报外出事由或隐瞒外出行程或未如实报告疑似症状而造成严重后果的，将依法依规追究相关责任。</p>
				<p class="p-style">6.认真学习安全知识，提高安全防范技能，注意饮食安全、人身财产安全、意外溺水等安全隐患，增强金融风险防范意识，警惕各类电信网络诈骗。</p>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.box-one {
		width: 700rpx;
		position: relative;
		left: 30rpx;
		margin: 30rpx 0;
	}
	
	.first-title {
		font-size: 40rpx;
		color: #464646;
	}
	
	.box-two {
		
	}
	
	.second-title-box {
		width: 700rpx;
		position: relative;
		left: 30rpx;
		margin: 20rpx 0;
	}
	
	.second-title {
		font-size: 30rpx;
		color: #464646;
	}
	
	.p-box {
		width: 720rpx;
		position: relative;
		left: 30rpx;
		line-height: 1.5;
	}
	
	.p-style {
		font-size: 30rpx;
		color: #464646;
		margin: 20rpx 0;
	}
</style>
