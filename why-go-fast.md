https://www.quora.com/How-does-the-Go-language-compile-so-fast-compared-to-Java

https://hackernoon.com/5-reasons-why-we-switched-from-python-to-go-4414d5f42690







Many reasons why Go compiles quickly:

  


* Fast compile times are an explicit design goal of Go.
* The grammar is compact and regular so it is simpler to parse.
* Each Go file declares its dependencies and it is an error to declare a dependency that is not used, so computing the dependency tree is efficient.
* The language has been designed to be easy to analyze and can be parsed without a symbol table
 
* The Go language itself is much simpler than Java so there is less for the compiler to do.
* The Go compiler is newer which means there is less crufty code in it.



### Why Go? {#7851}

**\#1 It Compiles Into Single Binary**

Golang built as a compiled language and Google developers did great job with it. Using _static linking_

it actually combining all dependency libraries and modules into one single binary file based on OS type and architecture. Which means if you are compiling your backend application on your laptop with Linux X86 CPU you can just upload compiled binary into server and it will work, without installing any dependencies there!



**\#2 Static Type System**

Type system is really important for large scale applications. Python is great and fun language but sometimes you are just getting unusual exceptions because trying to use variable as an integer but it turning out that it’s a string.

```
# Django will crash process because of this


def some_view(request):


    user_id = request.POST.get('id', 0)


    # If this post request has "id" parameter then


    # user_id would be a string, 


    # but you really thinking it is integer


    User.objects.get(id=user_id)
```

Go will let you know about this issue during compile time as a compiler error. This is where you winning time for this kind of stupid issues.

**\#3 Performance!!**

This could be surprising but in most of the application cases Go is faster than Python \(2 and 3\). Here is the results of[Benchmarking Game](https://benchmarksgame.alioth.debian.org/u64q/compare.php?lang=go&lang2=python3), which are unfair, it depends on application type and usecase.

For our case Go performed better because of his concurrency model and CPU scalability. Whenever we need to process some internal request we are doing it with separate Goroutine, which are 10x cheaper in resources than Python Threads. So we saved a lot of resources \(Memory, CPU\) because of the built in language features.

**\#4 You Don’t Need Web Framework For Go**

This is the most awesome thing about programming language. Go language creators and the community have built in so many tools natively supported by language core, that in most of the cases you really don’t need any 3rd party library. For example it has`http, json, html templating`built in language natively and you can build very complex API services without even thinking about finding library on Github!

But of course there is a lot of libraries and frameworks built for Go and making web applications with Go, but I’ll recommend build your web application or API service without any 3rd party library, because in most cases they are not making your life easier than using native packages.

**\#5 Great IDE support and debugging**

IDE support is one of the most important things when you are trying to switch your programming language. Comfortable IDE in average can save up to 80% of your coding time. I found[Go Plugin For JetBrains IDEA](https://github.com/go-lang-plugin-org/go-lang-idea-plugin)which has support also for \(Webstorm, PHPStorm, etc…\). That plugin is giving everything that you need for project development with the power of JetBrains IDEA you can really boost your development.

Based on our code base statistics, after rewriting all projects to Go we got 64% less code than we had earlier.

> You really don’t need to debug code which doesn’t exists. Less code, less troubles!

### Conclusion {#109a}

Go gave us huge flexibility, single language for all usecases and for all of them it working very very well. We got about 30% more performance on our Backend and API services. And now we can handle logging real time, transfer it to database and make a streaming with Websocket from single or multiple services! This is awesome outcome from Go language features.



