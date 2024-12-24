<template>
    <div class="personal-info-container single-container">
        <div class="personalInfo">
            <!-- 个人信息 -->
            <div style="margin-right: 10px;">
                <img src="/img/me.jpeg" alt="磊涛" 
                    style="width: 150px; 
                        height: auto;
                        margin: 0 auto; 
                        overflow: hidden;
                        border: 1px solid transparent;
                        border-radius: 100%;">
            </div>
            <div>
                <span style="font-size: 24px; font-weight: bolder;"> 胡磊涛 </span>
                <div style="display: flex; align-items: center;">
                    <UIcon name="i-material-symbols:position-top-right-rounded" 
                        class="w-5 h-5" />
                    <span class="PCDisplay">全栈开发程序员、devOps工程师</span>
                    <div class="mobileDisplay">
                        <span> 全栈开发程序员、 </span>
                        <br>
                        <span> devOps工程师 </span>
                    </div>
                </div>
                <div style="display: flex; align-items: center;">
                    <UIcon name="i-material-symbols:mail-rounded" 
                        class="w-5 h-5" />
                    <span style="margin-left: 10px;"> leitao0906@qq.com </span>
                </div>
                <div style="display: flex; align-items: center;">
                    <UIcon name="i-maki:college-11" 
                        class="w-5 h-5" />
                    <span style="margin-left: 10px;"> 三峡大学 | 本科 </span>
                </div>
                <div style="display: flex; align-items: center;">
                    <UIcon name="i-simple-icons:microsoftacademic" 
                        class="w-5 h-5" />
                    <span style="margin-left: 10px;"> 计算机科学与技术 </span>
                </div>
            </div>
        </div>
    </div>
</template>


<style>
.personal-info-container {
    height: 200px;
    margin-bottom: 10px;
}

.personalInfo {
    width: auto;
    display: flex; 
    justify-content: center; 
    align-items: center;
}

.PCDisplay {
    margin-left: 10px;
}

.mobileDisplay {
    display: none;
}


@media (max-width: 767px) {
    .personalInfo {
        width: 100%; 
        display: flex; 
        justify-content: center; 
        align-items: center;
    }
    .mobileDisplay {
        display: block;
        margin-left: 10px;
    }

    .PCDisplay {
        display: none;
    }
}
</style>