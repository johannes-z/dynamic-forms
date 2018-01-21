<docs>
  # TODO

  value binding
</docs>

<template>
  <component :is="tag" v-bind="$attrs">
    <slot>
      <FormElement
        v-for="(formElement, index) in children"
        :key="index"
        :tag="formElement.tag"
        :children="formElement.children"
      ></FormElement>
    </slot>
  </component>
</template>

<script>
export default {
  name: 'FormElement',
  props: {
    tag: {
      type: String,
      required: true
    },
    children: {
      type: Array,
      required: false,
      default () {
        return []
      }
    }
  },
  data () {
    return {
    }
  },
  methods: {
    addformElement (formElement) {
      this.formElements.children.push(formElement)
    },
    removeformElement (index) {
      this.formElements.children.splice(index, 1)
    }
  }
}
</script>
