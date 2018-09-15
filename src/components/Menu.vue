<template>
    <div class="menu">
        <ul>
            <li class="menu-item" v-for="(item,index) in items" :key="index" @click="toggleSubMenu(item)">
                <div class="item-left">
                    <img :src="item.img" alt="">
                    <span>{{ item.text }}</span>
                </div>
                <div class="item-right">
                    <img src="@/assets/expand.png" alt="" v-show="!item.isSelect" class="icon">
                    <img src="@/assets/collapse.png" alt=""  v-show="item.isSelect" class="icon">
                </div>
                <div style="clear: both"></div>
                <ul v-show="item.subItems && item.isSelect" class="sub-menu" @click.stop>
                    <li v-for="(subItem,subIndex) in item.subItems" :key="subIndex">
                        <router-link :to="subItem.path">
                            <span>{{ subItem.text }}</span>
                        </router-link>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</template>

<script>
import member from '@/assets/member.png'
import overtime from '@/assets/overtime.png'
import rest from '@/assets/rest.png'
import book from '@/assets/book.png'
export default {
    methods: {
        toggleSubMenu(item){
            item.isSelect = !item.isSelect;
        }
    },
    data(){
        return {
            items: [
                {
                    img: member,
                    text: '组员管理',
                    isSelect: true,
                    subItems: [
                        {
                            text: '组员列表',
                            isSelect: false,
                            path: '/member/list'
                        },
                        {
                            text: '添加组员',
                            isSelect: false,
                            path: '/member/add'
                        }
                    ]
                },
                {
                    img: overtime,
                    text: '加班管理',
                    isSelect: false,
                    subItems: [
                        {
                            text: '查询加班',
                            isSelect: false,
                            path: '/overtime/query'
                        },
                        {
                            text: '新增加班',
                            isSelect: false,
                            path: '/overtime/add'
                        }
                    ]
                },
                {
                    img: rest,
                    text: '请假管理',
                    isSelect: false,
                    subItems: [
                        {
                            text: '查询请假',
                            isSelect: false,
                            path: '/rest/query'
                        },
                        {
                            text: '新增请假',
                            isSelect: false,
                            path: '/rest/add'
                        }
                    ]
                },
                {
                    img: book,
                    text: '图书管理',
                    isSelect: false,
                    subItems: [
                        {
                            text: '书籍列表',
                            isSelect: false,
                            path: '/book/list'
                        },
                        {
                            text: '新增图书',
                            isSelect: false,
                            path: '/book/add'
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
.menu{
    width: 200px;
    height: 100%;
    background: rgb(255, 255, 255);
    ul{
        height: 100%;
    }
    .menu-item{
        width: 100%;
        position :relative;
        padding: 10px 0 0 5px;
        margin-bottom :5px;
        .item-left{
            float: left;
            margin-left: 15px;
        }
        .item-right{
            float: right;
            margin-right: 5px;
            margin-top: -5px;
        }
        .sub-menu{
            margin-left: 15px;
            li{
                height: 30px;
            }
        }
    }
}
</style>

