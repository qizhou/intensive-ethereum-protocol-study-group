
# Apr 7 (https://epf.wiki/#/eps/week3)
RANDAO mixing https://github.com/prysmaticlabs/prysm/blob/04f231a40083a5c1cf501abc7c46f39e2bf132f1/beacon-chain/core/blocks/randao.go#L30
- Shuffling https://github.com/prysmaticlabs/prysm/blob/cff5e2b5feb431e70d34d637677c6b9ebc49bf81/beacon-chain/core/helpers/beacon_committee.go#L278
- Committee https://github.com/prysmaticlabs/prysm/blob/f962d13407b75e6f95982eb232e6b23347c11a4a/beacon-chain/cache/committee.go#L74
- Attestation data structure https://github.com/prysmaticlabs/prysm/blob/8eb82dd378d5e0d8b6d0035c8870940fb85b6a5e/proto/prysm/v1alpha1/attestation.pb.go#L27

# Apr 7 Light Client
- Sync Committee (different block proposer committee) https://github.com/ethereum/consensus-specs/blob/dev/specs/altair/beacon-chain.md#sync-committee
  - 512 vs 128
  - Changes every 256 epochs (8192 slots)
  - https://eth2book.info/capella/part3/config/preset/#sync-committee
  - Sync Committee Election https://github.com/ethereum/consensus-specs/blob/dev/specs/altair/beacon-chain.md#get_next_sync_committee_indices
    - Validator can be duplicated in a committee
  - Block Proposer Committee Election https://github.com/ethereum/consensus-specs/blob/dev/specs/phase0/beacon-chain.md#compute_committee
    - Validator is unique in all committee of an epoch
- https://github.com/ethereum/portal-network-specs/blob/master/beacon-chain/beacon-network.md
- https://github.com/ethereum/consensus-specs/blob/b18bbd8c6199e6f310fac81ee790120c8136ced6/specs/altair/light-client/sync-protocol.md
