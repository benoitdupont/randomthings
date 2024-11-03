+++
title = 'Go'
date = 2024-11-03T17:52:56+01:00
draft = true
+++

# Are you ashamed to be an architect ?
Are you an architect ?

# Go: first encounter

Disclaimer: I'm a senior Java developper, with a biais against other languages (I don't like Frontend, other languages, ...)

Company needed my help urgently on a projet in Go, I was in a "Why not" mood so did accept "Just to see what's the fuss with Go"
(Did a lot of architecturing, missed plain old development)

First day is a bit weird, I'm quickly annoyed with tutorials, wanted to jump in fast on the projet. 
Syntax is a bit confusing, but not that hard (thanks IDE !)

Struggled a bit with Intellij and Go, I didn't realized that it was just GREAT with Java, but a bit limited with Golang (I'll try to explain later), didn't tested Goland though (one license is already enough for me)

First thing I did was to find the similarities between Java and Go to have something to rely on. 
For the rest, if it's just maintenance, it's more "easy" to jump in and copy what's already existing.

I was quickly able to write some Go, but I often got from review that I just wrote Java with a Go syntax (what does that mean ?)

One point for Go: everything is so FAST ! No long Maven build, slow startup, ... It was just insta fast. 

Second point noted is the "no framework rule". And here a quick side note: what I perceive as the Go experience, is just the Go experience at the present Company in the team, not the global Go feeling (like an interpretation of the spec, not the spec itself).
Never I ever considered writing much vanilla code myself, having been thaught since the beginning the "Don't reinvent the wheel" axiom, use proven librairies, where experienced people already took care of a lot of issues from the community, ...
I was an avid user of the Spring *framework*, using it everywhere: projects, pocs, ... Got a discussion with another colleague who didn't wanted Spring into the ESB in Camel, did not understand what he meant at the time (more on that later)

Project was in DDD also (not Go specific, but I see a lot of link between Go and DDD in the literature), why not ? Project structure was completely different from my experience in Java. 

I had a lot of trouble with finding files: Had a feeling that in Java, the fully qualified name of the class (or even just it's name) is usually unique whereas in the projet, there are several times the same -class- project file (sig... second big difficulity: no classes, no methods (ah but yes), but functions, changing my lingo)
-> I did even inveted the POGO instead of the POJO (https://en.wikipedia.org/wiki/Pogo_(dance))

Also, short variables ! As from Clean Code (I think) I cleradly used to use long variables ...


# Couple of months in 

The difference with the switch case 

Quizz Go: que va afficher l'exécution de ce test ? (c'est vicieux lol)

func TestEnum(t *testing.T) {
    code := "3"

    switch code {
    case "1":
    case "2":
    case "3":
    case "4":
       fmt.Println("Nombre entre 1 et 4")
       return
    case "5":
       fmt.Println("Nombre strictement plus grand que 4")
       return
    }
}

library 
