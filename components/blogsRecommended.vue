<script setup lang="ts">

const blogs = [
    {
        blog_name: '【打工日记】我的实习收获....',
        url: 'https://mp.weixin.qq.com/s/Rqg2ybnTnvww2cUYGUeKIg',
        blog_intro: `三个月，我作为实习生在深圳一家互联网公司的技术成长显著。虽技术栈固定，但实习生认识到技术选型需平衡新旧技术，重视技术调研过程。面对不熟悉的技术，实习生学会大胆提出方案，深入研究，提升解决问题能力。处理“屎山”代码时，实习生学会从宏观角度梳理业务逻辑，提高代码阅读效率。为减少Bug，实习生采用维护测试用例文档的方法，强调自测的重要性。总结认为，技术成长不仅是学习新工具，更是提升思维和解决问题的能力。`
    },
    {
        blog_name: '【dify】三分钟实现你的个人聊天助手',
        url: 'https://mp.weixin.qq.com/s/yG9qM0z4fr3gH1Dy9bryZA',
        blog_intro: `本文介绍并使用 docker-compose 实践了开源软件Dify，作为一个开源的大语言模型应用程序开发平台，它通过直观的界面结合了AI工作流、RAG、代理功能和模型管理等，极大地简化了从模型到应用的开发过程。该平台拥有52.1K的GitHub星标，提供了官网和详细的帮助文档。支持多种部署方式，包括docker-compose、本地源码启动和宝塔面板部署。用户可以选择不同的大模型供应商，并利用Dify提供的模板应用快速启动自己的AI对话应用。Dify还允许通过API将聊天助手集成到项目中，并提供了监控功能。此外，Dify支持工作流和Agent的高级拓展，遵循Apache License 2.0开源协议，适用于商业用途。`
    },
    {
        blog_name: '阿里云服务器被挂挖矿程序，如何解决以及原因思考',
        url: 'https://mp.weixin.qq.com/s/WLZSgidbikJUFXjvFkjbQg',
        blog_intro: `本文描述了我的阿里云服务器遭遇挖矿程序攻击的经历。我在更换服务器部署方式后，发现服务器异常，CPU使用率飙升至100%。通过排查，我发现了一个高占用的可疑进程，并采取了一系列措施清除挖矿程序，包括删除可疑文件、杀死进程、清除定时任务、检查并删除可疑用户，并修改了root密码。经判断我认为，Docker的使用可能是导致安全问题的一个因素，因为攻击者可能利用Docker的开放端口进行攻击。此外，本文还强调了服务器安全意识的重要性，并提供了一些基本的安全防护措施。`
    },
]

</script>

<template>
    <div class="blogs-recommended-container single-container">
        <div style="width: 100%;">
            <div class="containerTitle"><span style="font-size: 22px; color: white;">精选博客</span></div>
            <div v-for="(blog, index) in blogs" :key="index" style="margin: 10px 0;">
                <ULink
                    :to="blog.url"
                    active-class="text-primary"
                    inactive-class="text-gray-500 dark:text-gray-400 hover:text-gray-700 dark:hover:text-gray-200"
                    class="text-xl text-blod"
                    >
                    {{ blog.blog_name }}
                </ULink>
                <div>
                    <span style="white-space: pre-wrap;">{{ blog.blog_intro }}</span> 
                </div>
                <hr v-if="index !== blogs.length - 1" style="margin: 10px 0; border-style: dashed;">
            </div>
        </div>
    </div>
</template>


<style>
.blogs-recommended-container {
    height: auto;
    margin-bottom: 10px;
}

.containerTitle {
    width: 100%;
    padding-left: 20px;
    background-image: linear-gradient(180deg, #2af598 0%, #009efd 100%);;
}
</style>