<template>
  <div :class="className" class="form-wrapper">
    <div class="checkout-form w-full">
      <div class="mb-16 text-2xl font-extrabold">Billing Address</div>
      <div class="form-group">
        <div class="first-name">
          <div class="mb-1.5">First Name</div>
          <input type="text" v-model="firstName" class="w-full h-16">
        </div>
        <div class="last-name">
          <div class="mb-1.5">Last Name</div>
          <input type="text" v-model="lastName" class="w-full h-16">
        </div>
        <div class="email">
          <div class="mb-1.5">Email Address</div>
          <input type="text" v-model="email" class="w-full h-16">
        </div>
        <div class="country">
          <div class="mb-1.5">Country</div>
          <input type="text" v-model="country" class="w-full h-16">
        </div>
        <div class="address">
          <div class="mb-1.5">Address</div>
          <input type="text" v-model="address" class="w-full h-16">
        </div>
        <div class="zipcode">
          <div class="mb-1.5">Zip Code</div>
          <input type="text" v-model="zipcode" class="w-full h-16">
        </div>
        <div class="city">
          <div class="mb-1.5">City/Town</div>
          <input type="text" v-model="city" class="w-full h-16">
        </div>
        <div class="phone-code">
          <div class="mb-1.5">Phone Code</div>
          <input type="text" v-model="phoneCode" class="w-full h-16">
        </div>
        <div class="phone">
          <div class="mb-1.5">Phone</div>
          <input type="text" v-model="phone" class="w-full h-16">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BillingForm',
  props: ['className'],
  data() {
    return {
      firstName: '',
      lastName: '',
      email: '',
      country: '',
      address: '',
      zipcode: '',
      city: '',
      phoneCode: '',
      phone: '',
    }
  }
}
</script>

<style lang="scss" scoped>
.form-wrapper {
  padding: 5vw;
  background: #edf4f6;

  .form-group {
    display: grid;
    grid-template-rows: repeat(6, 1fr);
    grid-template-columns: repeat(6, 1fr);
    gap: 1rem;

    .first-name {
      grid-column: 1 / span 3;
    }
    .last-name {
      grid-column: 4 / span 3;
    }
    .email, .country, .address {
      grid-column: 1 / span 6;
    }
    .zipcode, .phone-code {
      grid-column: 1 / span 2;
    }
    .city, .phone {
      grid-column: 3 / span 4;
    }
  }
  @media (max-width:1000px) {
    .form-group {
      grid-template-rows: repeat(9, 1fr);
      grid-template-columns: repeat(1, 1fr);

      .first-name, .last-name, .email, .country, .address, .zipcode, .phone-code, .city, .phone {
        grid-column: 1 / span 1;
      }
    }
  }
}
</style>
