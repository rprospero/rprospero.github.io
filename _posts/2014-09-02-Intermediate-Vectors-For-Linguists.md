---

title: "Intermediate Vectors for Linguists"
layout: default
tags:
- physics
- intro
- units
- math

---

In my
[previous article](http://rprospero.github.io/2014/08/09/vectors-for-linguists.html),
I start introducing the idea of a vector from the perspective of
translating words between two languages.  Now that we have a way of
representing a translation, let's see what we can do with it.

Since I've declared that this is intermediate vectors, I am going to
allow myself the indulgence of using a couple of numbers.
Specifically, I'm going to use *0* and *1*, since they're quite useful
and come up a lot.

Since I have there numbers, I have a nice chance to expand a bit on a
the inner product that I discussed in my last post.  I had mentioned
that the inner product of two vectors represented how well they
matched up.  <animus|mind> was really big and <animus|pogo stick> was
really small.  As you might guess from the words "big" and "small",
we're going to use a number to represent this inner product.  This
isn't strictly necessary - you could use anything that has a big and
small.  You could use loaves of bread, with <animus|mind> being a
giant baguette and <animus|pogo stick> being a tiny little crumb.
Unfortunately, I don't have any bread, so we'll have to use numbers.
I say unfortunately mostly because I haven't had lunch yet and could
go for a sandwich right about now.

Out of the pair of numbers that we're using, lets go ahead and start
with zero.  In my last post, I said that two vectors were *orthogonal*
if their inner product was the smallest possible value.  Well, zero is
the smallest number we have, so we'll go with it.  If two vectors are
orthogonal, then they have an inner product of zero.

~~~
<pogo stick|animus> = 0
~~~

In the above line, I've made a fairly bold declaration for someone who
isn't a linguist.  That line says that there will never, ever be a
Latin text where, when translated into English, the correct way of
representing what the original author meant when she wrote "animus" is
to use the English phrase "pogo stick".  I've known enough linguists
to know that one will now construct such a sentence, but I hope that
you'll accept it as a general truth that no Roman author ever meant
"pogo stick" when writing "animus".

We've used one number, so it's time to use the other number.  I'm
going to declare a convention here that will make our lives easier.

~~~
<animus|animus> = 1
~~~

The above line says that, if the original Latin text had the word
"animus" and you're translating the text into Latin, it's always
appropriate to translate the word as "animus".

Or, to put it more succinctly, that it's always appropriate to
translate a word as itself.

If the inner product of a vector with itself is equal to 1, we say
that the vector is *normal*.  Now, it might seem that every vector
should be normal, but remember that we can add vectors together to
make new vectors.  The vectors may not be normal.  For example, we
will look at the vector (|animus> + |pogo stick>):

~~~
(<animus|+<pogo stick|)(|animius>+|pogo stick>)
= <animus|animius>+<animus|pogo stick>+<pogo stick|animius>+<pogo stick|pogo stick>
= 1 + 0 + 0 + 1
= 1+1
~~~

So the vector (|animus>+|pogo stick>) is NOT normal, since it has an
inner of 1+1, instead of one[^1].

Orthonormal Basis
====

In the previous post, I introduced an identity matrix that turns any
word back into itself.

~~~
ID = ∑ |word><word|
~~~

However, I'm afraid to say that I cheated slightly.  If we take the whole of the English language and use that to make the matrix, we won't get something that turns every word back into itself.  To take an example, let's take a subset of the English language that just contains the words "green" and "verdant".

~~~
ID = |green><green| + |verdant><verdant|
~~~

If we use this matrix on the |green> vector,
we get the following

~~~
ID|green> = (|green><green| + |verdant><verdant|)
= |green><green|green> + |verdant><verdant|green>
= |green>*1 + |verdant>*<verdant|green>
= 1*|green> + <verdant|green>*|verdant>
= |green> + <verdant|green>|verdant>
~~~

Now, we wanted to get back the vector |green>, but we got that plus
the extra <verdant|green>|verdant> term that we don't want.  We could
get rid of this term by saying that <verdant|green> = 0.  Except,
we've already declared that the inner product is zero when the two
words have nothing in common, so we know that the result is *not*
zero.  This *ID* vector is a total fraud!

Now, there is a way of fixing the identity matrix.  We look at a
subset of English again, but we insist that all of the words we look
at are orthogonal.  When you have a collection of vectors which are
each individually normal and are all orthogonal to each other, the
group is said to be *orthonormal*.  If we restrict our identity matrix
to only working over orthonormal words, then it will work again.

You might be disappointed that we had to drop the word |verdant> from
our vocabulary in order to keep this matrix representation.  However,
there's a trick that allows us to keep it.  This trick comes from the
fact that, while |green> and |verdant> are similar, they aren't
exactly the same.  We said that <verdant|green> wasn't zero, but it
isn't one, either.

We're going to make up a new word, *verdont*, which means something
that's verdant, without all of the bits of verdant that are green.

~~~
|verdont> = |verdant> - <verdant|green>|green>
~~~

This new word is orthogonal with green:

~~~
<green|verdont> = <green|verdant> - <green|<verdant|green>|green>
= <green|verdant> - <green|green><verdant|green>
= <green|verdant> - 1*<verdant|green>
= <green|verdant> - <verdant|green>
= <verdant|green> - <verdant|green>
= 0
~~~

However, this new word also let's us keep the concept of verdant
separate from the word green.

~~~
|verdant> = |verdont> + <verdant|green>|green>
~~~

So, our *ID* vector can work, as long as we have a subset of our
dictionary where a) all the words in the dictionary are orthonormal
and b) every word in our language can be formed from a combination of
words in our dictionary.  This special dictionary is called an
orthonormal basis.

Eigenvectors
=========

Now that we know how to make that *ID* matrix, we'll go head and make
two different vectors:

- *ID_e* :: The *ID* matrix for the English language
- *ID_l* :: The *ID* matrix for Latin.

~~~
ID_e = ∑ |English word><English word|
ID_l = ∑ |Latin word><Latin word|
~~~

We can then use these matrices to translate between the two languages.

~~~
ID_l |English word> = |Latin Translation>
ID_e |Latin word> = |English Translation>
~~~

We can extend this idea to translate back and forth.

~~~
ID_e ID_l |English word> = ID_e |Latin Translation> = |English Translation of Translation>
~~~

This bring me to the fun little site
[translationparty.com](http://www.translationparty.com).  The site
uses a little script to translate a phrase back and forth between two
languages until it gets the same result back.

Can we find something similar with our vectors?  What we want to do is
find some vector |x> and scaling factor *a* such that

~~~
ID_e ID_l |x> = a |x>
~~~

In other words, given the matrix (ID_e ID_l), we want to find a vector
that is merely scaled up or down after being multiplied by this
matrix. We perform the translations and get the same value back.

This vector is called an *eigenvector* for the matrix and *a* is it's
corresponding eigenvalue.  Eigenvalues and eigenvectors are quite
important in quantum mechanics, but that will probably need to wait
for a later post.

footnotes =========

[^1]: I said that I was only going to use 0 and 1 and, by golly, I'm going to stick with that.  If you want to start talking about this value of 1+1, you'll have to wait until Advanced Vectors for Linguists.
