# BSC Node Block Monitor
Bash script that compares local geth block number to BSCscan.com's API. If the local node is not a full node yet, it will monitor the log file + Geth to display data every few seconds. This script is useful when trying to monitor or sync a BSC node. Script also has some error handling built into it. See screenshots below.

## You will need to get a free API key from BSCScan.com
- https://bscscan.com/myapikey

### Setup:
- ```sudo apt install jq``` - requires JQ to be installed for parsing Json from BscScan API
- ```sudo chmod +x watchBlocksLive```
- Add ```BSCSCANAPIKEY``` from https://bscscan.com/myapikey

### Run:
- ```./watchBlocksLive```

* Result if the node hasn't converted into a full node yet, it will monitor the log for the age-from-live-block variable without clutter.
> ![2021-05-04_14-28-18](https://user-images.githubusercontent.com/28745523/117052143-5f392180-ace5-11eb-9fca-c411feffc51b.jpg)

* You're in sync and ahead of the BSCScan.com
> ![image](https://user-images.githubusercontent.com/28745523/117009521-da84de00-acb9-11eb-90a7-8e5e4a1abe48.png)
