## /stacks-blockchain/mainnet/headers.sqlite
### db_config
|   cid | name    | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | version | TEXT   |         1 |              |    0 |               |


### chain_work
|   cid | name     | type    |   notnull | dflt_value   |   pk | description   |
|------:|:---------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | interval | INTEGER |         0 |              |    1 |               |
|     1 | work     | TEXT    |         1 |              |    0 |               |


### headers
|   cid | name           | type    |   notnull | dflt_value   |   pk | description   |
|------:|:---------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | version        | INTEGER |         1 |              |    0 |               |
|     1 | prev_blockhash | TEXT    |         1 |              |    0 |               |
|     2 | merkle_root    | TEXT    |         1 |              |    0 |               |
|     3 | time           | INTEGER |         1 |              |    0 |               |
|     4 | bits           | INTEGER |         1 |              |    0 |               |
|     5 | nonce          | INTEGER |         1 |              |    0 |               |
|     6 | height         | INTEGER |         1 |              |    1 |               |
|     7 | hash           | TEXT    |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/peer.sqlite
### frontier
|   cid | name                | type    |   notnull | dflt_value   |   pk | description   |
|------:|:--------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | peer_version        | INTEGER |         1 |              |    0 |               |
|     1 | network_id          | INTEGER |         1 |              |    0 |               |
|     2 | addrbytes           | TEXT    |         1 |              |    0 |               |
|     3 | port                | INTEGER |         1 |              |    0 |               |
|     4 | public_key          | TEXT    |         1 |              |    0 |               |
|     5 | expire_block_height | INTEGER |         1 |              |    0 |               |
|     6 | last_contact_time   | INTEGER |         1 |              |    0 |               |
|     7 | asn                 | INTEGER |         1 |              |    0 |               |
|     8 | org                 | INTEGER |         1 |              |    0 |               |
|     9 | allowed             | INTEGER |         1 |              |    0 |               |
|    10 | denied              | INTEGER |         1 |              |    0 |               |
|    11 | initial             | INTEGER |         1 |              |    0 |               |
|    12 | in_degree           | INTEGER |         1 |              |    0 |               |
|    13 | out_degree          | INTEGER |         1 |              |    0 |               |
|    14 | slot                | INTEGER |         1 |              |    1 |               |


### asn4
|   cid | name   | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | prefix | INTEGER |         1 |              |    1 |               |
|     1 | mask   | INTEGER |         1 |              |    2 |               |
|     2 | asn    | INTEGER |         1 |              |    0 |               |
|     3 | org    | INTEGER |         0 |              |    0 |               |


### db_config
|   cid | name    | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | version | TEXT   |         1 |              |    0 |               |


### local_peer
|   cid | name               | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | network_id         | INT     |         1 |              |    0 |               |
|     1 | parent_network_id  | INT     |         1 |              |    0 |               |
|     2 | nonce              | TEXT    |         1 |              |    0 |               |
|     3 | private_key        | TEXT    |         1 |              |    0 |               |
|     4 | private_key_expire | INTEGER |         1 |              |    0 |               |
|     5 | addrbytes          | TEXT    |         1 |              |    0 |               |
|     6 | port               | INTEGER |         1 |              |    0 |               |
|     7 | services           | INTEGER |         1 |              |    0 |               |
|     8 | data_url           | TEXT    |         1 |              |    0 |               |


### allowed_prefixes
|   cid | name   | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | prefix | TEXT    |         1 |              |    0 |               |
|     1 | mask   | INTEGER |         1 |              |    0 |               |


### denied_prefixes
|   cid | name   | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | prefix | TEXT    |         1 |              |    0 |               |
|     1 | mask   | INTEGER |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/atlas.sqlite
### attachments
|   cid | name             | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | hash             | TEXT    |         0 |              |    1 |               |
|     1 | content          | BLOB    |         1 |              |    0 |               |
|     2 | was_instantiated | INTEGER |         1 |              |    0 |               |
|     3 | created_at       | INTEGER |         1 |              |    0 |               |


### attachment_instances
|   cid | name             | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | content_hash     | TEXT    |         0 |              |    0 |               |
|     1 | created_at       | INTEGER |         1 |              |    0 |               |
|     2 | index_block_hash | STRING  |         1 |              |    1 |               |
|     3 | attachment_index | INTEGER |         1 |              |    3 |               |
|     4 | block_height     | INTEGER |         1 |              |    0 |               |
|     5 | is_available     | INTEGER |         1 |              |    0 |               |
|     6 | metadata         | TEXT    |         1 |              |    0 |               |
|     7 | contract_id      | STRING  |         1 |              |    2 |               |
|     8 | tx_id            | STRING  |         1 |              |    0 |               |


