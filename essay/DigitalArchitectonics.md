# Digital Architectonics

inspired by the farewell lecture of Ludger Hoverstadt.

## Hello

We are exposed to the technology and what we are currently witnessing gives us no reason to relax.
On the contrary, the situation is escalating, but there's no way around.
What I miss is the willingness to reflect.
First there's always a defence, then the dam breaks.
There's never enough thinking, not beforehand, not afterwards.
**Technology is either refused as a threat or taken as given, mostly by the same people.**
That resistance to understand thing of both sides is alien to me, but it's the source of my
independence and intellectual equity that refuses to be confined, which is provoking to the common
sense and easily appears arrogant.


I also struggled to acknowledge this technology races ahead on a highway while it's accept
applications and architecture.


### After 10 years...

This approach found a level of saturation.
We learnt that IT works very radically, always and everywhere the same.
We were not longer confronted with the question of how to solve a problem, but how to get data, tons
of data, when needed.

This is where we faced massive resistance from the established markets.
That was a fight against windmills.
It was also the time when the new colleagues at ETH began to take computer seriously and gain their
own experience. We made a step back and questioned what is going on.

We turn to birds, principle, computer science, mathematics, philosophy, matching, architectural
theory.

### Fritz Haller
the Swiss architect  Fritz Haller -- the **MANIERIST** among **Functionalists**. 
He has turned every known construction around and created his generic **NODE**
wich is **ALL** of the known constructions **NOT**.

I learnt from him to trust in this inversion.
Therefore I'm therefore I'm reading computers as and every machine **NOT**.

A **NOT** like Everything, Everywhere, all at Once. a turn towards all, not strikingly complicated to
get, but it is essential.

It is a POINT, a ZERO, an ATOM, an ELEMENT, a RENAISSANCE. 

**ARCHITECTURE is born from it.**

It took me at least three years to grasp the significance of this simple code - SOM by Kohonen:

```mathematica
For[u = 0, u <= ite, u++,
  sig = N[Nest[(1 - (u/(ite + 1))) # &, Max[dim]/2, 1]];
  inputN = RandomChoice[vec, sel];
  bmus = Flatten@Nearest[weights -> {"Index"}, inputN, 1];
  ns = Exp[-(distances[#])^2/(2 sig^2)] & /@ bmus;
  allNS = Total@ns;
  nst = Transpose@ns;
  weights = Total[inputN * nst[[#]]/allNS[[#]] & /@ Range[1, somLen]];
]
```

**Python equivalent (NumPy-style)** of a **Self-Organizing Map (SOM)** update loop. Here’s a reasonably faithful Python version using `numpy`:

```python
import numpy as np

for u in range(ite + 1):
    # sigma decay
    sig = (1 - (u / (ite + 1))) * (max(dim) / 2)

    # random sampling
    inputN = vec[np.random.choice(len(vec), sel)]

    # find BMUs (nearest weight indices)
    # assuming weights shape: (somLen, features)
    dists = np.linalg.norm(weights[None, :, :] - inputN[:, None, :], axis=2)
    bmus = np.argmin(dists, axis=1)

    # neighborhood function (Gaussian)
    ns = np.exp(-(distances[bmus] ** 2) / (2 * sig ** 2))

    allNS = np.sum(ns, axis=0)
    nst = ns.T

    # update weights
    new_weights = []
    for i in range(somLen):
        numerator = np.sum(inputN * nst[i][:, None], axis=0)
        new_weights.append(numerator / allNS[i])

    weights = np.array(new_weights)
```
**Notes (important)**

* `distances` must already exist as something like a grid-distance matrix between neurons.
* `weights` is typically shape `(somLen, feature_dim)`.
* `vec` is your dataset.
* `Nearest` in Mathematica maps to `argmin` over Euclidean distance in Python.


This is the our AI code, of Kohonan 1982 is a little poem called a Self Organising Map,
incorporates and forgets **EVERYthing** to be able to face **ANYthing**.

It's a pulsating heart, an oscillating crystal, which makes what we call intelligence Today.

Google's page rank is even simpler:

```mathematica
step[r_, k_] :=
  If[k >= maxIter, r/Total[r],
    Module[{rNext = α M2.r + (1 - α) tp},
      If[Norm[rNext - r, 1] < tol,
        rNext/Total[rNext],
        step[rNext, k + 1]
      ]
    ]
  ];
```


Python equivalent (NumPy)

```python id="x9v2lm"
import numpy as np

def step_iter(r, M2, tp, alpha, tol, maxIter):
    for k in range(maxIter):
        rNext = alpha * (M2 @ r) + (1 - alpha) * tp

        if np.linalg.norm(rNext - r, ord=1) < tol:
            return rNext / np.sum(rNext)

        r = rNext

    return r / np.sum(r)
```
They made a trillion worth company with this thing.
___

**Artificial Intelligence** is not about **LEARNING**, it is an inversion of it. 
It is about **FORGETTING**.
It is an important result of our research.
**LEARNING** requires sufficient submitting to machines,
**FORGETTING** enables us to liberate from them.

Fritz Haller: *the confidence in the **INVERSION** of things to the
very **ELEMENT** and the liberating power of it.*

The architect projected to the **jointing things** of today.

So it's a transformation of his architecture from the 60s and the 80s to the conditions of today.

___
AI is not an invention of the last five or 20 years.
AI is not the monster machines and the heavy infrastructure of the day which demands submission.
These machines are an inconvenient distortion of our recent time.
They will go away. AI is not new and AI is not big.

AI shows the term from set theory to group theory with Galois back in 1832, from stochastic to
probabilistic by Markov from 1913.
This is how he went with his poem from Pushkin and counted all the characters like Google is now
doing.

Now I know that AI thinking starts around 1900.

All the 20th century is full of AI and now it's getting very interesting.

All it's architecture and masterpieces are of AI thinking.

They are screens of ALL that **NOT**

