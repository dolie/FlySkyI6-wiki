Telemetry values Error and SNR can be used as channel input to provide signal quality information back to FC/OSD without additional hardware. 
Configuration can be made in the aux-channel assignment menu. 
Selecting Err will use error rate. Channel value is calculated as:

Error = 0 -> channel value 2000;

Error = 100 ->  channel value 1000;


In case of SNR a logarithmic scale is being used - highest SNR seen since start is being used as reference signal.


![](https://github.com/qba667/FlySkyI6/raw/master/doc/ch_val_from_snr.png)
