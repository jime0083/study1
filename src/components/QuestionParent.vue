<template>
    <div>
        <h2>Q.好きな色は？</h2>
        <AnswerChild :options="options" @answer-selected="receiveAnswer" />
        <p v-if="selectedAnswer">あなたの回答:{{ selectedAnswer }}</p>
    </div>
</template>


<script>
import AnswerChild from './AnswerChild.vue';

export default{
    name:'QuestionParent',
    components:{
        AnswerChild
    },
    data(){
        return{
            options:['赤','青','緑'],
            selectedAnswer:''
        };
    },
    methods:{
        receiveAnswer(answer){
            this.selectedAnswer=answer;
        }
    }
};

</script>