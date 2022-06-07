<!-- <template>
  <h1>Composition Option API ref</h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is: {{count}}</span>
</template>

<script>
import {ref} from '@vue/reactivity'
export default {
  setup(){
    //state data. 
    const count = ref(0) //count변수를 0으로 초기화. ref는 레퍼런스 타입(즉, 객체. 그래서 속성을 가짐)

    //refs
    const result = ref(null) //null로 초기화 후 return 하면서 span 객체로 돌려줌

    //methods
    function addOne(){ //ref일때는 result.value라고 해야 온전하게 불러와짐. 
      result.value.textContent = `count is ${++count.value}`
    }

    return { //return하고 {}붙으면 자바스크립트에서는 리터럴객체 즉, {]안에는 value가 들어가야함.
      count, result, addOne //setup에서 쓴 것들을 리턴에 넣어야지 온전하게 쓸 수 있음
    }
  }
}
</script> -->


<template>
  <h1>Composition Option API ref</h1>
  <button @click="addOne">Add</button>
  <span ref="result">count is: {{count}}</span>
</template>

<script>
import {reactive, ref} from '@vue/reactivity' 
export default {
  setup(){
    // 복수개의 변수를 하나의 변수로 리턴하고자 할 때
    const state = reactive({
      count: ref(0),
    })

    const result = ref(null)  //null로 초기화 후 return 하면서 span 객체로 돌려줌


    function addOne(){ 
      result.value.textContent = `count is ${++state.count}`
    }

    return { 
      state, result, addOne 
    }
  }
}
</script>