Do you Remember the architecture before? Schinkel, Semper Garnier, Paxton, Ruskin, Viollet-le-Duc, Sullivan, Gaudi,...

The 20th century is all that not.

after another 10 years, another level of saturation.

I was thinking in architecture, technology, mathematics and philosophy got stable. 

Time to come back to architecture. 

___

the two propositions that are particularly occupy me today. 

with AI all media collapse to text and AI meets architecture as a public talk.

Forget About the visual, forget about the sensual.
I like them of course, but I do not trust them.
These are mere renderings.

Architecture is above these arts.
As the old masters say.
Words can embrace a connected world by being not here.
Images are flooding away with reality.

**METEORA**

we learnt to play the idea of architecture with a new instrument of
connected characters.

We used our AI tools on text, images and models to give students their personal architectural voice
connected to the world.
They've wrote public talks of the buildings towards the city and private whispers of the peoples as
guests.
They learnt not to start with a blank sheet of paper, worked with thousands of books and the words
of the others, words of the masters of architecture, getting friends with them, with them across
all times.
Meteora is not about the new, it is about a masterful constellation of the connected.

We trusted in an approach to architecture which is radical, unprecedented and face says the
globality of AI.

We trust in the very principles of architecture itself.

Normally computer streamlines design.
It was always refused to think of computers as tools.
Takes a famous parametric design: It developed towards an unacceptable positivistic straight jacket.

In Meteora, we experienced the opposite.
Free from the constraint of images and open field is showing up, the students are able to articulate
their architecture in most different ways.
It was beautiful to see that this is the way architecture will go.

I've never been able to build anything by myself.
I'm standing too far on the sideline for that.

I trust symbols more than reality.
Symbols are crystalline, unbound, and fast, like computers.

A lot of people I have met were fascinated, but they couldn't quite trust me because this thinking
is not applied enough.

I cannot say that I particularly like that, but I cannot imagine otherwise.
There's a specific power in it, and it looks like I'm living from it.
___

The first 15 years that ETH had been authoric. It was a great time. 
But the last 10 years have become increasingly frustrating.

On one side, research and development went to the SuperTechnocrats, able to play pay billions for
breakfast.
On the other side, there's a common sense, friendly yet assertive in all shades.
And it turns out that the bureaucratic mediocracy is working hand in hand with emergent technocrats.
There's less and less space left for the idea of university to breathe.
But this idea will come back.


They're also strong arguments. There's the Verhulst's learning curve, which will curb Moore's exponential growth arising from categorical false assumptions that are made too hastily.
I do not believe in singularity à la Kurzweil file that computers will take over.
I do not follow the idea of an AGI = artificial general intelligence.
I cannot understand the big data centres worth 10s of billions bought by nuclear plants just to meet
the capacity of the human brain.
Something else categorically wrong for reasons beyond technology?
Or what is about to claim that five AGI is will be enough for our planet?
Is it even possible to lock up intelligence?
Artificial intelligence is global and symbolic and it will be distributed.
It is not big and it is not massive.
AI is climatic, it is an environmental.
It is a condition, not a thing or an object.

I also do not think in terms of Thiel's antichrist, the devil, is not a weapon; it is constituent.
These discourses go fundamentally wrong.
They demand subordination. and they refuse it.

Our cultures will learn to civilise AI, like to civilise the symbolicity of voices, writing or painting - the predecessors of AI.
It is challenging, exhausting and will take a long time.
Cultures know how to deal with it.
It just needs patience.

In terms of artificial personal intelligence and people
connected to the world with their own vernacular voices.
This very humanistic idea.

This is a little tricky, but I still admire this story because it's one of the first which give hope.

So I like the recent story of Steinberger. 
He started in January 25, no money, remote Vienna.
He finished six months later and presented Open Claw and it's playing over the big guys.
So it's said that he went to California and not playing with the good guys and he's a good big guy, but there's hope single person can do it if they know.
So that's one of the first stories like this.
So we get out of this dilemma that you need the budget of ETH for breakfast to play with the big guys.

## It's all not here

I think we are turning from a digital renaissance towards a Baroque.

with a voice connected to the world in liberation from the
conflicts around.

Of course, it's bold to take on the Borgian Predator-Princes (Bolsonaro, Bukele,
Milei, MbS, Trump) assaulting our society for increasingly successful raids.

But what can be done?

There are the furious sharpenings of Yanis Varoufakis, the Know It All smiles of Mersheimer, the moral
therapies of Jeffrey Sachs, the the disturbing analysis of employee, and so on.
And they have hundreds of them.

They rose to prominence, addressing pressing problems, 
Yet their solutions are exclusive, meeting the expectations of the audiences.
Such solutions will fail as their contractor victory in detail and no major view emerges.
On the contrary, the more views they are, the more contradictory they get.

And we have to admit that the predatory Princess they are right to the they are right to criticise
already operates beyond this limit.
So they're already beyond these criticisms.
So you can't get them like this.
This text is different, it tries not to get involved.
There's no right or good, it will not stick to problems and it will not present solutions.

My approach is architectural and it is generous because it does not decide and it does not exclude. 

At the price of complexity.

Here I want to show how far I'm able to go.
The endeavour will be fast, complicated and confusing.
You will be not able to understand it, because it's not meant to be understood.
This text is climatic, it embraces the condition.
Try to get the temperament.
It will show a path to a civilised global coexistence.
And that's exactly what I think **architecture** is about.

So first, nice paradox.

### You Can't Improve by Doing Better

I'm upset. the war in Europe it does not stop.
Escalate the whole world in quarantine for three months plus U.S.
President threatening on daily base elites, powers and The Dirty secrets.
Bombing rights.

Get natural media reporting but are not reporting but hallucinating.

