<template>
	<div>
		<div style="height: 52px;">
			<mt-search v-model="value" @focus.native.capture="searchvideo()" ></mt-search>
  	   </div>
    	<ul class="videoList">
    		<li>
    			<video width="150" height="100" poster="../assets/logo.png" controls src="../assets/123.mp4"></video>
    		</li>
    		<li>
    			<video width="150" height="100" controls src="../assets/123.mp4"></video>
    		</li>
    	</ul>
	</div>
</template>

<script>
import { Search } from 'mint-ui'
export default {
	components:{ Search },
    name: 'HelloWorld',
	data () {
	    return {
	      value: ''
	    }
	},
	methods:{
	  	searchvideo(){
	  		this.$router.push({path: '/videoList'});
	  	}
	}
}
</script>

<style scoped="scoped">
	.videoList{
		padding: 0;
		width: 100%;
		height: 100%;
	}
	.videoList li {
		list-style: none;
		float: left;
		margin-left: 20px;
	}
</style>