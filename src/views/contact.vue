<template>
	<div class="qy-contact">
		<div class="top">
			<img src="http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/guoboxincheng.png">
		</div>
		<div class="main">
			<div class="main-top">
				<ul class="btn-ul">
					<li class="btn-ul-li current">联系方式</li>
					<li class="btn-ul-li">在线咨询</li>
				</ul>
			</div>
			<div class="main-title">
					<span class="index-title">联系我们 / CONTACT US</span>
				<div class="position">
					<span>您的位置：<router-link to="/index">首页</router-link> > <router-link to="/index">联系我们</router-link> > <a>联系方式</a></span>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	export default {
		name: 'app',
		components:{
		},
	}
</script>
<style scoped lang="less">
	.qy-contact{
		width: 100%;
		background: #e9f2f0;
		.top{
			width: 100%;
			height: 500px;
			img{
				width: 100%;
				height: 500px;
			}
		}
		.main{
			height: 500px;
			width: 1100px;
			margin: 0 auto;
			// border: 1px solid;
			margin-top: -10px;
			position: relative;
			z-index: 99999;
			.main-top{
				width: 100%;
				.btn-ul{
					float: right;
					.btn-ul-li{
						float: left;
						border: 1px solid #05473e;
						padding: 1px 10px;
						border-radius: 4px;
						background: #fff;
						color: #000;
					}
					.current{
						background: #05473e;
						color: #fff;
					}
				}
			}
			.main-title{
				// margin-top: 30px;
				padding-top: 30px;
				width: 100%;
				text-align: left;
				border-bottom: 1px solid #05473e;
				padding-bottom: 10px;
				.index-title{
					font-size: 16px;
					font-weight: bold;
					color: #05473e;
				}
				.position{
					margin-top: 5px;
					a{
						color: #000;
					}
				}
			}
		}
	}
</style>
