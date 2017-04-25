<template>
	<div class="qy-index">
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
		<!-- 成功案例 -->
		<div class="qy-cases">
			<span class="index-title">成功案例 / SUCCESSFUL CASE</span>
			<a class="more-btn">查看更多></a>
			<div class="case-main">
				<div class="item" v-for="cs in cases">
					<img :src="cs.url">
					<div class="bov-text">
						<span>{{cs.title}}</span>
					</div>
				</div>
			</div>
		</div>
		<!-- 关于我们 -->
		<div class="qy-about">
			<div class="main">
				<div class="left">
					<span class="index-title">关于我们 / ABOUT US</span>
					<a class="more-btn">查看更多></a>
					<div class="content">
						<img src="http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/home_com.png">
						<div class="left-content">
							<p>深圳市腾讯计算机系统有限公司成立于1998年11月，由马化腾、张志东、许晨晔、陈一丹、曾李青五位创始人共同创立。是中国最大的互联网综合服务提供商之一，也是中国服务用户最多的互联网企业之一。</p>
							<p>腾讯多元化的服务包括：社交和通信服务QQ及微信/WeChat、社交网络平台QQ空间、腾讯游戏旗下QQ游戏平台、门户网站腾讯网、腾讯新闻客户端和网络视频服务腾讯视频等。</p>
							<p>2004年6月16日，腾讯公司在香港联交所主板公开上市（股票代号00700），是香港恒生指数成分股之一，董事会主席兼首席执行官是马化腾。</p>
							<p>2015年，腾讯公司实现总收入1028.63亿元，同比增长30%；腾讯权益持有人应占盈利288.06亿元，同比增长21%...</p>
						</div>
					</div>
				</div>
				<div class="right">
					<span class="index-title">经典项目 / CLASSIC PROJECT</span>
					<div class="content">
						<img src="http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/s_guoboxincheng">
					</div>
				</div>
			</div>
		</div>
		<!-- 新闻动态 -->
		<div class="qy-news">
			<span class="index-title">新闻动态 / NEWS</span>
			<a class="more-btn">查看更多></a>
		</div>
		<!-- 产品展示 -->
		<div class="qy-products">
			<div class="main">
				<span class="index-title">产品展示 / PRODUCT DISPLAY</span>
				<a class="more-btn">查看更多></a>
				<div class="pro-content">
					<div class="item" v-for="pro in products">
						<img :src="pro.url">
						<div class="bov-text">
							<p>名称:{{pro.title}}</p>
							<p>型号:{{pro.type}}</p>
						</div>
					</div>
				</div>
			</div>
		</div>
		<!-- 合作伙伴 -->
		<div class="qy-partners">
			<span class="index-title">合作企业 / BUSINESS PARTNERS</span>
			<div class="main">
				<div class="up">
					<a><img src="http://olo3mdoqb.bkt.clouddn.com/08f790529822720e984871c17ecb0a46f21fab03.jpg" class="a-partner" title="腾讯logo"></a>
					<a><img src="http://olo3mdoqb.bkt.clouddn.com/08f790529822720e984871c17ecb0a46f21fab03.jpg" class="a-partner" title="腾讯logo"></a>
					<a><img src="http://olo3mdoqb.bkt.clouddn.com/08f790529822720e984871c17ecb0a46f21fab03.jpg" class="a-partner" title="腾讯logo"></a>
				</div>
				<div class="bot">
					<a><img src="http://olo3mdoqb.bkt.clouddn.com/08f790529822720e984871c17ecb0a46f21fab03.jpg" class="a-partner" title="腾讯logo"></a>
					<a><img src="http://olo3mdoqb.bkt.clouddn.com/08f790529822720e984871c17ecb0a46f21fab03.jpg" class="a-partner" title="腾讯logo"></a>
					<a><img src="http://olo3mdoqb.bkt.clouddn.com/08f790529822720e984871c17ecb0a46f21fab03.jpg" class="a-partner" title="腾讯logo"></a>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'hello',
		components:{
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
				hover:'hover',
				cases:[
				{ title:'沙湖明珠', url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/s_shahumingzhu.png' },
				{ title:'国博新城', url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/s_guoboxincheng' },
				{ title:'城市广场', url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/s_chengshiguangchang.png' },
				{ title:'东方雅苑', url:'http://yn-img-bucket.oss-cn-shanghai.aliyuncs.com/s_dongfangyayuan.png' },
				],
				products:[
				{ title:'GARDESA卡门', url:'http://ac-00QDJJp8.clouddn.com/3498b99898aae6b84fec.jpg', type:'URANO' },
				{ title:'GARDESA卡门', url:'http://ac-00QDJJp8.clouddn.com/8625a95b52b74884cb3e.jpg', type:'G200C' },
				{ title:'GARDESA卡门', url:'http://ac-00QDJJp8.clouddn.com/62239be9a72a1204bb12.jpg', type:'EGIDA100C' },
				{ title:'GARDESA卡门', url:'http://ac-00QDJJp8.clouddn.com/8ef6b3b960b6d1abe714.jpg', type:'DYNAMIC2A' },
				],

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

		// 轮播图
		.qy-carousel{
			width: 100%;
			height: 500px;
			img{
				width: 100%;
				height: 500px;
			}
		}
		// 案例
		.qy-cases{
			width: 1100px;
			margin:0 auto;
			height: 340px;
			text-align: left;
			padding-top: 30px;
			color: #05473e;
			// overflow: hidden;
			.case-main{
				margin-top: 15px;
				.item{
					float: left;
					width: 250px;
					margin-right:33px;
					height: 230px;
					text-align: center;
					font-size: 16px;
					background: #fff;
					cursor: pointer;
					img{
						width: 100%;
						height: 190px;
					}
					.bov-text{
						height: 40px;
						margin-top: -7px;
						padding: 8px 0;
						transition:.5s;
					}
				}
				.item:last-child
				{ 
					margin-right: 0;
				}
				.item:hover{
					.bov-text{
						background: #05473e;
						color: #fff;
					}
				}
				
			}
		}
		// 关于我们
		.qy-about{
			text-align: left;
			height: 310px;
			width: 100%;
			background: #e9f2f0;
			padding-top: 30px;
			.main{
				width: 1100px;
				margin: 0 auto;
				.left{
					width: 700px;
					float: left;
					.content{
						margin-top: 15px;
						img{
							width: 265px;
							float: left;
						}
						.left-content{
							width: 400px;
							float: right;
							p{
								text-indent: 2rem;
								color: #333;
							}
						}
					}
				}
				.right{
					width: 400px;
					float: left;
					padding-left: 50px;
					img{
						width: 345px;
						margin-top: 20px;
					}
				}
			}
		}
		// 新闻动态
		.qy-news{
			width: 1100px;
			margin:0 auto;
			height: 340px;
			text-align: left;
			padding-top: 30px;
			color: #05473e;
		}
		// 产品展示
		.qy-products{
			text-align: left;
			height: 500px;
			width: 100%;
			background: #e9f2f0;
			padding-top: 30px;
			.main{
				width: 1100px;
				margin: 0 auto;
				.pro-content{
					margin-top: 20px;
					.item{
						float: left;
						width: 250px;
						margin-right:33px;
						height: 400px;
						text-align: center;
						font-size: 16px;
						background: #fff;
						cursor: pointer;
						border: 1px solid #125b57;
						padding: 10px;
						transition:.5s;
						img{
							width: 230px;
							height: 300px;
						}
						.bov-text{
							height: 40px;
							margin-top: 7px;
							transition:.7s;
							p{
								line-height: 25px;
								color: #125b57;
							}
						}
					}
					.item:last-child
					{ 
						margin-right: 0;
					}
					.item:hover{
						background: #125b57;
						.bov-text{
							p{
								color:#fff;
							}
						}
					}
				}
			}
		}
		// 合作企业
		.qy-partners{
			width: 1100px;
			margin:0 auto;
			height: 200px;
			text-align: left;
			padding-top: 30px;
			color: #05473e;
			.main{
				.a-partner{
					width: 200px;
					margin: 2px 0 2px 20px;
					img{
						width: 100%;
					}
				}
				.up{
					float: right;
				}
				.bot{
					float: right;
					margin-right: 50px;
				}
				.a-partner:hover{
					opacity: .8;
				}
			}
		}
		.more-btn{
			float: right;
			color: #fff;
			background: #eb8a2d;
			padding: 0 4px;
		}
		.index-title{
			font-size: 18px;
			font-weight: bold;
			color: #125b57;
		}
	}
</style>
