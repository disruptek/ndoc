# ndoc

_aka disruptex_

like pydoc but for nim


## Goals

Keep it simple, stupid.

- get something useful in the console first, then maybe the web
- drop a url or a small number of lines into my clipboard
- produce a useful result even if no local docs exist
- let me zero in on a particular symbol; make assumptions if you must
- give me some highlighting so i can scan the results asap
- search only needs to be good enough that i can iterate on it
- a bot should be able to yield short, useful answers to queries

## Stories

Questions everyone asks (and needs fast answers to) which we want to be able to
answer within a second or so.

- _How do I reverse a seq?_
- _Syntax for printing a float with 4 digits precision?_
- _What are the arguments for newProc?_
- _How do I convert between Time and DateTime?_
- _What's the Oid proc that returns a Time?_

etc.

## How To Do?

We don't actually need to do syntax analysis, so nimsuggest doesn't make any
sense. I think I only need the following:
  - i provide a module name, you provide the contents
  - i provide a symbol name, you tell me what it means
  - ???

Probably rg, sk, or fzf runs against a database we build AOT. We may even be
able to do this faster than they can.
