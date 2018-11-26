# PlantUML demo

PlantUML is a tool that uses text formatting to create graphic diagrams.

http://plantuml.com/class-diagram


## Sequence diagram

![Sequence diagram](doc/sequence_diagram.png)

```plantuml
@startuml
!include styles.txt
System1 -> System2: Request
System2 --> System1: Response
@enduml
```


## Usecase diagram

![Usecase diagram](doc/usecase_diagram.png)

```plantuml
@startuml
!include styles.txt
left to right direction
User1 --> (Story1)
(Story1) --> (Story2)
(Story2) --> (Story3)
@enduml
```


## Object diagram

![Object diagram](doc/object_diagram.png)

```plantuml
@startuml
!include styles.txt
object Object1 {
  Alpha
  Bravo
  Charlie
}
object Object2 {
  Delta
  Echo
  Foxtrot
}
object Object3 {
  Golf
  Hotel
  Indigo
}
object Object4 {
  Juliet
  Kilo
  Lima
}
Object1 <|-- Object2
Object1 *-- Object3
Object1 o-- Object4
@enduml
```

## Class diagram

![Class diagram](doc/class_diagram.png)

```plantuml
@startuml
!include styles.txt
class Class1 {
  {field} Alpha
  {method} Bravo
  {method} Charlie
}
class Class2 {
  {field} Delta
  {method} Echo
  {method} Foxtrot
}
class Class3 {
  {field} Golf
  {method} Hotel
  {method} Indigo
}
class Class4 {
  {field} Juliet
  {method} Kilo
  {method} Lima
}
Class1 <|-- Class2
Class1 *-- Class3
Class1 o-- Class4
@enduml
```

## Activity diagram

![Activity diagram](doc/activity_diagram.png)

```plantuml
@startuml
!include styles.txt
start
-> Starting;
:Activity 1;
if (Question) then (yes)
  :Option 1;
else (no)
  :Option 2;
endif
:Activity 2;
-> Stopping;
stop
@enduml
```


## Component diagram

![Component diagram](doc/component_diagram.png)

```plantuml
@startuml
!include styles.txt
component "Component"
interface "Interface"
database "Database"
cloud "Cloud"
node "Node"
package "Package"
@enduml
```


## State diagram

![State diagram](doc/state_diagram.png)

```plantuml
@startuml
!include styles.txt
[*] --> State1 : Start
State1 -> State2 : Change1
State2 -> State3 : Change2
State3 --> [*] : Stop
State1 : Description 1
State2 : Description 2
State3 : Description 3
@enduml
```


## Deployment diagram

![Deployment diagram](doc/deployment_diagram.png)

```plantuml
@startuml
!include styles.txt
actor actor
agent agent
artifact artifact
boundary boundary
card card
cloud cloud
component component
control control
database database
entity entity
file file
folder folder
frame frame
interface  interface
node node
package package
queue queue
stack stack
rectangle rectangle
storage storage
usecase usecase
@enduml
```


## Timing diagram

![Timing diagram](doc/timing_diagram.png)

```plantuml
@startuml
!include styles.txt
concise "My Timeline" as T
@T
0 is Alpha
+100 is Bravo
+100 is Charlie
@50 <-> @+100 : My Note
@enduml
```


## Wireframe

![Wireframe](doc/wireframe.png)

```plantuml
@startuml
salt
{
  Hello world
  [Button]
  ()  Radio 1
  (X) Radio 2
  []  Checkbox 1
  [X] Checkbox 2
  "Enter text here   "
  ^This is a droplist^
}
@enduml
```


## Gantt chart

![Gantt chart](doc/gantt_chart.png)

```plantuml
@startgantt
[Task1] on {Alice} lasts 8 days
then [Task2] on {Bob} lasts 4 days at 50% 
then [Task3] on {Carol} lasts 2 days at 25%
@endgantt
```
