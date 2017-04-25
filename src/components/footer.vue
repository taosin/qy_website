<template>
	<div class="qy-footer">
		<div class="main">
			<ul class="ul-first">
				<li v-for="menu in menus" class="li-ul-first">
					<label>{{menu.text}}</label>
					<ul class="ul-child">
						<li v-for="ch in menu.child" class="li-ul-child">
							<router-link :to="ch.url" v-if="ch.url">{{ch.label}}</router-link>
							<a v-else>{{ch.label}}</a>
						</li>
					</ul>
				</li>
			</ul>
		</div>
		<div class="copyright">
			<p>版权所有 沪ICP1232213号-1</p>
			<p>@2017 XXXXXX有限公司 版权所有</p>
		</div>
	</div>
</template>
<script>
	export default {
		name: 'hello',
		data () {
			return {
				menus:[
				{ text:'关于我们',
				child:[
				{ label:'公司介绍', url:'/index' },
				{ label:'企业文化', url:'/index' },
				{ label:'企业荣誉', url:'/index' },
				{ label:'企业愿景', url:'/index' },
				]},
				{ text:'新闻动态',
				child:[
				{ label:'公司新闻', url:'/index' },
				{ label:'行业新闻', url:'/index' },
				]},
				{ text:'企业优势',
				child:[
				{ label:'高端商品', url:'/index' },
				{ label:'专业团队', url:'/index' },
				{ label:'成功案例', url:'/index' },
				{ label:'工程定制', url:'/index' },
				{ label:'售后服务', url:'/index' },
				]},
				{ text:'产品展示',
				child:[
				{ label:'防火门', url:'/index' },
				{ label:'实木复合门', url:'/index' },
				{ label:'墙板', url:'/index' },
				{ label:'系统门窗', url:'/index' },
				{ label:'GARDESA卡门', url:'/index' },
				]},
				{ text:'服务项目',
				child:[
				{ label:'住宅区', url:'/index' },
				{ label:'别墅区', url:'/index' },
				{ label:'写字楼', url:'/index' },
				]},
				{ text:'联系我们',
				child:[
				{ label:'地址：上海市' },
				{ label:'客服电话：021-3422-0000' },
				{ label:'电子邮件：service@qqq.com' }
				]}
				]
			}
		},
		attached(){
		}
	}
</script>

<style scoped lang="less">
	.qy-footer{
		width: 1100px;
		margin: 0 auto;
		height: 283px;
		border-top: 2px solid #a7b9b5;
		text-align: left;
		.main{
			padding: 20px;
			height: 200px;
			.ul-first{
				.li-ul-first{
					width: 140px;
					float: left;
					margin-right: 20px;
					color: #333;
					// text-align: center;
					label{
						font-size: 16px;
						font-weight: bold;
					}
					.ul-child{
						margin-top: 10px;
						line-height: 23px;
						font-size: 14px;
						a{
							color: #333;
						}
					}
				}
				.li-ul-first:first-child
				{ 
					text-align: left;
					margin-right: 0;
				}
				.li-ul-first:last-child
				{ 
					text-align: left;
					width: 240px;
					margin-right: 0;
					margin-left: 30px;
				}
			}
		}
		.copyright{
			width: 100%;
			background: #000;
			height: 80px;
			text-align: center;
			color: #fff;
			padding: 20px;
			font-size: 12px;
		}
	}
</style>