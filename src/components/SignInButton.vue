<template>
    <async-button :disabled="isPending" :color="color" @click="signIn">
      <span v-if="isPending">Signing in...</span>
      <slot />
    </async-button>
  </template>
  
  <script>
  import AsyncButton from './BaseAsyncButton.vue';
  import { signInAndGetUser } from '@/lib/microsoftGraph';
  
  export default {
    name: 'SignInButton',
    components: {
      AsyncButton,
    },
    inheritAttrs: false,
  
    props: {
      color: {
        type: String,
        default: 'primary',
      },
    },
  
    data() {
      return {
        isPending: false,
        user: null,
      };
    },
  
    methods: {
      async signIn() {
        this.isPending = true;

        try {
          this.user = await signInAndGetUser();
        } catch (error) {
          console.error(error);
        } finally {
          this.isPending = false;
        }
      },
    },
  };
  </script>
  