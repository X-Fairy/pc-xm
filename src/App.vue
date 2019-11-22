<template>
  <div id="app">
		<keep-alive>
			<router-view v-if="$route.meta.keepAlive">
			<!-- 这里是会被缓存的视图组件 -->
			</router-view>
        </keep-alive>
        <!--  这里是不会被缓存的视图组件 -->
		<router-view v-if="!$route.meta.keepAlive"></router-view>
  </div>
</template>

<script>
export default {
  	name: "App",
	provide(){
		return{
			reload: this.reload
		}
	},
	data(){
		return{
			isRouterAlive: true
		}
	},
	created() {
	},
	
	methods: {
		reload() {
			this.isRouterAlive = false;
			this.$nextTick(function () {
				this.isRouterAlive=true;
			})
		},
    }
};
</script>


<style>
    #app {
        font-family: "Avenir", Helvetica, Arial, sans-serif;
        position: relative;
        background: #fff;
        font-family: 'Microsoft yahei',Arial !important;
        
    }
</style>
