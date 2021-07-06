<template>
	<view>

		<!-- 	<basics v-if="PageCur=='basics'"></basics>
		<components v-if="PageCur=='component'"></components>
		<plugin v-if="PageCur=='plugin'"></plugin> -->
		<!-- <cu-custom bgColor="bg-white" :isBack="true">
					<block slot="content">背景</block>
		</cu-custom> -->
		<view class="align-center">
			<view class="bg-white padding radius text-center text-bold text-black ">
				<view class="text-lg">豆腐油耗</view>
			</view>
		</view>

		<view class="align-center">
			<view class="bg-gradual-blue padding radius text-center shadow-blur">
				<view class="flex  justify-between">
					<view class=" text-white text-xl">
						我的小车
					</view>
					<view class="text-white text-xl">
						<text class="cuIcon-location"></text> 宁波市
					</view>
				</view>
				<view class="flex justify-start margin-top-xl align-start">
					<view class=" text-s text-white">
						小奔奔 2021 最新款
					</view>
				</view>

			</view>
		</view>

		<view class="cu-card case">
			<view class="cu-item shadow ">
				<view class="flex justify-between">
					<view class="flex justify-start ">
						<view class="padding-sm bg-white solid-bottom">
									<view class='cu-tag radius'>95#</view> 7.5/升
						</view>
					</view>
					<view class="flex justify-start ">
						<view class="padding-sm bg-white solid-bottom">
									<view class='cu-tag radius'>下次调价</view>  2021/07/05
						</view>
					</view>
				</view>
			</view>
		</view>

		<view class="cu-card case">
			<view class="cu-item shadow ">
				<view class="flex justify-between padding-sm">
					<view class="text-df">最新油耗
						<text class="cuIcon-right"></text>
					</view>
					<view class="text-df">油耗评级
						<text class="cuIcon-right"></text>
					</view>
				</view>

				<view class="flex justify-between padding-lr-sm">
					<view>
						<text class="text-xsl text-blue">7.86</text>
						升/百公里
					</view>
					<view>
						<text class="text-xsl text-blue">A</text>
					</view>
				</view>
				
				<view class="flex justify-between padding-sm">
					<view class="solid-bottom align-start clear">
						<view >平均油耗</view>
						<view class="text-bold text-xl padding-tb-sm" >7.86</view>
						<view class="text-gray">升/百公里</view>
					</view>
					<view class="solid-bottom align-start clear">
						<view >平均行程</view>
						<view class="text-bold text-xl padding-tb-sm" >48.94</view>
						<view class="text-gray">公里/天</view>
					</view>
					<view class="solid-bottom align-start clear">
						<view >平均油费</view>
						<view class="text-bold text-xl padding-tb-sm" >0.54</view>
						<view class="text-gray">元/公里</view>
					</view>
				</view>

			</view>
		</view>



		<view class="cu-bar tabbar bg-white shadow foot">
			<view class="action" @click="NavChange" data-cur="basics">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/basics' + [PageCur=='basics'?'_cur':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='basics'?'text-green':'text-gray'">油耗</view>
			</view>
			<view class="action" @click="NavChange" data-cur="component">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/component' + [PageCur == 'component'?'_cur':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='component'?'text-green':'text-gray'">列表</view>
			</view>
			<view class="action" @click="NavChange" data-cur="plugin">
				<view class='cuIcon-cu-image'>
					<image :src="'/static/tabbar/plugin' + [PageCur == 'plugin'?'_cur':''] + '.png'"></image>
				</view>
				<view :class="PageCur=='plugin'?'text-green':'text-gray'">我的</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				PageCur: 'basics'
			}
		},
		methods: {
			NavChange: function(e) {
				this.PageCur = e.currentTarget.dataset.cur
			}
		}
	}
</script>

<style>

</style>