### db_config
|   cid | name    | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | version | TEXT   |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/burnchain/burnchain.sqlite
### burnchain_db_block_headers
|   cid | name              | type    |   notnull | dflt_value   |   pk | description   |
|------:|:------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | block_height      | INTEGER |         1 |              |    0 |               |
|     1 | block_hash        | TEXT    |         1 |              |    1 |               |
|     2 | parent_block_hash | TEXT    |         1 |              |    0 |               |
|     3 | num_txs           | INTEGER |         1 |              |    0 |               |
|     4 | timestamp         | INTEGER |         1 |              |    0 |               |


### burnchain_db_block_ops
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_hash | TEXT   |         1 |              |    0 |               |
|     1 | op         | TEXT   |         1 |              |    0 |               |
|     2 | txid       | TEXT   |         1 |              |    0 |               |


### affirmation_maps
|   cid | name            | type    |   notnull | dflt_value   |   pk | description   |
|------:|:----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | affirmation_id  | INTEGER |         0 |              |    1 |               |
|     1 | weight          | INTEGER |         1 |              |    0 |               |
|     2 | affirmation_map | TEXT    |         1 |              |    0 |               |


### sqlite_sequence
|   cid | name   | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | name   |        |         0 |              |    0 |               |
|     1 | seq    |        |         0 |              |    0 |               |


### anchor_blocks
|   cid | name         | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | reward_cycle | INTEGER |         0 |              |    1 |               |


### block_commit_metadata
|   cid | name                    | type    |   notnull | dflt_value   |   pk | description   |
|------:|:------------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | burn_block_hash         | TEXT    |         1 |              |    1 |               |
|     1 | txid                    | TEXT    |         1 |              |    2 |               |
|     2 | block_height            | INTEGER |         1 |              |    0 |               |
|     3 | vtxindex                | INTEGER |         1 |              |    0 |               |
|     4 | affirmation_id          | INTEGER |         1 |              |    0 |               |
|     5 | anchor_block            | INTEGER |         0 |              |    0 |               |
|     6 | anchor_block_descendant | INTEGER |         0 |              |    0 |               |


### overrides
|   cid | name            | type    |   notnull | dflt_value   |   pk | description   |
|------:|:----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | reward_cycle    | INTEGER |         1 |              |    1 |               |
|     1 | affirmation_map | TEXT    |         1 |              |    0 |               |


### db_config
|   cid | name    | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | version | TEXT   |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/burnchain/sortition/marf.sqlite
### marf_data
|   cid | name            | type    |   notnull |   dflt_value |   pk | description   |
|------:|:----------------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | block_id        | INTEGER |         0 |              |    1 |               |
|     1 | block_hash      | TEXT    |         1 |              |    0 |               |
|     2 | data            | BLOB    |         1 |              |    0 |               |
|     3 | unconfirmed     | INTEGER |         1 |              |    0 |               |
|     4 | external_offset | INTEGER |         1 |            0 |    0 |               |
|     5 | external_length | INTEGER |         1 |            0 |    0 |               |


### mined_blocks
|   cid | name       | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | block_id   | INTEGER |         0 |              |    1 |               |
|     1 | block_hash | TEXT    |         1 |              |    0 |               |
|     2 | data       | BLOB    |         1 |              |    0 |               |


### block_extension_locks
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_hash | TEXT   |         0 |              |    1 |               |


### schema_version
|   cid | name    | type    |   notnull |   dflt_value |   pk | description   |
|------:|:--------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | version | INTEGER |         1 |            1 |    0 |               |


### migrated_version
|   cid | name    | type    |   notnull |   dflt_value |   pk | description   |
|------:|:--------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | version | INTEGER |         1 |            1 |    0 |               |