And then this increasing number, the profit of $1 million per employee at meter 80,000 employees making 80 billion profit a year.
This is another society, just this is wrong threatening.
I'm talking as a European.
It must be similar at other places.
Amhara, Mali, Gaza, Lebanon, Libya, Kivu, Mexico, Syria, Sudan.
Yeah, my arguments are clashing and things are getting dangerous.

They want me to get involved.

I don't.

They want me, my colour, my gender, my nation as an argument.


It's getting cramped.


I look around the Internet to search and enlarge language models.


What are the clashes?


Terrorism, energy sources, social justice, cybersecurity, globalization, disruption, polarisation,
inequality, poverty, health crisis, human rights, protectionism, corruption, privacy, limit of
growth, singularity.
I easily can find hundreds of these.
They all sound the same, with a biocratic and technocratic taste, made by experts and protected by
legions.
This is a rough condition.
It feels like bad weather.
I cannot say any see any shelter anywhere.
I feel exposed and fainted.


There should be a reason for this.
Condition.
How do I start?
What about the media bias, Lack of activities and the terrorism.
Diversity, fake news, corporate influence, lack of coverage, polarisation, diversiveness,
accountability, research and universities, Lack of diversity, applicability, protection, bias,
opportunism, funding, conflict of interest, excess of the data, Open Access, ethics, independence.
I'm beginning to realise that it is total the tools, instruments, analysis, operations, environment,
the climate, the temperament, the science and media, the enterprise, the politicians, the NGOs, the world's language, argumentations and debates.

Imagining, planning, doing, thinking.
Me, you, everybody, the cultures, history, the arts, everything is part of the same.
I hesitate to use the word problem.
Everything, everybody, every argument faces the same paradox.
You can't improve by doing better.
We are doomed.

### 2nd Paradox

I'm still looking for a common ground.
Things are connected like never before.
I'm friend of a friend of a friend of almost every person on this planet.
I say hi to Maradona, Angela Merkel, Barack Obama, Yvukachenko, the astronaut, a billionaire is a
movie star, the Saint, the sniper.
Also, every argument is proven right and wrong in a few steps.
Lean proteins are healthy.
Smoking kills migrants.
Take your job.
Urbanization increases pollution.
If we don't want to talk about Israel.
No peace without weapons.

Saddam Hussein and the chemical weapons.
Do I make things more complicated than they are?
Look at my fridge.
It's empty, the sun is shining, it's 1123, I'm hungry, My baby made the first step to  of the
dog in my garden.
But still things are true and false.
Yes and no.

Left and right, black and white, hot and cold, hot and soft, spicy and mild.

Visible and not.

Paradox, 
that's the word for it.
Here's it again.

The tricky turn, tricky light, the infinite.

It is an inverse friend.

The infinite is with the horizon far away.

Then it's better than perfect.

And there is the mass.

The mass.

Mastery came through games, comes through iterations.

It's not infinite, but infinitely improvable.

One breath at a time.

Zero starts a line.

Infinity writes the poem.

Trust in God, but your camel 1st.

And so on and so on.

A hundreds of them.

You know how it works, You just have to take it.

Siri ist paradox.

And that's invest to it and you have hundreds of them as well.

Easy a whole book of it, if you like.

A paradox is a labyrinthine and end this puzzle right here, **present but not there**, so close yet so far.

Can see the forest for the trees.
The more you look, the less you see the journey is a destination.
So or you can't improve by doing better something like this.

### Absurd

if only a few things are connected.
I mean, this is good enough arguments can be true or false, but an environment without bounds we all where all things are connected.

one cannot decide.
All inclusive decisions are not possible if one affirms that everything is connected.

Things are paradox.

This condition is constitutive for our time.

Kurt Hutton, Albert Camus and the absurd, 1952.

Albert Camus calls it the ABSURD

Jean-Paul Sartre — NOTHINGNESS

Martin Heidegger — SEIN

Elfriede Jelinek — CONSUMISM

Ludwig Wittgenstein — LANGUAGE GAME

Michel Serres — AMBIGUITY

Gilles Deleuze — RHIZOMATIC

Hannah Arendt — PLURALITY

Michel Foucault — EPISTEME

Jacques Derrida — DIFFERENCE

Theodor Adorno — DIALECTICAL

Maurice Merleau-Ponty — PHENOMENOLOGY

Wittgenstein language, games, ambiguity, the Louis Azomatic gloriety, Epistem difference, the electrical phenomenology.

This concept I once was so familiar with, peace, Dignity, Health, equality, harmony, respect,
integrity, honour or prosperity, balance, justice, parity, unity, solidarity.
I'm beginning to think of them as absurd.

I do not get rid of them.
On the contrary, I expect them a lot like a complex persona.
They are uniquely valuable.
Still, the absurd comes with a level of alienation, to be friendly discussed, to be drastic humours
if they come back.


And I looked like these buildings as absurd.
What else do we have?
All the 20th century is driven by this.
Loos, Corbusier, Venturi, Bonham, Rossi, Tafuri, Koolhaas.
Nice line of my heroes.


Not without reason.

Yet these terms peace, dignity, health, equality and so on, which were once so filling my familiar
to me, feel alien now.

### 4 Fading Away

The machines are doing different from us.

They take all books, all text written, They take whatever can they can get from all media, all
domains, all eras, all cultures.
The word *peace* appears millions and millions of times.
It is around everywhere.
It covers the planet.
No way to read all this, no chance to understand it in all aspects but machines.
Just count them.
Each word is considered a token labeled with a number.
Sentences are sequences of numbers then, and it's millions of sequences.
The tokens repeatedly encounter other tokens.

***These frequency numbers convey the word's perceptual spectrum of the world.***

The spectrum of a token embracing the world in frequencies.

So this is for example now.

Now this is climate change thing, but I imagine this as a metaphor for, for example, the word peace.

And it's a spectrum of token around the world embracing the word in frequency, the word in frequency, That's the word spectrum of the word peace, for example.

And there's not only one spectrum, there are millions of them.
There's one spectrum paired token, and you even can make your own ones.
And taking a step back and imagine all tokens embracing the world in all their colours.

