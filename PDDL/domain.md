    (:types 
        location    ; there are several connected locations in the harbor 
        pile    ; attached to a location, holds a pallet + a stack of containers 
        robot   ; holds at most 1 container, only 1 robot per location
        crane   ; belongs to a location to pickup containers
        container)

(:predicates
    (adjacent   ?l1  ?l2 - location)        ; can move from ?l1 directly to ?l2
    (attached   ?p - pile ?l - location)    ; pile ?p attached to location ?l
    (belong     ?k - crane ?l - location)   ; crane ?k belongs to location ?l

    (at     ?r - robot ?l - location)   ; robot ?r is at location ?l
    (occupied   ?l - location)          ; there is a robot at location ?l
    (loaded     ?r - robot ?c - container ) ; robot ?r is loaded with container ?c
    (unloaded   ?r - robot)         ; robot ?r has no cargo

    (holding    ?k - crane ?c - container)  ; crane ?k is holding container ?c
    (empty      ?k - crane)         ; crane ?k is not holding anything

    (in     ?c - container ?p - pile)   ; container ?c is somewhere in pile ?p
    (top        ?c - container ?p - pile)   ; container ?c is on top of pile ?p
    (on     ?k1 ?k2 - container )       ; container ?k1 is on container ?k2
   )