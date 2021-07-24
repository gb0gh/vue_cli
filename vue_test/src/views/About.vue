<template>
    <div class="about">
        <h1>This is an about page</h1>
        <comptest>
            <template #header="head"> <!-- v-slot:header 를
                                  #header로 축약가능-->
                <div>
                    <h3>{{head.top}}</h3>
                    <h1>slot : header</h1>
                    <h2>hi</h2>
                    <h3>{{head.bottom}}</h3>
                    
                </div>
            </template>

            <template>
              <h1>slot : body</h1>
            </template>
            
        </comptest>
    </div>
</template>

<script>
    import comptest from '@/components/comp_test.vue';
    export default {
        components: {
            comptest
        },
        data() {
            return {}
        }
    }
</script>