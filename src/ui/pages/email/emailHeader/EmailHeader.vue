<template>
    <div class="flex email-header items-center justify-end container">
        <button :disabled="!readyToSend" v-on:click="sendEmail">Send</button>
    </div>
</template>

<script>
export default {
  name: 'EmailHeader',
  props: {
    readyToSend: Boolean,
    sendEmail: Function
  }
};
</script>

<style scoped lang="scss">
.email-header {
  height: 55px;
  border-bottom: 1px solid #a5c6df;
}
</style>
