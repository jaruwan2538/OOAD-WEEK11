# OOAD-WEEK11
State Diagram

ภาพที่ 1
```
@startuml
state "Water vapor" as WaterVapor
state "Liquid Water" as LiquidWater 
state "lce or Frose" as lceorFrose
  plasma --> WaterVapor : deionization
 WaterVapor -l-> LiquidWater:Condensation
 WaterVapor-r->lceorFrose:deposition
LiquidWater-->lceorFrose:freezing
@enduml
```
![](http://www.plantuml.com/plantuml/img/PP0x3i8m38PtdyBgdWjag2eXCJ7371638gLnSLA6dhucKKKGY-tV_loGfroSb7MEe44X76vg1TzkOHdGPQpw-f47SGclDVXMg4XBjCO3YdT25ZmBPwgG9bYg1CGbkZmxD6RivgD5Ju5Js5nH1tt9H4MxFVR4oLFAVwGHCtvNMKyBvr2XhjlyC0yXsa9w0WBeRG0J9QyVsG40)

ภาพที่ 2
```
@startuml

note right of Active : this is a short\nnote

note left of Inactive
  A note can also
  be defined on
  several lines
end note
@enduml
```
![](http://www.plantuml.com/plantuml/img/BOv13iCm20Jll6BVqLDox1zweJ6kBL4i6PBtXrgLEC3i8EtcmJFEhnAHZH3C_cc1KR4VqI_10z6w8uVXRSnusS_xsofroK_ZfHEmOoK76rXz97aBYjHkKZ0iRvTB9YiqaPDOMH-qvPP5RW00)

ภาพที่ 3การทำงานของหลอดไฟ
```
@startuml

[*] --> off
off --> [*]:OutOfOrder

off-->on:turnon
on-->off:turnoff
on-->[*]:outOfOrder
@enduml
```
![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuUAArefLqDMrKyXFI-C2OZ0RA6RbNrhYd-PVb99Qn0KI1mhdvrcLb1RbvUTnvUU1k6bf43v88qW0f2iVeSiXDIy5Q0C0)





ภาพที่ 4 การจำลองการทำงานของลิฟท์
```
@startuml
[*] -r-> Idle:TurnOn
Idle-r->MoveUp:WantUpGoUp
MoveUp-->Reach:DesiredFloorReached
Reach-down->Idle:Floor>1/GoDown
Idle-->MoveDown:WantDownGoDown
MoveDown-->Idle:Floor=1
MoveDown-->Reach:Floor<>1&\nDesiredFloorReached
Idle-up->[*]:Turnoff
@enduml

```
![](http://www.plantuml.com/plantuml/img/ROyn2y8m48Nt_8fE3i8XMOE63iNY889O7DGXc2iMOYwahVvzcuj21wUx-nxtxbxP3oOEuzE9o_9MG0HTxAn3THgZFtYH-WJtzC8cgBFnGnDgQeB8140VqTmVgiA-YsYtZYWoGIkuWgMt1ysch6gvggcQO3RFtcbczzHyvH-7-VP6pdc-pS9QoyNL_tk3pum1z9IGSr7RYXAzJQa_)



ภาพที่ 5 computer อยู่ในสถานะ shut down
```
@startuml
[*] -r-> Ready
Ready-r->off:SwitchIsTurnedOff
Ready : do/waitingFor
Ready : instructions
off : do/ShutDownThe
off :Power

off -r-> [*]
```
![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuOhMYbNGBTArKmXAJKofv0AJ87v-MffLS7bcINA6Pt58QL5UQef_MXf4Mi5A8ILVlpmnioGpBzqjlmWkcfbNN59KcboIcPzNp0Kq0A8mEAEqn2M_F2ya8nKY691Vdbh41MQ3RGOwWOlB8JKl1UGU0000)