### snapshots
|   cid | name                                | type    |   notnull | dflt_value   |   pk | description   |
|------:|:------------------------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | block_height                        | INTEGER |         1 |              |    0 | Bitcoin Block Height              |
|     1 | burn_header_hash                    | TEXT    |         1 |              |    0 |               |
|     2 | sortition_id                        | TEXT    |         1 |              |    1 |               |
|     3 | parent_sortition_id                 | TEXT    |         1 |              |    0 |               |
|     4 | burn_header_timestamp               | INT     |         1 |              |    0 |               |
|     5 | parent_burn_header_hash             | TEXT    |         1 |              |    0 |               |
|     6 | consensus_hash                      | TEXT    |         1 |              |    0 |               |
|     7 | ops_hash                            | TEXT    |         1 |              |    0 |               |
|     8 | total_burn                          | TEXT    |         1 |              |    0 |               |
|     9 | sortition                           | INTEGER |         1 |              |    0 |               |
|    10 | sortition_hash                      | TEXT    |         1 |              |    0 |               |
|    11 | winning_block_txid                  | TEXT    |         1 |              |    0 | BTC TX ID for the winning miner's bitcoin commitment. Sometimes there are two items returned here. If there are two, there could be two possible scenarios: 1) they're both the same TXID, or 2) one is a blank TXID filled with `0`'s and the other is the correct TXID.              |
|    12 | winning_stacks_block_hash           | TEXT    |         1 |              |    0 |               |
|    13 | index_root                          | TEXT    |         1 |              |    0 |               |
|    14 | num_sortitions                      | INTEGER |         1 |              |    0 |               |
|    15 | stacks_block_accepted               | INTEGER |         1 |              |    0 |               |
|    16 | stacks_block_height                 | INTEGER |         1 |              |    0 | Stacks Block Height              |
|    17 | arrival_index                       | INTEGER |         1 |              |    0 |               |
|    18 | canonical_stacks_tip_height         | INTEGER |         1 |              |    0 |               |
|    19 | canonical_stacks_tip_hash           | TEXT    |         1 |              |    0 |               |
|    20 | canonical_stacks_tip_consensus_hash | TEXT    |         1 |              |    0 |               |
|    21 | pox_valid                           | INTEGER |         1 |              |    0 |               |
|    22 | accumulated_coinbase_ustx           | TEXT    |         1 |              |    0 |               |
|    23 | pox_payouts                         | TEXT    |         1 |              |    0 |               |


### snapshot_transition_ops
|   cid | name          | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | sortition_id  | TEXT   |         0 |              |    1 |               |
|     1 | accepted_ops  | TEXT   |         1 |              |    0 |               |
|     2 | consumed_keys | TEXT   |         1 |              |    0 |               |


### leader_keys
|   cid | name             | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid             | TEXT    |         1 |              |    1 |               |
|     1 | vtxindex         | INTEGER |         1 |              |    0 |               |
|     2 | block_height     | INTEGER |         1 |              |    0 |               |
|     3 | burn_header_hash | TEXT    |         1 |              |    0 |               |
|     4 | sortition_id     | TEXT    |         1 |              |    2 |               |
|     5 | consensus_hash   | TEXT    |         1 |              |    0 |               |
|     6 | public_key       | TEXT    |         1 |              |    0 |               |
|     7 | memo             | TEXT    |         0 |              |    0 |               |


### block_commits
|   cid | name                | type    |   notnull | dflt_value   |   pk | description   |
|------:|:--------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid                | TEXT    |         1 |              |    1 | List of Bitcoin TX ID's from Stacks Miners' commits              |
|     1 | vtxindex            | INTEGER |         1 |              |    0 |               |
|     2 | block_height        | INTEGER |         1 |              |    0 | Bitcoin block height              |
|     3 | burn_header_hash    | TEXT    |         1 |              |    0 |               |
|     4 | sortition_id        | TEXT    |         1 |              |    2 |               |
|     5 | block_header_hash   | TEXT    |         1 |              |    0 |               |
|     6 | new_seed            | TEXT    |         1 |              |    0 |               |
|     7 | parent_block_ptr    | INTEGER |         1 |              |    0 |               |
|     8 | parent_vtxindex     | INTEGER |         1 |              |    0 |               |
|     9 | key_block_ptr       | INTEGER |         1 |              |    0 |               |
|    10 | key_vtxindex        | INTEGER |         1 |              |    0 |               |
|    11 | memo                | TEXT    |         0 |              |    0 |               |
|    12 | commit_outs         | TEXT    |         0 |              |    0 |               |
|    13 | burn_fee            | TEXT    |         1 |              |    0 | # of Sats spent by each miner for the block              |
|    14 | sunset_burn         | TEXT    |         1 |              |    0 |               |
|    15 | input               | TEXT    |         1 |              |    0 |               |
|    16 | apparent_sender     | TEXT    |         1 |              |    0 | List of Stacks Miners' Bitcoin addresses              |
|    17 | burn_parent_modulus | INTEGER |         1 |              |    0 |               |


