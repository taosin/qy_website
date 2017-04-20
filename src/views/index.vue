<template>
	<div class="index">
		<Carousel v-model="value1">
			<Carousel-item autoplay v-for="img in imgs">
				<div class="demo-carousel">
					<img :src="img.url">
				</div>
			</Carousel-item>
		</Carousel>
	</div>
</template>

<script>
	export default {
		name: 'hello',
		data () {
			return {
				msg: 'Welcome to Your Vue.js App',
				value1:0,
				imgs:[
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'},
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'},
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'},
				{url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png'}
				]
			}
		},
		attached(){
			this.$Message.info('11111');
		}
	}
</script>

<style scoped lang="less">
	.index{
	}
</style>
