<template>
    <div>
     <label for="">Name</label>
      <input 
        type="text" 
        :value = "value" 
        style="padding:30px; border : 2px solid balck"
        @input="$emit('input', $event.target.value)" 
        >
        <!-- 다른방법으로는  @input="updateName"으로 메소드를 만들어 사용할수있음 -->
        <!--js의 keypress? 이벤트?같음-->
    </div>  
</template>

<script>
export default {
    props : {
        value : { //value는 input의 value를 뜻함
            type : String,
            required : true
        }
    },
    //methods : {
    //    updateName(e){
    //        console.log('inputfield의 메소드');
    //        this.$emit('update-name', e.target.value);
    //    }
    //}
}
</script>
