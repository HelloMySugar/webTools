<template>
    <div class="home">
        <div style="color: blue; cursor: pointer" @click="downloadFiles">点击下载多文件</div>
        <!--    <img alt="Vue logo" src="../assets/logo.png">-->
        <!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    </div>
</template>

<script>
    // @ is an alias to /src
    // import HelloWorld from '@/components/HelloWorld.vue'
    import { download } from '../tools/download.js';

    export default {
        name: 'Home',
        data() {
            return {
                imgsArr: [
                    {
                        name: '推荐哈哈哈哈哈',
                        url: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1588939492487&di=b11c29c22f5f048c1ab82ac4f95e0b73&imgtype=0&src=http%3A%2F%2Fa.hiphotos.baidu.com%2Fzhidao%2Fpic%2Fitem%2F5366d0160924ab1857f1cbae35fae6cd7a890b47.jpg'
                    },
                    {
                        name: '顶顶顶',
                        url: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1588939492487&di=b11c29c22f5f048c1ab82ac4f95e0b73&imgtype=0&src=http%3A%2F%2Fa.hiphotos.baidu.com%2Fzhidao%2Fpic%2Fitem%2F5366d0160924ab1857f1cbae35fae6cd7a890b47.jpg'
                    },
                    {
                        name: '花哈话话花',
                        url: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1588939492487&di=b11c29c22f5f048c1ab82ac4f95e0b73&imgtype=0&src=http%3A%2F%2Fa.hiphotos.baidu.com%2Fzhidao%2Fpic%2Fitem%2F5366d0160924ab1857f1cbae35fae6cd7a890b47.jpg'
                    }
                ]
            }
        },
        components: {
            // HelloWorld
        },
        methods: {
            downloadFiles() {
                this.imgsArr.forEach((item) => {
                    download(item.url, item.name)
                })
            }
        }
    }
</script>
