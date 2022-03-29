<template>
  <div class="">
    <Header title="Profile" :pages="pages"/>
    <PasswordForm
      v-if="passwordEditMode"
      @normal_mode="deactivatePasswordEditMode"
      class-name="bg-white"
    />
    <ProfileForm
      v-else-if="profileEditMode"
      @normal_mode="deactivateProfileEditMode"
      :infos="infos"
      class-name="bg-white"
    />
    <Details
      v-else
      @profile_edit_mode="activateProfileEditMode"
      @password_edit_mode="activatePasswordEditMode"
      class-name="bg-white"
      :infos="infos"
    />
    <Summary className=""/>
  </div>
</template>

<script>
import Header from "../../components/default/Header";
import Summary from "../../components/default/Summary";
import Details from "../../components/user/account/profile/Details";
import ProfileForm from "../../components/user/account/profile/ProfileForm";
import PasswordForm from "../../components/user/account/profile/PasswordForm";


export default {
  name: 'ProfilePage',
  layout: 'user',
  head:{
    title: "Profile - Asthar Bazar - Promises 100% Reliance"
  },
  components: {Header, Summary, Details, ProfileForm, PasswordForm },
  data () {
    return {
      pages: [
        {name: "Home", url: "/account"},
        {name: "Profile", url: "/account/profile"},
      ],
      profileEditMode: false,
      passwordEditMode: false,
      infos: [
        {title: "Name", value: "Mr. User"},
        {title: "Username", value: "user88"},
        {title: "Email", value: "user@email.com"},
        {title: "Phone", value: ""},
        {title: "Address", value: ""},
        {title: "Zip Code", value: ""},
        {title: "City", value: ""},
        {title: "Country", value: ""},
        {title: "Joined", value: "2021-08-24"},
      ]
    }
  },
  methods: {
    activateProfileEditMode(){
      this.profileEditMode = true
    },
    deactivateProfileEditMode(){
      this.profileEditMode = false
    },
    activatePasswordEditMode(){
      this.passwordEditMode = true
    },
    deactivatePasswordEditMode(){
      this.passwordEditMode = false
    },
  }
}
</script>

<style scoped>

</style>
