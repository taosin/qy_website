<template>
	<div class="qy-index">
		<!-- 顶部菜单 -->
		<top></top>
		<!-- 轮播图 -->
		<div class="qy-carousel">
			<Carousel v-model="value1" autoplay>
				<Carousel-item v-for="img in imgs" :trigger="hover">
					<div class="demo-carousel">
						<img :src="img.url">
					</div>
				</Carousel-item>
			</Carousel>
		</div>
	</div>
</template>

<script>
	import top from './../components/header.vue';
	export default {
		name: 'hello',
		components:{
			top
		},
		data () {
			return {
				msg: 'Welcome to Your Vue.js App',
				value1:0,
				imgs:[
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'},
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'},
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'},
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'}
				],
				hover:'hover'
			}
		},
		attached(){
			this.$Message.info('11111');
		}
	}
</script>

<style scoped lang="less">
	.qy-index{
		text-align: center;
		.qy-carousel{
			width: 100%;
			height: 500px;
			img{
				width: 100%;
				height: 500px;
			}
		}
	}
</style>