### user_burn_support
|   cid | name                  | type    |   notnull | dflt_value   |   pk | description   |
|------:|:----------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid                  | TEXT    |         1 |              |    1 |               |
|     1 | vtxindex              | INTEGER |         1 |              |    0 |               |
|     2 | block_height          | INTEGER |         1 |              |    0 |               |
|     3 | burn_header_hash      | TEXT    |         1 |              |    0 |               |
|     4 | sortition_id          | TEXT    |         1 |              |    2 |               |
|     5 | address               | TEXT    |         1 |              |    0 |               |
|     6 | consensus_hash        | TEXT    |         1 |              |    0 |               |
|     7 | public_key            | TEXT    |         1 |              |    0 |               |
|     8 | key_block_ptr         | INTEGER |         1 |              |    0 |               |
|     9 | key_vtxindex          | INTEGER |         1 |              |    0 |               |
|    10 | block_header_hash_160 | TEXT    |         1 |              |    0 |               |
|    11 | burn_fee              | TEXT    |         1 |              |    0 |               |


### stack_stx
|   cid | name             | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid             | TEXT    |         1 |              |    1 |               |
|     1 | vtxindex         | INTEGER |         1 |              |    0 |               |
|     2 | block_height     | INTEGER |         1 |              |    0 |               |
|     3 | burn_header_hash | TEXT    |         1 |              |    2 |               |
|     4 | sender_addr      | TEXT    |         1 |              |    0 |               |
|     5 | reward_addr      | TEXT    |         1 |              |    0 |               |
|     6 | stacked_ustx     | TEXT    |         1 |              |    0 |               |
|     7 | num_cycles       | INTEGER |         1 |              |    0 |               |


### transfer_stx
|   cid | name             | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid             | TEXT    |         1 |              |    1 |               |
|     1 | vtxindex         | INTEGER |         1 |              |    0 |               |
|     2 | block_height     | INTEGER |         1 |              |    0 |               |
|     3 | burn_header_hash | TEXT    |         1 |              |    2 |               |
|     4 | sender_addr      | TEXT    |         1 |              |    0 |               |
|     5 | recipient_addr   | TEXT    |         1 |              |    0 |               |
|     6 | transfered_ustx  | TEXT    |         1 |              |    0 |               |
|     7 | memo             | TEXT    |         1 |              |    0 |               |


### missed_commits
|   cid | name                  | type   |   notnull | dflt_value   |   pk | description   |
|------:|:----------------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | txid                  | TEXT   |         1 |              |    1 |               |
|     1 | input                 | TEXT   |         1 |              |    0 |               |
|     2 | intended_sortition_id | TEXT   |         1 |              |    2 |               |


### db_config
|   cid | name    | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | version | TEXT   |         0 |              |    1 |               |


### epochs
|   cid | name               | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | start_block_height | INTEGER |         1 |              |    1 |               |
|     1 | end_block_height   | INTEGER |         1 |              |    0 |               |
|     2 | epoch_id           | INTEGER |         1 |              |    2 |               |
|     3 | block_limit        | TEXT    |         1 |              |    0 |               |
|     4 | network_epoch      | INTEGER |         1 |              |    0 |               |


### block_commit_parents
|   cid | name                      | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------------------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_commit_txid         | TEXT   |         1 |              |    1 |               |
|     1 | block_commit_sortition_id | TEXT   |         1 |              |    2 |               |
|     2 | parent_sortition_id       | TEXT   |         1 |              |    0 |               |


### delegate_stx
|   cid | name              | type    |   notnull | dflt_value   |   pk | description   |
|------:|:------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid              | TEXT    |         1 |              |    1 |               |
|     1 | vtxindex          | INTEGER |         1 |              |    0 |               |
|     2 | block_height      | INTEGER |         1 |              |    0 |               |
|     3 | burn_header_hash  | TEXT    |         1 |              |    2 |               |
|     4 | sender_addr       | TEXT    |         1 |              |    0 |               |
|     5 | delegate_to       | TEXT    |         1 |              |    0 |               |
|     6 | reward_addr       | TEXT    |         1 |              |    0 |               |
|     7 | delegated_ustx    | TEXT    |         1 |              |    0 |               |
|     8 | until_burn_height | INTEGER |         0 |              |    0 |               |


