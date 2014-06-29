---

title: Unsubstantiated Rumors about Archimedes
layout: default
tags:
- physics
- nudity
- Archimedes
- buoyancy
excerpt: You've probably heard the story of Archimedes and the golden
crown, but have you heard the full story?

---

If you made it through elementary school without hearing the story
Archimedes and the king's crown, pull up a chair (if you have heard
this story, just skip to the next section).

A long time ago, in the city of Syracuse, the king had commissioned
a crown of pure gold. However, once the crown had been made, the king
became suspicious. Was the crown truly pure gold? He'd paid for pure
gold, but the smith could have mixed in some cheaper metals and
pocketed the difference. Kind of like when you're not sure if the
mechanic actually replaced a head gasket or if they just charged you
$500 to replace a $7 spark plug.

Now, there was no Internet back then, so the king didn't have a blog
where he could complain about unscrupulous artisans.  However, he did
have the extraordinary advantage of having access to Archimedes, the
smartest man in antiquity. The king asked Archimedes to tell him
whether or not the crown was pure gold.

Of course, the answer to that problem was a no brainer. Break of part
of the crown, melt it down, and see if it's gold. You don't need the
smartest man in the world to tell you that.  However, the king had
spent a lot of, well, gold on this crown and wasn't particularly keen
to see it broken. Especially since there was a chance that the crown
was made entirely from gold and this would only ruin a perfectly good
crown.

It's at this point that most of us would have just given up. Just tell
the king that the crown looks like gold and he should stop worrying
about it. Archimedes, however, decided to figure it out.

As the story is told, he finds the solution during his evening
bath. As he lowers himself into the tub, he watches the water level
rise around him.  He bobs in and out of the tub a few times, watching
the water level go up and down.  Everything clicks together inside his
head in that way that normally only happens in poorly made detective
films. He then runs stark naked through the streets of Syracuse,
shouting to anyone who could hear that he'd solved the problem.
(I'd like to take a moment to thank Archimedes for giving me an excuse
to tag one of my posts with the keyword "nudity".  I'm sure this will
wind up being my most popular and most disappointing post).

Later, and presumable clothed, Archimedes fills a large container to
the brim with water. He then places the crown into the container,
causing some of the water to spill out. He takes the crown back out.

He then asks the king for a lump of pure gold that weighs just as much
as that super expensive crown that he's been so worried about. The
king pulls said lump out of his back pocket, for that's walking money
when you're a king. Archimedes places the lump into the water and the
crowd gasps as the water level doesn't reach the top of the
container. Archimedes says "The goldsmith's story *doesn't hold water*"
and puts on his sunglasses.

Reality Time
----

Alright, so I started sliding into artistic license near the end of
the story.  I'll defend myself in the classic seven-year-old fashion:
everyone else was doing it. Parts of this story never made any sense.

First, the king has to have a large enough gold reserve to have
essentially a spare crown's worth of gold sitting around.  Of course,
it's good to be the king, so that's a possibility. However, the next
question is how well does this actually work. After all, the first
thing that the goldsmith would do is point at the water level and say,
"Yeah, that's totally at the brim".  He'd then argue that the crown
was left when they took it out, so the water level wouldn't go all the
way back up to begin with. He'd then hire a lawyer who'd do a far
better job of arguing all the points I'm missing.

The point is, this isn't really a good way of measuring how much gold
is in a crown. Furthermore, if I'm smart enough to see this,
Archimedes certainly would have seen it.  His toenail clippings were
smarter than me. So he probably had a much better idea than just
dropping the crown in a bucket.

We also know that he loved levers. When the man saw a battle ship, his
first thought was "Hey, I could totally lift that with a lever".  Then
he did, because that's the sort of thing you do when you're the
smartest man in the world. The reason I mention this is because it
seems out of character to Archimedes to not throw in a lever here.
Well, a lever or a spiral, but I couldn't find a good way to work a
spiral into the solution here, so we'll just ignore it.

