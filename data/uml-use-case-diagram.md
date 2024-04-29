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
c -up- UC3
c -up- UC4
c -up- UC6
c -up- UC7
c -up- UC10
c -up- UC8
c -up- UC9

t -- UC1
t -- UC2
t -- UC3
t -- UC4
t -- UC5
t -- UC8
t -- UC9

UC4 .> UC2 : << extends >>
UC4 .> UC1 : << extends >>
UC2 .> UC7 : << includes >>
@enduml
```

link to PlantUML demo server: www.plantuml.com/plantuml/png/TP3DRkiW48NtFCKe-rpTsFbnhg8eLr7x0ccxfp2EQJ54CEwFghvxeJR2JPFTfpddp67OUUAEkbOpZJK1MN3gs118vL2GiePnGTR17NBHe0FkWORHNgDxZWCn30xKIJGKHvwncEVcg14EtUCJ2lBmmG0wZu9xXCcDL0I-bw15uf8JdyJm_NvspJZenLX_KFYQTF34INbImW_MScmze95WBAbQ2HwlIwxvsFLVId1OeqCZ45fEw1JNoRhurTs4GklUmTOWcd0o-e1dBrx-A3YTd7q9gwtCBnbbKjNgwfaIYIkTVDNOTwjqVB0vWbQUBcnTdzzgykBq_t_P9_CmdGOk4rG9rem9c7Qdo4N6CkCyupBZAc4io5nb39kfxvWbA1AK2UO95Wcg124VTFYpZK7u1viDu1kXaHwssopDBaX5BwrwIHcXEudVsYwOkbP_0G00

![image](https://github.com/vestr-at-work/mff-uk-introduction-to-software-engineering/blob/main/data/uml-usecase-diagram.png)