## 一款简单易用的个人主页代码，基于 NuxtJS

如标题所言，这是一款实现个人主页的代码，我实现了一些样式和基本的结构，以便您能够基于此快速地开发出您自己的个人主页。希望您不仅仅将其当作在线简历用于求职，这个页面足够简单，可以用来做一些更有趣的事！

您可以访问这里以 [这里](http://hlt.cab/) 最新的展示效果。

如果您喜欢本项目或者有更好的点子，欢迎 star 和提交 pr!

- 中文仓库：https://gitee.com/kkacdbdk/personal-homepage.git
- 英文仓库：https://github.com/spcodhu/personal-homepage.git


## 快速开始

####  本地运行

```
npm install
npm run dev -- -o
```

上面的代码会自动打开浏览器并访问 http://localhost:3000

#### Linux 上部署

推荐使用 PM2 。

拉取依赖并打包；

    ```
    npm install
    npm run build
    ```

在项目的根目录下准备一个 PM2 的配置文件 `ecosystem.config.js` 或者 `ecosystem.config.cjs`，内容如下：

    ```
    module.exports = {
        apps: [
            {
                name: 'PersonalHomePage',
                port: '3000',
                exec_mode: 'cluster',
                instances: 'max',
                script: './.output/server/index.mjs'
            }
        ]
    }

    ```

启动 PM2

    ```
    pm2 start ecosystem.config.js
    ```

如果您想要给这个页面配置一个域名的话，这里也提供了一个 Nginx 配置，最简单的即可。

    ```
    server {
        listen 80;
        server_name yourdomain.com www.yourdomain.com;

        location / {
            proxy_pass http://localhost:3000;
            proxy_set_header Host $host;
            proxy_set_header X-Real-IP $remote_addr;
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
            proxy_set_header X-Forwarded-Proto $scheme;
        }
    }
    ```

您需要确保您拥有一个已经备案的域名，且已经解析到当前服务器。

## 项目当前状态

**项目并未完全实现完成。** 因为我自己还是希望把这个做全一点的，具体来讲，还有几个点尚未完成：

- [ ] 需要加一个中英文切换的功能，使页面内容可用中英文展示；
- [ ] 页面内容尚未补充完整，比如旅游日记，后续准备加一个地图组件；
- [ ] 尝试给页面加上监控，考虑用第三方还是自己做。
欢迎 star，关注后续动态！

## 安全事项
请勿在公网个人主页中展示您的手机号码、携带 QQ 号码的 QQ 邮箱等个人信息；

在展示您的职业技能或项目信息时，也请注意信息脱敏；

在展示您的生活照片时，请不要直接将原图暴露在公网上，不法分子可以利用这些信息获取您的位置或其它隐私。您可以尝试将其动漫化处理。

## License
项目遵循 Apache-2.0 开源协议，且无商用限制。
    