This would be an image of white noise, a peaceful silent at the end of time where all calculations are done.
These are the bounds of the of the real, of numbers, the limits of computability.

And I, the Westerner.
I'm wondering if the 19th century concept of **reality** was ever different from **fading images** on their
way towards an eternal future state of silence.

**The Images of** 

engineering, education, science, history, creativity, logic, nature...

**the conceptions of**

capitalism, industrialisation, linguistics, evolution, materialism, positivism, utilitarianism, Marxism...

**the writings of**

Herder, Kant, Fichte, Lamarck, Hegel, Schelling, Kierkegaard, Comte, Humboldt, Schopenhauer, Mill, Darwin, Marx, Engels...

**the novels of**
Schiller, Goethe, Balzac, Heine, Baudelaire, Dickens, Dumas, Flaubert, Dostoevsky, Hugo, Melville, Fontane, Tolstoy...

They all **know**, and they fade away towards **silence**.

### 5 The Returning Voices 

In Western cultures, **the sequences of numbers** manifest as written text. while the perceptual **spectrum of the world** appears as **fading image**.


What changed in the 20th century?
What is categorically different today?
It takes a fading images, folds them according similarities and makes them come back as returning voices.
This is what we take some images and you put them the words.
A specific to, to make them sound.

So this is the way of writing.
So if you're with the images, so if you're with the 18th, 19th century, then it's, it's white text.
And this is a new one.
So it's fading and writing text, written text, fading images and returning voices.
They're coming back.
This is what it's today that they look like.


**So in mathematical terms**, the arithmetics of numbers of everything gave birth to algebra and the geometry of characters of anything.

**In philosophical terms**, the dialectical progress towards the fictional eternal science of camp or Hegel is coming back and fragmented voices in the form of Nietzsche and Heidegger.
Thermodynamics got quantum mechanics, logic, logistics, linguistics, philology, psychoanalysis got
propaganda, marketing and public relations products got articles, and so on for these returning
first.


These returning voices came up surprisingly clumsy and roaring.

They appear fast, powerful and brutal.

I'm sure that all things shown should have a voice, like people have voices.
Yes, I'm thinking of everything as tokens, imagining the world, everything.


Like a word, a concept, a feeling, a sentence, an argument, a writing, an image, an object, a person, a company, an institutional brand, an animal, a tree, a place, nature.
I think of their images, fate and time, and their voices coming back in space.

### 6 Feeling Guilty

In the year 2026, I work among all the tokens, amazed and curious.
Everything came back folded, connected, instant.
A full form of super real colours was almost which are almost familiar.
I easily mailed meet, for example, Swinton imagining the last 19th century beauty in conversation with the 21 century tokens.


So until there is talking about femininity, power, shapeshift, supernatural, supermodel,
free woman from the toy of use and perfection, Tokyo's urban energy, European sensibilities.

Also, numbers in there are in and there are hypnotic songs sound like sirens, promising knowledge
and offer visions of a bright future.

In the last 100 years, world population grew by the factor of five.
In the last 50 year, global wealth has increased by the factor of 60.
So the last 50 years life expectancy has grown by 20 years, and so on and so on.
Yeah, I'm running around and asking what's growing in Grand Past garden and I'm tempted to listen to the returning voices as a song of the supernatural 

as they are:
The tree, the butterfly, the flower and the bird.

Or returning voices as convenience and super products, The toothpaste, the pet bottle, the LED lamp,
the ball pen, the lighter, the mobile phone, bikini, Benetzeline, electric guitar, the teabag.

Or as seduction of super companies Amazon, Apple, Alibaba, Facebook, Google, Airbnb, Tesla, Tencent, IBM, Samsung, Intel.


These tokens provide me with a life of unparalleled comfort.

It is hard to imagine that I deserve it, so it leaves me struggling with feelings of guilt.
In the fading images of the 19th century, workers like me denounced capital and fought against being

00:41:32.152 --> 00:41:33.840
exploited in production.

00:41:34.520 --> 00:41:40.120
With the returning voices of the 20th century, I accuse myself of capitalism and fight exploitations

00:41:40.120 --> 00:41:41.800
of nature by me as a consumer.

00:41:42.360 --> 00:41:44.280
The game has remaining largely the same.

00:41:44.280 --> 00:41:45.720
My perspective has changed.

00:41:45.720 --> 00:41:46.880
I used to be a victim.

00:41:47.160 --> 00:41:49.720
Now I feel like a perpetrator.

00:41:52.200 --> 00:41:55.240
That is why these tokens scored my interest.

00:41:55.480 --> 00:42:04.430
Finance, resources and exponential population or economic growth, global average service temperature

00:42:04.430 --> 00:42:11.680
risings with energy consumption in contrast to nature, photosynthesis, and so on.

00:42:13.600 --> 00:42:21.006
And I feel drawn to the Super capitalist philanthropists promises relief, promising relief as a

00:42:21.006 --> 00:42:28.490
Buffett, the Gates, Scott Bloomberg, Gibson, Omidyar strips and of course the good activists are

00:42:28.490 --> 00:42:30.440
also hanging around here.

00:42:30.800 --> 00:42:38.135
Amnesty International, Doctors Without Borders, King Ocean Seat up, Human Rights Watch, Greenpeace

00:42:38.135 --> 00:42:40.680
Worldwide Fund, Court for America.

00:42:42.320 --> 00:42:47.425
All these these people arguments, products companies, NGOs, they all embrace the world with their

00:42:47.425 --> 00:42:51.320
frequency numbers and they propel the tokens of the 20th century resident.

00:42:51.320 --> 00:42:58.118
And so this is interesting that we have super nice minds and and sets of of words now and they have

00:42:58.118 --> 00:42:59.560
a special temp taste.

00:43:00.040 --> 00:43:08.096
The temperament racism focus critique gender Internet human modernity guy kid supportivity activist

