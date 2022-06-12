<template>
    <div class="profile">
        <HeaderTop title="我的"></HeaderTop>
        <div class="profile-number" >
            <router-link to="/login" class="profile-link">
                <div class="profile_image">
                    <i class="iconfont icon-person"></i>
                </div>
                <div class="user-info">
                    <p class="user-info-top">登录/注册</p>
                    <p>
                <span class="user-icon">
                  <i class="iconfont icon-shouji icon-mobile"></i>
                </span>
                        <span class="icon-mobile-number">暂无绑定手机号</span>
                    </p>
                </div>
                <span class="arrow">
              <i class="iconfont icon-jiantou1"></i>
            </span>
            </router-link>
        </div>
        <section class="profile_info_data border-1px">
            <ul class="info_data_list">
                <a href="javascript:" class="info_data_link">
                    <span class="info_data_top"><span>0.00</span>元</span>
                    <span class="info_data_bottom">我的余额</span>
                </a>
                <a href="javascript:" class="info_data_link">
                    <span class="info_data_top"><span>0</span>个</span>
                    <span class="info_data_bottom">我的优惠</span>
                </a>
                <a href="javascript:" class="info_data_link">
                    <span class="info_data_top"><span>0</span>分</span>
                    <span class="info_data_bottom">我的积分</span>
                </a>
            </ul>
        </section>
        <section class="profile_my_order border-1px">
            <!-- 我的订单 -->
            <a href='javascript:' class="my_order">
            <span>
              <i class="iconfont icon-order-s"></i>
            </span>
                <div class="my_order_div">
                    <span>我的订单</span>
                    <span class="my_order_icon">
                <i class="iconfont icon-jiantou1"></i>
              </span>
                </div>
            </a>
            <!-- 积分商城 -->
            <a href='javascript:' class="my_order">
            <span>
              <i class="iconfont icon-jifen"></i>
            </span>
                <div class="my_order_div">
                    <span>积分商城</span>
                    <span class="my_order_icon">
                <i class="iconfont icon-jiantou1"></i>
              </span>
                </div>
            </a>
            <!-- 硅谷外卖会员卡 -->
            <a href="javascript:" class="my_order">
            <span>
              <i class="iconfont icon-vip"></i>
            </span>
                <div class="my_order_div">
                    <span>硅谷外卖会员卡</span>
                    <span class="my_order_icon">
                <i class="iconfont icon-jiantou1"></i>
              </span>
                </div>
            </a>
        </section>
        <section class="profile_my_order border-1px">
            <!-- 服务中心 -->
            <a href="javascript:" class="my_order">
            <span>
              <i class="iconfont icon-fuwu"></i>
            </span>
                <div class="my_order_div">
                    <span>服务中心</span>
                    <span class="my_order_icon">
                <i class="iconfont icon-jiantou1"></i>
              </span>
                </div>
            </a>
        </section>
    </div>
    </div>
    </section>
</template>

<script>
    import HeaderTop from "@/components/HeaderTop/HeaderTop";
    export default {
        name: "Profile",
        components: {HeaderTop}
    }
</script>

<style lang="less">
    @import "../../common/less/mixins";
    // Color variables (appears count calculates by raw css)
    @color0: #ffffff; // Appears 5 times
    @color1: #02a774; // Appears 3 times
    @color2: #f1f1f1; // Appears 2 times
    @color3: #333333; // Appears 2 times
    @color4: #ff9900; // Appears 2 times
    @color5: #ff5f3e; // Appears 2 times

    // Width variables (appears count calculates by raw css)
    @width0: 100%; // Appears 4 times
    @width2: 20px; // Appears 2 times

    // Height variables (appears count calculates by raw css)
    @height1: 20px; // Appears 2 times

    .profile {
        width: @width0;
        overflow: hidden;
        .profile-number {
            margin-top: 45.5px;
            .profile-link {
                .clearFix();
                background: @color1;
                display: block;
                padding: 20px 10px;
                position: relative;
                .profile_image {
                    border-radius: 50%;
                    float: left;
                    height: 60px;
                    overflow: hidden;
                    vertical-align: top;
                    width: 60px;
                    .icon-person {
                        background: #e4e4e4;
                        font-size: 62px;
                    }
                }
                .user-info {
                    float: left;
                    margin-left: 15px;
                    margin-top: 8px;
                    p {
                        color: @color0;
                        font-size: 18px;
                        font-weight: 700;
                        .user-icon {
                            display: inline-block;
                            height: @height1;
                            margin-left: -15px;
                            margin-right: 10px;
                            width: @width2;
                            .icon-mobile {
                                font-size: 30px;
                                vertical-align: text-top;
                            }
                        }
                        .icon-mobile-number {
                            color: @color0;
                            font-size: 14px;
                        }
                    }
                    p.user-info-top {
                        padding-bottom: 8px;
                    }
                }
                .arrow {
                    height: 12px;
                    position: absolute;
                    right: 15px;
                    top: 40%;
                    width: 12px;
                    .icon-jiantou1 {
                        color: @color0;
                        font-size: 5px;
                    }
                }
            }
        }
        .profile_info_data {
            .bottom-border-1px(#e4e4e4);
            background: @color0;
            overflow: hidden;
            width: @width0;
            .info_data_list {
                .clearFix();
                .info_data_link {
                    border-right: 1px solid @color2;
                    float: left;
                    text-align: center;
                    width: 33%;
                    .info_data_top {
                        color: @color3;
                        display: block;
                        font-size: 14px;
                        padding: 15px 5px 10px;
                        width: @width0;
                        span {
                            color: @color4;
                            display: inline-block;
                            font-size: 30px;
                            font-weight: 700;
                            line-height: 30px;
                        }
                    }
                    .info_data_bottom {
                        color: #666666;
                        display: inline-block;
                        font-size: 14px;
                        font-weight: 400;
                        padding-bottom: 10px;
                    }
                    &:nth-of-type(2) {
                        .info_data_top {
                            span {
                                color: @color5;
                            }
                        }
                    }
                    &:nth-of-type(3) {
                        border: 0;
                        .info_data_top {
                            span {
                                color: #6ac20b;
                            }
                        }
                    }
                }
            }
        }
        .profile_my_order {
            .top-border-1px(#e4e4e4);
            background: @color0;
            margin-top: 10px;
            .my_order {
                align-items: center;
                display: flex;
                padding-left: 15px;
                .my_order_div {
                    border-bottom: 1px solid @color2;
                    color: @color3;
                    display: flex;
                    font-size: 16px;
                    justify-content: space-between;
                    padding: 18px 10px 18px 0;
                    width: @width0;
                    span {
                        display: block;
                    }
                    .my_order_icon {
                        height: 10px;
                        width: 10px;
                        .icon-jiantou1 {
                            color: #bbbbbb;
                            font-size: 10px;
                        }
                    }
                }
            }
            .my_order>span {
                align-items: center;
                display: flex;
                height: @height1;
                width: @width2;
                .icon-order-s {
                    color: @color1;
                }
                .icon-jifen {
                    color: @color5;
                }
                .icon-vip {
                    color: @color4;
                }
                .icon-fuwu {
                    color: @color1;
                }
            }
            .my_order>span>.iconfont {
                font-size: 30px;
                margin-left: -10px;
            }
        }
    }
</style>