### ast_rule_heights
|   cid | name         | type               |   notnull | dflt_value   |   pk | description   |
|------:|:-------------|:-------------------|----------:|:-------------|-----:|:--------------|
|     0 | ast_rule_id  | INTEGER PRIMAR KEY |         1 |              |    0 |               |
|     1 | block_height | INTEGER            |         1 |              |    0 |               |


### __fork_storage
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | value_hash | TEXT   |         1 |              |    1 |               |
|     1 | value      | TEXT   |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/chainstate/mempool.sqlite
### mempool
|   cid | name                     | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid                     | TEXT    |         1 |              |    1 |               |
|     1 | origin_address           | TEXT    |         1 |              |    0 |               |
|     2 | origin_nonce             | INTEGER |         1 |              |    0 |               |
|     3 | sponsor_address          | TEXT    |         1 |              |    0 |               |
|     4 | sponsor_nonce            | INTEGER |         1 |              |    0 |               |
|     5 | tx_fee                   | INTEGER |         1 |              |    0 |               |
|     6 | length                   | INTEGER |         1 |              |    0 |               |
|     7 | consensus_hash           | TEXT    |         1 |              |    0 |               |
|     8 | block_header_hash        | TEXT    |         1 |              |    0 |               |
|     9 | height                   | INTEGER |         1 |              |    0 |               |
|    10 | accept_time              | INTEGER |         1 |              |    0 |               |
|    11 | tx                       | BLOB    |         1 |              |    0 |               |
|    12 | last_known_origin_nonce  | INTEGER |         0 |              |    0 |               |
|    13 | last_known_sponsor_nonce | INTEGER |         0 |              |    0 |               |
|    14 | fee_rate                 | NUMBER  |         0 |              |    0 |               |


### fee_estimates
|   cid | name     | type   |   notnull | dflt_value   |   pk | description   |
|------:|:---------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | txid     | TEXT   |         1 |              |    1 |               |
|     1 | fee_rate | NUMBER |         0 |              |    0 |               |


### schema_version
|   cid | name    | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | version | NUMBER |         0 |              |    1 |               |


### txid_bloom_counter
|   cid | name       | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | counts     | BLOB    |         1 |              |    0 |               |
|     1 | num_bins   | INTEGER |         1 |              |    0 |               |
|     2 | num_hashes | INTEGER |         1 |              |    0 |               |
|     3 | hasher     | BLOB    |         1 |              |    0 |               |


### removed_txids
|   cid | name   | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | txid   | TEXT   |         1 |              |    1 |               |


### randomized_txids
|   cid | name        | type   |   notnull | dflt_value   |   pk | description   |
|------:|:------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | txid        | TEXT   |         1 |              |    1 |               |
|     1 | hashed_txid | TEXT   |         1 |              |    0 |               |


### tx_blacklist
|   cid | name         | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | txid         | TEXT    |         1 |              |    1 |               |
|     1 | arrival_time | INTEGER |         1 |              |    0 |               |


### tx_blacklist_size
|   cid | name   | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | size   | INTEGER |         1 |              |    0 |               |


### nonces
|   cid | name    | type    |   notnull | dflt_value   |   pk | description   |
|------:|:--------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | address | TEXT    |         1 |              |    1 |               |
|     1 | nonce   | INTEGER |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/chainstate/vm/index.sqlite
### marf_data
|   cid | name            | type    |   notnull |   dflt_value |   pk | description   |
|------:|:----------------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | block_id        | INTEGER |         0 |              |    1 |               |
|     1 | block_hash      | TEXT    |         1 |              |    0 |               |
|     2 | data            | BLOB    |         1 |              |    0 |               |
|     3 | unconfirmed     | INTEGER |         1 |              |    0 |               |
|     4 | external_offset | INTEGER |         1 |            0 |    0 |               |
|     5 | external_length | INTEGER |         1 |            0 |    0 |               |


### mined_blocks
|   cid | name       | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | block_id   | INTEGER |         0 |              |    1 |               |
|     1 | block_hash | TEXT    |         1 |              |    0 |               |
|     2 | data       | BLOB    |         1 |              |    0 |               |