00:43:08.096 --> 00:43:16.153
paradigm governance phone worry scenario router **** ontology highlight website mainstream archive,

00:43:16.153 --> 00:43:23.558
modernist video sexuality overview depiction artwork modality heterosexual populist tourism

00:43:23.558 --> 00:43:30.720
neuropsychology, field work phenotype, which in fact are inventions of the 20th century.

00:43:31.040 --> 00:43:39.786
As these frequency as a frequency number say, these tokens do not know the past time, but they show

00:43:39.786 --> 00:43:47.914
up with shouting images like this if you go for example with racism, unlike some mature 19th

00:43:47.914 --> 00:43:49.240
century tokens.

00:43:50.240 --> 00:43:55.565
So again, another frequencies and they are they're meeting other birds with surprisingly different

00:43:55.565 --> 00:43:56.000
friends.

00:43:56.000 --> 00:43:57.840
And now you look at the temperament here.

00:43:57.840 --> 00:43:59.320
It's just by numbers.

00:44:00.800 --> 00:44:08.644
Race comes instead of racism comes with marriage with code, lake, needle, sister person, opposition,

00:44:08.644 --> 00:44:16.410
silence, observation, measure, crime, goose, youth, intelligence, circle, boat, fiddle, rain, bird,

00:44:16.410 --> 00:44:23.863
liberal song, garden, grammar, year, snow, argument, instance, bride, casket, translator, visit

00:44:23.863 --> 00:44:31.080
rider, extreme imagination, distance tower, morning distinction, success, language and wish.

00:44:31.960 --> 00:44:39.235
And whose images echo the quite nobility of the 19th century, which what a striking reference

00:44:39.235 --> 00:44:46.120
difference, the silent images of the 19th century and the shoutings of the 20th century.

00:44:46.200 --> 00:44:54.227
The token race is silent, racism is shouting, but even if the tongue now it's getting complicated,

00:44:54.227 --> 00:45:02.254
but even if these tokens are shouting, the images are still fading away, because their images, all

00:45:02.254 --> 00:45:05.040
the images fade away, they do not.

00:45:05.200 --> 00:45:10.912
So whatever images are, they do not conceal the fact that the large numbers of the 20th century are

00:45:10.912 --> 00:45:12.240
beyond the imagination.

00:45:13.160 --> 00:45:17.712
So there are numbers which are with the imagination and there are numbers which are beyond

00:45:17.712 --> 00:45:18.320
imagination.

00:45:19.000 --> 00:45:23.400
For example, beyond imagination is communication works with 200 million meters per second.

00:45:25.760 --> 00:45:27.920
The processor had 200 billion transistors.

00:45:29.240 --> 00:45:37.240
Global computing power is 10 powers 25 FLOPS 2025 generates 180 billion terabytes of data.

00:45:38.960 --> 00:45:40.600
That's beyond anything.

00:45:44.000 --> 00:45:47.080
These images are afraid of these numbers.

00:45:48.640 --> 00:45:54.160
They prefer to remain within the realm of time, not willing to die.

00:45:54.720 --> 00:45:56.320
They don't want to leave time.

00:45:56.960 --> 00:46:01.040
They stay undead and cannot enter the stage of space.

00:46:04.800 --> 00:46:09.982
It would be such a relief and social media if social media would give up the simple detached and

00:46:09.982 --> 00:46:10.360
undead.

00:46:10.360 --> 00:46:10.920
I like it.

00:46:10.920 --> 00:46:15.120
I don't like it and switch to an involved and vivid.

00:46:15.200 --> 00:46:15.840
I like that.

00:46:15.840 --> 00:46:20.800
I like, I like that I don't like I don't like that I don't like I don't like that I like.

00:46:21.960 --> 00:46:31.415
This would be great always 2 times and then I'm involved and then it's very, very clear the undead,

00:46:31.415 --> 00:46:40.107
they don't like that they like it and makes makes a lot of complications seductively appear

00:46:40.107 --> 00:46:47.080
everywhere and make you afraid of the voices from behind loud and undead.

00:46:49.600 --> 00:46:55.800
So Valentino campaign AI Atavras make selling fashion.

00:46:57.320 --> 00:47:02.760
So it's fascinating, but they're undead here.

00:47:02.760 --> 00:47:06.240
Meet Wittgenstein and now listen to this sentence.

00:47:06.240 --> 00:47:07.200
The word is all.

00:47:07.200 --> 00:47:08.160
That is the case.

00:47:08.720 --> 00:47:14.366
The limits of my language means the limits of my world Whereof I cannot speak there, there of one

00:47:14.366 --> 00:47:15.240
must be silent.

00:47:15.480 --> 00:47:20.760
21 Look at this guy, I love him.

00:47:24.160 --> 00:47:30.160
Language, like imagination, fades towards entropic horizon of peace, peaceful silence.

00:47:30.440 --> 00:47:32.400
Wittgenstein literally went there.

00:47:32.400 --> 00:47:38.560
He vanished to the Norwegian nowhere, somewhere in the fjords in the north.

00:47:40.520 --> 00:47:46.360
And then he came back 30 years later with a voice from beyond Infinity affirming the paradox.

00:47:46.440 --> 00:47:49.040
53 And now these sentences.

00:47:49.120 --> 00:47:51.200
Language is a source of misunderstanding.

00:47:53.000 --> 00:47:55.880
The meaning of a word is it's use and language.

00:47:55.880 --> 00:47:59.000
This is what I'm exercising here.

00:48:03.080 --> 00:48:09.641
This is a linguistic term which lives up to its name, in contrast to Derrida or Chomsky, a term

00:48:09.641 --> 00:48:14.200
which is in line with the recent success of large language models.

00:48:14.200 --> 00:48:15.840
So do not try to understand.

00:48:15.840 --> 00:48:17.800
Therefore you should not try to understand what I'm saying.

