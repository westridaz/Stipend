# Stipend
Shell script to install a [Stipend Masternode](http://stipend.me) on a Linux server running Ubuntu 16.04. Use it on your own risk.  
The script will install Stipend version **1.0.8**
***

## Installation:  

wget -q https://raw.githubusercontent.com/zoldur/Stipend/master/stipend_install.sh  
bash stipend_install.sh
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Stipend Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **5000** SPD to **MN1**.  
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**  
***

## Usage:  
```
stipendd masternode status
stipendd getinfo
```  
Also, if you want to check/start/stop **Stipend** , run one of the following commands as **root**:
``` 
systemctl status Stipend #To check the service is running.  
systemctl start Stipend #To start Stipend service.  
systemctl stop Stipend #To stop Stipend service.  
systemctl is-enabled Stipend #To check whetether Stipend service is enabled on boot or not.  
```  
***

## Donations:
  
Any donation is highly appreciated  

**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LXrWbfeejNQRmRvtzB6Te8yns93Tu3evGf  
