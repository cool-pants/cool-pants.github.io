---
title: "Starting Out"
date: 2024-04-01T00:21:25+05:30
description: Introduction to Posts
menu:
  sidebar:
    name: Introduction
    identifier: intro
    weight: 40
tags: ["Basic", "Introduction", "Updates"]
categories: ["Basic", "Updates"]
---

Greetings, this is Mainak 👋. 

And this is one of *(hopefully)* many posts that I am planning about my insights on various domains ranging from **DSA**, **API Design**, **Tech**, etc.

So let's talk about what can be expected from some of my future posts.

# The Plan
So, first things first, to address the elephant in the room.
{{< alert type="success" >}}
Why self hosted instead of `dev.to`, `medium`, `wordpress`, yadi yada?
{{< /alert >}}

And to that my answer would be: **Why not?**

Numero uno vice of any self-respecting developer: 
> If you can self-host anything, you will self host it.

On a serious note, hosting my blogs, posts on my portfolio site feels more personal. And since I don't actually any complex analytics doesn't actually make sense to use the aforementioned services.

And to those arguing, 
> *B-but you can have XYZ handle the CMS and analytics and have your site use their delivery API to serve your articles on your site as well....*,

Well....you pose a pretty good point, I have no excuse other than **I Forgot XD**, moving on.

{{< alert type="success" >}}
Why write articles? You are a developer right? 👀
{{< /alert >}}

I have learnt that putting stuff to words or even writing stuff down do help a lot in proofing ideas. That along with putting this on the interwebs, open myself up to a lot of people who can see and call me out on the gaps of my knowledge (*free knowledge? yessir*).

This also helps me keep a repository of all the things I have already seen/read/implemented.

## Roadmap

So here are a couple of topics I am working on right now:
1. 1BRC: The 1 Billion Row Challenge - Python Edition
2. The Latency Lie
3. EasySplit: Building a Over Engineered Budgeting API
4. Do I Know ______?

So just a brief on each of these topics so you know what to expect.

### 1BRC: The 1 Billion Row Challenge - Python Edition
> *Calculate the min, max, and average of 1 billion measurements*

Is the basic problem statement of this. And as the title suggests, I will be working on a python implementation of this solution and try to optimise this as much as possible. And the easiest part of this statement is to solve the problem, the difficult part is to optimise the code to high ends.

Originally proposed and solved in Java, with the benchmark set for 1.5s, we will see how much we can optimise Python, a language *made* for processing large amounts of data easily and fast.

### The Latency Lie
So **Latency** is a common term we come across while developing APIs. But what does this mean?
> Latency, from a general point of view, is a time delay between the cause and the effect of some physical change in the system being observed.

What are these numbers I see after my Load Test? What is 95%ile, 90%ile Latency? How to interpret these results?

Followed by trying to engineer a Load Testing tool Feat. Vegeta and K6. I will also try to highlight some of the pitfalls I found while trying to implement my own load tester dubbed `go-meter`, later changed to `gogeta`. Surprisingly taking sum of difference of the start and end times of each request, and divinding the difference by the number of calls doesn't give an accurate average (who would've thought, well not me for sure XD).

### EasySplit: Building a Over Engineered Budgeting API
There are a lot of tutorials of building XYZ from scratch. But no one teaches you to over engineer 🗿, well no worries, I am here to proof stupid stuff and bad practices.

The main purpose of this is to create a robust API, given the following assumptions
- To target around **3000 concurrent users** with a **minimum local latency of 3s**
- Handling around **100_000+ transactions** (in total) per user (This is the data that we need to process for analytics and splits)
- Handling real time group transactions (like Splitwise)
- Handling Real time simplification of debts
- Group Analytics
- Monitoring, Metrics and Logging for the APIs

The Goal is to go from the ground up. Designing the DB, APIs, Selecting the Stack for the implementation, implementing said designs.

### Do I Know ______?
A Planned bi-weekly segment, where I explore topics and check whether I really know it inside out, and trying to reverse engineer a simplified implementation.
Plan is to explore topics ranging from standard library implementations of libraries, Data-structures, applications like Text, Vim, etc., Algorithms, or even Languages.

A fun exercise to solidify mostly basic and some not-so-basic concepts. Mostly a reinvent-the-wheel exercise, to see how things work internally.

So just an example, here's a sneak of the planned first Edition of this.

#### Edition 1: Do I Know Databases?
Well not really I don't 🙃. I know that data is stored in a file, but aside from that everything is mostly a blackbox.

So the first step is to find out, what a database does, what makes it different from a file IO. Well you may argue that it allows us to perform queries and parse the data faster than normal, but let me remind you that is a feature of the DBMS, not the database itself.

From my base understanding of a database is that it is a structured data-store, but so is a JSON or a YAML file. And this is not wrong, JSON and YAML files do allow for easy retrieval and querying of data and hence are considered databases. But can we create our own structured parser and syntax?

Well that is something that I will have to see while writing the article 😅.

## Signing Out
Well that's about it for this introductory post. Signing out for this week.
