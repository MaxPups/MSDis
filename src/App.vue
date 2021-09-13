<template>
  <FolderView/>
</template>

<script>
import FolderView from './components/FolderView.vue'
import data from './data/list';

export default {
  name: 'App',
  components: {
    FolderView
  },
  data: () => data
}
</script>


