Storage locations for token
```k
syntax Int ::= "#Token.balances" "[" Int "]" [function]
// -----------------------------------------------
// doc: The token balance of `$0`
rule #Token.balances[A] => #hashedLocation("Solidity", 0, A)
```

```k
syntax Int ::= "#Token.supply" [function]
// -----------------------------------------------
// doc: The token balance of `$0`
rule #Token.supply => 1
```

```k
syntax Int ::= "#Token.allowance" "[" Int "][" Int "]" [function]
// -----------------------------------------------
// doc: The token balance of `$0`
rule #Token.allowance[A][B] => #hashedLocation("Solidity", 2, A B)
```
