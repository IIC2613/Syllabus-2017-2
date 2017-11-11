# Tests Tarea 1

---

# Parte 1

### Test básico 

```prolog
% Estado inicial
block(B) :- member(B, [a, b]).
color(rob, B) :- member(B, [blue]).
color(bor, B) :- member(B, [red]).
holds(F, s0) :- member(F, [clear(a), on(a, b), ontable(b)]).
holds(color(B, white), s0) :- block(B).

% Test 1
time((legal(S), holds(color(a, blue), S))).

% Test 2
time((legal(S), holds(color(b, blue), S), holds(color(a, red), S))).
```

### Test pro

```
% Estado inicial
block(B) :- member(B, [a, b, c, d, e, f, g]).
color(rob, B) :- member(B, [blue]).
color(bor, B) :- member(B, [red]).
holds(F, s0) :- member(F, [clear(a), on(a, b), on(b, c), ontable(c), ontable(d), on(e, d), on(f, e), clear(f), ontable(g), clear(g)]).
holds(color(B, white), s0) :- block(B).

% Test 1
time((legal(S), holds(on(b, c), S), holds(ontable(a), S))).

% Test 2
time((legal(S), holds(on(b, d), S), holds(on(c, b), S), holds(on(a, c), S))).
```

---

## Parte 2

### Test básico

```
% Estado inicial
block(B) :- member(B, [a, b]).
color(rob, B) :- member(B, [blue]).
color(bor, B) :- member(B, [red]).
holds(F, s0) :- member(F, [clear(a), on(a, b), ontable(b)]).
holds(color(B, white), s0) :- block(B).

% Test
time((plies(Actions, SitSet), holdsAll(color(a, blue), SitSet))).
```

### Test pro

```
% Estado inicial
block(B) :- member(B, [a, b, c, d, e, f, g]).
color(rob, B) :- member(B, [blue]).
color(bor, B) :- member(B, [red]).
holds(F, s0) :- member(F, [clear(a), on(a, b), on(b, c), ontable(c), ontable(d), on(e, d), on(f, e), clear(f), ontable(g), clear(g)]).
holds(color(B, white), s0) :- block(B).

% Test
time((plies(Actions, SitSet), holdsAll(color(c, blue), SitSet))).
```

---

## Bonus

Se revisó el código y se hizo un par de pruebas para revisar si la implementación funcionaba. Además, la mayoría hizo un buen README sobre esto, lo que facilitó la corrección :grin: