---
title: Building the Foundation of Hosanna
meta_title: ""
description: ""
date: 2026-08-05T00:26:00.000Z
image: ""
categories: []
authors:
  - Tiago Inês
tags: []
draft: false
---
# Building the Foundation of Hosanna

**From a song file to an entire application architecture.**

After the initial idea for Hosanna became a real project, the next challenge was much less exciting than designing interfaces.

We had to make the thing actually work.

And work reliably.

One of the biggest lessons from the early development of Hosanna was that a worship application cannot be designed like a normal web application.

If you're standing in front of a congregation and your song doesn't load because the network disappeared, it doesn't matter how good the API is.

The song still didn't load.

That shaped a lot of our technical decisions.

## Local first

Hosanna was designed around the idea that the client should have what it needs locally.

Songs are stored and cached on the device rather than requiring every interaction to go through a server.

The server can provide synchronisation and collaboration, but the application itself shouldn't become useless simply because the connection isn't perfect.

This also meant that we had to think carefully about how data moves between the dashboard, server and mobile application.

Eventually, this became a proper synchronisation system rather than simply fetching everything whenever the application opened.

## Building the ChordPro engine

Another major part of the foundation was ChordPro itself.

It sounds simple at first:

> Take a text file and display the chords.

In reality, formatting music properly involves quite a lot more.

Chords need to be positioned correctly. Songs need to be transposed. Formatting directives need to be interpreted. Different layouts need to work across different screen sizes.

The engine gradually became its own reusable piece of Hosanna's architecture.

That work eventually led to shared packages containing the common logic used throughout the different Hosanna applications.

## Three applications, one ecosystem

As the project grew, it became clear that there wasn't really one Hosanna application.

There were several.

The mobile application is where musicians interact with their music.

The dashboard is where churches manage their library and prepare things.

The server provides the infrastructure connecting everything together.

Keeping those pieces separate while still sharing the same logic became an important architectural goal.

Instead of duplicating functionality, common functionality could live in shared packages.

That made development faster and, more importantly, kept the different parts of Hosanna consistent.

## Making it feel like a real product

This was also when Hosanna started getting the features that made it feel less like a technical experiment.

Folders and tags.

BPM information.

Song management.

Transposition.

Better formatting.

Caching.

Synchronisation.

And eventually the beginnings of service planning.

Every feature introduced another question:

**How should this work during an actual church service?**

That question became our most important design constraint.

We're not building software for someone to stare at for eight hours a day.

We're building software that needs to work quietly and reliably for a few minutes at exactly the right moment.

That changes everything.

And this foundation became the platform on which the rest of Hosanna could be built.
