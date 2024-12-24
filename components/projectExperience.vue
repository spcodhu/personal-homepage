<script setup lang="ts">

const projects = [
    {
        pro_name: '电力行业客户自助服务系统',
        dateRange: '2024年06月 至 2024年07月',
        position: '后端开发',
        pro_intro: `系统实现了进行电力账单查询，用电查询，电力账单缴费，用电报装等操作，创新功能AI语音客服，客户可随时使用语音与AI客服进行交流。项目技术栈SpringCloud+Vue2，我负责的主要工作：
1. 负责构建后端基础框架，采用nacos结合SpringCloud技术，涵盖支付、文件处理及AI服务等模块；
2. 云服务器上docker部署环境的搭建； 
3. 使用企业账户调用支付宝支付（实际支付，非沙箱）； 
4. 使用aliyunSMS实现短信验证；
5. 腾讯云语音转文字+百度文心大模型的调用等功能。项目实现效果良好。
`
    },
    {
        pro_name: '班级信息化建设',
        dateRange: '2023年10月 至 2023年12月',
        position: '前端开发',
        pro_intro: `系统主要实现从用户上传的表格中计算考试的各种指标，并统计教师的分数并且需要导出教师的对比数据，实现帮助学校分析教师的教学成果。我负责的主要工作：
1. 从需求分析、功能编码到测试部署上线，全流程带领团队五名同学完成项目；
2. 使用SpringBoot、POI，MyBatisPlus，JWT，JavaMailSender，腾讯云 COS 对象存储等技术实现后端，并利用Knife4j生成接口文档；
3. 在计算大数据量的指标时，用redis实现后端进度条，通过桥接设计模式优化计算。
`
    },
    {
        pro_name: '示范基地平台建设',
        dateRange: '2023年03月 至 2023年06月',
        position: '后端开发',
        pro_intro: `系统主要是为基地、市级、省级三种权限中，实现文件和数据的来回预览审批，并修改Echarts地图组件实现展示各个地区的优秀基地分布。我负责的主要工作：
1. 参与文件审批系统开发，实现省、市、基地三级权限管理，确保文件高效流转；
2. 采用Vue 2 + ElementUI + Echarts技术栈，构建复杂页面，提升用户体验；
3. 运用Echarts图表展示全省优秀基地分布，实现数据可视化，辅助决策分析；
4. 与后端紧密合作，实现数据交互，精准呈现省级和市级优秀基地分布详情；
5. 遵循企业开发模式和统一代码规范，确保项目质量，项目已上线使用并获高度认可。
`
    }
]

</script>


<template>
    <div class="project-experience-container single-container">
        <div style="width: 100%;">
            <div class="containerTitle"><span style="font-size: 22px; color: white;">项目经历</span></div>
            <div v-for="(project, index) in projects" :key="index">
                <div style="width: 100%; height: 30px; margin: 5px 0;">
                    <span class="projectTitle">{{ project.pro_name }}</span>
                    <span class="projectDate smallSpan">{{ project.dateRange }}</span>
                </div>
                <div style="width: 100%;">
                    <span class="smallSpan">{{ project.position }}</span>
                </div>
                <div>
                   <span style="white-space: pre-wrap;">{{ project.pro_intro }}</span> 
                </div>
                <hr v-if="index !== projects.length - 1" style="margin: 10px 0;">
            </div>
        </div>
    </div>
</template>


<style>
.project-experience-container {
    height: auto;
    margin-bottom: 10px;
}

.containerTitle {
    width: 100%;
    padding-left: 20px;
    background-image: linear-gradient(180deg, #2af598 0%, #009efd 100%);;
}

.projectTitle {
   float: left;
   font-size: 20px;
   font-weight: bolder;
}

.projectDate {
    height: 30px;
    line-height: 30px;
    float: right;
}

.smallSpan {
    color: rgb(211,211,211);
}
</style>