我是光年实验室高级招聘经理。
我在github上访问了你的开源项目，你的代码超赞。你最近有没有在看工作机会，我们在招软件开发工程师，拉钩和BOSS等招聘网站也发布了相关岗位，有公司和职位的详细信息。
我们公司在杭州，业务主要做流量增长，是很多大型互联网公司的流量顾问。公司弹性工作制，福利齐全，发展潜力大，良好的办公环境和学习氛围。
公司官网是http://www.gnlab.com,公司地址是杭州市西湖区古墩路紫金广场B座，若你感兴趣，欢迎与我联系，
电话是0571-88839161，手机号：18668131388，微信号：echo 'bGhsaGxoMTEyNAo='|base64 -D ,静待佳音。如有打扰，还请见谅，祝生活愉快工作顺利。

# hacktoberfest

A little web app for tracking participation in the devICT Hacktoberfest event.
The entire idea and name "Hacktoberfest" comes from the [Digital Ocean and
GitHub event](https://hacktoberfest.digitalocean.com/) by the same name.

## Contribute

Make Wichita a better place through code. Hop on over to [Our Hacktoberfest
app](https://devict-hacktoberfest.herokuapp.com) and register with your GitHub
portfolio.

# Development

You need to create an application on GitHub
[here](https://github.com/settings/applications/new). Set the "Homepage URL" to
`http://localhost:8080` and "Authorization callback URL" to
`http://localhost:8080/auth/github`, then put the ID
and secret in a file `secret.env` like this:

```
GITHUB_KEY=123abc123abc
GITHUB_SECRET=123abc123abc123abc123abc
```

# Running

You can run the app locally using [Docker](https://docker.com). There is
a docker-compose file that will run the app and database.

Using the configured compose file if you edit anything under `public/`
or `templates/` then the change will be available immediately. If you
change any `.go` files you will have to rebuild the image.

I'd recommend starting the db first in daemon mode then start the web
service in the foreground so you can easily restart it by canceling with
`Ctrl-c` then restart.

    docker-compose up -d db
    docker-compose up --build web
