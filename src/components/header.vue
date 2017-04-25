<template>
	<div class="qy-header">
		<div class="main">
			<div class="logo">
				<img src="./../assets/logo.png" height="50" width="50">
			</div>
			<div class="content">
				<ul>
					<li>网站首页</li>
					<li>关于我们</li>
					<li>新闻动态</li>
					<li>成功案例</li>
					<li>产品展示</li>
					<li>联系我们</li>
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
				ul{
					li{
						float: left;
						font-size: 16px;
						padding: 15px 20px;
						color: #fff;
						cursor: pointer;
					}
					li:hover{
						font-weight: bold;
						opacity: .8;
					}
				}
			}
			.language{
				// width: 100px;
				float: left;
				padding: 15px;
				ul{
					color: #fff;
					font-size: 10px !important;
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