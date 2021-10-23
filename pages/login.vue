<template>
  <div>
    <el-form ref="form" :model="form" label-width="120px">
      <el-form-item label="Correo">
        <el-input v-model="form.name" type="email"></el-input>
      </el-form-item>
      <el-form-item label="Contraseña">
        <el-input v-model="form.password" type="password"></el-input>
      </el-form-item>
      <el-form-item label="Recordarme">
        <el-checkbox v-model="rememberMe"></el-checkbox>
      </el-form-item>
        <el-button type="primary" @click="onSubmit">Create</el-button>
        <el-button>Cancel</el-button>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'Login',
  layout: 'form',
  data() {
    return {
      form: {
        email: '',
        password: '',
        rememberMe: false,
      },
    }
  },
  methods: {
    onSubmit() {
      console.log('submit!')
    },
  },
}
</script>