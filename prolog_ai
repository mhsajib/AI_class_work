parent(john, ann). %the fact that John is a parent of Ann
parent(john, mike). %the fact that John is a parent of Mike
parent(mary, mike).
parent(mike, pat).
parent(mike, bob).
parent(pat, ben).
female(mary). %the fact that Mary is a female
female(ann).
female(pat).
male(john). %the fact that John is a male
male(mike).
male(bob).
male(ben).
mother(X,Y) :- parent(X, Y), female(X). %definition of the predicate mother
father(X,Y) :- parent(X, Y), male(X). %definition of the predicate father
brother(Y,Z) :- parent(X,Y),parent(X,Z),male(Y).
sister(Z,Y) :- parent(X,Y),parent(X,Z),female(Z).
grandfather(X,Y) :- father(X,Z),parent(Z,Y).
grandmother(X,Y) :- mother(X,Z),parent(Z,Y).
uncle(X,Z) :- parent(Y,Z), brother(X,Y).
aunt(Z,Y) :- parent(X,Y), sister(Z,X).
sibling(Y,Z) :- parent(X,Y),parent(X,Z).
cousin(X,Y) :- parent(Z,X),parent(W,Y),sibling(W,Z).
grandson(X,Y) :- parent(Z,X),parent(Y,Z),male(X).
son(X,Y) :- parent(Y,X),male(X).
grandparent(X,Y) :- parent(X,Z),parent(Z,Y).
greatgrandfather(X,Y):-grandparent(Z,Y),father(X,Z). 
greatgrandmother(X,Y):-grandparent(Z,Y),mother(X,Z).
