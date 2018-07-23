
* cotton.conf: contains configuration settings for cottond or cotton-qt
* cottond.pid: stores the process id of cottond while running
* blocks/blk000??.dat: block data (custom, 128 MiB per file); since 0.8.0
* blocks/rev000??.dat; block undo data (custom); since 0.8.0 (format changed since pre-0.8)
* blocks/index/*; block index (LevelDB); since 0.8.0
* chainstate/*; block chain state database (LevelDB); since 0.8.0
* database/*: BDB database environment; only used for wallet since 0.8.0
* db.log: wallet database log file
* debug.log: contains debug information and general logging generated by cottond or cotton-qt
* fee_estimates.dat: stores statistics used to estimate minimum transaction fees and priorities required for confirmation: since 0.10.0
* budget.dat: stores data for budget objects
* masternode.conf: contains configuration settings for remote masternodes
* mncache.dat: stores data for masternode list
* mnpayments.dat: stores data for masternode payments
* peers.dat: peer IP address database (custom format); since 0.7.0
* wallet.dat: personal wallet (BDB) with keys and transactions

Only used in pre-0.8.0
---------------------
* blktree/*; block chain index (LevelDB); since pre-0.8, replaced by blocks/index/* in 0.8.0
* coins/*; unspent transaction output database (LevelDB); since pre-0.8, replaced by chainstate/* in 0.8.0

Only used before 0.8.0
---------------------
* blkindex.dat: block chain index database (BDB); replaced by {chainstate/*,blocks/index/*,blocks/rev000??.dat} in 0.8.0
* blk000?.dat: block data (custom, 2 GiB per file); replaced by blocks/blk000??.dat in 0.8.0

Only used before 0.7.0
---------------------
* addr.dat: peer IP address database (BDB); replaced by peers.dat in 0.7.0