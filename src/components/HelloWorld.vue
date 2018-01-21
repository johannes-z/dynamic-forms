<template>
  <div class="hello">
    <!-- <FormInput tag="input" type="number" /> -->

    <FormElement tag="div">
      <FormElement tag="input" type="number" />
    </FormElement>

    <!-- <FormInput v-for="(formInput, index) in formElements" :key="index"
      :tag="formInput.tag"
      :children="formInput.children">
    </FormInput> -->
  </div>
</template>

<script>
import FormElement from './FormElement.vue'

export default {
  components: {
    FormElement
  },
  data () {
    return {
      formElements: [
        {
          tag: 'div',
          children: [
            { tag: 'input' }
          ]
        }
      ]
    }
  }
}
</script>
