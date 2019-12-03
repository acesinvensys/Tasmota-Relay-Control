# Tasmota-Relay-Control
Tasmota Sonoff Relay Timer conrol will on off relay on boot

Rule1 
on system#boot do
Backlog  stat/backdoor/POWER1 off ; Backlog   stat/backdoor/POWER2 off ;
 ;Backlog   stat/backdoor/POWER3 off ;
 ; Backlog  stat/backdoor/POWER4 off ;
Backlog delay 10;

Backlog stat/backdoor/POWER1 on ;Backlog   stat/backdoor/POWER2 off ;
 ;Backlog   stat/backdoor/POWER3 off ;
 ; Backlog  stat/backdoor/POWER4 off ;
Backlog delay 99;
Backlog  stat/backdoor/POWER2 on ; Backlog  stat/backdoor/POWER1 off ;
 ;Backlog   stat/backdoor/POWER3 off ;
 ; Backlog  stat/backdoor/POWER4 off ;
Backlog  delay 99;

Backlog  stat/backdoor/POWER3 on ;Backlog   stat/backdoor/POWER1 off ;
 ;Backlog   stat/backdoor/POWER2 off ;
 ;Backlog   stat/backdoor/POWER4 off ;
Backlog  delay 99;

Backlog  stat/backdoor/POWER4 on ; Backlog   stat/backdoor/POWER1 off ;
 ; Backlog   stat/backdoor/POWER2 off ;
 ; Backlog   stat/backdoor/POWER3 off ;
delay 99;


Rule on system#boot do Backlog stat/backdoor/POWER1 off ;  Backlog  stat/backdoor/POWER2 off ; Backlog   stat/backdoor/POWER3 off ; Backlog  stat/backdoor/POWER4 off ; Backlog delay 99; Backlog stat/backdoor/POWER1 on ;   endon
