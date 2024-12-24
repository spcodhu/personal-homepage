<template>
  <div class="app-container">
    <personalInfo></personalInfo>
    <projectExperience></projectExperience>
    <jobExperience></jobExperience>
    <blogsRecommended></blogsRecommended>
    <pageFooter></pageFooter>
  </div>
</template>

<style scoped>
  /* 主页面的样式 */
  .app-container {
    padding: 20px;
    min-height: 100vh;
    background-color: whitesmoke;
    display: flex;
    flex-direction: column;
    align-items: center; /* 使子元素水平居中 */
  }

  /* 每单个组件的盒子样式统一 */
  .single-container {
    width: 70%;
    max-width: 1140px;
    margin: 0 auto; 
    padding: 10px;
    margin-bottom: 10px;
    background-color: white;
  }

  .page-footer-container {
    margin-bottom: 0;
  }

/* 手机端样式（小于768px） */
@media (max-width: 767px) {
  /* 主页面的样式 */
  .app-container {
    width: 100%;
    padding: 0; /* 移除左右padding */
  }

  /* 每单个组件的盒子样式统一 */
  .single-container {
    width: 100%;
    max-width: 100%; 
    margin: 0; 
    padding: 5px;
    margin-bottom: 10px;
    background-color: white;
  }

  .page-footer-container {
    margin-bottom: 0;
  }
}

/* 确保响应式布局正常工作 */
@media screen and (max-width: 1200px) {
  .single-container {
    width: 80%;
  }
}

@media screen and (max-width: 992px) {
  .single-container {
    width: 100%;
    padding: 10px;
  }
}
</style>