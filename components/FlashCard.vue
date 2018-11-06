<template>
	<div>
		<div>
		<el-radio-group v-model="flipTime" @change="onChangeRadio">
		  <el-radio-button :label="2">2秒後</el-radio-button>
		  <el-radio-button :label="4">4秒後</el-radio-button>
		  <el-radio-button :label="6">6秒後</el-radio-button>
		</el-radio-group>
		</div>
		<el-card class="box-card">
		  <div v-if="isFront">{{ drill[this.index].text1 }} </div>
		  <div v-else>{{ drill[this.index].text2 }}</div>
		</el-card>
		<el-button  @click="goNext">次の問題</el-button>
	</div>
</template>


<script>
export default {
	mounted() {
		this.flip()
	},
	props: {
	    drill: {
	      type: Array,
	      required: true
	    }
	},
	data() {
		return {
			index: 0,
			isFront: true,
			flipTime: 2,
		}
	},
	methods: {
		onChangeRadio() {
			this.isFront = true
			this.flip()
		},
		flip() {
			const seconds = this.flipTime * 1000
			setTimeout( () => {
				this.isFront = false
			}, seconds);
		},
		goNext() {
			if (this.index === this.drill.length - 1) {
				this.open2()
				return
			}
			this.isFront = true
			this.index += 1
			this.flip()
		},
		open2() {
	        this.$confirm('全ての問題が終了しました、再度、実行しますか？', 'Warning', {
	         confirmButtonText: 'OK',
	          cancelButtonText: 'Cancel',
	           type: 'warning'
        }).then(() => {
            this.$message({
              type: 'success',
                message: '再度実行します'
          });
	        this.isFront = true
	        this.index = 0;
	        this.flip()
        }).catch(() => {
            this.$message({
             type: 'info',
               message: '問題終了'
           });          
         });	
	   }
	}
}
</script>

<style>
  .text {
    font-size: 14px;
  }

  .item {
    padding: 18px 0;
  }

  .box-card {
    width: 480px;
  }


</style>