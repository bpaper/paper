<template>
  <div class="login-container">
    <img src="../../assets/logo.png" alt="LoginLogo" class="logo" />
    <div class="tile-container">
      <p>隧道环境及人员</p>
      <p>监测系统</p>
    </div>

    <mu-container>
      <mu-form ref="form" :model="validateForm" class="mu-demo-form">
        <mu-form-item
          icon="account_circle"
          prop="username"
          :rules="usernameRules"
        >
          <mu-text-field
            placeholder="用户名"
            v-model="validateForm.username"
            prop="username"
          >
          </mu-text-field>
        </mu-form-item>
        <mu-form-item icon="locked" prop="password" :rules="passwordRules">
          <mu-text-field
            placeholder="密码"
            type="password"
            v-model="validateForm.password"
            prop="password"
          ></mu-text-field>
        </mu-form-item>

        <mu-form-item icon="code" prop="captcha" :rules="captchaRules">
          <mu-text-field
            placeholder="验证码"
            src=""
            alt="captcha"
          ></mu-text-field>
        </mu-form-item>

        <mu-form-item>
          <mu-button color="primary" @click="submit">提交</mu-button>
        </mu-form-item>
      </mu-form>
    </mu-container>

    <mu-dialog title="提示" width="360" :open.sync="openSimple">
      this is simple Dialog
      <mu-button slot="actions" flat color="primary" @click="closeSimpleDialog"
        >关闭</mu-button
      >
    </mu-dialog>

    <div class="bio-container">
      <p>Copyright © paper</p>
    </div>
  </div>
</template>

<script lang="ts">
</script>

<style lang="scss">
$font: #2d3a4b;
$bio: #2d3a4bcb;
$dark_gray: #889aa4;
$light_gray: #eee;

.login-container {
  background-color: $light_gray;
  min-height: 100%;
  width: 100%;
  overflow: hidden;
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  .title-container {
    font-size: 120px;
    color: $font;
    margin: 0px auto 180px auto;
    text-align: center;
    font-weight: bold;
  }
  .logo {
    width: 400px;
    height: 400px;
    margin: 200px auto 200px auto;
  }
  .mu-demo-form {
    width: 90%;
    margin: 0 auto;
    position: relative;
    .captcha {
      position: absolute;
      bottom: 80px;
      right: -50px;
    }
  }

  .bio-container {
    font-size: 60px;
    color: $bio;
    position: absolute;
    bottom: 10px;
    right: 60px;
  }
}
</style>
