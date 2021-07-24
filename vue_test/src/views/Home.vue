<template>
  <div>
    <h1>test</h1>
    <form action="">
      <inputField v-model="name"/>
      <!-- v-model 사용시 자식 컴포넌트에 알아서 전송됨-->
      <!--  @update-name="updateName" 
           이방법을 사용할시 메소드를 사용해야함
      -->
     <button @click="updatedName">submit</button>
    </form>
    {{ name }}
  </div>

</template>

<script>
import inputField from '@/components/inputField.vue';

export default {
  components: { inputField },
  data() {
    return {
      name : 'life cycle'
    }
  },

  beforeCreate(){
      console.log('beforeCreate',this.name);
  }, //생성 전에는 데이터 접근 불가능

  created(){
       console.log('beforeCreate',this.name);
  }, //생성후에는 접근가능

  beforeMount(){
       alert('before mounted');
  },

  mounted(){
        alert('mounted');
  }, //여기서부터 dom 접근가능

  beforeUpdate(){
       alert('before Update');
  },

  updated() {
      alert('updated');
  },

  beforeDestroy() {
       alert('before Destory');
  },
 
  destroyed(){
      alert('Destoryed');
  },

  methods : {
    updatedName() {
        this.name = 'update';
    }
  }

  //methods :{
  //  updateName(name) {
  //    console.log("home's updateName")
  //    this.name = name;
  // }
  //}
}
</script>

<style scoped>
h1 {
  color : red;
}
</style>
