<template>
    <v-card>
      <v-card-title>{{ title }}</v-card-title>
      <v-card-text>
        <v-form v-model="formOK" >
          <v-text-field
            label="Solo"
            :placeholder="title.toString()"
            solo
            v-model="idModel"
            :rules="rules.id"
            class="textfeld"

          ></v-text-field>
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-btn :disabled="!formOK" @click="$emit('submit',idModel)" color="primary" style="color: blue">
          Confirm
        </v-btn>
      </v-card-actions>
    </v-card>
</template>

<script>
export default {
  name: 'FormForm',
  props: {
    id: {
      type: Number,
      default: 0,
      require: true
    },
    title: {
      type: String,
      default: '',
      require: false
      // ne pisat
    }
  },
  data () {
    return {
      formOK: false,
      rules: {
        id: [
          v => !!v || 'Required',
          v => v < 5 || 'Too long'
          // !! zadano
        ]
      }
    }
  },
  computed: {
    title2 () {
      return this.id + '5'
    },
    idModel: {
      get () {
        return this.id
      },
      set (value) {
        this.$emit('update:id', value)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  // .textfeld{
  //   background-color: #fff ;
  // }
  // .input-38{
  //     background-color: green;
  //   }
// .textfield{
//   &:focus-within{
//     &::v-deep{
//       .v-input__slot{
//         fieldset
//           border-width: 2px
//           border-color: #785ECF
//           -webkit-box-shadow: 0 0 5px 1px #392E5F
//           box-shadow: 0 0 5px 1px #392E5F
//   &:hover
//     &::v-deep
//       .v-input__slot
//         fieldset
//           border-color: #785ECF
//   &::v-deep
//     .v-input__slot
//       fieldset
//         border-width: 2px
//         border-color: #392E5F
//         border-radius: 10px
//     .v-text-field__slot
//       color: white
//       .v-application
//         .primary--text
//           color: white !important
//   }
</style>
