<template>
	<div>
		<div class="nav">
			<div class="nav-bar">
				<ul class="nav-list">
					<li class="nav-item"><router-link to="/home">首页</router-link></li>
					<li class="nav-item"><router-link to="/explore">发现</router-link></li>
					<li class="nav-item"><router-link to="/question/waiting">等你来答</router-link></li>
					<li class="nav-item nav-right"><router-link to="/login">登录</router-link></li>
				</ul>
			</div>
		</div>
		<router-view/>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		created() {
			
		},
		methods: {
			
		},
		computed: {
			
		}				
	}
</script>

<style lang="scss" scoped>
	.router-link-active {
		border-bottom: 2px solid #fff;
	}
	.nav {
		background: rgb(7, 104, 203);
	}
	.nav-right {
		float: right;
	}
</style>
