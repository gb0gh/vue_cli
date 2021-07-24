<template>
    <div>
        <p>Header</p>
        <slot name="header" :comp="comp"></slot>
        <p>Body</p>
         <slot></slot>
         <p>footer</p>
        <button @click="updateName">update</button>
    </div>
</template>
<script>
export default {
    props : {
        title : {
            type : Object, //String, Number, Object형을 세팅가능
                        //타입이 안맞을시 에러
            required : true //true 항상 보내주는걸 설정
                            //false 안보내도됨
                            //default : 'default value' 항상 디폴트값을 전송하게됨                
        },
        name : {
            type : String,
            default : 'default name'
        },
       
    },

    data(){
        return {
            comp : {
                top : 'header top',
                bottom : 'header bottom'}
            //name : 'compTest'
        }
    }, 

    methods : {
        updateName() {
            //this.name = 'comp Test button'; 
            //부모에서 자식으로 변경시 error호출
        }
    }
}
</script>

<style scoped>

</style>