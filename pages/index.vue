<template>
  <div>
    <div class="uk-flex uk-flex-center">
      <div class="uk-width-2-3 uk-margin-medium-top">
        <Search />
      </div>
    </div>
    <Latest />
  </div>
</template>

<script>
import Search from '@/components/Search'
import Latest from '@/components/device/Latest'

export default {
  components: { Latest, Search }
}
</script>
