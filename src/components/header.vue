<template>
    <div class="header">
        <div class="header-info">
            <div class="left">
                <div>
                    <img src="@/assets/images/LOGO.png" alt="">
                    <span class="line"></span>
                </div>
                <div style="margin-top: 25px;">
                    
                    <p>加盟咨询</p>
                    <h2>400-863-5888</h2>
                </div>
            </div>
            <div class="right">
                <Menu mode="horizontal"  :active-name="tab" @on-select="router">
                    <MenuItem name="1">首页</MenuItem>
                    <MenuItem name="2">关于熙美</MenuItem>
                    <MenuItem name="3">招商加盟</MenuItem>
                    <MenuItem name="4">店面展示</MenuItem>
                    <MenuItem name="5">新闻资讯</MenuItem>
                    <MenuItem name="6">商学院</MenuItem>
                    <!-- <MenuItem name="7">熙美公益</MenuItem> -->
                    <MenuItem name="8">产品分类</MenuItem>
                </Menu>
                <span>|</span>
                <span>EN</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['tab'],
    data(){
        return {
            
        }
    },
    created() {
      
    },
    methods: {
        router(name){
            document.scrollingElement.scrollTop=0;
            switch (Number(name)){
                case 1:
                    this.$router.push({path: '/'});
                break;
                case 2:
                    this.$router.push({path: '/about'});
                break;
                case 3:
                    this.$router.push({path: '/order'});
                break;
                case 4:
                    this.$router.push({path: '/store'});
                break;
                case 5:
                    this.$router.push({path: '/news'});
                break;
                case 6:
                    this.$router.push({path: '/school'});
                break;
                case 7:
                    this.$router.push({path: '/publicGood'});
                break;
                default:
                    this.$router.push({path: '/product'});
                break;
            }
        }
    }
}
</script>

