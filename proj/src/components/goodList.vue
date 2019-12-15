<template>
	<div name="show">
		<ul class="goodList">
			<li v-for="good in list">
				<img v-bind:src="good.img" />
				<p>{{good.goodName}}</p>
			</li>
		</ul>
	</div>
</template>
<style>
	.goodList li{
		list-style: none;
		width: 250px;
		height: 250px;
		float: left;
		color: red;
		
	}
</style>
<script type="text/javascript">
	export default{
		name:"show",
		data(){
			var obj=this;
			var url="";
			if(obj.goodId==1){
				url="json/phone.json";
			}else if(obj.goodId==2){
				url="json/bjb.json";
			}else{
				url="json/bjb.json";
			}
			this.$http.get(url).then(function(res){
				obj.list=res.data;
			})
			return {
				list:[]
			}
		},
		props:{
				goodId:Number
			},
			watch:{
				goodId(){
					var obj=this;
					var url="";
					if(obj.goodId==1){
						url="json/phone.json";
					}else if(obj.goodId==2){
						url="json/bjb.json";
					}else{
						url="json/bjb.json";
					}
					this.$http.get(url).then(function(res){
						obj.list=res.data;
					})
					return {
						list:[]
					}
				}
			}
	}
</script>