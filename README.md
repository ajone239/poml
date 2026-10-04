# poML: the wrong tool for the job

```
                          __  _____
             ____  ____  /  |/  / /
      /| ___/ __ \/ __ \/ /|_/ / /
O|===|* >__/ /_/ / /_/ / /  / / /___
      \|  / .___/\____/_/  /_/_____/
         /_/
```

A sword is a well crafted, balanced instrument.
The pommel is the end bit of the handle often used for bludgeoning.

poML is an ML-styled languaged I'm writing as a learning project.
It will be slow and note very useful, but, it'll be fun.

# TODO


- [-] Parsing
  + [-] Setup
    * [x] Parse pairs into the AST enum
    * [ ] keep spans
  + [ ] Literals
    * int: `42`
    * bool: `true`
    * string: `"hi"`
  + [ ] Variables: `x`, `foo_bar`
  + [ ] Parens: `(e)`
  + [ ] Application by juxtaposition: `f x y`
  + [ ] Lambda: `fun x y -> e` (desugar to nested Lam)
  + [ ] Let: `let x = e1 in e2`
  + [ ] Let rec: `let rec f x = e1 in e2`
  + [ ] If: `if c then a else b`
  + [ ] Binary operators and precedence: `1 + 2 * 3`, `a == b`
  + [ ] Type exprs
    + int: 
    * int: `42: int`
    * bool: `true: boolean`
    * string: `"hi" : str`
    * lambda: `fun x y -> e: a -> b -> c` 
  + [ ] REPL prints the AST (Debug)
  + [ ] Parser tests

- [ ] Types and unification
  + [ ] Type enum (TVar, TCon, TArrow)
  + [ ] Substitution: apply, compose
  + [ ] Fresh type variable supply
  + [ ] Unify with occurs check
  + [ ] Unit tests for unify

- [ ] Algorithm W, monomorphic
  + [ ] Type env
  + [ ] Lit, Var, Lam, App, If
  + [ ] Thread substitution through each step
  + [ ] REPL prints inferred type (Debug)
  + [ ] Mismatch errors with spans

- [ ] Let-polymorphism
  + [ ] Scheme (Forall vars, type)
  + [ ] Free type vars of Type, Scheme, Env
  + [ ] Instantiate on Var lookup
  + [ ] Generalize at let
  + [ ] Tests: id, const, compose, (f 3, f "hi")

- [ ] Let rec
  + [ ] Bind name to fresh mono var, infer body, unify, then generalize
  + [ ] Tests: factorial, fib

- [ ] Typed IR
  + [ ] IR enum with types on nodes
  + [ ] Lower typed AST to IR
  + [ ] Desugar leftovers

- [ ] Eval
  + [ ] Value enum (Int, Bool, Str, Closure)
  + [ ] Env
  + [ ] Tree-walk the IR
  + [ ] Builtin operators
  + [ ] Tie the knot for let rec
  + [ ] REPL prints value and type

- [ ] ADTs and pattern matching
  + [ ] Type declarations with constructors
  + [ ] Constructors in the type env
  + [ ] Infer patterns
  + [ ] Eval patterns
  + [ ] Exhaustiveness check

- [ ] Later
  + [ ] Pretty-print types (rename vars to a, b, c)
  + [ ] Run a file
  + [ ] Split into workspace (core, cli)
  + [ ] Typeclasses
  + [ ] Bytecode VM
  + [ ] WASM playground
