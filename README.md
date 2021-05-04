# BSC Node Block Monitor
Bash script that compares local geth block number to BSCscan.com's API. If the local node is not a full node yet, it will monitor the log file and display the "Age" from live block from the log every few seconds. This script is useful when trying to monitor or sync a BSC node. Script also has some error handling built into it. See screenshots below.

## You will need to get a free API key from BSCScan.com
- https://bscscan.com/myapikey

### Setup:
- ```sudo apt install jq``` - requires JQ to be installed for parsing Json from BscScan API
- ```sudo chmod +x watchBlocksLive```
- Add ```BSCSCANAPIKEY``` from https://bscscan.com/myapikey

### Run:
- ```./watchBlocksLive```

<p align="center">
  Result if the node hasn't converted into a full node yet, it will monitor the log for the age-from-live-block variable without clutter.
  <img src="https://user-images.githubusercontent.com/28745523/117009256-8974ea00-acb9-11eb-8aa9-5bab9edbbf40.png">
</p>

<p align="center">
  You were a full node, but now behind in blocks
  <img src="https://user-images.githubusercontent.com/28745523/117009362-a7dae580-acb9-11eb-9c51-25fb5ad8a25a.png">
</p>

<p align="center">
  You're in sync and ahead of the BSCScan.com
  <img src="https://user-images.githubusercontent.com/28745523/117009521-da84de00-acb9-11eb-90a7-8e5e4a1abe48.png">
</p>
