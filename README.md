# BSC Node Block Monitor
Bash script that compares local geth block number to BSCscan.com's API. If out of sync, it will monitor the log file and display the "Age" from live block from the log. This script is useful when trying to monitor or sync a BSC node. If you are in sync with the latest block, then your node will be AHEAD of the api which lags behind a couple blocks.

You will need to get a free API key from BSCScan.com
- https://bscscan.com/myapikey

Setup:
- sudo apt install jq - requires JQ to be installed for parsing Json from BscScan API
- sudo chmod +x watchBlocksLive - needs execute rights
- Script assumes Geth is in the same directory, if not edit line 42 (./geth attach http://127.0.0.1:8545 --exec 'eth.blockNumber')

Run:
- ./watchBlocksLive