### block_extension_locks
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_hash | TEXT   |         0 |              |    1 |               |


### schema_version
|   cid | name    | type    |   notnull |   dflt_value |   pk | description   |
|------:|:--------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | version | INTEGER |         1 |            1 |    0 |               |


### migrated_version
|   cid | name    | type    |   notnull |   dflt_value |   pk | description   |
|------:|:--------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | version | INTEGER |         1 |            1 |    0 |               |


### block_headers
|   cid | name                       | type    |   notnull | dflt_value   |   pk | description   |
|------:|:---------------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | version                    | INTEGER |         1 |              |    0 |               |
|     1 | total_burn                 | TEXT    |         1 |              |    0 | Total amount of BTC spent, to date, to secure the Stacks Network              |
|     2 | total_work                 | TEXT    |         1 |              |    0 | Stacks block height?              |
|     3 | proof                      | TEXT    |         1 |              |    0 |               |
|     4 | parent_block               | TEXT    |         1 |              |    0 |               |
|     5 | parent_microblock          | TEXT    |         1 |              |    0 |               |
|     6 | parent_microblock_sequence | INTEGER |         1 |              |    0 |               |
|     7 | tx_merkle_root             | TEXT    |         1 |              |    0 |               |
|     8 | state_index_root           | TEXT    |         1 |              |    0 |               |
|     9 | microblock_pubkey_hash     | TEXT    |         1 |              |    0 |               |
|    10 | block_hash                 | TEXT    |         1 |              |    2 |               |
|    11 | index_block_hash           | TEXT    |         1 |              |    0 |               |
|    12 | block_height               | INTEGER |         1 |              |    0 | Stacks block height              |
|    13 | index_root                 | TEXT    |         1 |              |    0 |               |
|    14 | consensus_hash             | TEXT    |         1 |              |    1 |               |
|    15 | burn_header_hash           | TEXT    |         1 |              |    0 | Bitcoin block hash              |
|    16 | burn_header_height         | INT     |         1 |              |    0 | Bitcoin block height              |
|    17 | burn_header_timestamp      | INT     |         1 |              |    0 | Bitcoin block timestamp              |
|    18 | parent_block_id            | TEXT    |         1 |              |    0 |               |
|    19 | cost                       | TEXT    |         1 |              |    0 | Contains a JSON object with the following keys: "write_length", "write_count", "read_length", "read_count", "runtime"              |
|    20 | block_size                 | TEXT    |         1 |              |    0 |               |
|    21 | affirmation_weight         | INTEGER |         1 |              |    0 |               |


### payments
##### Note: if you look up items in this table using `stacks_block_height`, you may see sibling blocks where the data from one is not part of the main blockchain. To get around this, you can use the bitcoin height to get the `block_hash` or `index_block_hash` from another table (such as block_headers). Then you'll want to use that hash to get what you need from this table.
|   cid | name                     | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-------------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | address                  | TEXT    |         1 |              |    0 | Block winning miner's Stacks address              |
|     1 | block_hash               | TEXT    |         1 |              |    0 |               |
|     2 | consensus_hash           | TEXT    |         1 |              |    0 |               |
|     3 | parent_block_hash        | TEXT    |         1 |              |    0 |               |
|     4 | parent_consensus_hash    | TEXT    |         1 |              |    0 |               |
|     5 | coinbase                 | TEXT    |         1 |              |    0 | Number of newly minted micro STX              |
|     6 | tx_fees_anchored         | TEXT    |         1 |              |    0 | *?Total fees confirmed in anchor block?*              |
|     7 | tx_fees_streamed         | TEXT    |         1 |              |    0 | *?Total fees streamed?*              |
|     8 | stx_burns                | TEXT    |         1 |              |    0 | Number of micro STX burned (e.g., via BNS name-preorder function)              |
|     9 | burnchain_commit_burn    | INT     |         1 |              |    0 | Number of Sats spent by Winning miner for the block              |
|    10 | burnchain_sortition_burn | INT     |         1 |              |    0 | Number of Sats spent by all miners for the block              |
|    11 | miner                    | INT     |         1 |              |    0 | *?Number of miners for the block?*              |
|    12 | stacks_block_height      | INTEGER |         1 |              |    0 | Stacks block height              |
|    13 | index_block_hash         | TEXT    |         1 |              |    0 |               |
|    14 | vtxindex                 | INT     |         1 |              |    0 |               |
|    15 | recipient                | TEXT    |         0 |              |    0 | Block winning miner's Stacks reward address; *Question: this seems to be a duplicate of the `address` field... Could it be removed to marginally increase the node's efficiency?*              |


