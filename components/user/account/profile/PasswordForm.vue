<template>
  <div :class="className" class="form-wrapper">
    <div class="profile-form w-full">
      <div class="mb-16 text-2xl font-extrabold">Update Password</div>
      <div class="form-group">
        <div class="form-item">
          <div class="mb-1.5">Old Password</div>
          <input type="password" v-model="oldPassword" class="w-full h-16">
        </div>
        <div class="form-item">
          <div class="mb-1.5">New Password</div>
          <input type="password" v-model="newPassword" class="w-full h-16">
        </div>
        <div class="form-item">
          <div class="mb-1.5">Confirm Password</div>
          <input type="password" v-model="confirmedPassword" class="w-full h-16">
        </div>
      </div>
    </div>
    <div class="form-buttons">
      <button
        @click="setNormalMode"
        class="form-buttons__button bg-green text-sm uppercase font-bold px-5 py-3">Cancel</button>
      <button class="form-buttons__button bg-green-inverted text-sm uppercase font-bold px-5 py-3">Save</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProfileForm',
  props: ['className', 'infos'],
  data() {
    return {
      oldPassword: '',
      newPassword: '',
      confirmedPassword: '',
    }
  },
  methods: {
    setNormalMode(){
      this.$emit('normal_mode', false)
    }
  }
}
</script>

<style lang="scss" scoped>
.form-wrapper {
  padding: 5vw;

  .profile-form {
    padding: 5vw;
    background: #edf4f6;

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }
  }

  .form-buttons {
    display: flex;
    justify-content: flex-end;
    gap: 1rem;
    margin: 1rem 0;

    .bg-white {
      background: #ddd;
      color: #414141;
      transition: 0.15s;

      &:hover {
        background: #414141;
        color: #fff;
      }
    }
  }

  @media (max-width: 765px) {
    .form-buttons {
      justify-content: flex-start;
    }
  }
}
</style>
