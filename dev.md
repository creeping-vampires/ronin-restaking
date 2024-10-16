### Current deployment stage on ronin

```
========================================
[×] ProviderError: execution reverted
at HttpProvider.request (/Users/aamir/Desktop/3poch/asif/core/node_modules/hardhat/src/internal/core/providers/http.ts:107:21)
at processTicksAndRejections (node:internal/process/task_queues:95:5)
at async HardhatEthersProvider.estimateGas (/Users/aamir/Desktop/3poch/asif/core/node_modules/@nomicfoundation/hardhat-ethers/src/internal/hardhat-ethers-provider.ts:246:27)
at async /Users/aamir/Desktop/3poch/asif/core/node_modules/@nomicfoundation/hardhat-ethers/src/signers.ts:235:35
at async Promise.all (index 0)
at async HardhatEthersSigner.\_sendUncheckedTransaction (/Users/aamir/Desktop/3poch/asif/core/node_modules/@nomicfoundation/hardhat-ethers/src/signers.ts:256:7)
at async HardhatEthersSigner.sendTransaction (/Users/aamir/Desktop/3poch/asif/core/node_modules/@nomicfoundation/hardhat-ethers/src/signers.ts:125:18)
at async ContractFactory.deploy (/Users/aamir/Desktop/3poch/asif/core/node_modules/ethers/src.ts/contract/factory.ts:111:24)
at async deployContractType2 (/Users/aamir/Desktop/3poch/asif/core/lib/deploy.ts:69:20)
at async deployContract (/Users/aamir/Desktop/3poch/asif/core/lib/deploy.ts:99:12)
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

- Failing at step 09 on
  await updateProxyImplementation(Sk.lidoLocator, "LidoLocator", locator.address, proxyContractsOwner, [locatorConfig]);

state before step 09

{
accountingOracle: { deployParameters: { consensusVersion: 1 } },
apmRegistryFactory: {
contract: '@aragon/os/contracts/factory/APMRegistryFactory.sol',
address: '0x5d032E4d086a13c4cBc350FC91DC650eaD3A619C',
constructorArgs: [
'0x5f7D177956734aaa0170E9528992344814B5F724',
'0x50B16F9FB558CBED43444AB07527806dD11D15d3',
'0x48cD1E3b5bcD84Cc7E39fECe3d59D8E023a4bdCD',
'0x0e00a3113A0518b1EE14909C986792Da5Cb17ACb',
'0x61Db7Fa9ad51327d383B568EcA8b6C8Edbaf9C8e',
'0x0000000000000000000000000000000000000000'
]
},
'app:aragon-agent': {
implementation: {
contract: '@aragon/apps-agent/contracts/Agent.sol',
address: '0x62844620E969C033E03F9e936A0D399F4A7be538',
constructorArgs: []
},
aragonApp: {
name: 'aragon-agent',
fullName: 'aragon-agent.lidopm.eth',
id: '0x701a4fd1f5174d12a0f1d9ad2c88d0ad11ab6aad0ac72b7d9ce621815f8016a9'
},
proxy: {
address: '0xF9cbB4BA3a2ebb011438f2f4C2a250a1E5D19EB5',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'app:aragon-finance': {
implementation: {
contract: '@aragon/apps-finance/contracts/Finance.sol',
address: '0xCe02F56570511aB220A4d4697C55Bd23E7Cf5fc4',
constructorArgs: []
},
aragonApp: {
name: 'aragon-finance',
fullName: 'aragon-finance.lidopm.eth',
id: '0x5c9918c99c4081ca9459c178381be71d9da40e49e151687da55099c49a4237f1'
},
proxy: {
address: '0x30a7325263364d410047Fe23d8b6593647D6abb7',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'app:aragon-token-manager': {
implementation: {
contract: '@aragon/apps-lido/apps/token-manager/contracts/TokenManager.sol',
address: '0xb9441222f23B2342e40b54511EBA808A76744ff9',
constructorArgs: []
},
aragonApp: {
name: 'aragon-token-manager',
fullName: 'aragon-token-manager.lidopm.eth',
id: '0xcd567bdf93dd0f6acc3bc7f2155f83244d56a65abbfbefb763e015420102c67b'
},
proxy: {
address: '0x03ab53BEcCc2a3078882611015e740a499Af8351',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'app:aragon-voting': {
implementation: {
contract: '@aragon/apps-lido/apps/voting/contracts/Voting.sol',
address: '0x1F57C8C36e533973d223AE5Fd0c047f49dc3F571',
constructorArgs: []
},
aragonApp: {
name: 'aragon-voting',
fullName: 'aragon-voting.lidopm.eth',
id: '0x0abcd104777321a82b010357f20887d61247493d89d2e987ff57bcecbde00e1e'
},
proxy: {
address: '0x37bBeb73433143b573bEB23A1fFC114Eaa049647',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'app:lido': {
implementation: {
contract: 'contracts/0.4.24/Lido.sol',
address: '0xA4C942cFa4D5795c2B552738d2A0302B567f0f8E',
constructorArgs: []
},
aragonApp: {
name: 'lido',
fullName: 'lido.lidopm.eth',
id: '0x3ca7c3e38968823ccb4c78ea688df41356f182ae1d159e4ee608d30d68cef320'
},
proxy: {
address: '0xDa7621b079977dc1D3d72a36Ce2675808ED063A5',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'app:node-operators-registry': {
implementation: {
contract: 'contracts/0.4.24/nos/NodeOperatorsRegistry.sol',
address: '0x77f0807caA801022970C9183840A85aE8D043452',
constructorArgs: []
},
aragonApp: {
name: 'node-operators-registry',
fullName: 'node-operators-registry.lidopm.eth',
id: '0x7071f283424072341f856ac9e947e7ec0eb68719f757a7e785979b6b8717579d'
},
proxy: {
address: '0x1F692bF8F0c1C2feF08fDbC13ccE0b2f27F559A9',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'app:oracle': {
implementation: {
contract: 'contracts/0.4.24/oracle/LegacyOracle.sol',
address: '0x4A0B744F79636dD9aa4dCc9F779dc26e3079bF31',
constructorArgs: []
},
aragonApp: {
name: 'oracle',
fullName: 'oracle.lidopm.eth',
id: '0x8b47ba2a8454ec799cd91646e7ec47168e91fd139b23f017455f3e5898aaba93'
},
proxy: {
address: '0x551dC221e2e0dE31870bD6ef87b82d50104d93f2',
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol',
constructorArgs: [Array]
}
},
'aragon-acl': {
implementation: {
contract: '@aragon/os/contracts/acl/ACL.sol',
address: '0xD59C995b22c94fD81C7BB7da862C23411d87192F',
constructorArgs: []
},
proxy: {
address: '0x28736935ea7bd4ef4E696b6c1253d6d3bF7047E7',
constructorArgs: [Array],
contract: '@aragon/os/contracts/apps/AppProxyUpgradeable.sol'
},
aragonApp: {
name: 'aragon-acl',
id: '0xe3262375f45a6e2026b7e7b18c2b807434f2508fe1a2a3dfb493c7df8f4aad6a'
}
},
'aragon-apm-registry': {
implementation: {
contract: '@aragon/os/contracts/apm/APMRegistry.sol',
address: '0x50B16F9FB558CBED43444AB07527806dD11D15d3',
constructorArgs: []
},
proxy: { address: '0x1E93BeBa547f55a727f438f09283156e8428e82e' }
},
'aragon-evm-script-registry': {
proxy: {
address: '0xDd50E8c20bFCDCB56E196fE6089898A984a15b9C',
constructorArgs: [Array],
contract: '@aragon/os/contracts/apps/AppProxyPinned.sol'
},
aragonApp: {
name: 'aragon-evm-script-registry',
id: '0xddbcfd564f642ab5627cf68b9b7d374fb4f8a36e941a75d89c87998cef03bd61'
},
implementation: {
address: '0x8Eab45Fd0e411F8a917814Dd2B6Ddf1f4374Ba76',
contract: '@aragon/os/contracts/evmscript/EVMScriptRegistry.sol',
constructorArgs: []
}
},
'aragon-kernel': {
implementation: {
contract: '@aragon/os/contracts/kernel/Kernel.sol',
address: '0x468d7CB019e5A3792706D730961bd5F50cB5664D',
constructorArgs: [Array]
},
proxy: {
address: '0x43fc60964eA958422C73f07890464E41defb66A2',
contract: '@aragon/os/contracts/kernel/KernelProxy.sol',
constructorArgs: [Array]
}
},
'aragon-repo-base': {
contract: '@aragon/os/contracts/apm/Repo.sol',
address: '0x48cD1E3b5bcD84Cc7E39fECe3d59D8E023a4bdCD',
constructorArgs: []
},
aragonEnsLabelName: 'aragonpm',
aragonID: {
address: '0x12975733e2e2D503e85028ece7a01e79f41C2657',
contract: '@aragon/id/contracts/FIFSResolvingRegistrar.sol',
constructorArgs: [
'0x61Db7Fa9ad51327d383B568EcA8b6C8Edbaf9C8e',
'0xb784D5e745Cf6F99b7d1eE0950Dc1DF2f337506e',
'0x7e74a86b6e146964fb965db04dc2590516da77f720bb6759337bf5632415fd86'
]
},
burner: {
deployParameters: { totalCoverSharesBurnt: '0', totalNonCoverSharesBurnt: '0' }
},
callsScript: {
address: '0xBeac961FcaC3Bc0C9B71F0E8131AA03C1d5607fF',
contract: '@aragon/os/contracts/evmscript/executors/CallsScript.sol',
constructorArgs: []
},
chainId: 2021,
chainSpec: {
slotsPerEpoch: 32,
secondsPerSlot: 12,
genesisTime: 1639659600,
depositContract: '0x0b67552488F47FC1335B12A54D086274882aB19E'
},
createAppReposTx: '0xc26c1015c44ab6e7d8d20b7c445718303a2d8e93746d7a9f7d9d23d1dd19ab5e',
daoAragonId: 'lido-dao',
daoFactory: {
address: '0x5f7D177956734aaa0170E9528992344814B5F724',
contract: '@aragon/os/contracts/factory/DAOFactory.sol',
constructorArgs: [
'0x468d7CB019e5A3792706D730961bd5F50cB5664D',
'0xD59C995b22c94fD81C7BB7da862C23411d87192F',
'0x2fD8a7D57F7059375DE302D415d662B62dAc9aEE'
]
},
daoInitialSettings: {
voting: {
minSupportRequired: '500000000000000000',
minAcceptanceQuorum: '50000000000000000',
voteDuration: 900,
objectionPhaseDuration: 300
},
fee: { totalPercent: 10, treasuryPercent: 50, nodeOperatorsPercent: 50 },
token: { name: 'TEST Lido DAO Token', symbol: 'TLDO' }
},
deployer: '0x8BD0e959E9a7273D465ac74d427Ecc8AAaCa55D8',
depositContract: {
contract: 'contracts/0.6.11/deposit_contract.sol',
address: '0x0b67552488F47FC1335B12A54D086274882aB19E',
constructorArgs: []
},
depositSecurityModule: {
deployParameters: {
maxDepositsPerBlock: 150,
minDepositBlockDistance: 5,
pauseIntentValidityPeriodBlocks: 6646,
usePredefinedAddressInstead: '0x0000000000000000000000000000000000000000'
},
address: '0x0000000000000000000000000000000000000000'
},
ens: {
address: '0x61Db7Fa9ad51327d383B568EcA8b6C8Edbaf9C8e',
constructorArgs: [ '0x8BD0e959E9a7273D465ac74d427Ecc8AAaCa55D8' ],
contract: '@aragon/os/contracts/lib/ens/ENS.sol'
},
ensFactory: {
contract: '@aragon/os/contracts/factory/ENSFactory.sol',
address: '0x2a270d39d6604E8642299bA167ac2628961A08f0',
constructorArgs: []
},
ensNode: {
nodeName: 'aragonpm.eth',
nodeIs: '0x9065c3e7f7b7ef1ef4e53d2d0b8e0cef02874ab020c1ece79d5f0d3d0111c0ba'
},
ensSubdomainRegistrar: {
implementation: {
contract: '@aragon/os/contracts/ens/ENSSubdomainRegistrar.sol',
address: '0x0e00a3113A0518b1EE14909C986792Da5Cb17ACb',
constructorArgs: []
}
},
evmScriptRegistryFactory: {
contract: '@aragon/os/contracts/factory/EVMScriptRegistryFactory.sol',
address: '0x2fD8a7D57F7059375DE302D415d662B62dAc9aEE',
constructorArgs: []
},
gateSeal: {
address: null,
factoryAddress: '0x0000000000000000000000000000000000000000',
sealDuration: 518400,
expiryTimestamp: 1714521600,
sealingCommittee: []
},
hashConsensusForAccountingOracle: { deployParameters: { fastLaneLengthSlots: 10, epochsPerFrame: 12 } },
hashConsensusForValidatorsExitBusOracle: { deployParameters: { fastLaneLengthSlots: 10, epochsPerFrame: 4 } },
ldo: {
address: '0x5D79DBf4Da361AC55c8aa81cE99f8A3D019725fC',
contract: '@aragon/minime/contracts/MiniMeToken.sol',
constructorArgs: [
'0x69aff7Fd15eD081D1836DA99AEEdb8Dc0b630B8f',
'0x0000000000000000000000000000000000000000',
0,
'TEST Lido DAO Token',
18,
'TLDO',
true
]
},
legacyOracle: { deployParameters: { lastCompletedEpochId: 0 } },
lidoApm: {
deployArguments: [
'0x93cdeb708b7545dc668eb9280176169d1c33cfd8ed6f04690a0bcc88a93fc4ae',
'0x90a9580abeb24937fc658e497221c81ce8553b560304f9525821f32b17dbdaec'
],
deployTx: '0x87407e7bb39de46461b2a40a2487b24b1bb8359a88a60c15938aa0ede46f0448',
address: '0x1E84a48C667728fe24b3E8092aD34f91986Db491'
},
lidoApmEnsName: 'lidopm.eth',
lidoApmEnsRegDurationSec: 94608000,
lidoTemplate: {
contract: 'contracts/0.4.24/template/LidoTemplate.sol',
address: '0x0CCFB349a97b1D2B3BBc57fc57A3a61aE6296824',
constructorArgs: [
'0x8BD0e959E9a7273D465ac74d427Ecc8AAaCa55D8',
'0x5f7D177956734aaa0170E9528992344814B5F724',
'0x61Db7Fa9ad51327d383B568EcA8b6C8Edbaf9C8e',
'0x69aff7Fd15eD081D1836DA99AEEdb8Dc0b630B8f',
'0x12975733e2e2D503e85028ece7a01e79f41C2657',
'0x5d032E4d086a13c4cBc350FC91DC650eaD3A619C'
],
deployBlock: 31112017
},
lidoTemplateCreateStdAppReposTx: '0x6d21a85c114a522c8568e54bfaf9e20768b2a011105194dab19256b0973b577f',
lidoTemplateNewDaoTx: '0xcf99f337f7527a9cd0d7b913f39cef3f5f379e05b9393175efce02fd45664c2b',
miniMeTokenFactory: {
address: '0x69aff7Fd15eD081D1836DA99AEEdb8Dc0b630B8f',
contract: '@aragon/minime/contracts/MiniMeToken.sol',
constructorArgs: []
},
networkId: 2021,
nodeOperatorsRegistry: {
deployParameters: {
stakingModuleTypeId: 'curated-onchain-v1',
stuckPenaltyDelay: 172800
}
},
oracleDaemonConfig: {
deployParameters: {
NORMALIZED_CL_REWARD_PER_EPOCH: 64,
NORMALIZED_CL_REWARD_MISTAKE_RATE_BP: 1000,
REBASE_CHECK_NEAREST_EPOCH_DISTANCE: 1,
REBASE_CHECK_DISTANT_EPOCH_DISTANCE: 23,
VALIDATOR_DELAYED_TIMEOUT_IN_SLOTS: 7200,
VALIDATOR_DELINQUENT_TIMEOUT_IN_SLOTS: 28800,
NODE_OPERATOR_NETWORK_PENETRATION_THRESHOLD_BP: 100,
PREDICTION_DURATION_IN_SLOTS: 50400,
FINALIZATION_MAX_NEGATIVE_REBASE_EPOCH_SHIFT: 1350
}
},
oracleReportSanityChecker: {
deployParameters: {
churnValidatorsPerDayLimit: 1500,
oneOffCLBalanceDecreaseBPLimit: 500,
annualBalanceIncreaseBPLimit: 1000,
simulatedShareRateDeviationBPLimit: 250,
maxValidatorExitRequestsPerReport: 2000,
maxAccountingExtraDataListItemsCount: 100,
maxNodeOperatorsPerExtraDataItemCount: 100,
requestTimestampMargin: 128,
maxPositiveTokenRebase: 5000000
}
},
scratchDeployGasUsed: '76276957',
validatorsExitBusOracle: { deployParameters: { consensusVersion: 1 } },
vestingParams: {
unvestedTokensAmount: '0',
holders: {
'0xCD1f9954330AF39a74Fd6e7B25781B4c24ee373f': '820000000000000000000000',
'0xaa6bfBCD634EE744CB8FE522b29ADD23124593D3': '60000000000000000000000',
'0xBA59A84C6440E8cccfdb5448877E26F1A431Fc8B': '60000000000000000000000',
'0xF9cbB4BA3a2ebb011438f2f4C2a250a1E5D19EB5': '60000000000000000000000'
},
start: 0,
cliff: 0,
end: 0,
revokable: false
},
withdrawalQueueERC721: {
deployParameters: {
name: 'Lido: stETH Withdrawal NFT',
symbol: 'unstETH',
baseUri: null
}
}
}

args :

updateProxyImplementation : [
'0x82E2d82EAC1D754B6778627754460447bf999f9f',
'0x0000000000000000000000000000000000000000',
'0x21e4757AAD21a048F731BD678053c3eBFBfdDf4C',
'0x551dC221e2e0dE31870bD6ef87b82d50104d93f2',
'0xDa7621b079977dc1D3d72a36Ce2675808ED063A5',
'0x09b9605c6c8dC5F428f9aA69473d2878B29449E9',
'0x551dC221e2e0dE31870bD6ef87b82d50104d93f2',
'0xcF1E289f63E9cc7BFA92bC2FAfD9E76A25b491Ce',
'0x3448571F00C9aB28691c70D2F77734800d198003',
'0xF9cbB4BA3a2ebb011438f2f4C2a250a1E5D19EB5',
'0xd7C3dD9C44D22b302804Ef5d62958a33F0433FC1',
'0xdD343d16AEAf45AE33eBCC9C48271B97812E630a',
'0x5E5cFe77805071AF7577F66DC481Afe3420cffc3',
'0x62F43C057bb32193ce38286d254191341DE6AcfE'
];

state before the error

{
state: {
accountingOracle: { deployParameters: [Object] },
apmRegistryFactory: {
contract: '@aragon/os/contracts/factory/APMRegistryFactory.sol',
address: '0x5d032E4d086a13c4cBc350FC91DC650eaD3A619C',
constructorArgs: [Array]
},
'app:aragon-agent': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'app:aragon-finance': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'app:aragon-token-manager': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'app:aragon-voting': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'app:lido': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'app:node-operators-registry': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'app:oracle': { implementation: [Object], aragonApp: [Object], proxy: [Object] },
'aragon-acl': { implementation: [Object], proxy: [Object], aragonApp: [Object] },
'aragon-apm-registry': { implementation: [Object], proxy: [Object] },
'aragon-evm-script-registry': { proxy: [Object], aragonApp: [Object], implementation: [Object] },
'aragon-kernel': { implementation: [Object], proxy: [Object] },
'aragon-repo-base': {
contract: '@aragon/os/contracts/apm/Repo.sol',
address: '0x48cD1E3b5bcD84Cc7E39fECe3d59D8E023a4bdCD',
constructorArgs: []
},
aragonEnsLabelName: 'aragonpm',
aragonID: {
address: '0x12975733e2e2D503e85028ece7a01e79f41C2657',
contract: '@aragon/id/contracts/FIFSResolvingRegistrar.sol',
constructorArgs: [Array]
},
burner: { deployParameters: [Object] },
callsScript: {
address: '0xBeac961FcaC3Bc0C9B71F0E8131AA03C1d5607fF',
contract: '@aragon/os/contracts/evmscript/executors/CallsScript.sol',
constructorArgs: []
},
chainId: 2021,
chainSpec: {
slotsPerEpoch: 32,
secondsPerSlot: 12,
genesisTime: 1639659600,
depositContract: '0x0b67552488F47FC1335B12A54D086274882aB19E'
},
createAppReposTx: '0xc26c1015c44ab6e7d8d20b7c445718303a2d8e93746d7a9f7d9d23d1dd19ab5e',
daoAragonId: 'lido-dao',
daoFactory: {
address: '0x5f7D177956734aaa0170E9528992344814B5F724',
contract: '@aragon/os/contracts/factory/DAOFactory.sol',
constructorArgs: [Array]
},
daoInitialSettings: { voting: [Object], fee: [Object], token: [Object] },
deployer: '0x8BD0e959E9a7273D465ac74d427Ecc8AAaCa55D8',
depositContract: {
contract: 'contracts/0.6.11/deposit_contract.sol',
address: '0x0b67552488F47FC1335B12A54D086274882aB19E',
constructorArgs: []
},
depositSecurityModule: {
deployParameters: [Object],
address: '0x0000000000000000000000000000000000000000'
},
dummyEmptyContract: {
contract: 'contracts/0.8.9/utils/DummyEmptyContract.sol',
address: '0x625c16498A3995371b5c54D4F214Ba9626E11CE8',
constructorArgs: []
},
eip712StETH: {
contract: 'contracts/0.8.9/EIP712StETH.sol',
address: '0xa8B5A26b1bE497dC34921818C425ca304E0449A2',
constructorArgs: [Array]
},
ens: {
address: '0x61Db7Fa9ad51327d383B568EcA8b6C8Edbaf9C8e',
constructorArgs: [Array],
contract: '@aragon/os/contracts/lib/ens/ENS.sol'
},
ensFactory: {
contract: '@aragon/os/contracts/factory/ENSFactory.sol',
address: '0x2a270d39d6604E8642299bA167ac2628961A08f0',
constructorArgs: []
},
ensNode: {
nodeName: 'aragonpm.eth',
nodeIs: '0x9065c3e7f7b7ef1ef4e53d2d0b8e0cef02874ab020c1ece79d5f0d3d0111c0ba'
},
ensSubdomainRegistrar: { implementation: [Object] },
evmScriptRegistryFactory: {
contract: '@aragon/os/contracts/factory/EVMScriptRegistryFactory.sol',
address: '0x2fD8a7D57F7059375DE302D415d662B62dAc9aEE',
constructorArgs: []
},
gateSeal: {
address: null,
factoryAddress: '0x0000000000000000000000000000000000000000',
sealDuration: 518400,
expiryTimestamp: 1714521600,
sealingCommittee: []
},
hashConsensusForAccountingOracle: { deployParameters: [Object] },
hashConsensusForValidatorsExitBusOracle: { deployParameters: [Object] },
ldo: {
address: '0x5D79DBf4Da361AC55c8aa81cE99f8A3D019725fC',
contract: '@aragon/minime/contracts/MiniMeToken.sol',
constructorArgs: [Array]
},
legacyOracle: { deployParameters: [Object] },
lidoApm: {
deployArguments: [Array],
deployTx: '0x87407e7bb39de46461b2a40a2487b24b1bb8359a88a60c15938aa0ede46f0448',
address: '0x1E84a48C667728fe24b3E8092aD34f91986Db491'
},
lidoApmEnsName: 'lidopm.eth',
lidoApmEnsRegDurationSec: 94608000,
lidoLocator: { proxy: [Object], implementation: [Object] },
lidoTemplate: {
contract: 'contracts/0.4.24/template/LidoTemplate.sol',
address: '0x0CCFB349a97b1D2B3BBc57fc57A3a61aE6296824',
constructorArgs: [Array],
deployBlock: 31112017
},
lidoTemplateCreateStdAppReposTx: '0x6d21a85c114a522c8568e54bfaf9e20768b2a011105194dab19256b0973b577f',
lidoTemplateNewDaoTx: '0xcf99f337f7527a9cd0d7b913f39cef3f5f379e05b9393175efce02fd45664c2b',
miniMeTokenFactory: {
address: '0x69aff7Fd15eD081D1836DA99AEEdb8Dc0b630B8f',
contract: '@aragon/minime/contracts/MiniMeToken.sol',
constructorArgs: []
},
networkId: 2021,
nodeOperatorsRegistry: { deployParameters: [Object] },
oracleDaemonConfig: {
deployParameters: [Object],
contract: 'contracts/0.8.9/OracleDaemonConfig.sol',
address: '0x62F43C057bb32193ce38286d254191341DE6AcfE',
constructorArgs: [Array]
},
oracleReportSanityChecker: {
deployParameters: [Object],
contract: 'contracts/0.8.9/sanity_checks/OracleReportSanityChecker.sol',
address: '0x09b9605c6c8dC5F428f9aA69473d2878B29449E9',
constructorArgs: [Array]
},
scratchDeployGasUsed: '89911866',
validatorsExitBusOracle: { deployParameters: [Object] },
vestingParams: {
unvestedTokensAmount: '0',
holders: [Object],
start: 0,
cliff: 0,
end: 0,
revokable: false
},
withdrawalQueueERC721: {
deployParameters: [Object],
proxy: [Object],
implementation: [Object]
},
withdrawalVault: { implementation: [Object] },
wstETH: {
contract: 'contracts/0.6.12/WstETH.sol',
address: '0xBc27bc28AC7fA29dA6248B83AbF344e619F96996',
constructorArgs: [Array]
}
}
}
