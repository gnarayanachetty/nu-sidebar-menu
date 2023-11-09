<template>
  <component
    :is="icon.element ? icon.element : 'i'"
    v-if="typeof icon === 'object' && icon.text"
    v-bind="attributes"
  >
    {{ icon.text }}
  </component>
  <p>{{ icon.text }}</p>
  <component
    :is="icon.element ? icon.element : 'i'"
    v-if="typeof icon === 'object' && !icon.text"
    v-bind="attributes"
  /> 
  <i v-if="!typeof icon == 'object'" v-bind="attributes" />
</template>

<script>
export default {
  compatConfig: { MODE: 3 },
  name: 'SidebarMenuIcon',
  props: {
    icon: {
      type: [String, Object],
      default: '',
    },
  },
  computed: {
    attributes() {
      return {
        class: [
          'vsm--icon',
          typeof this.icon === 'object' ? this.icon.class : this.icon,
        ],
        'aria-hidden': true,
        ...this.icon.attributes,
      }
    },
  },
}
</script>
