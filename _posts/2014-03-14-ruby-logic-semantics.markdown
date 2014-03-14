---
layout: post
title:  "Ruby Logic Semantics"
date: 2014-04-14
categories:
---

I was looking through some of the <a href="http://www.ruby-doc.org">Ruby Core API</a> to sharpen the saw and maybe finally figure out symbols.

So I wrote up this silly script:
{% highlight ruby %}
def routine(n)
	until (n < -10)||(n > 10)
		det = rand(0..1)
			if det == 1
				n += 1
			else
				n -=1
			end
		puts n
	end
throw :done
end
catch(:done){routine(0)}

at_exit {puts "Tug O' War: Over"}
{% endhighlight %}

I want to get it down to something close to this:
{% highlight ruby %}
def routine(n)
	until (n < -10)||(n > 10)
		n rand(+,-) 1
		puts n
	end
throw :done
end
catch(:done){routine(0)}

at_exit {puts "Tug O' War: Over"}
{% endhighlight %}

I tried all kinds of variations
{% highlight ruby %}
until (n < -10)||(n > 10) #...
	n Random.[+, -] 1
	n rand[+, -] 1
	n (+||-) 1 # obviously silly
	n rand(:+, :-) 1
	# I noticed that `||` is a boolean function (binary)
	# while `|` is a unary function
	# not clear on the difference
{% endhighlight %}

Any ideas? I'm working on implementing a comments section <a href="https://github.com/mpalmer/jekyll-static-comments#readme">github.com/mpalmer/jekyll-static-comments</a> for times like this. But for now, I think my one MAYBE two reader(s) knows how to reach me.
