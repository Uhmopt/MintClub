# Mint Club
Smart token builder for everyone - [Mint.club](https://mint.club)

## Deployed on Binance Smart Chain (BSC)
Contract addresses are updated on: https://docs.mint.club/contracts

## Run Tests
```bash
npx hardhat test
```

## Deploy
```bash
npx hardhat compile

HARDHAT_NETWORK=bscmain node scripts/initial-deploy.js

# Verify source code on Etherscan
npx hardhat verify --network bscmain {contract address} "parameter 1" "parameter 2"
```

## Gas Consumption
```
·---------------------------------------------|---------------------------|--------------|----------------------------·
|             Solc version: 0.8.3             ·  Optimizer enabled: true  ·  Runs: 1500  ·  Block limit: 8000000 gas  │
··············································|···························|··············|·····························
|  Methods                                    ·               20 gwei/gas                ·      2450.55 usd/eth       │
························|·····················|·············|·············|··············|··············|··············
|  Contract             ·  Method             ·  Min        ·  Max        ·  Avg         ·  # calls     ·  usd (avg)  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubBond         ·  buy                ·     126875  ·     197930  ·      194502  ·         133  ·       9.53  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubBond         ·  createToken        ·          -  ·          -  ·      207685  ·         135  ·      10.18  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubBond         ·  sell               ·      42364  ·     102111  ·       99843  ·          63  ·       4.89  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubToken        ·  approve            ·      46575  ·      49265  ·       47093  ·         333  ·       2.31  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubToken        ·  burn               ·          -  ·          -  ·       33830  ·           1  ·       1.66  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubToken        ·  init               ·      91902  ·      91986  ·       91982  ·         142  ·       4.51  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubToken        ·  mint               ·      53505  ·      70617  ·       62154  ·         273  ·       3.05  │
························|·····················|·············|·············|··············|··············|··············
|  MintClubToken        ·  renounceOwnership  ·          -  ·          -  ·       28103  ·           1  ·       1.38  │
························|·····················|·············|·············|··············|··············|··············
|  Deployments                                ·                                          ·  % of limit  ·             │
··············································|·············|·············|··············|··············|··············
|  MintClubBond                               ·    1422126  ·    1422150  ·     1422148  ·      17.8 %  ·      69.70  │
··············································|·············|·············|··············|··············|··············
|  MintClubFactoryMock                        ·     572514  ·     572526  ·      572525  ·       7.2 %  ·      28.06  │
··············································|·············|·············|··············|··············|··············
|  MintClubToken                              ·          -  ·          -  ·     1016769  ·      12.7 %  ·      49.83  │
·---------------------------------------------|-------------|-------------|--------------|--------------|-------------·
```