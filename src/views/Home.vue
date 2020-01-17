<template>
	<div>
		<div class="container">
			<div class="topstory-tabs">
				<div class="topstory-tabs-bar">
					<ul class="topstory-tabs-list">
						<li class="nav-item"><router-link to="/home/recommend">推荐</router-link></li>
						<li class="nav-item"><router-link to="/home/follow">关注</router-link></li>
						<li class="nav-item"><router-link to="/home/hot">热榜</router-link></li>
					</ul>
				</div>
			</div>
		</div>
		<router-view />
	</div>
</template>

<script>
export default {
	data() {
		return {};
	},
	created() {},
	methods: {}
};
</script>

<style lang="scss" scoped>
.router-link-active {
	// border-bottom: 2px solid #fff;
	color: rgb(7, 104, 203);
}
.topstory-tabs {
	position: fixed;
	width: auto;
	top: 50px;
	z-index: 999;
}
.topstory-tabs-bar {
	width: 100%;
	height: 50px;
	background: #aaaaaa;
}
.topstory-tabs-list {
	width: 80%;
	margin: 0 auto;
	display: flex;
	align-items: center;
}
</style>