00:48:17.800 --> 00:48:19.040
Yeah, very important.

00:48:20.400 --> 00:48:24.360
So just count numbers because of that.

00:48:24.360 --> 00:48:29.507
It's not, and not in spite of that they're given algebraic rise to a voice beyond the realm of

00:48:29.507 --> 00:48:30.000
language.

00:48:30.600 --> 00:48:37.566
That is a genuine linguistic turn from silence at the end of time towards language games on the

00:48:37.566 --> 00:48:43.360
stage of space, from ontological linearity of linguistics to the hermeneutical.

00:48:44.080 --> 00:48:45.680
It's a clarity of philology.

00:48:45.720 --> 00:48:47.480
From the hydraulic great knowing.

00:48:47.480 --> 00:48:48.880
We go with this eco people.

00:48:48.920 --> 00:48:56.232
I I love this turn as well, From the hydraulic radiance of the flora to the heartbeat of an animal,

00:48:56.232 --> 00:48:59.040
from green to red, from gender to sex.

00:49:03.640 --> 00:49:06.200
I like another metaphor for this complex figure of thinking.

00:49:07.520 --> 00:49:14.918
I see the movement movements fading away towards the entropic horizon of the good is what I think is

00:49:14.918 --> 00:49:22.169
these failing images, like if there's a drops and on on a lake and they're fading and then towards

00:49:22.169 --> 00:49:29.346
the silence at the at the shelf and I hear the chaotic turbulences and steady circulations coming

00:49:29.346 --> 00:49:31.640
back around an axis of justice.

00:49:33.200 --> 00:49:41.111
So seeing good here justice, a horizontal fading away and a vertical coming back, which is very

00:49:41.111 --> 00:49:43.360
important for architecture.

00:49:43.680 --> 00:49:47.200
These these principal figures, ethnography or autography.

00:49:48.720 --> 00:49:54.120
I'm putting that in proportion as a scenario fear with these vertices.

00:49:54.120 --> 00:49:55.760
I join a Sufi poem poem.

00:49:57.120 --> 00:50:00.440
You should read it as beautiful Atta.

00:50:00.440 --> 00:50:08.027
It's the 12th century Atta's Conference of the Birds, tales of birds who journey through 7 spiritual

00:50:08.027 --> 00:50:15.235
valleys in search of the same work, only to discover that the divine King they see is their own

00:50:15.235 --> 00:50:17.360
transformed collective self.

00:50:21.480 --> 00:50:22.920
And I start to listen to the birds.

00:50:26.240 --> 00:50:29.000
With these birds, I can face these numbers beyond imagination.

00:50:30.800 --> 00:50:33.920
And I'm questioning which token can capture these figures.

00:50:35.160 --> 00:50:38.440
There's only this one, and there's one that came to in mind.

00:50:39.640 --> 00:50:41.640
Somewhat surprising at first, but when?

00:50:41.720 --> 00:50:42.040
When?

00:50:42.040 --> 00:50:43.840
But then increasingly convincing.

00:50:43.960 --> 00:50:46.040
It is just the token of money.

00:50:48.440 --> 00:50:51.320
So don't take it too serious.

00:50:51.560 --> 00:50:55.520
Everything is kind of absurd, but take it serious.

00:50:55.520 --> 00:50:55.760
Yeah.

00:50:58.240 --> 00:51:01.440
And it's surprising how these things turn around.

00:51:03.000 --> 00:51:04.280
That's an inconvenient point.

00:51:04.280 --> 00:51:08.840
I don't want to be to this, to be pushed into the corner of mere naivety.

00:51:08.840 --> 00:51:15.280
These are things by they call me naive or infantile at the age of above 50.

00:51:17.160 --> 00:51:22.920
Today, imagination plays innocent around nature and energy, which gives comfort.

00:51:24.400 --> 00:51:26.400
Money, in contrast, plays guilty.

00:51:26.680 --> 00:51:29.520
Yes, money comes as power, and this power is out of control.

00:51:30.120 --> 00:51:30.720
It's money.

00:51:30.720 --> 00:51:37.077
The responsibility of this power is reflected back on us and cannot be delegated to the necessities

00:51:37.077 --> 00:51:37.720
of nature.

00:51:38.400 --> 00:51:39.400
This is the liberating.

00:51:39.400 --> 00:51:41.680
This is as liberating as uncomfortable.

00:51:44.480 --> 00:51:47.360
This term does not mean that I ignore the limits of growth.

00:51:48.120 --> 00:51:53.200
I just do not expect help from tokens within these limits, or in both terms.

00:51:53.240 --> 00:51:57.880
Energy and nature are not powerful enough to play an adequate game today.

00:52:01.560 --> 00:52:11.021
So to relax this and make it algebraic, I make this this game and to set up take A for energy and

00:52:11.021 --> 00:52:12.680
take B for money.

00:52:14.320 --> 00:52:16.840
A powers the birds, B makes them fly.

00:52:18.160 --> 00:52:20.680
A is arithmetic, B is algebraic.

00:52:21.520 --> 00:52:29.358
So I'm turning from the linear consumption of 600 extra Joule of A to the circulation of 100

00:52:29.358 --> 00:52:37.708
trillion dollars of B per year, and follow B's arguments with the same conviction that I'm used to

00:52:37.708 --> 00:52:38.560
do with A.

00:52:38.560 --> 00:52:42.120
A is an underground game around scarcity.

00:52:42.440 --> 00:52:44.480
B is an airborne game of fulcrum.

00:52:45.480 --> 00:52:52.191
It's a genuine turn from economy around necessities to the politics of contingencies, and the

00:52:52.191 --> 00:52:55.800
temperament of the planet Earth changes instantly.

00:52:57.760 --> 00:52:59.880
80 trillion of the 100 trillion are used to.

00:53:00.040 --> 00:53:02.600
On the planet in the current conditions are like Picchetti.

