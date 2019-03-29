<template>
  <div class="hello">
  	  <div style="height: 52px;">
  				<mt-search v-model="value" @focus.native.capture="videoList()" ></mt-search>
  	  </div>
      <div class="banner">
	      	<mt-swipe :auto="4000">
				  	<!--<mt-swipe-item><img src="../assets/蜂蜜1.jpg"></mt-swipe-item>-->
				  	<mt-swipe-item><img src="../assets/m3.jpg"></mt-swipe-item>
				  	<mt-swipe-item><img src="../assets/m2.jpg"></mt-swipe-item>
					</mt-swipe>
			</div>
			<div class="content">
				<h3>推荐</h3>
				<ul>
					<li>
						<video controls></video>
					</li>
				</ul>
			</div>
  </div>
</template>

<script>
import { Search,Swipe, SwipeItem } from 'mint-ui'

export default {
	components:{ Search, Swipe, SwipeItem },
  name: 'HelloWorld',
  data () {
    return {
      value: ''
    }
  },
  methods:{
  	videoList(){
  		this.$router.push({path: '/videoList'});
  		console.log(111)
  	}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .content{
  	text-align: center;
  }
  .banner{
  	height:150px;
  }
  .banner img{
  	height:100%;
  	width:100%;
  }
</style>
