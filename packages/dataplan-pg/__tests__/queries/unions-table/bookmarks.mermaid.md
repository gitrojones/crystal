```mermaid
graph TD
    classDef path fill:#eee,stroke:#000,color:#000
    classDef plan fill:#fff,stroke-width:3px,color:#000
    classDef itemplan fill:#fff,stroke-width:6px,color:#000
    classDef sideeffectplan fill:#f00,stroke-width:6px,color:#000
    classDef bucket fill:#f6f6f6,color:#000,stroke-width:6px

    %% subgraph fields
    P1{{"~"}}:::path
    P2{{">personByPersonId"}}:::path
    P3([">pe…nId>personId"]):::path
    %% P2 -.-> P3
    P4([">pe…nId>username"]):::path
    %% P2 -.-> P4
    P5[/">pe…nId>personBookmarksList"\]:::path
    P6>">pe…nId>personBookmarksList[]"]:::path
    P5 -.- P6
    P7([">pe…nId>pe…t[]>id"]):::path
    %% P6 -.-> P7
    P8{{">pe…nId>pe…t[]>person"}}:::path
    P9([">pe…nId>pe…t[]>person>username"]):::path
    %% P8 -.-> P9
    %% P6 -.-> P8
    P10{{">pe…nId>pe…t[]>bookmarkedEntity"}}:::path
    P11([">pe…nId>pe…t[]>bo…ity>personId"]):::path
    %% P10 -.-> P11
    P12([">pe…nId>pe…t[]>bo…ity>username"]):::path
    %% P10 -.-> P12
    P13([">pe…nId>pe…t[]>bo…ity>postId"]):::path
    %% P10 -.-> P13
    P14{{">pe…nId>pe…t[]>bo…ity>author"}}:::path
    P15([">pe…nId>pe…t[]>bo…ity>author>username"]):::path
    %% P14 -.-> P15
    %% P10 -.-> P14
    P16([">pe…nId>pe…t[]>bo…ity>body"]):::path
    %% P10 -.-> P16
    P17([">pe…nId>pe…t[]>bo…ity>commentId"]):::path
    %% P10 -.-> P17
    P18{{">pe…nId>pe…t[]>bo…ity>author"}}:::path
    P19([">pe…nId>pe…t[]>bo…ity>author>username"]):::path
    %% P18 -.-> P19
    %% P10 -.-> P18
    P20{{">pe…nId>pe…t[]>bo…ity>post"}}:::path
    P21([">pe…nId>pe…t[]>bo…ity>post>body"]):::path
    %% P20 -.-> P21
    %% P10 -.-> P20
    P22([">pe…nId>pe…t[]>bo…ity>body"]):::path
    %% P10 -.-> P22
    %% P6 -.-> P10
    %% P2 -.-> P5
    %% P1 -.-> P2
    %% end

    %% define plans
    __Value_3["__Value[_3∈0]<br /><context>"]:::plan
    __Value_5["__Value[_5∈0]<br /><rootValue>"]:::plan
    __TrackedObject_6["__TrackedObject[_6∈0]"]:::plan
    InputStaticLeaf_7["InputStaticLeaf[_7∈0]"]:::plan
    PgSelect_8[["PgSelect[_8∈0]<br /><people>"]]:::plan
    First_12["First[_12∈0]"]:::plan
    PgSelectSingle_13["PgSelectSingle[_13∈0]<br /><people>"]:::plan
    PgClassExpression_14["PgClassExpression[_14∈0]<br /><__people__.#quot;person_id#quot;>"]:::plan
    PgClassExpression_15["PgClassExpression[_15∈0]<br /><__people__.#quot;username#quot;>"]:::plan
    __Item_21>"__Item[_21∈1]<br /><_100>"]:::itemplan
    PgSelectSingle_22["PgSelectSingle[_22∈1]<br /><person_bookmarks>"]:::plan
    PgClassExpression_23["PgClassExpression[_23∈1]<br /><__person_b...rks__.#quot;id#quot;>"]:::plan
    First_29["First[_29∈1]"]:::plan
    PgSelectSingle_30["PgSelectSingle[_30∈1]<br /><people>"]:::plan
    PgClassExpression_31["PgClassExpression[_31∈1]<br /><__people__.#quot;username#quot;>"]:::plan
    PgClassExpression_32["PgClassExpression[_32∈1]<br /><__person_b...ed_entity#quot;>"]:::plan
    PgClassExpression_33["PgClassExpression[_33∈1]<br /><(__person_...person_id#quot;>"]:::plan
    PgClassExpression_34["PgClassExpression[_34∈1]<br /><(__person_....#quot;post_id#quot;>"]:::plan
    PgClassExpression_35["PgClassExpression[_35∈1]<br /><(__person_...omment_id#quot;>"]:::plan
    List_36["List[_36∈1]<br /><_33,_34,_35>"]:::plan
    PgPolymorphic_37["PgPolymorphic[_37∈1]"]:::plan
    First_42["First[_42∈1]"]:::plan
    PgSelectSingle_43["PgSelectSingle[_43∈1]<br /><people>"]:::plan
    PgClassExpression_44["PgClassExpression[_44∈1]<br /><__people__.#quot;person_id#quot;>"]:::plan
    PgClassExpression_45["PgClassExpression[_45∈1]<br /><__people__.#quot;username#quot;>"]:::plan
    First_50["First[_50∈1]"]:::plan
    PgSelectSingle_51["PgSelectSingle[_51∈1]<br /><posts>"]:::plan
    PgClassExpression_52["PgClassExpression[_52∈1]<br /><__posts__.#quot;post_id#quot;>"]:::plan
    First_58["First[_58∈1]"]:::plan
    PgSelectSingle_59["PgSelectSingle[_59∈1]<br /><people>"]:::plan
    PgClassExpression_60["PgClassExpression[_60∈1]<br /><__people__.#quot;username#quot;>"]:::plan
    PgClassExpression_61["PgClassExpression[_61∈1]<br /><__posts__.#quot;body#quot;>"]:::plan
    First_66["First[_66∈1]"]:::plan
    PgSelectSingle_67["PgSelectSingle[_67∈1]<br /><comments>"]:::plan
    PgClassExpression_68["PgClassExpression[_68∈1]<br /><__comments...omment_id#quot;>"]:::plan
    First_74["First[_74∈1]"]:::plan
    PgSelectSingle_75["PgSelectSingle[_75∈1]<br /><people>"]:::plan
    PgClassExpression_76["PgClassExpression[_76∈1]<br /><__people__.#quot;username#quot;>"]:::plan
    Access_79["Access[_79∈0]<br /><_3.pgSettings>"]:::plan
    Access_80["Access[_80∈0]<br /><_3.withPgClient>"]:::plan
    Object_81["Object[_81∈0]<br /><{pgSettings,withPgClient}>"]:::plan
    First_82["First[_82∈1]"]:::plan
    PgSelectSingle_83["PgSelectSingle[_83∈1]<br /><posts>"]:::plan
    PgClassExpression_84["PgClassExpression[_84∈1]<br /><__posts__.#quot;body#quot;>"]:::plan
    PgClassExpression_85["PgClassExpression[_85∈1]<br /><__comments__.#quot;body#quot;>"]:::plan
    Map_86["Map[_86∈1]<br /><_22:{#quot;0#quot;:1}>"]:::plan
    List_87["List[_87∈1]<br /><_86>"]:::plan
    Map_88["Map[_88∈1]<br /><_22:{#quot;0#quot;:3,#quot;1#quot;:4}>"]:::plan
    List_89["List[_89∈1]<br /><_88>"]:::plan
    Map_90["Map[_90∈1]<br /><_51:{#quot;0#quot;:1}>"]:::plan
    List_91["List[_91∈1]<br /><_90>"]:::plan
    Map_92["Map[_92∈1]<br /><_22:{#quot;0#quot;:6,#quot;1#quot;:7,#quot;2#quot;:8}>"]:::plan
    List_93["List[_93∈1]<br /><_92>"]:::plan
    Map_94["Map[_94∈1]<br /><_67:{#quot;0#quot;:1}>"]:::plan
    List_95["List[_95∈1]<br /><_94>"]:::plan
    Map_96["Map[_96∈1]<br /><_67:{#quot;0#quot;:2}>"]:::plan
    List_97["List[_97∈1]<br /><_96>"]:::plan
    Map_98["Map[_98∈1]<br /><_22:{#quot;0#quot;:10,#quot;1#quot;:11,#quot;2#quot;:12,#quot;3#quot;:13}>"]:::plan
    List_99["List[_99∈1]<br /><_98>"]:::plan
    Access_100["Access[_100∈0]<br /><_12.0>"]:::plan

    %% plan dependencies
    __Value_5 --> __TrackedObject_6
    Object_81 --> PgSelect_8
    InputStaticLeaf_7 --> PgSelect_8
    PgSelect_8 --> First_12
    First_12 --> PgSelectSingle_13
    PgSelectSingle_13 --> PgClassExpression_14
    PgSelectSingle_13 --> PgClassExpression_15
    Access_100 ==> __Item_21
    __Item_21 --> PgSelectSingle_22
    PgSelectSingle_22 --> PgClassExpression_23
    List_87 --> First_29
    First_29 --> PgSelectSingle_30
    PgSelectSingle_30 --> PgClassExpression_31
    PgSelectSingle_22 --> PgClassExpression_32
    PgSelectSingle_22 --> PgClassExpression_33
    PgSelectSingle_22 --> PgClassExpression_34
    PgSelectSingle_22 --> PgClassExpression_35
    PgClassExpression_33 --> List_36
    PgClassExpression_34 --> List_36
    PgClassExpression_35 --> List_36
    PgClassExpression_32 --> PgPolymorphic_37
    List_36 --> PgPolymorphic_37
    List_89 --> First_42
    First_42 --> PgSelectSingle_43
    PgSelectSingle_43 --> PgClassExpression_44
    PgSelectSingle_43 --> PgClassExpression_45
    List_93 --> First_50
    First_50 --> PgSelectSingle_51
    PgSelectSingle_51 --> PgClassExpression_52
    List_91 --> First_58
    First_58 --> PgSelectSingle_59
    PgSelectSingle_59 --> PgClassExpression_60
    PgSelectSingle_51 --> PgClassExpression_61
    List_99 --> First_66
    First_66 --> PgSelectSingle_67
    PgSelectSingle_67 --> PgClassExpression_68
    List_95 --> First_74
    First_74 --> PgSelectSingle_75
    PgSelectSingle_75 --> PgClassExpression_76
    __Value_3 --> Access_79
    __Value_3 --> Access_80
    Access_79 --> Object_81
    Access_80 --> Object_81
    List_97 --> First_82
    First_82 --> PgSelectSingle_83
    PgSelectSingle_83 --> PgClassExpression_84
    PgSelectSingle_67 --> PgClassExpression_85
    PgSelectSingle_22 --> Map_86
    Map_86 --> List_87
    PgSelectSingle_22 --> Map_88
    Map_88 --> List_89
    PgSelectSingle_51 --> Map_90
    Map_90 --> List_91
    PgSelectSingle_22 --> Map_92
    Map_92 --> List_93
    PgSelectSingle_67 --> Map_94
    Map_94 --> List_95
    PgSelectSingle_67 --> Map_96
    Map_96 --> List_97
    PgSelectSingle_22 --> Map_98
    Map_98 --> List_99
    First_12 --> Access_100

    %% plan-to-path relationships
    __TrackedObject_6 -.-> P1
    PgSelectSingle_13 -.-> P2
    PgClassExpression_14 -.-> P3
    PgClassExpression_15 -.-> P4
    Access_100 -.-> P5
    PgSelectSingle_22 -.-> P6
    PgClassExpression_23 -.-> P7
    PgSelectSingle_30 -.-> P8
    PgClassExpression_31 -.-> P9
    PgPolymorphic_37 -.-> P10
    PgClassExpression_44 -.-> P11
    PgClassExpression_45 -.-> P12
    PgClassExpression_52 -.-> P13
    PgSelectSingle_59 -.-> P14
    PgClassExpression_60 -.-> P15
    PgClassExpression_61 -.-> P16
    PgClassExpression_68 -.-> P17
    PgSelectSingle_75 -.-> P18
    PgClassExpression_76 -.-> P19
    PgSelectSingle_83 -.-> P20
    PgClassExpression_84 -.-> P21
    PgClassExpression_85 -.-> P22

    %% allocate buckets
    classDef bucket0 stroke:#696969
    class __Value_3,__Value_5,__TrackedObject_6,InputStaticLeaf_7,PgSelect_8,First_12,PgSelectSingle_13,PgClassExpression_14,PgClassExpression_15,Access_79,Access_80,Object_81,Access_100 bucket0
    classDef bucket1 stroke:#a52a2a
    class __Item_21,PgSelectSingle_22,PgClassExpression_23,First_29,PgSelectSingle_30,PgClassExpression_31,PgClassExpression_32,PgClassExpression_33,PgClassExpression_34,PgClassExpression_35,List_36,PgPolymorphic_37,First_42,PgSelectSingle_43,PgClassExpression_44,PgClassExpression_45,First_50,PgSelectSingle_51,PgClassExpression_52,First_58,PgSelectSingle_59,PgClassExpression_60,PgClassExpression_61,First_66,PgSelectSingle_67,PgClassExpression_68,First_74,PgSelectSingle_75,PgClassExpression_76,First_82,PgSelectSingle_83,PgClassExpression_84,PgClassExpression_85,Map_86,List_87,Map_88,List_89,Map_90,List_91,Map_92,List_93,Map_94,List_95,Map_96,List_97,Map_98,List_99 bucket1

    subgraph Buckets
    Bucket0("Bucket 0 (root)<br />~"):::bucket
    style Bucket0 stroke:#696969
    Bucket1("Bucket 1 (__Item[_21])<br />>perso…sonId>personBookmarksList[]"):::bucket
    style Bucket1 stroke:#a52a2a
    Bucket0 --> Bucket1
    end
```