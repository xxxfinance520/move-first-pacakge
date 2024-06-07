package id: 0x8eee349052bcf659085f893160dac950406d65af87a1b6b97e58422cd865bdca
Forge id: 0xd5263bc65717b7c2dab5d9c81eceb638b1411d9b77ac0c38182366f0b0da1bf7
Coin: 0x0ca3d3bf9e0aac61243dbebf441de8a731e8f88f20d62a67d39e2a4f811ec1e6
UpgradeCap: 0x2c9b32c7f824ec1d9492fdd1e38324643cff6e2540899b8bbd1ef4e886ac303d

sui client call --package 0x8eee349052bcf659085f893160dac950406d65af87a1b6b97e58422cd865bdca --module my_module --function swords_created --args 0xd5263bc65717b7c2dab5d9c81eceb638b1411d9b77ac0c38182366f0b0da1bf7


# 铸造代币
sui client call --package 0xa629edf44a17c2d5481bfe938c7132238dca97762e28dec994a562a55607e10c --module mycoin --function mint --args 0x3f995829e93cf5a8bcccfc86b393782383cfc1e1c52b85abeb3d09d134535a14 10000000 0x9b9b99b7eb6107fc7bc03addf92fbef4d60b41a3984e2e906077954a014cb2c4

//account1: 0x4b55fcf59a0347eb690045a5b56b0762546162e32d90a80a1357943c74617108
		  : 0x8695b0ae98760f85cf8fd45a5cd578e3ecafeb88e26b1c31301f3a21e78b1d71

//account2: 
 			0x4806a380bd58191f84d83accc32a72cbce89041e4966b00865357fd4926a8bbd
          : 0xad9394dc719cb3fb542635cf308ef382cb7a1fb16fe26d64701fa39fda6df376
		  :  0x4806a380bd58191f84d83accc32a72cbce89041e4966b00865357fd4926a8bbd
```
    sui client ptb \
	--assign forge @0xd5263bc65717b7c2dab5d9c81eceb638b1411d9b77ac0c38182366f0b0da1bf7 \
	--assign to_address @0x9b9b99b7eb6107fc7bc03addf92fbef4d60b41a3984e2e906077954a014cb2c4 \
	--move-call 0x8eee349052bcf659085f893160dac950406d65af87a1b6b97e58422cd865bdca::my_module::new_sword forge 3 3 \
	--assign sword \
	--transfer-objects "[sword]" to_address \
	--gas-budget 20000000
```