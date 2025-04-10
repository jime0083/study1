<template>
    <div>
        <ul>
            <li v-for="(option,index) in options" :key="index">
                <button @click="selectOption(option)">{{ option }}</button>
            </li>
        </ul>
    </div>
</template>

<script>
export default{
    name:'AnswerChild',
    props:{
        options:Array
    },
    methods:{
        selectOption(option){
            this.$emit('answer-selected',option);
        }
    }
};
</script>