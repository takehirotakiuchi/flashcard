<template>
	<div>
		<h1 class="title">
         ファイナンシャルプランナー
        </h1>
        <h2>
        	カテゴリー別
        </h2>
		  <ul>
		  	 <li>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/0">ライフプランニングと資金計画</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/1">リスク管理</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/2">金融資産運用</nuxt-link>
			    </el-card> 
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/3">タックスプランニング</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/4">不動産</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/5">タックスプランニング</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/6">相続、事業継承</nuxt-link>
			    </el-card> 
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/7">ライフプランニングと資金計画</nuxt-link>
			    </el-card>
		   </li>
		 </ul>
        <h2>
        	年代別
        </h2>
		  <ul>
		  	 <li>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/8">2016年1月</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/9">2016年5月</nuxt-link>
			    </el-card>
			    <el-card shadow="hover">
			      <nuxt-link to="/quiz/10">2016年9月</nuxt-link>
			    </el-card>
		   </li>
		 </ul>
	</div>
</template>

<script>
	
	export default {
		data(){
			return {

			}
		}
	}

</script>


<style scoped>
	li {
		list-style: none;
	}

	a {
		color: black;
		text-decoration: none;
		margin-top: 30px;
	}

	.title {
	  text-align: center;
	  margin-bottom: 10px;
	  font-weight: 500;
	  font-size: 50px;
	  color: #35495e;
	  letter-spacing: 1px;
    }
  
    nuxt-link {
    	margin: 30px;
    }

</style>