<template>
    <main>
        <router-view></router-view>
        <Overlay v-if="loading">
            <Spinner />
        </Overlay>
        <Overlay v-if="serverMsg !== ''">
            <ServerMessage :title="serverMsg" :okButtonConfirmed="resetAjax" />
        </Overlay>
    </main>
</template>

<script>
import Spinner from '../Spinner.vue';
import Overlay from '../Overlay.vue';
import ServerMessage from '../ServerMessage.vue';

export default {
  name: 'Main',
  components: {
    Spinner,
    Overlay,
    ServerMessage
  },
  props: {
    loading: Boolean,
    error: String,
    resetAjax: Function,
    serverMsg: String
  }
};
</script>
