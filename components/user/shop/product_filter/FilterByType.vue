<template>
  <div :class="className">
    <button @click="toggleOptions">{{ buttonName }}  <i class="fas fa-caret-down"></i></button>
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
  name: "FilterByType",
  props: ['className'],
  data() {
    return {
      buttonName: "Type",
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
    toggleOptions(){
      this.show ? this.hideOptions() : this.showOptions();
    },
    selectOption(option){
      this.buttonName = option.name
      this.hideOptions()
    }
  }
}
</script>

<style scoped>
.option-list{
  position: absolute;
  right: 60px;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  background: #f6f8fa;
  padding: 1rem;
}
</style>
