---
parent: Decisions
nav_order: 1
---
# Dual License the Work

## Context and Problem Statement

Everything needs to be licensed, otherwise the default copyright laws apply.
For instance, in Germany that means users may not alter anything without explicitly asking for permission.
For more information see <https://help.github.com/articles/licensing-a-repository/>.

We want to have MADR used without any hassle and that users can just go ahead and write MADRs.

## Considered Options

* [CC0](https://creativecommons.org/share-your-work/public-domain/cc0/)
* BSD3
* MIT
* Dual license with MIT and CC0
* No license
* Other open source licenses

## Decision Outcome

Chosen option: "Dual license", because this lets users choose whether CC0 or MIT fits better on their work.

## Pros and Cons of the Options

## CC0

* Good, because this license donates the content to "public domain" and does so as legally as possible.
* Bad, because it does not contain attribution - and [attribution is important](https://opensource.stackexchange.com/a/9126/5671).

## BSD3

* Bad, because it [is unclear whether it can be used for documentation](https://opensource.stackexchange.com/a/9545/5671)

## MIT

* Good, because it [explicitly may be used for documentation](https://opensource.stackexchange.com/a/9545/5671)
* Good, because it is lean.

## Dual license with MIT and CC0

With the SPDX identifier `MIT OR CC0-1.0`, the receiver of the documents can decide which license thay want to use.

* Good, because offers freedom at the receiver
* Bad, because dual licensing is not widely known
