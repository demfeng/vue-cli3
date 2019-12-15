<template>
	<div>
	<div class="remen">热门推荐</div>
	  
	  	<ul class="menu">
	  		<li @click="menu1" >手机</li>
	  		<li @click="menu2" >电脑</li>
	  		<li @click="menu3" >服饰</li>
	  		<li @click="menu4" >手表</li>	  		
	  		<li>家电</li>
	  		<li>学习用品</li>
	  		<li>办公用品</li>
	  		<li>游戏必备</li>
	  		<li>游戏卡通</li>
	  	</ul>
	  
    </div>
</template>

<script type="text/javascript">
	import Msg from "./msg.js"
	
	export default{
		methods:{
			menu1:function(){
				Msg.$emit("val","1");
			},
			menu2:function(){
				Msg.$emit("val","2");
			},
			menu3:function(){
				Msg.$emit("val","3");
			},
			menu4:function(){
				Msg.$emit("val","4");
			}
			
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style type="text/css">

</style>
