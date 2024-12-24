<script setup lang="ts">

const findNumber = 10086
const weChat = "呼哧好大枫"

</script>


<template>
    <div class="page-footer-container single-container">
        <div style="width: 100%;">
            <div class="baseFooterInfo">
                <span class="footerSpan"><a href="https://www.cnblogs.com/spcodhu">博客园（作者博客尚在迁移中）</a></span>
                <span class="verticalDivider">|</span>
                <span class="footerSpan">微信公众号：{{ weChat }}</span>
                <span class="verticalDivider">|</span>
                <span class="footerSpan"><a href="https://it.ctgu.edu.cn/">三峡大学计信学院</a></span>
            </div>
            <div style="width: 100%; display: flex; justify-content: center;"> 
                <span class="footerSpan"><a href="https://beian.miit.gov.cn/">鄂ICP备2022018360号-3</a></span>
                <span class="verticalDivider mobileDisplayNone">|</span>
                <span class="footerSpan mobileDisplayNone">本站源码可以在 <a href="">此处</a> 找到！</span>
            </div>
        </div>
    </div>
</template>

<style>
.page-footer-container {
    margin-bottom: 10px;
}

.footerSpan {
    margin: 0 5px;
}

.verticalDivider {
    color: rgb(211, 211, 211);
}

.baseFooterInfo {
    width: 100%; 
    display: flex; 
    justify-content: center;
}


@media (max-width: 767px) {
.baseFooterInfo {
    display: none;
}

.mobileDisplayNone {
    display: none;
}
}
</style>