Alternate Solution
----

Here's an alternate solution to Archimedes problem that's more in
character with what we know of him as a scientist.  When I first
started writing this blog post, I was quite proud of myself for
figuring all of this out.  Over the course of my research, I found
that Galileo proposed this same adjustment to the story, so it's not
exactly a novel idea.  On the other hand, it's still not included in
the elementary school version of the tale, so it's still worth
spreading - I just won't get any credit.  Darn.

Moving back to the physics, let's say that crown had a weight
$$W_{crown}$$ and a volume $$V_{crown}$$.  Let's also say that the
king donates a tiny piece of gold with weight $$W_{gold}$$ and volume
$$V_{gold}$$. Archimedes can then hang both pieces from opposite ends
of a long straight rod.

This is a place holder until I can actually make a drawing.

~~~~~~~
       |
       |                              
    ___|____________________________  
    | d              D             |  
    |                              |  
    |                              |  
    |                              |  
    |                              |  
    |                              |  
    |                              |  
  crown                           gold

~~~~~~~

As I've marked above, $$d$$ is the distance from the crown to the
hanging point of the balance.  Similarly, $$D$$ is the distance to the
sample of pure gold.

Now, as Archimedes knew about levers, for a balanced lever, the
distance times the weight has to be the same on both sides.
Therefore, $$d W_{crown} = D W_{gold}$$.

So far, all we've done is hang a crown and piece of bold off of a
stick. The beauty comes when we submerge this the whole thing in
water.

~~~~~~~
       |
       |                              
    ___|____________________________  
    | d              D             |  
    |                              |  
I   |                              |     I  
I~~~|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|~~~~~I
I   |                              |     I
I   |                              |     I
I   |                              |     I
I crown                           gold   I
I                                        I
I========================================I
~~~~~~~

Here were going to take advantage of a scientific law known as
**Archimedes Principle** (see how that might be relevant?).  The
principle states that, when something is submerged in water, its
weight is decreased by the weight of the water that would have been in
the space that it's taking up.  This is why boats float - they take up
so much space that they don't weigh enough to push all of that water
out of the way.

So our equation from before changes. For the scale to remain in
balance, we now need $$d (W_{crown}-\sigma_{water} V_{crown}) = D
(W_{gold} - \sigma_{water} V_{gold})$$, where $$\sigma_{water}$$ is
the density of water.  I'm mostly going to try and avoid putting too
many Greek letters into the math in this blog, but I felt I should
include one here, in honor of Archimedes.

Now, I haven't talked much about density up till now.  Density is the
relationship between mass and volume.  We're going to be a bit sloppy
here and say it's the relationship between weight and volume, because
Archimedes wasn't really in a situation to care about the difference
between mass and weight.  I'm pretty sure that he did all of his
measurements on Earth.  Pretty sure.

So the value $$\sigma_{water} V_{crown}$$ is just the weight of an
amount of water that takes up the same space as the crown.  Similarly,
$$\sigma_{gold} V_{gold}$$ is the weight of water that takes up the
same space as our test piece of pure gold.

If we play with the algebra for a bit, we can find that $$
\frac{W_{crown}}{V_{crown}} = \frac{W_{gold}}{V_{gold}} $$.  Since the
density is the relationship between the weight and the volume, that
just becomes $$\sigma_{crown}=\sigma{gold}$$. In other words, if the
two sides of the balance remain even after everything has been lowered
into the water, then the density of the crown and the gold must be the
same.  We can then go a step further: if the goldsmith added in less
valuable metals during the making of the crown, the two sides will
lose balance when everything has been submerged.

This makes for a far more compelling courtroom drama.  Archimedes
carefully balances the crown and the gold.  He then makes a little
mark where he balanced the gold.  The crowd holds their breath as the
scares are submerged in the water, only to gasp as the weight of the
tiny piece of gold raises the debased crown.

"And that's why Justice *carries scales*." say Archimedes, while
putting on his sunglasses.
