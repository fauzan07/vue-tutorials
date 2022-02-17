<template>
    <div>
        <h3>{{getResult}}</h3>
        <h3>{{getResultmethods}}</h3>
    </div>
</template>

<script>
export default {
    name : "ComputedProperty",
    data(){
        return {
            dollers : 100,
            rupeeVal : 70,
            discount : 10,
        }
    },
    //dynamic cal can be done with method but low performance
    methods : {
        getResultmethods(){
            return(this.dollers*this.rupeeVal)-this.discount;
        }
    },
    //dynamic cal provide high performance always use computed
    computed : {
        getResult(){
            return(this.dollers*this.rupeeVal)-this.discount;
        }
    }
}
</script>