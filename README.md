# Notes on Matching Logic
<img src="https://cdn.pixabay.com/photo/2017/06/16/07/26/under-construction-2408059_960_720.png" width="100">

_These notes reflect my, and my alone, current understanding about Matching Logic._

Matching Logic (ML) is the underlying logic of the [K Framework](https://github.com/runtimeverification/k): a language agnostic framework for programming language development, in a quite broad understanding of it. K is being developed at [Runtime Verification Inc](http://runtimeverification.com).

In this notes I write down some of my understanding about ML in the hope that it will help me gain a better understanding of it. And maybe it can help other people too.

## Why Matching Logic?

There are various logics to specify programming languages and reason about programs. Why yet another one? The idea of computation and deduction being two sides of the same coin is wonderful but not new. To be programming language agnostic, semantics-based, from where one can create many many language tools, is also not new. But the logic and its proof system allows for an implemenentation that integrates _seamlessly_ with SMT technology. And I think this is _awesome_.

Matching Logic has a very nice relationship with First Order Logic with equality. 
```
|=FOL ϕ iff F |= ϕ
```
where `F = {∃z :s . σ(x1 :s1, . . . , xn :sn) = z | σ ∈ Σs1...sn,s} ` where `Σ` is a signature and `si` are sorts.

A term rewrite system seem to have a straight forward representation too as rule application seems to be represented as `ϕ1 -> ϕ2`, with `ϕi` patterns.

## What is Matching Logic?

Is a logic where formulae are patterns interpreted as subsets of the domain such that they _match_ the given pattern. 
