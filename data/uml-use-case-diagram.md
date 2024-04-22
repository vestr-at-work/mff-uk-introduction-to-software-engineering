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
t -- UC4
t -- UC5
t -- UC8
t -- UC9

UC4 .> UC2 : << extends >>
UC4 .> UC1 : << extends >>
@enduml

link to PlantUML demo server: www.plantuml.com/plantuml/png/TP3BJiCm44Nt_efHzqMqz96YgYggu0SAx8qzQGoE7NacF8JuTs8rbbDATqTpxznvR8bbuBQsmcB9m1w2ELGCsWHKRBmJKh4Fy8XILHX04d1VsbaCRx6W-iAUMusEOuc4YFtI7Ip2ldrvHSK4tmAW9LII44RtsZ3GKO8QMMh9SXIRdtQJIyPUdmxrPuCVIGTYoOROAEgjDqFh7fq6vzcKHibuNNBDXguxhI5WYG6TGgWbOp3I9klyR7PbY7tu0b-2ghgJaIAURhmu6T0qmRztqLxdJGOzQTJoufaQMHgRVCNGzs1iNDWTm1hYVr9NVszrEJZz_rhy28BnE3umGP5W9OI2STj4dcQSPLnaN2QCgPcBZ5qS7uCd2MO9vWcA19sxq-5g4uV3BQpNW9-CJXDiDbcQd4dR3jhQ_W80

![image](https://github.com/vestr-at-work/mff-uk-introduction-to-software-engineering/assets/32305565/e9bd8e22-6d7b-4666-9da1-54cf15c63675)