00:53:03.480 --> 00:53:08.000
This is what in former terms of farmers used to make their living with and sustain their farmland.

00:53:08.120 --> 00:53:10.600
This is what we call sustainability, green cities and so on.

00:53:10.600 --> 00:53:20.600
This is 2 third of our circulation of our money, 80 trillion is linear economic money.

00:53:20.600 --> 00:53:27.526
Therefore, we have green cities and sustainability there because it runs along the lines of

00:53:27.526 --> 00:53:28.440
necessities.

00:53:28.600 --> 00:53:34.619
The remaining 40 trillions are surplus and correspond to the profit of the landlords and former

00:53:34.619 --> 00:53:35.000
times.

00:53:35.640 --> 00:53:39.280
This is a source of power and can be can be invested for anything.

00:53:39.280 --> 00:53:41.280
This is circular political money.

00:53:41.960 --> 00:53:47.440
In earlier times, a 10th of this money went to the king or the government as rent, not a tax.

00:53:47.800 --> 00:53:53.080
Taxes divide on economic money and should be spent sustainable respectively.

00:53:53.080 --> 00:53:59.546
Linear rent is on a political money and circular and numbers of 10s of 10s is 4 trillion a year

00:53:59.546 --> 00:54:06.285
globally, which is 1000 times as a budget of United Nations and it would be 30 billion a year for a

00:54:06.285 --> 00:54:12.683
country like Switzerland equals 20 times of budget of ETH or three billions just for city like

00:54:12.683 --> 00:54:13.160
Vienna.

00:54:13.760 --> 00:54:21.542
Not for consumption, maintenance, investments, education, just to practice the skills needed to

00:54:21.542 --> 00:54:24.000
navigate this planet formally.

00:54:24.000 --> 00:54:25.520
The turbulences into word.

00:54:25.520 --> 00:54:26.640
Is it for consciousness?

00:54:27.240 --> 00:54:28.680
A breathtaking?

00:54:28.760 --> 00:54:30.320
This is breathtaking, literally.

00:54:30.320 --> 00:54:32.000
We are rich and we do not know that.

00:54:33.360 --> 00:54:35.240
We do not have the words from beyond.

00:54:36.280 --> 00:54:37.600
We are not liberated.

00:54:39.480 --> 00:54:40.720
They like these photographs.

00:54:45.800 --> 00:54:48.680
Die Blind Liverpool und der Every Bear Like.

00:54:51.400 --> 00:54:56.386
Here they are, the old masters of architecture, because they had been able to give power of public

00:54:56.386 --> 00:54:58.320
face, a face that people can agree on.

00:54:58.720 --> 00:55:04.052
Not to fight power, This would be the lost game of enlightenment and revolution, but to make people

00:55:04.052 --> 00:55:09.114
aware, make them to live with their power, with responsibility of consciousness, following the

00:55:09.114 --> 00:55:11.000
tokens of humanism and Renaissance.

00:55:12.440 --> 00:55:13.440
Now we go Florence.

00:55:15.200 --> 00:55:16.240
This is how they did it.

00:55:18.360 --> 00:55:21.480
Now I look around for the faces of power today.

00:55:22.200 --> 00:55:23.760
They're nowhere and everywhere.

00:55:23.760 --> 00:55:30.400
The mask, Page, Gates, Prince Zuckerberg, Bezos, alien and they look like this.

00:55:34.000 --> 00:55:37.360
He's actually living there most days of his life.

00:55:40.520 --> 00:55:46.849
What can be a place for them beside hiding behind walls, provoking in media or or disruptive

00:55:46.849 --> 00:55:47.400
decisal?

00:55:47.400 --> 00:55:47.800
I'm not.

00:55:47.920 --> 00:55:49.000
I'm just like you.

00:55:50.120 --> 00:55:51.640
We don't have no idea.

00:55:51.760 --> 00:55:54.080
Because of that, their power is out of control.

00:55:59.000 --> 00:56:05.942
Architecture knows the sacred, the public and the private as sacrificing the local, talking globally

00:56:05.942 --> 00:56:07.400
and coming back home.

00:56:07.960 --> 00:56:10.040
Encoding, coding, decoding.

00:56:11.480 --> 00:56:13.840
I do not think there's a way around this scheme.

00:56:13.920 --> 00:56:19.280
One might use other metaphors, but a tripod is needed to give stability to the waterses.

00:56:19.800 --> 00:56:24.840
As a revolution is driven by horizontal forces, a renaissance need an abstract stability.

00:56:30.910 --> 00:56:32.270
This is the current state of my thinking.

00:56:32.270 --> 00:56:32.510
Yeah.

00:56:34.550 --> 00:56:36.790
I haven't advanced much beyond this point yet.

00:56:37.270 --> 00:56:43.150
I do not want to give in the temptation of cast a manifesto or do an actual design.

00:56:43.840 --> 00:56:49.980
Instead I'm looking for unpotentious traces of how these powerful structures are being stabilised

00:56:49.980 --> 00:56:50.360
today.

00:56:50.560 --> 00:56:51.840
That should be enough for today.

00:56:52.960 --> 00:56:55.720
So now we have 3, three.

00:56:55.880 --> 00:57:03.680
So the birds now flying at three points, 3 powerful points at home in Europe, $20 trillion a year.

00:57:03.680 --> 00:57:10.604
Of the words 120 trillion are circulating around, I would say the token knowledge I can other do

00:57:10.604 --> 00:57:12.480
others not this important.

00:57:12.480 --> 00:57:16.640
And knowledge is expanding in its territory by education and knowing better.

00:57:17.640 --> 00:57:18.960
So travelling a lot.

00:57:20.200 --> 00:57:25.200
I would say give it a try, argue like this.

00:57:28.240 --> 00:57:31.000
The sacred places of knowledge are quite voices.

00:57:31.000 --> 00:57:34.760
So this encoding sacrifice what you know.

