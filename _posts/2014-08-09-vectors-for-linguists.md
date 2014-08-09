---

title: "Linear Algrebra for Linguists"
layout: default
tags:
- physics
- intro
- units
- vectors
- math
excerpt: People often thing that math is just about numbers.  I intend to disabuse this notion by discussing linear algebra from a linguistic perspective.

---


A common complaint about mathematics is that it just doesn't seem
useful.  After all, early math courses are often dedicated to simply
pushing numbers around. There are very few people whose lives involve
pushing numbers around, so it seems like a big waste of time. Word
problems are often given as ways to make the math seem practical, but
those word problems are often window dressing around the same number
pushing.

This is unfortunate, because math is about numbers in the same way
that ovens are about reheating frozen pizzas.  It's about the easiest
thing that you can do, but, if that's all that you're doing, you've
missed out on most of the good bits.

Inspired by a recent
[post](http://nclatin.blogspot.co.uk/2014/08/of-math-and-latin.html)
by Indiana's Teacher of the Year[^1], I'm going to try to explain
linear algebra through the idea of translating foreign texts.

We'll start by taking a word which you wish to translate.

~~~
|animus>
~~~

Notice the | and > around the word?  I'm using Dirac's bra-ket[^2]
notation.  Anything with a | at the front and a > at the back is a
word that we want to translate.  This is a *ket*.

Now, what about possible translations?

~~~
<mind|
~~~

If something with a | at the start and a > at the end is a *ket*, then
something with a < at the front and a | at the end you might guess to
be a *bra*.  Your guess would be right.  A person snickering at the
word *bra* you might guess to be twelve years old.

Now, what if we combine the two together?

~~~
<mind|animus>
~~~

When you combine a *bra* and a *ket*, you get what we call an
*inner-product*.  You can think of an *inner-product* as a measure of
how well two things match up.  So <mind|animus> is probably pretty
big, since they match up well, while <cerebellum|animus> is pretty
small.  The biggest possible value that you can get is
<animus|animus>, since everything means the same things as itself.

While there's nothing bigger than <animus|animus>, there's nothing
smaller that <pogo stick|animus>.  That's not to say that there aren't
any other translations that are just as bad.

~~~
<pogo stick|animus> = <Cleveland|animus> = <lepidiota bettle|animus>
~~~

When two words have absolutely nothing in common, we say that they are
*orthogonal*.  This won't come up again in this post, but I may need
the idea again in a later one.

Enter the Matrix
===

Somewhere, there's a smart-alec reader who will pretend that, back
when I said that we were going to combine the bra and ket, that she
thought that I was going to write

~~~
|animus><mind|
~~~

First, you didn't think that I was going to combine them that way.
Besides the fact that it's *bra-ket* notation, so the *bra* obviously
goes first, there's also the fact that <mind|animus> looks like a UFO,
which makes it more awesome than |animus><mind|, which just looks like
a twisted ribbon.

Still, because I'm a bigger smart-alec than she is, I'm going to point
out that |animus><mind| is an actual thing, called an *outer-product*.
These are often represented by *matrices*, which are just big tables of
numbers.  But we're not doing numbers in this articles.  I wish that
we were - there are a couple of things that's be easier if I could put
in a number.  But I said that I was going to do this without numbers,
so we'll just move on.

*Outer-products* are also known as operators, as they can be used to
 change what we're looking at.  We'll start with the easiest
 operator - the identity operator.

~~~
ID = ∑ |word><word|
~~~

The big sigma[^3] is just an easy way of writing "add up all the
things".  I could have just as easily written

~~~
ID = |mind><mind| + |carrot><carrot| + |cotinga><cotinga| + |ladle><ladle| + ⋯
~~~

The idea is that *ID* has the outer product of every word with
itself. So, if you use the operator on any word, you get the same
thing back again.  for instance

~~~
ID|cat> = |cat>
~~~

To give a more interesting example, we'll make the Elmer Fudd[^4] operator.

~~~
Fudd = ID - |rabbit><rabbit| + |wabbit><rabbit|
~~~

We can then use the operator Fudd operator on some words.

~~~
Fudd(|I'll> + |get> + |that> + |rabbit>)
= |I'll> + |get> + |that> + |wabbit>
~~~

You can think of this as a kind of translation, from English into
Fudd.  We can then extend this idea into a more useful kind of
translation.  We're going to make a matrix called *E* which is similar
to identity, except that it only has words in English.

~~~
E = ∑ |English word><English word|
~~~

This simple little operator takes a phrase in any language and returns
every possible translation into English, weighted by the quality of
the translation.  For instance, imagine that our word is *animus*
again. Using the operator on the |animus> *ket* gives us:

~~~
E |animus> = ∑ |English word><English word|animus>
~~~

From what we know about inner products, we know that the <English
word|animus> part tells us how well each word translates |animus>.
That part is then multiplied by the actual word vector, to give us the
weighted vector.

We'll stop here for right now. Translating every language that exists
or ever will exist with a single line of algebra is probably enough
for one blog post.  My next post will continue with this to explain
some more advanced concepts, like eigenvectors, and how they relate to
goofy toys like [translationparty.com](http://translationparty.com).

Footnotes
===

[^1]: Incidentally, Magister Perkins is also my old high school Latin teacher and scholar of the highest order.

[^2]: This is what happens when you let physicists name things.

[^3]: Don't complain about my using the greek alphabet.  I said that this was going to be for linguists. If the physicist is comfortable with it, you should be, too.

[^4]: I spent much of my childhood with a speech impediment that hampered my ability to pronounce the letter R.  Some individuals likened it to sounding like Elmer Fudd.
