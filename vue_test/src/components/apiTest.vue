<!--
<template>
    <div id="watchexample">
		<p>
			마법의 소라고동: <input v-model="question">
		</p>
		<p>{{ answer }}</p>
		<img :src= "img_src">
	</div>
</template>

<script>
var watchExampleVM = new Vue({
  el: '#watchexample',  
  data: {
    question: '',
    answer: '질문을 하기 전까지는 대답할 수 없습니다.',
    img_src : '',
  },
  watch: {
    // 질문이 변경될 때 마다 이 기능이 실행됩니다.
    question: function (newQuestion) {
      this.answer = '입력을 기다리는 중...'
      this.debouncedGetAnswer()
    }
  },
  created: function () {
    this.debouncedGetAnswer = _.debounce(this.getAnswer, 500)
  },
  methods: {
    getAnswer: function () {
      if (this.question.indexOf('?') === -1) {
        this.answer = '질문에는 일반적으로 물음표가 포함 됩니다. ;-)'
        return
      }
      this.answer = '생각중...'
      var vm = this
      axios.get('https://yesno.wtf/api')
        .then(function (response) {
          vm.img_src = ""
          vm.answer = _.capitalize(response.data.answer)
          vm.img_src = _.capitalize(response.data.image)
        })
        .catch(function (error) {
        	
          vm.answer = '에러! API 요청에 오류가 있습니다. ' + error
        })
    },

  }
})
</script>

<style scoped>

</style>
-->