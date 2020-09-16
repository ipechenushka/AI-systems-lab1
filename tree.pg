% predicates
% first + second generation 
    parent(leonid, elena).
    parent(leonid, alexander).
    parent(galina, alexander).
    parent(galina, elena).
    parent(valentina, vladimir).
    parent(valentina, irina_l).
    parent(petr, vladimir).
    parent(petr, irina_l).
  
% second + third generation 
    parent(elena, ilya).
    parent(elena, tanya).
    parent(vladimir, ilya).
    parent(vladimir, tanya).
    parent(alexander, vitaliy).
    parent(alexander, violeta).
    parent(irina_o, violeta).
    parent(irina_o, vitaliy).
    parent(irina_l, evgeniy).
    parent(irina_l, julia).
    parent(sergey, evgeniy).
    parent(sergey, julia).

% third + fourth generetion
    parent(vitaliy, anissia).
    parent(vitaliy, alexander_jr).
    parent(vitaliy, alexey).
    parent(varvara, anissia).
    parent(varvara, alexander_jr).
    parent(varvara, alexey).
    parent(julia, anjelika).
    parent(julia, sofia).
    parent(roman, anjelika).
    parent(roman, sofia).
    parent(evgeniy, margarita).
    parent(vera, margarita).

% males
    male(leonid).
    male(petr).
    male(vladimir).
    male(alexander).
    male(sergey).
    male(ilya).
    male(vitaliy).
    male(roman).
    male(evgeniy).
    male(alexander_jr).
    male(alexey).

% females
    female(galina).
    female(valentina).
    female(elena).
    female(tanya).
    female(violeta).
    female(irina_o).
    female(irina_l).
    female(varvara).
    female(julia).
    female(vera).
    female(anissia).
    female(anjelika).
    female(sofia).
    female(margarita).

% rules
    predecessor(A, B) :- parent(A, B).
    predecessor(A, B) :- parent(A, C), predecessor(C, B).
    grandfather(A, B) :- parent(A, C), parent(C, B), male(A).
    grandmother(A, B) :- parent(A, C), parent(C, B), female(A).
    spouses(A, B) :- parent(A, Y), parent(B, Y).
    spouses(A, B) :- spouses(B, A).
    husband(A, B) :- spouses(A, B), male(A), female(B). 
    wife(A, B) :- husband(B, A).
    siblings(A, B) :- mother(C, A), mother(C, B), father(Z, A), father(Z, B), A \= B. 
    sister(A, B) :- siblings(A, B), female(A).
    brother(A, B) :- sister(B, A).
    uncle(A, B) :- parent(C, B), siblings(A, C), male(A).
    aunt(A, B) :- parent(C, B), siblings(A, C), female(A).
    son(A, B) :- parent(B, A), male(A).
    daughter(A, B) :- parent(B, A), female(A).
    mother(A, B) :- parent(A, B), female(A).
    father(A, B) :- parent(A, B), male(A).
    grandson(A, B) :- male(A), parent(C, A), parent(B, C).
    granddaughter(A, B) :- female(A), parent(C, A), parent(B, C).
