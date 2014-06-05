---
layout: post
title: github pages(for users)搭建过程
category: tech
tags: [github, page, jeklly]
---
{% include JB/setup %}

花了几天终于把网站搭好了，下面简单地写一下过程

##1.账号和域名
    在github上完成注册。新建一个repo,名字必须和登录名一致。
	买一个域名，我的是在godaddy上买的。买好之后还要设置一下，据说godday的DNS被墙了，
所以要设置一下nameserver。添加dnspod提供的两个dns到nameserver。之后在dnspod进行注册，添加刚买好的域名，
使用cname指向usr.github.io。这样域名设置部分就完成了。
##2.搭建
    可以自己搭建也可以找现有的pages修改，模板挺多。我用了ErnestDu的模板，具体代码如下：
	{% highlight bash %}
	git clone https://github.com/ErnestDu/ErnestDu.github.io.git
	git remove -rf ./git
	git clone https://github.com/zhangcz828/zhangcz828.github.io.git
	cp -r Ernest zhangcz828
	//change personal info to myself
	git add --all
	git commit
	git push
	{% endhighlight %}
	OK!Now I have my own blog!
