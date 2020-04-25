<template>
<div class="login">
  <div class="login-container">
    <div class="login-container-account">
      <span class="login-container-account-text">学号</span>
      <input class="login-container-account-input" type="text" placeholder="请输入学号...">
    </div>
    <div class="login-container-pwd">
      <span class="login-container-pwd-text">密码</span>
      <input class="login-container-pwd-input" type="password" placeholder="请输入密码...">
    </div>
    <button class="login-container-btn">登录</button>
  </div>
</div>
</template>
<style lang="less" scoped>
  .login {
    padding: 0 10rem;
    &-container {
      display: flex;
      width: 30rem;
      height: 15rem;
      margin: 10rem 23rem;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      border: 1px solid #eee;
      border-radius: 4px;
      box-shadow: 5px 5px 10px #ccc;
      background-color: rgba(240,240,240,0.4);
      &-account,&-pwd {
        padding-bottom: 1rem;
        &-input {
          margin-left: 1rem;
          padding: 0.2rem 0.5rem;
          width: 15rem;
          height: 2rem;
          border: 1px solid #aaa;
          border-radius: 0.2rem;
          font-size: 1rem;
          &:hover {
            border-color: #42b983;
          }
        }
      }
      &-btn {
        width: 10rem;
        height: 2.5rem;
        border-radius: 0.5rem;
        border: none;
        font-size: 1rem;
        color: #fff;
        background-color: #42b983;
        cursor: pointer;
        &:hover {
          background-color: #42aa70;
        }
      }
    }
  }
</style>
