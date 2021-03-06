# MnemonicRecoveryTool

"The aim of this repo is to create a program that can show you all possibilities for your last word in a mnemonic phrase."

## examples :

here's a mnemonic : toddler pepper buddy gentle crack heart cannon match answer stage shine nominee agree crouch steel cheese mean turtle final person close scorpion latin puzzle

```
python3 mnemonic_gen.py "toddler pepper buddy gentle crack heart cannon match answer stage shine nominee agree crouch steel cheese mean turtle final person close scorpion latin"

Phrase : toddler pepper buddy gentle crack heart cannon match answer stage shine nominee agree crouch steel cheese mean turtle final person close scorpion latin

Lasts words finded :

[0] : book
[1] : couch
[2] : empty
[3] : jacket
[4] : pact
[5] : puzzle
```

here the [5] was the word we searched. <br>
works with any mnemonic phrase (12, 15, 18, 21, 24) <br>


The number of expected words finded is: 2^(-1/3 L + 12) - 1 <br>

where L is the lenght of the complete mnemonic (in our case 24) <br>

nbits_to_fill = (L * 11)  - (L / 3)  -   ( (L - 1) * 11 ) = -(1/3)L + 11 <br>
expected number of word finded = 2^(nbits_to_fill + 1) - 1
