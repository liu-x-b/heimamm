<template>
  <div class="login-box">
    <div class="login-left">
      <div class="top">
        <img src="../assets/矢量智能对象 拷贝 9.png" alt class="top-pic" />
        <span class="top-left">黑马界面</span>
        <i class="top-center"></i>
        <span class="top-right">用户登录</span>
      </div>
      <el-form ref="form" :model="form" class="form">
        <el-form-item>
          <el-input v-model="form.name" placeholder="请输入手机号">
            <i slot="prefix" class="el-input__icon el-icon-user"></i>
          </el-input>
        </el-form-item>
        <el-form-item>
          <el-input v-model="form.name" placeholder="请输入密码">
            <i slot="prefix" class="el-input__icon el-icon-lock"></i>
          </el-input>
        </el-form-item>
        <el-form-item>
          <el-col :span="16">
            <div class="grid-content bg-purple">
              <el-input v-model="form.name" placeholder="请输入验证码">
                <i slot="prefix" class="el-input__icon el-icon-key"></i>
              </el-input>
            </div>
          </el-col>
          <el-col :span="8">
            <div class="grid-content bg-purple-light">
              <img src="../assets/erweima.png" alt class="er-img" />
            </div>
          </el-col>
        </el-form-item>
        <el-form-item>
          <el-checkbox-group v-model="form.type">
            <el-checkbox name="type">
              我已阅读并同意
              <el-link type="primary">用户协议</el-link>和
              <el-link type="primary">隐私条款</el-link>
            </el-checkbox>
          </el-checkbox-group>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" class="bth-elm">登录</el-button>
          <el-button type="primary" class="bth-elm">注册</el-button>
        </el-form-item>
      </el-form>
    </div>
    <img src="../assets/login_banner_ele.png" alt class="login-right" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: "",
        region: "",
        date1: "",
        date2: "",
        delivery: false,
        type: [],
        resource: "",
        desc: ""
      }
    };
  }
};
</script>

<style lang='less'>
.login-box {
  box-sizing: border-box;
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    225deg,
    rgba(20, 147, 250, 1),
    rgba(1, 198, 250, 1)
  );
  .login-left {
    width: 478px;
    height: 550px;
    background-color: #f5f5f5;
    padding-top: 48px;
    padding-left: 44px;
    padding-right: 44px;
    padding-bottom: 44px;
    box-sizing: border-box;
    .form {
      box-sizing: border-box;
      .bth-elm {
        width: 100%;
        margin-bottom: 20px;
      }
      .er-img {
        width: 100%;
        height: 40px;
      }
      .bth-elm + .bth-elm {
        margin: 0;
      }
    }
    .top {
      display: flex;
      align-items: center;
      margin-bottom: 20px;
      .top-pic {
        width: 22px;
        height: 17px;
        margin-right: 16px;
      }
      .top-left {
        font-size: 24px;
        margin-right: 14px;
      }
      .top-center {
        background-color: #c7c7c7;
        margin-right: 12px;
        width: 1px;
        height: 28px;
      }
      .top-right {
        font-size: 22px;
      }
    }
  }
  .login-right {
    width: 633px;
    height: 435px;
  }
}
</style>