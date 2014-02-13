# Compilation considered harmful

Manual compilation is a weakness of the runtime environment not to be able to do this for the developer when necessary. Since automated compilation wouldn't need a name, we can simply state: *Compilation considered harmful*.

## Differentiation

This doesn't imply what we sometimes refer to as "compiled languages" are in any way evil. Also, optional code transformation steps, e.g. for performance reasons, to be able to ship stuff in a single file or even for hiding code are a good thing. But the necessity to *always* execute manual steps is evil.

### Automation

First and foremost, it requires a further step which can easily be automated. Not automating it means wasting developer time.

### Invoking the compiler is not art but boilerplate

Second, compiler tools usually require a bunch of parameters. You need to pass a multitude of them (eventually making you create build scripts as a workaround), never know the right ones (chosing based on "sounds good" principle), and may even chose the wrong ones (changing the behaviour of the resulting program).

### Compilation time

Third, compilation in lots of cases is so painstakingly slow that people start wondering what to do. This may be because of the afforementioned parameter hell, or because of inefficient build scripts, or other reasons. What it causes is this:

![XKCD: Compiling](http://imgs.xkcd.com/comics/compiling.png)

*[XKCD: Compiling](http://xkcd.com/303/)*

Then, coming back, you discover this:

```sh
query_expression.cpp:(.text+0x24b4): undefined reference ...

make: *** [all] Error 2
real    103m3.057s
user    96m47.171s
sys     5m37.441s
```

Why does it take nowadays' computers still hours(!) to come to that conclusion?

It's not better if compilation only takes minutes, it's actually worse: That's too short to start something new, but long enough to interrupt your flow.

## Conclusion

The disruptions of having to execute manual compilation steps kills creativity and [RAD](http://de.wikipedia.org/wiki/Rapid_Application_Development).

## Further reading

* [Static typing considered harmful](http://blog.jayfields.com/2008/02/static-typing-considered-harmful.html), containing the interesting idea *In 5 years, we'll view compilation as the weakest form of unit testing.*
* [What to do while compiling?](https://productivity.stackexchange.com/questions/970/what-to-do-while-compiling), especially this answer: *I'm not a software developer so hopefully this question isn't totally ignorant, but if you're doing tens of edit/compile cycles a day and each compile cycle takes 10 minutes then it seems like a good use of that time would be using it to work on shortening the compile cycle.*
