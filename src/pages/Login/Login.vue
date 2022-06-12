<template>
    <div class="loginContainer">
        <div class="loginInner">
            <div class="login_header">
                <h2 class="login_logo">硅谷外卖</h2>
                <div class="login_header_title">
                    <a href="javascript:;" class="on">短信登录</a>
                    <a href="javascript:;">密码登录</a>
                </div>
            </div>
            <div class="login_content">
                <form>
                    <div class="on">
                        <div class="login_message">
                            <input type="tel" maxlength="11" placeholder="手机号">
                            <button disabled="disabled" class="get_verification">获取验证码</button>
                        </div>
                        <div class="login_verification">
                            <input type="tel" maxlength="8" placeholder="验证码">
                        </div>
                        <div class="login_hint">
                            温馨提示：未注册硅谷外卖帐号的手机号，登录时将自动注册，且代表已同意
                            <a href="javascript:;">《用户服务协议》</a>
                        </div>
                    </div>
                    <div>
                        <div>
                            <div class="login_message">
                                <input type="tel" maxlength="11" placeholder="手机/邮箱/用户名">
                            </div>
                            <div class="login_verification">
                                <input type="tel" maxlength="8" placeholder="密码">
                                <div class="switch_button off">
                                    <div class="switch_circle"></div>
                                    <span class="switch_text">...</span>
                                </div>
                            </div>
                            <div class="login_message">
                                <input type="text" maxlength="11" placeholder="验证码">
                                <img class="get_verification" src="../../static/images/captcha.svg" alt="captcha">
                            </div>
                        </div>
                    </div>
                    <button class="login_submit">登录</button>
                </form>
                <a href="javascript:;" class="about_us">关于我们</a>
            </div>
            <a href="javascript:" class="go_back" @click="$router.back()">
                <i class="iconfont icon-jiantou2"></i>
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Login"
    }
</script>

<style lang="less">
    // Color variables (appears count calculates by raw css)
    @color0: #ffffff; // Appears 7 times
    @color1: #02a774; // Appears 6 times
    @color2: #dddddd; // Appears 4 times
    @color3: #999999; // Appears 3 times

    // Width variables (appears count calculates by raw css)
    @width0: 100%; // Appears 3 times
    @width1: 30px; // Appears 2 times

    // Height variables (appears count calculates by raw css)
    @height0: 100%; // Appears 2 times
    @height1: 48px; // Appears 2 times
    @height2: 16px; // Appears 2 times

    .loginContainer {
        background: @color0;
        height: @height0;
        width: @width0;
        .loginInner {
            margin: 0 auto;
            padding-top: 60px;
            width: 80%;
            .login_header {
                .login_logo {
                    color: @color1;
                    font-size: 40px;
                    font-weight: bold;
                    text-align: center;
                }
                .login_header_title {
                    padding-top: 40px;
                    text-align: center;
                }
                .login_header_title>a {
                    color: #333333;
                    font-size: 14px;
                    padding-bottom: 4px;
                    &:first-child {
                        margin-right: 40px;
                    }
                }
                .login_header_title>a.on {
                    border-bottom: 2px solid @color1;
                    color: @color1;
                    font-weight: 700;
                }
            }
            .login_content>form>div {
                display: none;
                input {
                    border-radius: 4px;
                    border: 1px solid @color2;
                    box-sizing: border-box;
                    font: 400 14px Arial;
                    height: @height0;
                    outline: 0;
                    padding-left: 10px;
                    width: @width0;
                    &:focus {
                        border: 1px solid @color1;
                    }
                }
                .login_message {
                    background: @color0;
                    font-size: 14px;
                    height: @height1;
                    margin-top: 16px;
                    position: relative;
                    .get_verification {
                        background: transparent;
                        border: 0;
                        color: #cccccc;
                        font-size: 14px;
                        position: absolute;
                        right: 10px;
                        top: 50%;
                        transform: translateY(-50%);
                    }
                }
                .login_verification {
                    background: @color0;
                    font-size: 14px;
                    height: @height1;
                    margin-top: 16px;
                    position: relative;
                    .switch_button {
                        border-radius: 8px;
                        border: 1px solid @color2;
                        color: @color0;
                        font-size: 12px;
                        height: @height2;
                        line-height: @height2;
                        padding: 0 6px;
                        position: absolute;
                        right: 10px;
                        top: 50%;
                        transform: translateY(-50%);
                        transition: background-color 0.3s, border-color 0.3s;
                        width: @width1;
                    }
                    .switch_button.off {
                        background: @color0;
                        .switch_text {
                            color: @color2;
                            float: right;
                        }
                    }
                    .switch_button.on {
                        background: @color1;
                    }
                    .switch_button>.switch_circle {
                        background: @color0;
                        border-radius: 50%;
                        border: 1px solid @color2;
                        box-shadow: 0 2px 4px 0 rgba(0,0,0,0.1);
                        height: @height2;
                        left: -1px;
                        position: absolute;
                        top: -1px;
                        transition: transform 0.3s;
                        width: 16px;
                    }
                }
                .login_hint {
                    color: @color3;
                    font-size: 14px;
                    line-height: 20px;
                    margin-top: 12px;
                }
                .login_hint>a {
                    color: @color1;
                }
            }
            .login_content>form>div.on {
                display: block;
            }
            .login_content>form {
                .login_submit {
                    background: #4cd96f;
                    border-radius: 4px;
                    border: 0;
                    color: @color0;
                    display: block;
                    font-size: 16px;
                    height: 42px;
                    line-height: 42px;
                    margin-top: 30px;
                    text-align: center;
                    width: @width0;
                }
            }
            .login_content {
                .about_us {
                    color: @color3;
                    display: block;
                    font-size: 12px;
                    margin-top: 20px;
                    text-align: center;
                }
            }
            .go_back {
                height: 30px;
                left: 5px;
                position: absolute;
                top: 5px;
                width: @width1;
            }
            .go_back>.iconfont {
                color: @color3;
                font-size: 20px;
            }
        }
    }
</style>