# Tarea 1 - Bloques Cooperativos y Competitivos

**Semestre:** 2017, Segundo semestre

**Entrega:** 2 de Octubre, 23:59 hrs.

**Nombre:** Antonio Ossa

---

| Parte 1 | Parte 2 | Bonus |
| ------- | ------- | ----- |
| Si      | Si      | No    |

## Tests

```prolog
%% Object Declaration (problem-specific)
block(B) :- member(B,[a,b,c,d,e,f,g]).

color(rob, B) :- member(B, [blue]).
color(bor, B) :- member(B, [red]).

%% Initial Situation (problem-specific)
holds(F,s0) :- member(F,[clear(a),on(a,b),on(b,c),ontable(c),ontable(d),on(e,d),on(f,e),clear(f),ontable(g),clear(g)]).
holds(color(B,white),s0) :- block(B).
```

### Parte 1

```prolog
?- time((legal(S),holds(on(b,d),S),holds(on(c,b),S),holds(on(a,c),S))).
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
S = ... ;
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
S = ... .
```

```prolog
?- time((legal(S),holds(color(d,blue),S),holds(on(b,d),S),holds(color(b,red),S),holds(ontable(d),S))).
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
S = ... ;
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
S = ... .
```

```prolog
?- time((legal(S),holds(color(c,blue),S),holds(on(b,c),S),holds(color(b,red),S),holds(color(d,red),S))).
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
S = ... ;
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
S = ... .
```

### Parte 2

```prolog
?- time((plies(Actions,SitSet),holdsAll(color(c,blue),SitSet))).
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
Actions = [...],
SitSet = [...] ;
% _ inferences, _ CPU in _ seconds (_% CPU, _ Lips)
Actions = [...],
SitSet = [...] .
```

## Comentarios

La ayudantía de Prolog que hizo Antonio podría haber sido mejor si hubiese hecho X o Y :ok_hand:. La tarea hubiera sido más entretenida si hubise cubierto X tema.