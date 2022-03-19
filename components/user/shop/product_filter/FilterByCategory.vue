<template>
  <div :class="className">
    <button @mouseenter="showOptions">{{ buttonName }}  <i class="fas fa-caret-down"></i></button>
    <div v-if="show" class="option-list shadow-2xl" @mouseleave="hideOptions">
      <button
        v-for="(option, i) in options"
        :key="i"
        @click="selectOption(option)"
      >{{ option.name }}</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "FilterByCategory",
  props: ['className'],
  data() {
    return {
      buttonName: "Category",
      options: [
        {url: "", name: "All"},
        {url: "", name: "দুগ্ধজাত"},
        {url: "", name: "মসলা"},
      ],
      show: false,
    }
  },
  methods: {
    showOptions(){
      this.show = true
    },
    hideOptions(){
      this.show = false;
    },
    selectOption(option){
      this.buttonName = option.name
    }
  }
}
</script>

<style scoped>
.option-list{
  position: absolute;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  background: #f6f8fa;
  padding: 1rem;
}
</style>
