<template>
	<div class="main">
	<div class="left">
	  		<Left></Left>
	  </div>
	  <div class="right">
	  	<div class="top">
	  		<div class="titl"><img src="../../public/img/titl.jpg"/></div>
	  	</div>
	  	<div class="bottom">
	  		<Right></Right>
	  	</div>
	  </div>
  </div>
</template>

<script type="text/javascript">
	import Left from "../components/Left.vue"
	import Right from "../components/Right.vue"
	export default{
		components:{
			Left,
			Right
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style type="text/css">
	*{
	margin: 0px;
	padding: 0px;
}
.main{
	margin-top: 10px;
}
.menu li{
	list-style: none;
	line-height: 80px;
	background-color: white;
	cursor: pointer;
	font-size: 20px;
}
.left{
	width: 160px;
	float: left;
	margin-left: 70px;
	background-color: #f5f5f5;
}
.right{
	width: 1000px;
	float: left;
	margin-left: 10px;
}

.titl img{
	width: 1000px;
}
.bottom{
	width: 1000px;
	height: 200px;
}
.remen{
	color: red;
}
</style>
