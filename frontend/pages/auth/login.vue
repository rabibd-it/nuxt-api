<script setup>
const from = reactive({
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
      <h5 class="text-xl font-medium text-gray-900 dark:text-white">Sign in to our platform</h5>
      <div>
        <FromLabel for="email">Email</FromLabel>
        <FromInput v-model="from.email" type="email" placeholder="Email Address"></FromInput>
      </div>
      <div>
        <FromLabel for="password">Password</FromLabel>
        <FromInput v-model="from.password" type="password" placeholder="Password"></FromInput>
      </div>
      <div class="flex items-start">
        <div class="flex items-start">
          <div class="flex items-center h-5">
            <input id="remember" type="checkbox" value="" class="w-4 h-4 border border-gray-300 rounded bg-gray-50 focus:ring-3 focus:ring-blue-300 dark:bg-gray-700 dark:border-gray-600 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800" required>
          </div>
          <label for="remember" class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300">Remember me</label>
        </div>
        <a href="#" class="ml-auto text-sm text-blue-700 hover:underline dark:text-blue-500">Lost Password?</a>
      </div>
      <ButtonPrimary type="submit">
        Login to your account
      </ButtonPrimary>
      <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
        Not registered? <NuxtLink to="/auth/register" class="text-blue-700 hover:underline dark:text-blue-500">Create account</NuxtLink>
      </div>
    </form>
  </div>
</template>
