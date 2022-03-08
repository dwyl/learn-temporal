<div align="center">
  <a href="https://temporal.io/">
    <img src="https://user-images.githubusercontent.com/194400/158250447-78d23304-94aa-4850-a8d6-9c3e3815a304.jpeg" alt="Temporal Logo">
  </a>
  <p>
    <strong>Learn Temporal</strong>: a <em><strong>quick intro</strong></em> to 
    <strong><a href="https://temporal.io">temporal.io</a></strong> (<em>Workflow Engine</em>)
    for <em><strong>busy engineers</strong></em>.
  </p>
</div>

## Why?

<!--
You are building a system used by _millions_ of people
and processing _billions_ of transactions each day.
-->

You need the declarative log-based transactional workflow engine 
with built-in task queue, state management and retry mechanism 
to handle communicating/coordinating with several slow 
or unreliable 3rd party systems.

If that sounds like a bit of a buzzword soup, 
don't worry, we will break it down below.


<!--
You need to build a robust system but don't want to use Elixir/Erlang 
which has all of this either built-in or easily reachable e.g: https://github.com/safwank/ElixirRetry
-->


## What?

A workflow engine that can simplify writing orchestration between various APIs/services.

### Building Construction Analogy

If we use real-world construction as the basis for an analogy.

<img width="1047" alt="image" src="https://user-images.githubusercontent.com/194400/158482229-c4de7310-6f60-40a9-90fd-347392126293.png">

If you're building a free-standing single-family home,
you can probably just use a basic framing 
(bricks+mortar, timber & standard job-site tools)
to accomplish a good result.
However if you are building a **sky scraper** or a new **city**,
you need to think about the _infrastructure_ and use a very different 
construction method,
e.g. steel reinforced concrete, 
large quantities of structural glass,
excavators, tower cranes & specialised engineering contractors.

Temporal is a framework for a different level of engineering challenge.
If you're not building the digital equivalent of a Skyscraper,
use something simpler that doesn't require a dedicated DevOps person on your team!




## Who?

If you are building a complex app that has many moving parts 
e.g: microservices, datastores & 3rd party / unreliable APIs,
Temporal can greatly simplify this process.

If you're _not_ building something 
that has many moving parts,
you **_probably_**
[**don't need**](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it) 
Temporal, yet. 
You can still _learn_ how Temporal Workflows work 
if you're _curious_;
that's great!
But don't feel the need to over-engineer
a simple App just because you have a shiny new tool.

<div align="center">
  <a href="https://en.wikipedia.org/wiki/Overengineering">
    <img src="https://user-images.githubusercontent.com/194400/158479521-81cfdde3-8c4c-43fb-829a-2ca0459094eb.png" 
    alt="over engineering">
  </a>
  <p>
    <a href="https://imgs.xkcd.com/comics/the_general_problem.png">
      https://imgs.xkcd.com/comics/the_general_problem.png
    </a>
  </p>
</div>




## How?

Hello World Walkthrough in TypeScript:
https://docs.temporal.io/docs/typescript/hello-world/


# Want a 10 min Step-by-Step Tutorial?

Your wish is my command: 
[**`/tutorial`**](https://github.com/dwyl/learn-temporal/tree/main/tutorial)


## Recommended Reading

+ Temporal architecture:
https://docs.temporal.io/blog/workflow-engine-principles/#temporal-architecture-2010
+ Choreography vs Orchestration in the land of serverless: 
https://theburningmonk.com/2020/08/choreography-vs-orchestration-in-the-land-of-serverless/
+ What is a Temporal Cluster?
https://docs.temporal.io/docs/concepts/what-is-a-temporal-cluster/
+ TypeScript Introduction:
https://docs.temporal.io/docs/typescript/introduction/
+ TypeScript Getting Started: 
https://docs.temporal.io/docs/typescript/introduction/#getting-started
+ Getting Started Google Doc (Presentation):
https://docs.google.com/presentation/d/1mAPYXNmRdDKepXylB91F2uqFyHm8rG12K2PMRHxoUfM/edit#slide=id.g104dc941926_0_187
+ Workflows in TypeScript:
https://docs.temporal.io/docs/typescript/workflows/
+ Activities in TypeScript: 
https://docs.temporal.io/docs/typescript/activities/
+ TypeScript SDK:
https://github.com/temporalio/sdk-typescript
