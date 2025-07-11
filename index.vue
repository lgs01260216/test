<template>
    <view class="content">

        <!-- 头部 -->
        <view class="header">
            <u-navbar :is-back="false" :border-bottom="false" title="医院器械租赁" :background="background"
                back-icon-color="#fff" title-color="#fff" title-size="32"> </u-navbar>
        </view>
        <!-- { background: 'transparent' } -->
        <!-- 全部 -->
        <view>
            <!-- 轮播图 -->
            <view class="wrap">
                <u-swiper :list="list" height="593"></u-swiper>
            </view>

            <!-- 搜索 -->
            <view class="search u-flex u-row-between">
                <view class="u-flex">
                    <image class="u-m-r-15" src="../../static/icon/search.png" style="width: 30rpx;height: 30rpx;">
                    </image>
                    <u-input placeholder='输入搜索' placeholder-style="color:#aeaeae; font-size:26rpx;"></u-input>
                </view>
                <view class="search1">
                    <view>搜索</view>
                </view>
            </view>

            <!-- 公告 -->
            <view class="notice u-flex u-row-between">
                <view class="u-flex">
                    <view class="new">最新公告</view>
                    <view class="notice-bar  u-flex">
                        <u-notice-bar :volume-icon="false" mode="horizontal" :list="list1" bg-color="#fff"
                            color="#030303">
                        </u-notice-bar>
                    </view>
                </view>

                <view class="more">更多</view>
            </view>

            <!-- 推荐商品 -->
            <view class="u-font-36 u-m-l-20" style="color: #000; font-weight: 500;">推荐商品</view>
            <!-- 推荐商品内容 -->
            <view class="recommend" v-for="index in 5" :key="index">
                <view class="goods" >
                    <view class="u-flex">
                        <image class="u-m-r-22" src="../../static/image/home-page-image.jpg"
                            style="width: 243rpx;height: 184rpx;">
                        </image>
                        <view @click="$gTo('/pages/index/detail')">
                            <view class="title u-font-32" style="color: #0a1831;font-weight: 500;width: 450rpx;">
                                雾化器NE-C25S 医用雾化细腻守护全家健康</view>
                            <view class="u-font-23" style="color: #9ea4ad;">历史租赁 200</view>
                            <view style="color: #fc410a;font-weight: 500;">
                                <text class="u-font-26">￥</text>
                                <text class="u-font-38">1690</text>
                                <text class="u-font-26">/月</text>
                                <text class="u-font-26 u-m-l-12">租赁价格</text>
                            </view>
                        </view>
                    </view>
                    <view style="display: flex;justify-content: flex-end;" @click="$gTo('/pages/index/detail')">
                        <view class="need">我要租赁</view>
                    </view>
                </view>
            </view>
        </view>
        <!--  -->
    </view>
</template>

<script>
    export default {
        data() {
            return {
                background: {
                     // backgroundColor: "#001f3f",
                     backgroundImage: 'linear-gradient(180deg, #0066ca, #0e6ecd,#1b76d0,#227bd1)',
                },
                list: [{
                        image: "../../static/image/home-page.jpg"
                    },
                    {
                        image: "../../static/image/home-page.jpg"
                    },
                    {
                        image: "../../static/image/home-page.jpg"
                    },
                    {
                        image: "../../static/image/home-page.jpg"
                    },
                ],
                list1: [
                    '欢迎来到医疗器械租赁官方平台',
                    '欢迎来到医疗器械租赁官方平台'

                ]
            };
        },
        methods: {},
    };
</script>

<style>
    page {
        background-color: #fff;
        padding-bottom: 100rpx;
    }

    /* 头部 */
    .header {
        position: absolute;
        top: 0;
    }

    /* 搜索 */
    .search {
        position: absolute;
        top: 110rpx;
        width: 92%;
        background-color: #fff;
        padding: 7rpx 6rpx 8rpx 29rpx;
        margin: 0 20rpx;
        border-radius: 60rpx;
    }

    .search1 {
        background-color: #0b67fd;
        color: #fff;
        font-size: 26rpx;
        line-height: 26rpx;
        padding: 16rpx 28rpx;
        border-radius: 60rpx;
    }

    /* 公告 */
    .notice {
        margin: 18rpx 32rpx 20rpx 20rpx;
    }

    .new {
        background-color: #1b76ff;
        color: #fff;
        font-size: 22rpx;
        line-height: 22rpx;
        padding: 8rpx 14rpx 9rpx 12rpx;
        border-radius: 10rpx;
    }

    .more {
        border-radius: 60rpx;
        border: 1rpx solid #2580fe;
        padding: 8rpx 20rpx;
        text-align: center;
        color: #2580fe;
        font-size: 22rpx;
        line-height: 22rpx;
    }

    .notice-bar {
        background-color: #f4f5f8;
        width: 450rpx;
    }

    /* 推荐商品 */
    .recommend {
        padding: 40rpx 20rpx 0 20rpx;
    }

    .goods {
        border-bottom: 1rpx solid #e9e9e9;
        padding-bottom: 26rpx;
    }

    .title {
        display: -webkit-box;
        -webkit-box-orient: vertical;
        overflow: hidden;
        -webkit-line-clamp: 2;
        text-overflow: ellipsis;
    }

    .need {
        background-color: #e7f1ff;
        color: #1677ff;
        font-size: 26rpx;
        line-height: 26rpx;
        padding: 20rpx;
        border-radius: 15rpx;
    }
</style>