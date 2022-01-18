To define a type, the following must be specified:
- **Formation**: how to form new types of this kind, e.g. for a function type we need to have two types.
- **Construction**: how to build an element of the new type
- **Elimination**: how to move from this type to another type (ideally to the types used in the constructor above)
- **Computation**: how the eliminator acts on a constructor
- (Optional) Uniqueness principle