<script setup>
  import {
    ref,
    reactive,
    computed,
    onMounted,
    onUnmounted,
    watch,
    watchEffect,
    provide,
    readonly,
    createApp
  } from 'vue'
  // const firstName = ref('john')
  // const lastName = ref('Doe')

  // const fullName = computed({
  //   get() {
  //     return firstName.value + ' ' + lastName.value;
  //   },
  //   set(newValue) {
  //     console.log(newValue,1010);
  //     [firstName.value, lastName.value] = newValue.split(' ');
  //   }
  // })
  // fullName.value = 'hhh aaa'
  // const classObj = reactive({
  //   active1: true,
  //   active2: false
  // })

  // const isActive = ref(true)
  // const error = ref(null)

  // const classObj = computed(() => ({
  //   active2: true,
  //   active1: false
  // }))
  // const styleObj = reactive({
  //   color: 'red',
  //   fontSize: '20px'
  // })
  // const myObj = reactive({
  //   title: '111',
  //   name: '222',
  //   age: '333'
  // })
  // function greet(event) {
  //   console.log(111);
  //   console.log(event);
  // }
  // const toggle = ref(null)
  // function inputChange(value) {
  //   console.log(toggle);
  // }

  // onMounted(() => {
  //   console.log(111);
  // })
  // const count = ref(0);
  //   watch(count, (newVal, oldVal) => {
  //     console.log(newVal,11);
  //     console.log(oldVal ,22);
  //   })
  // const todoId = ref(1)
  // const data = ref(null)
  // watchEffect(async () => {
  //   const response = await fetch(`https://jsonplaceholder.typicode.com/todos/${todoId.value}`)
  //   data.value = await response.json();
  //   console.log(data,1010);
  // })
  // watchEffect(async () => {
  //   todoId++
  // })
  // const input = ref(null)
  // onMounted(() => {
  //   input.value.focus()
  // })
  // const list = ref(['11','22','33'])

  // const itemRefs = ref([])

  // onMounted(() => {
  //   console.log(itemRefs.value);
  // })
  // const input = ref(null)
  // onMounted(() => {
  //   console.log(input);
  // })
  import point from './point.vue'
  // const name = ref('text')
  // const number = ref(2)
  // function onClick() {
  //   number++
  // }
  // provide('name', 'xiaoming')
  // provide('number', readonly(number))

  // function add() {
  //   number.value ++
  // }

  // const x = ref(0)
  // const y = ref(0)
  // function update(event) {
  //   x.value = event.pageX;
  //   y.value = event.pageY;
  // }
  // onMounted(() => window.addEventListener('mousemove', update))
  // onUnmounted(() => window.removeEventListener('mousemove', update))
  // import {useMouse} from './mouse.js'
  // const {x, y} = useMouse();

  // const vFocus = {
  //   mounted: (el) => el.focus()
  // }
  // const vColor = {
  //   mounted: (el, binding) => {
  //     el.style.color = binding.value
  //   }
  // }
  const vDemo = {
    mounted: (el, binding) => {
      el.style.border = `1px solid ${binding.value.color}`;
      // el.innerHTML = binding.value.text;
    }
  }
</script>

<template>
  <point v-demo="{color: 'pink', text: 'hello!'}">
    
  </point>
  <!-- <p v-demo="{color: 'pink', text: 'hello!'}">大大大大</p> -->
  <!-- <p>x：{{x}} y：{{y}}</p> -->
  <!-- <input v-focus type="text" name="" id="" style="width: 200px; height: 30px"> -->

  </template>