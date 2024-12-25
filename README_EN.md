## A Simple and Easy-to-Use Personal Homepage Code, Based on NuxtJS

As the title suggests, this is a codebase for a personal homepage that I have implemented with some styles and basic structure, allowing you to quickly develop your own personal homepage. I hope you will use it not only as an online resume for job seeking but also for some more interesting things!

You can visit [here](http://hlt.cab/) to see the latest showcase.

If you like this project or have better ideas, feel free to star and submit a pull request (PR)!

- Chinese repository: [Gitee](https://gitee.com/kkacdbdk/personal-homepage.git)
- English repository: [GitHub](https://github.com/yourusername/personal-homepage)

## Quick Start

#### Local Running

```
npm install
npm run dev -- -o
```

The above command will automatically open a browser and navigate to http://localhost:3000.

#### Deployment on Linux

It is recommended to use PM2.

Pull dependencies and package:

```
npm install
npm run build
```

Prepare a PM2 configuration file `ecosystem.config.js` or `ecosystem.config.cjs` in the root directory of the project, with the following content:

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

Start PM2:

```
pm2 start ecosystem.config.js
```

If you want to configure a domain name for this page, here is a simple Nginx configuration provided.

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

You need to ensure that you have a domain name that has been filed and has been resolved to the current server.

## Project Current Status

**The project is not fully implemented.** I personally hope to make it more comprehensive, specifically, there are a few points that are not yet completed:

- [ ] Need to add a Chinese-English toggle feature to display the page content in both languages;
- [ ] The page content is not yet complete, such as travel diaries, and I plan to add a map component later;
- [ ] Trying to add monitoring to the page, considering using a third party or doing it myself.
Welcome to star and follow for updates!

## Security Matters
Please do not display your phone number, QQ email with QQ number, or other personal information on your public personal homepage;

When showcasing your professional skills or project information, please also pay attention to information de-identification;

When displaying your life photos, do not directly expose the original images on the public internet, as malicious actors can use this information to obtain your location or other privacy. You can try to process them into anime style.

## License
The project follows the Apache-2.0 open-source agreement, with no commercial restrictions.
