https://www.1fzd.com/thread-179914-1-1.html        //实名认证

https://www.cnblogs.com/code1992/p/11220261.html   //Failed to connect to github.com port 443: Timed out

https://www.jianshu.com/p/c2eb995ac42a             //SourceTree Push 代码报错：remote: Support for password authentication was removed on August 13, 2021

https://www.freesion.com/article/4493589183/       //【COCOS CREATOR 基础教程(其他)】—— 利用 GITHUB PAGES 发布游戏

https://www.jianshu.com/p/84de47d5050b             //Git操作Support for password authentication was removed on August 13, 2021. Please use a personal ac...

https://www.jianshu.com/p/740db404b925             //git密码修改问题解决方案(Window &Mac)

https://www.jianshu.com/p/d044b8a8bf48             //nodejs源码打包为可执行程序

https://www.jianshu.com/p/b6dfc7c886a9             //在github上部署静态网页

https://github.com/whtree/README.git


问题描述：

        我用sourcetree clone代码的时候报错。错误信息：error: RPC failed; curl 56 OpenSSL SSL_read: SSL_ERROR_SYSCALL, errno 10054

解决方法：

        网上搜到的命令：git config http.sslVerify "false"

        执行后无法识别，提示：git config http.sslVerify "false" fatal: not in a git directory

        输入：git config  --globle   http.sslVerify "false" 
		
		git config --global http.sslVerify "false"
		
		
1.1.4 Failed to connect to github.com port 443: Timed out问题解决
fatal: unable to access ‘https://github.com/xxxxx/xxxx.git/’: Failed to connect to github.com port 443: Timed out
今天使用git push的时候提示"fatal: unable to access ‘https://github.com/xxxxx/xxxx.git/’: Failed to connect to github.com port 443: Timed out"

git -c diff.mnemonicprefix=false -c core.quotepath=false --no-optional-locks fetch --no-tags origin
fatal: unable to access 'https://github.com/whtree/README.git/': Failed to connect to github.com port 443: Timed out

然后我输入了下面的这些命令：

git config --global http.proxy

查询到当前设置了代理，所以我取消这个设置：

git config --global --unset http.proxy

git config --global http.proxy
git config --global --unset http.proxy

再查询，已经没有了代理，然后再push,成功了！

然后就可以继续push了。

git -c diff.mnemonicprefix=false -c core.quotepath=false --no-optional-locks push -v --tags origin main:main
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: Authentication failed for 'https://github.com/whtree/README.git/'
Pushing to https://github.com/whtree/README.git

#your_token 在github中生成的token
#USERNAME 在GitHub中的用户名（不是你的登录账号）
#REPO 仓库名
git remote set-url origin https://<your_token>@github.com/<USERNAME>/<REPO>.git

git config --global --unset git.proxy
 
https://whtree.github.io/game-hcdxg/

















		
		