### user_supporters
|   cid | name           | type   |   notnull | dflt_value   |   pk | description   |
|------:|:---------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | address        | TEXT   |         1 |              |    1 |               |
|     1 | support_burn   | INT    |         1 |              |    0 |               |
|     2 | block_hash     | TEXT   |         1 |              |    2 |               |
|     3 | consensus_hash | TEXT   |         1 |              |    3 |               |


### db_config
|   cid | name     | type    |   notnull | dflt_value   |   pk | description   |
|------:|:---------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | version  | TEXT    |         1 |              |    0 |               |
|     1 | mainnet  | INTEGER |         1 |              |    0 |               |
|     2 | chain_id | INTEGER |         1 |              |    0 |               |


### staging_microblocks
|   cid | name                  | type   |   notnull | dflt_value   |   pk | description   |
|------:|:----------------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | anchored_block_hash   | TEXT   |         1 |              |    1 |               |
|     1 | consensus_hash        | TEXT   |         1 |              |    2 |               |
|     2 | index_block_hash      | TEXT   |         1 |              |    0 |               |
|     3 | microblock_hash       | TEXT   |         1 |              |    3 |               |
|     4 | parent_hash           | TEXT   |         1 |              |    0 |               |
|     5 | index_microblock_hash | TEXT   |         1 |              |    0 |               |
|     6 | sequence              | INT    |         1 |              |    0 |               |
|     7 | processed             | INT    |         1 |              |    0 |               |
|     8 | orphaned              | INT    |         1 |              |    0 |               |


### staging_microblocks_data
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_hash | TEXT   |         1 |              |    1 |               |
|     1 | block_data | BLOB   |         1 |              |    0 |               |


### invalidated_microblocks_data
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_hash | TEXT   |         1 |              |    1 |               |
|     1 | block_data | BLOB   |         1 |              |    0 |               |


### staging_blocks
|   cid | name                       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:---------------------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | anchored_block_hash        | TEXT   |         1 |              |    1 |               |
|     1 | parent_anchored_block_hash | TEXT   |         1 |              |    0 |               |
|     2 | consensus_hash             | TEXT   |         1 |              |    2 |               |
|     3 | parent_consensus_hash      | TEXT   |         1 |              |    0 |               |
|     4 | parent_microblock_hash     | TEXT   |         1 |              |    0 |               |
|     5 | parent_microblock_seq      | INT    |         1 |              |    0 |               |
|     6 | microblock_pubkey_hash     | TEXT   |         1 |              |    0 |               |
|     7 | height                     | INT    |         1 |              |    0 |               |
|     8 | attachable                 | INT    |         1 |              |    0 |               |
|     9 | orphaned                   | INT    |         1 |              |    0 |               |
|    10 | processed                  | INT    |         1 |              |    0 |               |
|    11 | commit_burn                | INT    |         1 |              |    0 |               |
|    12 | sortition_burn             | INT    |         1 |              |    0 |               |
|    13 | index_block_hash           | TEXT   |         1 |              |    0 |               |
|    14 | download_time              | INT    |         1 |              |    0 |               |
|    15 | arrival_time               | INT    |         1 |              |    0 |               |
|    16 | processed_time             | INT    |         1 |              |    0 |               |


### staging_user_burn_support
|   cid | name                | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | anchored_block_hash | TEXT   |         1 |              |    0 |               |
|     1 | consensus_hash      | TEXT   |         1 |              |    0 |               |
|     2 | address             | TEXT   |         1 |              |    0 |               |
|     3 | burn_amount         | INT    |         1 |              |    0 |               |
|     4 | vtxindex            | INT    |         1 |              |    0 |               |


### transactions
|   cid | name             | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | id               | INTEGER |         0 |              |    1 |               |
|     1 | txid             | TEXT    |         1 |              |    0 |               |
|     2 | index_block_hash | TEXT    |         1 |              |    0 |               |
|     3 | tx_hex           | TEXT    |         1 |              |    0 |               |
|     4 | result           | TEXT    |         1 |              |    0 |               |


