@startuml
left to right direction
actor Teacher as t
actor Clerk as c

package Subjects {
  usecase "Edit subject metadata" as UC1
  usecase "Edit subject" as UC2
}
c --> UC2
t --> UC1
@enduml

link to PlantUML demo server: https://www.plantuml.com/plantuml/uml/TOvB3e9044JtVOeAUnPu04D2F85wWBQdXP4FPgPO6UykA5jtbVVw9LrdQk8o3ZBudU2C5DkE236vCSwJg75EkBXQvmcQmHqrWwT-0oRoLEkrTPoNssFjCbu2BDbDiwCuXKZadyBerA3KOaklJVNlSFS7UOkXB8_VpNrLKliKrhS_

![image](https://github.com/vestr-at-work/mff-uk-introduction-to-software-engineering/assets/32305565/9ad1818f-494a-4648-9113-307a2ab5d057)
