# Parse du_stats_XXX.txt for each UE Time DL/UL Tput, BLER percent and MCS

online tool => https://dustinchen26.github.io/parse_du5

## Example
```
Please paste the whole du_stats_XXX.txt content below, then it will parse the DL/UL Tput, BLER, MCS.
formula 1: DL-BLER = DL-RETX / (DL-RETX + DL-TX)
formula 2: UL-BLER = UL-CRC-FAIL / (UL-CRC-SUCC + UL-CRC-FAIL)

【Input】
#############################################################################################
                       GNB DU Statistics  Thu Feb 29 06:13:22 2024
#############################################################################################
---------------------------------------------------------------------------------------------
                       UE Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID     BEAM-ID   CSIRS-PORT   PCELL-ID  DL-PKT-RX   DL-TPT    UL-PKT-TX UL-TPT    DL-LC-1   DL-LC-2   DL-LC-3   DL-LC-4   UL-LC-1   UL-LC-2   UL-LC-3   UL-LC-4   DL-PADDING  UL-PADDING  DL-PRB    UL-PRB    NUM-SR    NUM-BSR-TMR    SCELL-ACT-CE   TA-CE     NUM-TA-TMR   TA        
17093     0         0            1         0           0.0000    0         0.0000    0.0000    0.0000    0.0000    0.0000    0.0000    0.0000    0.0000    0.0000    0.0000      0.0000      0         53        303       0              0              0         0            0         
17122     0         0            1         3837        0.1396    7669      8.6189    0.2185    0.0000    0.0000    0.0000    8.6346    0.0000    0.0000    0.0000    0.1110      6.0618      1         79        386       0              0              857       0            27        
17643     0         0            1         3693        0.1350    7337      8.2637    0.2046    0.0000    0.0000    0.0000    8.2761    0.0000    0.0000    0.0000    0.1033      5.8957      1         75        4         0              0              856       0            32        
---------------------------------------------------------------------------------------------
                       UE MAC-Scheduler Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID   CELL-ID   ON-SUL   DL-NEWTX  DL-RETX   ACK-TB[0] NACK-TB[0]  BLER-TB[0]  DTX-TB[0] ACK-TB[1] NACK-TB[1]  BLER-TB[1]  DTX-TB[1] DL-MCS  DL-RI-PER   DL-CQI-PER     UL-NEWTX  UL-RETX  UL-CRC-SUCC   UL-CRC-FAIL   UL-CRC-DTX   UL-CQI  UL-MCS  UL-RI   NUM-BSR   SHR-BSR ST-BSR  LNG-BSR LT-BSR  NUM-CSI   NUM-SRS   UL-BLER   
17093   1         0        0         0         0         0           0           0         0         0           0           0         0       0           0              1529      4471     0             6001          0            10      0       0       0         0       0       0       0       0         0         100       
17122   1         0        2755      0         2752      0           0           0         0         0           0           0         9       1           8              5807      155      5804          159           0            10      8       0       4379      1302    0       3077    0       0         0         2         
17643   1         0        2804      0         2805      0           0           0         0         0           0           0         9       1           8              5908      82       5908          83            0            10      8       0       4495      1349    0       3146    0       0         0         1         

【Output】
GNB DU Statistics  Thu Feb 29 06:13:22 2024
GNB DU Statistics
UE-ID=17093   DL-TPT=0.0000    UL-TPT=0.0000  
UE-ID=17122   DL-TPT=0.1396    UL-TPT=8.6189  
UE-ID=17643   DL-TPT=0.1350    UL-TPT=8.2637  
UE-ID=17093   DL-TX=0       DL-RETX=0       DL-BLER=NaN     DL-BLER-percent=0       DL-MCS=0       UL-CRC-SUCC=0       UL-CRC-FAIL=6001    UL-BLER=1.0000  UL-BLER-percent=100     UL-MCS=0       
UE-ID=17122   DL-TX=2755    DL-RETX=0       DL-BLER=0.0000  DL-BLER-percent=0       DL-MCS=9       UL-CRC-SUCC=5804    UL-CRC-FAIL=159     UL-BLER=0.0267  UL-BLER-percent=2       UL-MCS=8       
UE-ID=17643   DL-TX=2804    DL-RETX=0       DL-BLER=0.0000  DL-BLER-percent=0       DL-MCS=9       UL-CRC-SUCC=5908    UL-CRC-FAIL=83      UL-BLER=0.0139  UL-BLER-percent=1       UL-MCS=8    
```