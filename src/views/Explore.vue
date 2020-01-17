<template>
	<div class="container">
		<div class="row" >
			<div class="col-6" v-for="(item, index) in specials" :key="index">
				<img :src="item.banner" alt="">
				<h3>{{ item.title }}</h3>
				<p class="meta">{{ item.updated }}更新，{{ item.viewCount }}次浏览</p>
				<p class="intro">{{ item.introduction }}</p>
				<span v-for="(section, index) in item.sections" :key="index" class="section">
					{{ section.sectionTitle}}
				</span>
			</div>
		</div>
		<button class="btn btn-rd"><router-link to="/special/all">全部专题</router-link></button>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				specials:[]
			}
		},
		created() {
			this.axios.get('http://localhost:8080/api/special').then(res => {
				console.log(res);
				this.specials = res.data.data;
			});
		},
		methods: {
			
		},
		computed: {
			
		}				
	}
</script>

<style lang="scss" scoped>
	.container {
		margin-top: 60px;
	}
	.col-6 {
		margin-bottom: 5px;
		img {
			width: 98%;
		}
	}
</style>
