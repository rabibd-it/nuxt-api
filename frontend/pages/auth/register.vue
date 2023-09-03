<script setup>
const from = reactive({
  name:null,
  mobile:null,
  email:null,
  password:null
});

const handleFromSubmit = ()=>{
  console.log(from)
}
</script>
<template>
  <div class="w-full mx-auto max-w-sm p-4 bg-white border border-gray-200 rounded-lg shadow sm:p-6 md:p-8 dark:bg-gray-800 dark:border-gray-700">
    <form class="space-y-6" @submit.prevent="handleFromSubmit">
      <h5 class="text-xl font-medium text-gray-900 dark:text-white">Create account</h5>
      <div>
        <FromLabel for="name">Name</FromLabel>
        <FromInput v-model="from.name" type="text" placeholder="Full Name"></FromInput>
      </div>
      <div>
        <FromLabel for="mobile">Mobile</FromLabel>
        <FromInput v-model="from.mobile" type="text" placeholder="Mobile Number"></FromInput>
      </div>
      <div>
        <FromLabel for="email">Email</FromLabel>
        <FromInput v-model="from.email" type="email" placeholder="Email Address"></FromInput>
      </div>
      <div>
        <FromLabel for="password">Password</FromLabel>
        <FromInput v-model="from.password" type="password" placeholder="Password"></FromInput>
      </div>
      <ButtonPrimary type="submit">
       Register to your account
      </ButtonPrimary>
      <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
        Already registered? <NuxtLink to="/auth/login" class="text-blue-700 hover:underline dark:text-blue-500">Login</NuxtLink>
      </div>
    </form>
  </div>
</template>
