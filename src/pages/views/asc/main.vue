<style lang="less" module>
    @import '../../../assets/less/const.less';
    .wrap{
        background-image: url('@img/asc/banner.png');
        background-repeat: no-repeat;
        background-position: center;
        background-size: 100% 100%;
        min-height: 946*@px2rem;
        padding-top: 30*@px2rem;
    }
    .header{
        color: #fff;
    }
    .title{
       font-weight: bolder;
       width: 105*@px2rem;
       height: 55*@px2rem;
       background-image: url('@img/asc/title.png');
       background-repeat: no-repeat;
       background-size: 100%  100%;
    }
    .link{
        display: block;
        border: 2*@px2rem solid #FFFFFF;
        width: 200*@px2rem;
        height: 60*@px2rem;
        line-height: (60-4)*@px2rem;
        border-radius: 7*@px2rem;
        font-size: 32*@px2rem;
        color: #fff;
    }
    .content{
        width: 75%;
        min-width: 45*@px2rem;
        margin: 0 auto;
        padding: 0 .5rem;
        .logo{
            margin-top: 28*@px2rem;
            margin-left: auto;
            margin-right: auto;
            width: 119*@px2rem;
            height: 143*@px2rem;
            background:url('@img/asc/asc-logo.png') no-repeat;
            background-size: 100% 100%;
        }
        .desc{
            color: #fff;
            .dfn1{
                font-weight: bolder;
                margin-top: 23*@px2rem;
                font-size: 36*@px2rem;
                span{
                    padding: 0 7*@px2rem;
                    background: #FF4F4F;
                    border-radius: 7*@px2rem;
                }
            }
            .countDown{
                width: 480*@px2rem;
                overflow: hidden;
                margin: 60*@px2rem auto;
                padding: 4*@px2rem 50*@px2rem;
                border: 1*@px2rem solid #00CB38;
                border-radius: 7*@px2rem;
                font-size: 24*@px2rem;
                &.long{
                  width: 520*@px2rem;  
                   padding: 4*@px2rem 30*@px2rem;
                }
                .cdL{
                    float: left;
                }
                .cdR{
                    float: right;
                }
                .ct{
                    color: #00CB38;
                }
            }
            .dfn2{
                font-weight: bold;
                margin-top: 22*@px2rem;
                font-size: 32*@px2rem;
                .progress{
                    margin-top: 20*@px2rem;
                    height: 51*@px2rem;
                    border: 1*@px2rem solid #FFFFFF;
                    border-radius: 99*@px2rem;
                    overflow: hidden;
                    .fill{
                        height: 100%;
                        width: 10%;
                        background-image: linear-gradient(-90deg, #34DFF4 0%, #7B35FF 100%);
                    }
                }
                .addr{
                    margin-top: 16*@px2rem;
                    color: #4F9EF8;
                    font-size: 20*@px2rem;
                }
            }
            .dfn3{
                font-weight: bolder;
                margin-top: 50*@px2rem;
                font-size: 40*@px2rem;
            }
             .dfn4{
                margin-top: 15*@px2rem;
                font-size: 18*@px2rem;
            }
        }
    }
    .panel{
        font-size: 20*@px2rem;
        text-align: left;
        overflow: hidden;
        position: relative;
        .panelItem{
            
            color: #fff;
            padding-left: 20*@px2rem;
            border-left: 1px solid #fff;
            &:first-child{
                float: left;
            }
            &:nth-child(2){
                position: absolute;
                top: 0;
                left: 45%;
            }
            &:last-child{
                float: right;
            }
           
            .second{
                margin-top: 17*@px2rem;
            }
        }
    }
     .red{
                color: rgb(255,0,0);
            }
</style>

<template>
    <div :class="$style.wrap">
        <div :class="$style.content">
            <header :class="[$style.header,'clearfix']">
                <a :class="[$style.title,'fl']" href="./"></a>
                <a :class="[$style.link,'fr','text-center']" href="http://www.asc.services/pdf/asc.pdf" target="_blank">whiterpaper</a>
            </header>
            <div class="text-center">
                <div :class="$style.logo"></div>
                <article :class="$style.desc">
                    <div :class="$style.dfn1"><span>Anonymous</span> Service Chain</div>
                    <div :class="[$style.countDown,{[$style.long]:timeObj.distanceDay > 0}]">
                        <div :class="$style.cdL">Time left：</div>
                        <div :class="$style.cdR">
                            <template v-if="timeObj.distanceDay > 0">
                                <span :class="$style.ct">{{timeObj.distanceDay}} days</span> : <span :class="$style.ct">{{timeObj.distanceHour}} hours</span> : <span :class="$style.ct">{{timeObj.distanceMinute}} mins</span>
                            </template>
                            <template v-else>
                                <span :class="$style.ct">{{timeObj.distanceHour}}</span> : <span :class="$style.ct">{{timeObj.distanceMinute}}</span> : <span :class="$style.ct">{{timeObj.distanceSecond}}</span>
                            </template>
                        </div>
                    </div>
                    <div :class="$style.panel">
                        <div :class="$style.panelItem">
                            <div>
                                <span>Pre ICO Coin offering: </span>
                                <span :class="$style.red">100,000,000 (10%)</span>
                            </div>
                            <div>
                                <span>Current Bouns: </span>
                                <span :class="$style.red">50%</span>
                            </div>
                        </div>
                        <div :class="$style.panelItem">
                            <div>
                                <span>ETH Raised: </span>
                                <span :class="$style.red">10%</span>
                            </div>
                            <div>
                                <span>Soft Cap: </span>
                                <span :class="$style.red">4,999 ETH</span>
                            </div>
                        </div>
                        <div :class="$style.panelItem">
                            <div>
                                <span>1 ETH  =  20,000 AST</span>
                            </div>
                            <div>
                                <span>Bonus: </span>
                                <span :class="$style.red">50%</span>
                            </div>
                        </div>
                    </div>
                    <div :class="$style.dfn2">
                        <div :class="$style.progress">
                            <div :class="$style.fill"></div>
                        </div>
                        <div :class="$style.addr">
                            Take ETH only，send directly to the address：<span :class="$style.red">0x1a67B519f983bA54eB5936B17209F4b4c8481c89</span> we are totaly anonymous!
                        </div>
                    </div>
                    <div :class="$style.dfn3">What is ASC？</div>
                    <div :class="$style.dfn4">Anonymous Service Chain (ASC) is based on the blockchain technology, serving the global personal and small service providers of all industries, to provide the solution of anonymous reputation and payment . To build a standard of reputation for global anonymous services, along with the trusted payment for them .</div>
                </article>
            </div>
        </div>
    </div>
</template>
<script>
    const FINAL_DATE = new Date('2018/01/31 00:00:00').getTime();

    let numberFormat = (num)=>{
        if(num < 10){
            num = '0'+num;
        }
        return num;
    }
    let getCountElement = ()=>{
        let currentTime = Date.now();
        let distance = FINAL_DATE - currentTime;
        let distanceDay;
        let distanceHour;
        let distanceMinute;
        let distanceSecond;
        if(distance<0){
             distanceDay = '00';
             distanceHour = '00';
             distanceMinute = '00';
             distanceSecond = '00';
        }else{
             distanceDay = numberFormat(parseInt(distance/(24*60*60*1000)));
             distanceHour = numberFormat(parseInt(distance/(60*60*1000))%24);
             distanceMinute = numberFormat(parseInt(distance/(60*1000)%60));
             distanceSecond = numberFormat(parseInt(distance/(1000)%60));
        }
       
        return {
            distanceDay,
            distanceHour,
            distanceMinute,
            distanceSecond
        }

    }
    export default {
        data(){
            return{
                timeObj:{}
            }
        },
        methods:{
             countdown(){
                this.timeObj = getCountElement();
                window.setInterval(()=>{
                    var obj = getCountElement();
                    this.timeObj = obj;
                },1000);
            },
        },
        created(){
            this.countdown();
        }
    }

</script>

