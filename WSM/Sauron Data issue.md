---
created: 2022-08-31T21:51:05-04:00
updated: 2022-08-31T21:51:05-04:00
---
select distinct alias from cloud_sec.saurons where  
                                    alias in  
('SAURON-321180', 'SAURON-321065', 'SAURON-321152', 'SAURON-321222'  
'SAURON-321232','SAURON-321144' , 'SAURON-321103', 'SAURON-321221' , 'SAURON-321223'  
, ' SAURON-320961'  
);

Result: 
SAURON-321180
SAURON-321223
SAURON-321221
SAURON-321065
SAURON-321152
SAURON-321144
SAURON-321103

watchlist: 
![[attachments/Pasted image 20220831215106.png]]

Sauron IDs  SAURON- 321152, SAURON- 320961, SAURON-321222 three issues are missing in DW, two go to StayPuft, one goes to WSM with status as carry over