## Versions
anchor-cli 1.1.2 · node 22.x · @codama/cli 1.6.3

## TODO 3
Required: fundraiser, vault. Optional: contributorAccount, contributorAta,
tokenProgram, systemProgram. `contribute` seeds the fundraiser PDA on
`fundraiser.maker`, a field of the account being derived, so the finder
would need the account to find the account. `initialize` seeds it on the
`maker` account, which the caller has, so there it is optional.

## Bonus
Attempted — passing. Built the instruction with getContributeInstructionAsync,
converted it with toWeb3Instruction, sent it through provider.sendAndConfirm,
and confirmed the vault balance grew by exactly AMOUNT.

## One thing that surprised me
How readable the generated TypeScript is, expected boilerplate, got clear,
well typed builders that were easier to read than I thought a
code gen tool would produce.