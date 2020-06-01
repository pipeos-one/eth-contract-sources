# eth-contract-sources

mainnet:
60,664 records

ropsten:
53,574 records


rinkeby:
31,023 records
389.3 MB

kovan:
8,321 records
120.5 MB

goerli:
3,178 records
31.9 MB

## Notes

Zip chunks created with:
```
zip -s 95m  -r kovan_sources.zip kovan_sources.sql.zip
```

All tables have the same structure:

CREATE TABLE `goerli_sources` (
  `id` int(11) NOT NULL,
  `address` varchar(45) NOT NULL,
  `blockscout` smallint(1) DEFAULT 0,
  `verified` smallint(1) DEFAULT 0,
  `checked` smallint(1) DEFAULT 0,
  `failed` smallint(1) DEFAULT 0,
  `contractName` varchar(125) DEFAULT NULL,
  `compilerVersion` varchar(45) DEFAULT NULL,
  `optimization` tinyint(4) DEFAULT NULL,
  `runs` int(11) DEFAULT NULL,
  `evmVersion` varchar(45) DEFAULT NULL,
  `sourceCode` longtext DEFAULT NULL,
  `bytecode` longblob DEFAULT NULL,
  `constructorArguments` blob DEFAULT NULL,
  `libraries` varchar(10000) DEFAULT NULL,
  `abi` longtext CHARACTER SET utf8 DEFAULT NULL,
  `block` int(11) DEFAULT NULL,
  `txhash` varchar(100) DEFAULT NULL,
  `timestamp` datetime NOT NULL DEFAULT current_timestamp(),
  `sourcemap` longtext DEFAULT NULL,
  `swarm` varchar(255) DEFAULT NULL,
  `license` varchar(255) DEFAULT NULL,
  `sourceCodeJson` longtext DEFAULT NULL,
  `donotcheck` smallint(1) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
