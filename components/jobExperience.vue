<script setup lang="ts">

const jobs = [
    {
        job_name: '深圳市信锐网科技术有限公司',
        dateRange: '2024年09月 至 2024年12月',
        logoDir: '/img/sundray.jpg',
        position: '研发实习生',
        address: '深圳',
        jobIntro: `1、使用 Python 实现自动爬取数据的脚本（使用 Playwright 替换 bs4和谷歌搜索API），每周爬取数据量在千条以上，并调用公司内部大模型和接口对数据进行处理。现已部署在公司 Jenkins 上，连续稳定运行一个月未出现问题。得到了研发主管的肯定和奖励；
2、优化 AI 自动化生成测试样例的前端（Vue，ElementUI，JSDiff），接受用户传递的指令描述，分片分段整理成指令格式，传递给后端大模型生成测试样例。使用文本差异比较库 JsDiff 避免指令的重复请求。前端稳定运行，一周内大幅优化前端使用体验。
3、实现客户信息查询前端，帮助出差同事快速了解客户基本信息和诉求（Vue，ElementUI，marked.js，flask）。实现前端关键字查询、关联信息查询和多种筛选功能。项目在 PC 端和移动端企业微信都有很好的展示效果，再次得到研发主管奖励。
        `
    }
]

</script>


<template>
    <div class="job-experience-container single-container">
        <div style="width: 100%;">
            <div class="containerTitle"><span style="font-size: 22px; color: white;">实习经历</span></div>
            <div v-for="(job, index) in jobs" :key="index">
                <div style="display: flex; margin: 10px 0;">
                    <div style="width: 75px; display: inline-flex; overflow: hidden; margin-right: 10px;">
                        <img :src="job.logoDir" style="width: 100%; height: auto;" alt="信锐">
                    </div>
                    <div style="width: 85%; display: flex; flex-direction: column;">
                        <span style="font-size: 18px; 
                                     font-weight: bold;
                                     display: block;">
                            {{ job.job_name }}</span>
                            <div style="display: flex; flex-wrap: wrap;">
                                <span>{{ job.dateRange }}</span>
                            </div>
                            <div style="display: flex; flex-wrap: wrap;">
                                <span>{{ job.position }}</span>
                                <span class="verticalDivider">|</span>
                                <span>{{ job.address }}</span>
                            </div>
                    </div>
                </div>
                <div>
                    <span style="white-space: pre-wrap;">{{ job.jobIntro }}</span>
                </div>
            </div>  
        </div>
    </div>
</template>


<style>
.job-experience-container {
    height: auto;
    margin-bottom: 10px;
}

.containerTitle {
    width: 100%;
    padding-left: 20px;
    background-image: linear-gradient(180deg, #2af598 0%, #009efd 100%);;
}

.verticalDivider {
    color: rgb(211, 211, 211);
    margin: 0 10px;
}
</style>