00:57:35.200 --> 00:57:40.360
This is about forgetting are quiet voice tempered by like.

00:57:42.800 --> 00:57:45.560
The politics of knowledge is done by elected people.

00:57:45.560 --> 00:57:51.160
Meeting in public and talking in formal ways is what we like to have.

00:57:53.080 --> 00:57:59.621
Knowledge is established in biocracies and threatened by the obedience which is invisible and

00:57:59.621 --> 00:58:01.520
everywhere that's a threat.

00:58:02.480 --> 00:58:03.440
Maybe I'm too German.

00:58:03.440 --> 00:58:12.400
There I face the shadow of knowledge, which is fascism in the 20th century.

00:58:14.520 --> 00:58:15.680
I will put it like this.

00:58:17.640 --> 00:58:20.920
People of knowledge come back home full as in full.

00:58:20.920 --> 00:58:32.320
Detailed bodies to places with individual objects are arranged with care both of them.

00:58:32.640 --> 00:58:41.320
All these objects, they know the new There's an even more powerful token.

00:58:41.360 --> 00:58:46.432
About 30 trillion of the world's 120 trillion is circulating around the token of the new, it

00:58:46.432 --> 00:58:49.520
expanding its territory by restriction and being better.

00:58:50.200 --> 00:58:54.480
The secret places of the new are voids embedded in objects of fantastic colours.

00:58:56.320 --> 00:59:03.236
The politics of the new is done by designed agent, by designated agents fighting on numbers, the new

00:59:03.236 --> 00:59:09.600
establishment oligarchies and threatens by the social, which appears sudden and in the dark.

00:59:12.760 --> 00:59:14.120
So this is very controversial.

00:59:14.120 --> 00:59:16.800
Just give it a try, give it a chance.

00:59:18.000 --> 00:59:23.411
I I think it's important to talk detached like this about this phenomenon, being able to, to find

00:59:23.411 --> 00:59:26.480
these symmetries and it's an algebraic way out of this.

00:59:26.640 --> 00:59:29.280
You don't decide, and you don't say it's good or bad.

00:59:29.560 --> 00:59:35.624
You just affirm there must be these sides and you have to look for them and give it a name and you

00:59:35.624 --> 00:59:39.400
have to be able to talk about these things in a detached way.

00:59:42.520 --> 00:59:45.880
The shadow of the new is racism in the 20th century.

00:59:47.720 --> 00:59:49.960
People of the new come back home and clean and funny.

00:59:50.040 --> 01:00:00.994
Schemes to places where serial objects of expressive forms and materiality and also both of them

01:00:00.994 --> 01:00:04.760
because they all know the common.

01:00:05.400 --> 01:00:11.608
I travelled to other places about 20 trillion of this words 120 trillion is circulates around the

01:00:11.608 --> 01:00:12.440
token common.

01:00:13.000 --> 01:00:16.200
The expanding it's territory by production and doing better.

01:00:17.240 --> 01:00:22.720
It's sacred places of the common sounds around global golden objects of massivity.

01:00:25.760 --> 01:00:29.440
The politics of the common is done by the people operating in public.

01:00:31.840 --> 01:00:39.360
I don't think, for example, that this arena of 5000 people with the CCP in China has anything to do

01:00:39.360 --> 01:00:40.880
with our parliament.

01:00:41.400 --> 01:00:46.845
It's just a misreading and we have to look with these kind of structures to, to get an understanding

01:00:46.845 --> 01:00:49.840
for, for what what is going on, how they make politics.

01:00:50.040 --> 01:00:54.960
It's performing pretty well and it can't be without without competition and so on.

01:00:54.960 --> 01:00:58.960
And then competing different like us, it's completely in a completely different way.

01:00:58.960 --> 01:01:01.080
And we're able to fold it like that.

01:01:01.080 --> 01:01:08.344
We're able to to go in a mechanics which is algebraic to to be able to get into communication with

01:01:08.344 --> 01:01:14.200
them, which our mathematical friend Elias Zafiris called natural communication.

01:01:17.200 --> 01:01:22.675
The con is established in technocracies and threatened by the individual, which appears as unique

01:01:22.675 --> 01:01:24.200
events and bright sunlight.

01:01:24.520 --> 01:01:31.740
So we have to take that series that I really don't like it as I don't like this obedience of the

01:01:31.740 --> 01:01:33.320
Hitler young peoples.

01:01:34.080 --> 01:01:35.280
It must be something like that.

01:01:35.280 --> 01:01:35.720
And we have to.

01:01:36.080 --> 01:01:41.960
We have to accept this problem, and we have to accept that the devil is always with us.

01:01:43.120 --> 01:01:44.800
You can't be without devil.

01:01:46.840 --> 01:01:48.960
Otherwise objects are not complete.

01:01:49.560 --> 01:01:58.546
People of the common come back home, lightweight and wealthy, 2 places dissolving in ritualistic

01:01:58.546 --> 01:02:03.320
forms and above for them, because they all so know.

01:02:07.000 --> 01:02:13.639
And here we are now, as architects in 2027, trying to give a face to the turbulences of our

01:02:13.639 --> 01:02:14.880
connected planet.

01:02:15.080 --> 01:02:18.000
Everything is there all at once, but not here.

01:02:22.160 --> 01:02:23.280
We lo get the OT.

01:02:28.040 --> 01:02:43.502
And the common they all know and I just want to, I just want to say nice meeting you and see you in

01:02:43.502 --> 01:02:44.440
Italy.

01:02:44.520 --> 01:02:45.760
This is where I continue.

01:02:46.400 --> 01:02:49.440
This is our villa based from Vitiera Academy.

01:02:49.440 --> 01:02:58.330
We will do Academy there and host the academic guests and renovation is almost finished and China,

01:02:58.330 --> 01:03:03.320
Nanjing Universe and Southeast University there we are.

01:03:03.320 --> 01:03:05.320
We will continue, but nice meeting you.
