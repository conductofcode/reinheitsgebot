# Getters and Setters lead to non-OO code

Writing getter and setter method breaks data encapsulation. It allows to leak implementation details of an object and violates the "Tell, don't ask" principle. When one object collaborates with another one, it shouldn't ask for it's things, but rather tell it to do something, and passing any required data when needed.

## Further reading

 * http://typicalprogrammer.com/doing-it-wrong-getters-and-setters/
 * http://www.javaworld.com/article/2073723/core-java/why-getter-and-setter-methods-are-evil.html
