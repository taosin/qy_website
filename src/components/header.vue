<template>
	<div class="qy-header">
		<div class="main">
			<div class="logo">
				<img src="./../assets/logo.png" height="50" width="50">
			</div>
			<div class="content">
				<ul>
					<li v-for="(menu, index) in menus" @click="current=index"><router-link :to="menu.url" :class="current === index ? 'current-li':''">{{menu.text}}</router-link></li>
				</ul>
			</div>
			<div class="language">
				<ul>
					<li class="current">中文</li>
					<li>English</li>
				</ul>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		name: 'hello',
		data () {
			return {
				menus:[
				{ text:'网站首页', url:'/index' },
				{ text:'关于我们', url:'/hello' },
				{ text:'新闻动态', url:'/index' },
				{ text:'成功案例', url:'/index' },
				{ text:'产品展示', url:'/index' },
				{ text:'联系我们', url:'/index' },
				],
				current:0
			}
		},
		attached(){
		}
	}
</script>

<style scoped lang="less">
	.qy-header{
		width: 100%;
		margin: 0 auto;
		height: 100px;
		position: absolute;
		z-index: 99;
		.main{
			max-width: 1100px;
			width: 100%;
			background: #05473e;
			margin: 0 auto;
			border-radius: 0 0 6px 6px;
			height: 70px;
			text-align: left;
			padding: 10px;
			.logo{
				float: left;
				width: 100px;
				margin-left: 10px;
			}
			.content{
				width: 730px;
				height: 10px;
				// background: red;
				float: left;
				margin-left: 100px;
				a{
					color: #fff;
					display: inline-block;
					width: 100%;
					height: 100%;
				}
				ul{
					li{
						float: left;
						font-size: 16px;
						padding: 15px 20px;
						cursor: pointer;
						color: #fff;
					}
					li:hover{
						font-weight: bold;
						opacity: .8;
					}
					.current-li{
						color: #39f;
					}
				}
			}
			.language{
				// width: 100px;
				float: left;
				padding: 15px;
				ul{
					color: #fff;
					li{
						float: left;
						background: #5a8143;
						padding: 0 3px;
						cursor: pointer;
					}
					.current{
						background: #eb8a2d;
					}
				}
			}
		}
	}
</style>