### epoch_transitions
|   cid | name     | type   |   notnull | dflt_value   |   pk | description   |
|------:|:---------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_id | TEXT   |         0 |              |    1 |               |


### matured_rewards
|   cid | name                       | type    |   notnull | dflt_value   |   pk | description   |
|------:|:---------------------------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | address                    | TEXT    |         1 |              |    0 |               |
|     1 | recipient                  | TEXT    |         0 |              |    0 | The winning miner's reward address              |
|     2 | vtxindex                   | INTEGER |         1 |              |    0 |               |
|     3 | coinbase                   | TEXT    |         1 |              |    3 | Number of newly minted micro STX tokens; awarded to the recipient              |
|     4 | tx_fees_anchored           | TEXT    |         1 |              |    0 |               |
|     5 | tx_fees_streamed_confirmed | TEXT    |         1 |              |    0 |               |
|     6 | tx_fees_streamed_produced  | TEXT    |         1 |              |    0 |               |
|     7 | child_index_block_hash     | TEXT    |         1 |              |    2 |               |
|     8 | parent_index_block_hash    | TEXT    |         1 |              |    1 |               |


### burnchain_txids
|   cid | name             | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | index_block_hash | TEXT   |         0 |              |    1 |               |
|     1 | txids            | TEXT   |         1 |              |    0 |               |


### __fork_storage
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | value_hash | TEXT   |         1 |              |    1 |               |
|     1 | value      | TEXT   |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/chainstate/vm/clarity/marf.sqlite
### marf_data
|   cid | name            | type    |   notnull |   dflt_value |   pk | description   |
|------:|:----------------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | block_id        | INTEGER |         0 |              |    1 |               |
|     1 | block_hash      | TEXT    |         1 |              |    0 |               |
|     2 | data            | BLOB    |         1 |              |    0 |               |
|     3 | unconfirmed     | INTEGER |         1 |              |    0 |               |
|     4 | external_offset | INTEGER |         1 |            0 |    0 |               |
|     5 | external_length | INTEGER |         1 |            0 |    0 |               |


### mined_blocks
|   cid | name       | type    |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:--------|----------:|:-------------|-----:|:--------------|
|     0 | block_id   | INTEGER |         0 |              |    1 |               |
|     1 | block_hash | TEXT    |         1 |              |    0 |               |
|     2 | data       | BLOB    |         1 |              |    0 |               |


### block_extension_locks
|   cid | name       | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | block_hash | TEXT   |         0 |              |    1 |               |


### schema_version
|   cid | name    | type    |   notnull |   dflt_value |   pk | description   |
|------:|:--------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | version | INTEGER |         1 |            1 |    0 |               |


### migrated_version
|   cid | name    | type    |   notnull |   dflt_value |   pk | description   |
|------:|:--------|:--------|----------:|-------------:|-----:|:--------------|
|     0 | version | INTEGER |         1 |            1 |    0 |               |


### data_table
|   cid | name   | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | key    | TEXT   |         0 |              |    1 |               |
|     1 | value  | TEXT   |         0 |              |    0 |               |


### metadata_table
|   cid | name      | type   |   notnull | dflt_value   |   pk | description   |
|------:|:----------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | key       | TEXT   |         1 |              |    0 |               |
|     1 | blockhash | TEXT   |         0 |              |    0 |               |
|     2 | value     | TEXT   |         0 |              |    0 |               |




## /stacks-blockchain/mainnet/chainstate/estimates/cost_estimator_pessimistic.sqlite
### pessimistic_estimator
|   cid | name          | type   |   notnull | dflt_value   |   pk | description   |
|------:|:--------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | estimate_key  | TEXT   |         0 |              |    1 |               |
|     1 | current_value | NUMBER |         1 |              |    0 |               |
|     2 | samples       | TEXT   |         1 |              |    0 |               |




## /stacks-blockchain/mainnet/chainstate/estimates/fee_estimator_scalar_rate.sqlite
### scalar_fee_estimator
|   cid | name         | type   |   notnull | dflt_value   |   pk | description   |
|------:|:-------------|:-------|----------:|:-------------|-----:|:--------------|
|     0 | estimate_key | NUMBER |         0 |              |    1 |               |
|     1 | high         | NUMBER |         1 |              |    0 |               |
|     2 | middle       | NUMBER |         1 |              |    0 |               |
|     3 | low          | NUMBER |         1 |              |    0 |               |




