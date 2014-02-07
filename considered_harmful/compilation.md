# Compilation considered harmful

Manual compilation is a weakness of the runtime environment not to be able to do this for the developer when necessary. Since automated compilation wouldn't need a name, we can simply state: *Compilation considered harmful*.

## Automation
First and foremost, it requires a further step which can easily be automated. Not automating it means wasting developer time.

## Compilation time
Second, compiler tools usually require a bunch of parameters. Invoking the compiler is not art but boilerplate, so this usually results in subpar efficiency, and that again leads to:

![XKCD: Compiling](http://imgs.xkcd.com/comics/compiling.png)

## Fail

```sh
query_expression.cpp:(.text+0x24b4): undefined reference ...

make: *** [all] Error 2
real    103m3.057s
user    96m47.171s
sys     5m37.441s
```

Don't you just hate these kinds of things? I mean, come on, why does it take nowadays' computers still hours(!) to come to that conclusion?

## Further reading

* [Static typing considered harmful](http://blog.jayfields.com/2008/02/static-typing-considered-harmful.html)