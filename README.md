# THE SIEVE OF ERATOSTHENES, IN INTERCAL

> "It is universally acknowledged that a programmer in possession of a working
> compiler must be in want of a problem unworthy of it."

Herein is presented `sieve.i`, a faithful rendering of the Sieve of
Eratosthenes in the only programming language with the good taste to have been
designed with no real influences whatsoever. The program enumerates every prime
not exceeding one hundred and READs them OUT, as is proper, in butchered Roman
numerals.

The compiler is invited to find it INTERCAL Compiler Internal Library
compliant; the reader is invited to find it incomprehensible. Both invitations
are expected to be accepted with enthusiasm.

## ON THE NATURE OF THE ACHIEVEMENT

The discerning student of antiquity will observe that this is a *genuine* sieve
and not the trial-division impostor so often passed off as one in less rigorous
company. No number is ever divided by another. Multiples are STRUCK from the
firmament by the patient and dignified accumulation of sums, exactly as
Eratosthenes himself would have done had he been cursed with a teletype and an
abundance of PLEASEs.

That such restraint should be exercised in a language offering no fewer than
five flavours of stash and not a single usable conditional is, we submit, the
whole of the point.

## CONCERNING ITS OPERATION

Should you be so bold as to possess the C-INTERCAL compiler (`ick`), the
program may be coerced into an executable and thereafter run:

```
ick sieve.i
./sieve
```

The output appears in the customary notation:

```
II  III  V  VII  XI  XIII  XVII  XIX  XXIII  XXIX  XXXI  XXXVII
XLI  XLIII  XLVII  LIII  LIX  LXI  LXVII  LXXI  LXXIII  LXXIX
LXXXIII  LXXXIX  XCVII
```

These are, for the benefit of the Arabically inclined, the twenty-five primes
below one hundred. The reader who counts them and arrives at a different total
is encouraged to recount, the program having been verified against a reference
sieve of impeccable but regrettably ordinary pedigree.

## A WORD ON THE WORKINGS, OFFERED RELUCTANTLY

For the morbidly curious, and against our better judgement:

- **The sieve** is the 16-bit array `,1`, dimensioned to the limit. An element
  holds `#0` for so long as its index remains respectable, and `#1` once it has
  been struck out and shamed.
- **The bookkeeping** is entrusted to `.10` (the candidate), `.11` (the
  multiple under sentence), and `.12` (the limit). These reside above `.6`,
  where the system library, for all its meddling, has the decency not to tread.
- **Arithmetic** is begged from the standard library: `(1020)` to advance,
  `(1000)` to add, `(1010)` to subtract.
- **Comparison**, that luxury of decadent languages, is reconstructed from
  first principles: one subtracts, then inspects the sign bit with the SELECT
  operator (`~#32768`), a `#1` or `#2` being thereby manufactured for the
  edification of `RESUME`.
- **The conditional** — there being no such thing — is impersonated by the
  time-honoured practice of RESUMEing through a carefully chosen depth of the
  stack, the two branches reconvening by way of a `COME FROM` of the sort that
  has given the construct its sterling reputation.

Those who require the limit raised above one hundred need only amend the two
appearances of `#100`. Those who raise it very far are reminded that the answers
will continue to arrive in Roman numerals, and may reflect on their choices.

## ON POLITENESS

The compiler, like any institution of standing, declines to associate with the
insufficiently courteous and is equally repelled by the obsequious. The source
has accordingly been tuned to a temperate `PLEASE` in something under a quarter
of its statements. The author trusts this strikes the reader as neither curt
nor cloying.

## LICENCE

Do with it as you will, PLEASE.
