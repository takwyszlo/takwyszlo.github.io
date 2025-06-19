---
layout: post
title: "Reactiveness in practice"
subtitle: "<subtitle>"
date: <2021-06-07 08:00:00 -0400>
background-color: "<#2c5d88>"
---

## Motivation
In this post, I would like to share knowledge about building software workflows for .net library. Few months ago I decided to publicly release my **dotnet library [Middlink](https://github.com/Measureit/Middlink)** by using GitHub actions. So far my all private projects was hosted in GitLab and it's time to use something else.

I always try touch few different solutions to grab some experience and grow as a software developer. This approach help changing the perspective during solving problems and increases decision-making.

## Table of contents

1. [Introduction](#id-introduction)
7. [Summary](#id-summary)

<div id='id-introduction'/>

## 1. Introduction

Reactive extensions

## 2. IEnumerable vs IObservable

Po opisowym wstępie czas przejsc do zrozumienia sedna sprawy. w tym celu posłyżę się dobrze znanym interfesjem IEnumerable, który symbolizuje kolekcję. Czy na pewno? nie konieczne. IEnumerbale exposes the enumerator and enumerator responsibility is which supports a simple iteration over a collection of a specified type.
IEnumeratro i Enumerable + diagram i przykład


Where we can use this interface. NAjprostsza technika użycia jest petla foreach. Chemy przejsc przez kolekcje i wykonać jaka operacje na elemencie - iterate throuht

Co to znaczy, że foreach under the hood .  -> we decide by invoke MoveNExt when element is expose -> it is pull operation


Lets imagine case that we will have some element but int he futer

IEnumerbale<Trade> + 

IEnumerable discrabe how to iterate throught collection

IObsevable represents change directon 

Nonobservable sequences are what we normally call enumerables (or collections), which
implement the IEnumerable interface and return an iterator that implements the
OnCompleted
OnError(Exception)
Strings
.Where(s => s.StartsWith("A"))
.Select(s => s.ToUpper())
aa Abc Ba Ac
Abc Ac
ABC AC
16 CHAPTER 1 Reactive programming
IEnumerator interface. When using enumerables, you pull values out of the collection,
usually with a loop. Rx observables behave differently: instead of pulling, the
values are pushed to the observer. Tables 1.1 and 1.2 show how the pull and push
models correspond to each other. This relationship between the two is called the duality
principle.5
a There’s one exception to the duality here, because the twin of the GetEnumerator parameter (which is void) should have been
transformed to the Subscribe method return type (and stay void), but instead IDisposable was used.
Observables and observers fill the gap .NET had when dealing with an asynchronous
operation that needs to return a sequence of values in a push model (pushing each
item in the sequence). Unlike Task<T> that provides a single value asynchronously,
or IEnumerable that gives multiple values but in a synchronous pull model, observables
emit a sequence of values asynchronously. This is summarized in table 1.3.

<div id='id-summary'/>

## 7. Summary



#### Links

- <link>
