<template>
    <div class="order">
        <HeaderTop title="订单列表"></HeaderTop>
        <div class="order_no_login">
            <img src="../../static/images/order/person.png">
            <h3>登录后查看外卖订单</h3>
            <button>立即登陆</button>
        </div>
    </div>
</template>

<script>
    import HeaderTop from "@/components/HeaderTop/HeaderTop";
    export default {
        name: "Order",
        components: {HeaderTop}
    }
</script>

<style lang="less">
    // Width variables (appears count calculates by raw css)
    @width0: 100%; // Appears 2 times


    .order {
        width: @width0;
        .order_no_login {
            margin: 0 auto;
            padding-top: 140px;
            text-align: center;
            width: 60%;
        }
        .order_no_login>img {
            display: block;
            height: 30%;
            width: @width0;
        }
        .order_no_login>h3 {
            color: #6a6a6a;
            font-size: 17px;
            padding: 10px 0;
        }
        .order_no_login>button {
            background: #02a774;
            border-radius: 5px;
            border: 0;
            color: #ffffff;
            display: inline-block;
            font-size: 14px;
            outline: none;
            padding: 10px 20px;
        }
    }
</style>