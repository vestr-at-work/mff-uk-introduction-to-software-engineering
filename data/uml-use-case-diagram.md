```
@startuml
left to right direction
actor Teacher as t
actor Clerk as c
actor Student as s

rectangle Subjects {
  usecase "Edit subject metadata" as UC1
  usecase "Edit subject" as UC2
  usecase "View subject statistics" as UC3
  usecase "Send notifications" as UC4
  usecase "Add reference materials" as UC5
  usecase "View history of changes of subject" as UC6
  usecase "Approve modifications of subjects" as UC7
  usecase "View subject details" as UC8
  usecase "Filtering list of subjects" as UC9
  usecase "Add new subject" as UC10
}
s -- UC3
s -- UC8
s -- UC9

c -up- UC2
c -up- UC4
c -up- UC6
c -up- UC7
c -up- UC10
c -up- UC8
c -up- UC9

t -- UC1
t -- UC2
t -- UC4
t -- UC5
t -- UC8
t -- UC9

UC4 .> UC2 : << extends >>
UC4 .> UC1 : << extends >>
UC2 .> UC7 : << includes >>
@enduml
```
link to PlantUML demo server: www.plantuml.com/plantuml/png/TP3RRk8m48Rl_HGZxbcHS22i46A5Tb-0RUzTUqBSEZQo9psewhlNRc8vfN3tPVvlPZpPU-AEkbOpZJK1MN3gr118vL2GiePnGTR1V-IYGGVS0msbWqRt50jYA1ofasWebZnZiP-RaqOuTW-FuSF3EmFeF0hk4IP_fIBmVGGj4fUS-2GstnsAM-AGb-FyNk5Boi4J9-L92J-eyx5wH2F1M5Ar4ZnUbwp5sFeZ9JYiqQ4H22qdT8hhf2v_x6x2GklUmDOWcd0o-e0NBrvzMt0-E_kCq5gPNpBgIQlMDy-KI5pfv5LZxv_IyS7c15fvkZ9rStchoOFJ_v-n3-PXEWqyJr0bs30cODgT8vSP5nbN6TSPYrdcAcCOH_tW8a6PO95WcQ1A4Df23hzsqOVViDq2lX8QwM6tor5n9IhxQDr7oWZTIVpAza7gMlq9

![image](https://github.com/vestr-at-work/mff-uk-introduction-to-software-engineering/assets/32305565/720e3fb5-081a-4082-a788-c9b0088de1d3)


