<template>
  <base-header/>
  <slot></slot>
  <base-footer/>
</template>

<script>
import BaseFooter from "@/components/BaseFooter";
import BaseHeader from "@/components/BaseHeader";
export default {
  name: 'BasicLayout',
  components: {BaseHeader, BaseFooter}
}
</script>

<style>

</style>